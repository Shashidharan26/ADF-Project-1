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



2. Ingested Data from on prem system using get meta data, for each activity and copy activity, also appplied dynamic mapping to all 3 csv files.

<img width="1234" height="413" alt="pipeline_csv_ingestion_1" src="https://github.com/user-attachments/assets/0886596e-9cf2-4531-9373-ec16d4792e39" />
<img width="1299" height="797" alt="pipeline_csv_ingestion_2" src="https://github.com/user-attachments/assets/03e679e3-3cb2-48a5-b7ab-f9e804756027" />



3. Ingested json Data from github using api call.

<img width="1345" height="802" alt="pipeline_api_ingestion" src="https://github.com/user-attachments/assets/cb7f9368-88e6-4101-a65c-cbfe8a7185c1" />

4. Ingested SQL Data Incrementally from Azure SQL.

<img width="1290" height="783" alt="pipeline_sql_ingestion_incremental loading" src="https://github.com/user-attachments/assets/ed5a68a1-21b6-4b90-96e8-e366cf4f01fc" />
<img width="1535" height="788" alt="initial_load" src="https://github.com/user-attachments/assets/f391919d-28ba-4241-b13c-0d47905dcda8" />
<img width="1574" height="825" alt="incremental_load" src="https://github.com/user-attachments/assets/3d44206b-6d87-4b84-85a5-ad67e2e6dc0e" />

5. Performed Transformation using Data FLow and ingested transformed data into silver layer

<img width="1227" height="344" alt="dataflow_silver" src="https://github.com/user-attachments/assets/5c614ce6-7248-40ca-9516-00ef2ecac9a1" />

6. Performed Transformation using Data Flow and ingested Aggregated data into gold layer

<img width="1494" height="369" alt="dataflow_gold" src="https://github.com/user-attachments/assets/3b5f33bf-94db-4fbc-8148-956eaa2fcf46" />

7.Created Logic app alerts to recieve update on pipeline runs

<img width="1566" height="833" alt="web alert" src="https://github.com/user-attachments/assets/af67a30b-ef49-4074-93d6-5cd8b26adef6" />
<img width="1625" height="771" alt="logic-app" src="https://github.com/user-attachments/assets/03466e4e-3043-4d22-bf09-63a2ccb46630" />











