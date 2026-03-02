# End-to-End Data Pipeline using Azure Data Factory

**Summary:**
Built an end-to-end data pipeline using Azure Data Factory to ingest, transform, and load data using Medallion Architecture. The pipeline incrementally loads JSON, SQL, CSV data from on-prem, API and Azure SQL database into bronze layer, applies transformations using Dataflows on bronze layer and loads it into silver layer, and stores data in gold layers as inline Delta Lake dataset format for Business View.

**Parent Pipeline:**
<img width="992" height="239" alt="image" src="https://github.com/user-attachments/assets/7e0fdf65-bf9b-40ac-b86a-2709603ab631" />

**Tech Used:**
•	Azure Data Factory (ADF)
•	Azure Data Lake Storage (ADLS)
•	Integration Runtime (IR)
•	Logic App
•	Azure SQL

**Steps:**
1. Created an integration runtime to connect on prem system to azure using self hosted integration runtime by azure.

<img width="785" height="558" alt="integration-runtime" src="https://github.com/user-attachments/assets/20cb815a-b5a0-491d-91b6-7218642a1909" />
<img width="1626" height="369" alt="integration-runtime-azure" src="https://github.com/user-attachments/assets/7a3be463-ba49-44fa-a225-2afd1261f5fc" />
<img width="628" height="903" alt="New LS connection success" src="https://github.com/user-attachments/assets/90da4917-c6e4-4015-a922-0d3880aff0cc" />

2. Got Data from on prem system using copy activity and get meta data, also appplied dynamic mapping to all 3 csv files

<img width="1234" height="413" alt="pipeline_csv_ingestion_1" src="https://github.com/user-attachments/assets/0886596e-9cf2-4531-9373-ec16d4792e39" />
<img width="1299" height="797" alt="pipeline_csv_ingestion_2" src="https://github.com/user-attachments/assets/03e679e3-3cb2-48a5-b7ab-f9e804756027" />


