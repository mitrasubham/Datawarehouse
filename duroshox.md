flowchart LR

A[SAP S4 HANA Public Cloud] --> B(Data Ingestion Layer)
C[SAP ECC] --> B
D[Excel / CSV] --> B
E[Manual Data Entry] --> B
F[Future Sources SFDC / PLM / IoT] --> B

B --> G[Azure Data Factory]
B --> H[SAP OData / APIs]
B --> I[Batch File Ingestion]

G --> J[Azure Data Lake Storage Gen2]

J --> K[Bronze Layer Raw Data]

K --> L[Data Processing Layer]

L --> M[Azure Databricks / Synapse]

M --> N[Silver Layer Harmonized Data]

N --> O[Golden Data Layer Single Source of Truth]

O --> P[Semantic Model]

P --> Q[Power BI Dataset]

Q --> R[Power BI Dashboards]

O --> S[Advanced Analytics]
S --> T[Predictive Models / ML]
