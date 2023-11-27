I am currently engaged in a comprehensive exploration of YouTube data for my capstone project, with the ultimate objective of launching my own channel. Through a meticulous analysis of the available data, I aspire to extract valuable insights pertaining to optimal strategies for channel initiation, audience attraction, and subscriber acquisition on the YouTube platform.

Project Description

STAGE ONE: Data Flow Architecture
The data flow architecture, meticulously designed using draw.io, is accessible in the Screenshot folder under the title "Project Architecture."

STAGE TWO: Data Acquisition from YouTube API

Conducted a thorough investigation of YouTube documentation to establish a developer account and obtain the necessary API key.
Identified and documented the essential columns based on the available features on the website (Youtube.com).
Discovered relevant API endpoints, including search_url, video_url, and channels_url.
Developed a code to extract pertinent data, such as comments, likes, duration, views, channel name, date posted, subscribers, and video title, which was subsequently saved as a CSV file on the local machine.

STAGE THREE: Infrastructure Setup

Installed Docker Desktop.
Deployed Postgres and PgAdmin on Docker (refer to the Postgres folder).
Implemented the deployment of Airflow using the Astronomer method.
STAGE FOUR: Data Movement to PostgresSQL

Developed code to extract data from the YouTube API and store it in PostgresSQL.
Files for this process can be found in the folder titled "Youtube_to_psql.py" and "load_youtube_to_psql.py."
Utilized a hook method to grant Airflow permission to access Postgresql, ensuring successful data transfer.
STAGE FIVE: Google Cloud Platform Integration

Established a Google Cloud Platform setup.
Created a bucket and a BigQuery.
Granted the necessary permissions through Iam and downloaded them as a JSON file.
STAGE SIX: Data Transformation and Modeling with DBT

Installed Data Build Tool (DBT) on the local machine, making necessary installations via extensions (YAML, Better Jinja, Git Ignore).
Organized a project folder with required components.
Established a connection from DBT to BigQuery.
Modeled data with staging, intermediate, and mart folders.
Created a star schema in the intermediate folder and developed associated YAML files for table descriptions.
Resolved various issues by creating mart tables, including queries for total views, likes, subscribers, and video upload statistics.
STAGE SEVEN: Deployment and Integration

Deployed the project to DBT Cloud.
Created a job for execution.
Established a hook for connectivity, integrating Airflow to execute the DBT job seamlessly.
Successfully executed all jobs using Airflow.
For additional details, visual representations, and lineage information, please refer to the respective folders and files mentioned throughout the stages.

SUMMARY

Successfully constructed an Airflow pipeline, hosted on Astronomer, to extract data from the YouTube API endpoint. The data was loaded into PostgreSQL and simultaneously transferred from the API endpoint to a Google Cloud (GC) bucket and then to BigQuery. Utilized Dbt for comprehensive transformation and analysis. Deployed the processed data to Dbt Cloud, and executed Dbt Cloud jobs seamlessly within the Airflow environment.

CONCLUSION

In conclusion, the implemented Airflow pipeline, orchestrated on Astronomer, demonstrated a robust and flexible solution for handling data extraction, transformation, and loading (ETL) processes. The seamless integration with the YouTube API allowed for efficient extraction of data, which was then seamlessly loaded into both PostgreSQL and Google Cloud resources.

The parallel loading of data from the API endpoint to a Google Cloud bucket and subsequently to BigQuery showcased the versatility of the pipeline, catering to different storage and processing needs. The incorporation of Dbt for data transformation and analysis further enriched the pipeline, providing a powerful layer for shaping and understanding the data.

Deploying the processed data to Dbt Cloud extended the capabilities of the pipeline, enabling the execution of Dbt Cloud jobs directly within the Airflow environment. This integration not only streamlined the workflow but also facilitated the execution of comprehensive data transformations and analytics in a cloud-native environment.

Overall, the successful implementation of this end-to-end pipeline highlights the efficacy of Airflow, Astronomer, and Dbt in orchestrating and optimizing complex data workflows, from extraction to analysis, in a scalable and efficient manner.





