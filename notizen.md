1. Ordnerstruktur
2. Systemdesign image
3. To Do
4. Installation

---

Step-by-Step Implementation Guide
Phase 1: The "Engine" (ELK)

    Install Docker: This is non-negotiable for a "large app" feel. Use Docker Desktop.

    Spin up ELK: Create a docker-compose.yml file to run Elasticsearch and Kibana.

    Data Ingestion: Configure Logstash to connect to your first Open Data source (e.g., a public CSV file or a SQL dump). Verify the data is there by using Kibana Dev Tools.

Phase 2: The "Brain" (Java Backend)

    Generate Project: Use start.spring.io to create a Maven project with Spring Web and Spring Data Elasticsearch.

    Define the Model: Create a Java class that matches your data schema (e.g., a PublicRecord.java class with @Document annotations).

    Build the Controller: Create a @RestController with a /search endpoint. This endpoint will take a keyword from the user and call the Elasticsearch repository.

Phase 3: The "Face" (Vue.js Frontend)

    Project Setup: Initialize a Vue 3 project using Vite.

    Search Interface: Build a clean search input. On "Enter," use axios to send a GET request to your Java backend (e.g., localhost:8080/search?q=test).

    Result Rendering: Use a v-for loop to display the JSON results as beautiful cards.
