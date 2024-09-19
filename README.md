<h1 align="center">AWS Project 1</h1>


# Project Description: Implementation and Analysis of Animal Control Data
* This project involves setting up a comprehensive data analytics platform using AWS services to manage the City of Vancouver’s animal control data.

## Project Title: AWS Data Analytic Platform for the City of Vancouver - Part 1
* This project goal was to streamline data sourcing, storage, cleaning, transformation, and analysis, all while maintaining high standards of data security and governance. The platform was built with a focus on handling large datasets, securing sensitive information, and providing real-time insights through data visualization.
## Project Objective:
* The objective of this project is to design and implement a secure AWS-based Data Analytics Platform (DAP) for processing and analyzing the City of Vancouver’s Animal Control Lost and Found inventory data. The platform ensures data protection, efficient processing, and the provision of actionable insights to assist city officials in better managing animal-related cases.
## Methodology:
* The process of DAP designing and implementation is as follows.
### 1. Data Analytical Question Formulation
Key analytical questions addressed by the platform include:
- What are the trends in 3-1-1 inquiries received over the years?
- Which departments received the most inquiries in 2023 and 2024?
### 2. Data Discovery
- The dataset for 3-1-1 inquiry volumes was sourced from Vancouver’s Open Data portal, which provided a detailed view of inquiries received across various departments.
![image](https://github.com/user-attachments/assets/e131eaf5-6a17-41e8-aba9-701aa1fc0ee7)


### 3. Storage Design
To manage the data, AWS S3 was used with three separate buckets:
- Raw Bucket: Stores unprocessed data.
- Landing Bucket: Contains data post-initial processing and staging.
- Curated Bucket: Holds processed data ready for analysis.

![image](https://github.com/user-attachments/assets/188d1e3e-2685-4be7-bc1e-c7e276d590b3)


### 4. Data Preparation
- AWS DataBrew was employed to clean and transform the data by removing irrelevant data points, handling null values, and standardizing data formats.
![image](https://github.com/user-attachments/assets/95a4ac88-441e-43f9-b13c-ba1d2ed77663)



### 5. Data Injection
- The cleaned data was ingested into the S3 Raw bucket for further processing.
![image](https://github.com/user-attachments/assets/4c6ceb14-dd87-418f-8791-3d5acef45dc1)
![image](https://github.com/user-attachments/assets/75957713-5463-4288-8c05-4a3143e26383)

### 6. Data Pipeline Design
- AWS Glue was used to automate the ETL (Extract, Transform, Load) process. The pipeline ensured smooth data flow from storage to processing and transformation.
![image](https://github.com/user-attachments/assets/cda0d36b-b624-413f-9ba9-30ef3d47c73f)


### 7. Data Cleaning
- Further cleaning steps were taken to eliminate any errors or inconsistencies in the data, improving overall data quality. AWS Glue Jobs handled row-level transformations and schema filtering.
![image](https://github.com/user-attachments/assets/fbdccb52-cbab-4e88-bfb9-fb5e09c9a53e)

### 8. Data Structuring
- The data was structured according to departments and yearly trends to make it easier to analyze the inquiry patterns.
![image](https://github.com/user-attachments/assets/893f20a9-cd16-4cff-bc65-7f81c0db7eba)


### 9. Data Pipeline Implementation
- AWS Glue Jobs were created to ensure data transformation and loading were completed properly. The final processed data was saved in the S3 Curated bucket.
![image](https://github.com/user-attachments/assets/2df2c947-b99f-461a-8191-7f12c9a65f4b)
![image](https://github.com/user-attachments/assets/aa9e5256-7312-41eb-863b-af83140215fc)


### 10. Data Analysis
- AWS Athena was employed for running SQL queries to analyze the inquiry data. For example, a query was executed to compare the inquiry counts across departments in 2023 and 2024.
![image](https://github.com/user-attachments/assets/fe2ac114-bef2-4d6f-b635-002e50f99606)


### 11. Data Visualization
- Visualization of the data was carried out to compare the number of inquiries between 2023 and 2024. This helped identify which departments handled the highest volumes of inquiries.
![image](https://github.com/user-attachments/assets/c604c74a-b33d-45a8-9b41-cbeac7d3ef34)

### 12. Data Publishing
- An AWS EC2 instance was deployed to publish the analysis results. This allowed stakeholders to access the results remotely, enhancing visibility and decision-making.
![image](https://github.com/user-attachments/assets/7410cf29-3049-41d0-842b-1f42e0ad5fdb)


