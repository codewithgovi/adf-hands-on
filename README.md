# Azure Data Factory (ADF) — Concepts Brush-up & Learning Sandbox

## Project Purpose
This repository serves as a dedicated hands-on workspace for brushing up, testing, and solidifying my core **Azure Data Factory (ADF)** skills. The goal is to move beyond theoretical knowledge by configuring active components, managing code versions via GitHub integration, and implementing standard enterprise data engineering patterns.

## Core Concepts Reviewed & Implemented
This sandbox covers the practical application of essential ADF pillars:

*   **Data Movement & Orchestration:** Configuring pipelines using the Copy Activity, controlling workflow logic with Lookups, Get Metadata, and Web activities.
*   **Dynamic Parameterization:** Implementing reusable Datasets and Linked Services parameterized with dynamic content to prevent environment hardcoding.
*   **Compute Environments:** Testing pipeline execution across different Integration Runtimes (Azure IR vs. Self-Hosted IR design principles).
*   **Enterprise Security:** Integrating pipelines with **Azure Key Vault** to fetch secrets dynamically rather than storing connection strings in code.
*   **CI/CD & Git Workflows:** Managing feature branches, pulling requests, and tracking how ADF automatically compiles assets into the `adf_publish` ARM templates.

## Learning Architecture
```text
[Sources: Blob / HTTP API / SQL] 
       │
       ▼ (Orchestrated by ADF via Linked Services & Datasets)
[Azure Data Lake Storage Gen2] ──► [Data Transformation / Mapping Data Flows] ──► [Target Database]
       ▲
       │ (Secure Authentication)
[Azure Key Vault Secrets]
```

