I am delving into YouTube data as my capstone project with the goal of launching my own channel. By analyzing the available data, I aim to gain insights on optimal strategies for starting, attracting viewers, and garnering subscribers for my YouTube channel.

Project Description 

STAGE ONE:
Data flow Architecture which was desgign using draw.io and can be found in the Screeshot folder Tittled Project architecture

STAGE TWO:
1. I search for the Youtube documentation went to create the developer account the get the api key
2. Note dow the column i thing i will need base the available features on the vebsise
-- Website : Youtube.com
3. Search for the endpoint where i will get my datas from
--  search_url = "https://www.googleapis.com/youtube/v3/search"
    video_url = "https://www.googleapis.com/youtube/v3/videos"
    channels_url = "https://www.googleapis.com/youtube/v3/channels"
4. I wrote a code to extract the data to be saved as a csv file on my local maching which the columns are

   --comments,
   --  likes,
   -- duration,
   -- views,
   --`channel name` , 
   -- `date posted` , 
   --subscribers,
   -- `video title` as video_title 

STAGE THREE:
1. I downloaded and installed Docker desktop
2. I deployed Postgres and Pgadming on Docker which can be find in Posgres folder
3  I delpoyed airflow using Asrtonomer way of deloyment

STAGE FOUR:
1. i developed a code the extract data from the Youtube api and stored it on PosgresSQL
2. The file can be found in the folder titled Youtube_to_psql.py and load_youtube_to_psql.py
3. Used a hook method to give the airflow permission to access the Postgresql
4. The data was moved succeefully

STAGE FOUR:
1. Set up a Google cloud platform 
2. creates a bucket and a bigquerry
3. Granted the required permition to using the Iam the downloaded it as a json file.

STAGE FIVE:
1. Developed a code to extract the data fropm psql and moved to GC Bucket and Bigquerry
2. The files can be found in the folder titled extract_from_psql_dag
3. Used a hook method to give the airflow permission to access the GCP
4. The data was moved succeefully

STAGE SIX:
1. I install Data Build Tool on my local machine which i made some installions via extenstions like YAML, Better Jinja , Git Ignore
2. So i create a project_foldel and have all my reqired 
3. In my model folder i have 3 folder called Staging , Intermidiate and Marts folde
4. I created a connection from DBT to Bigquerry
5. I brought the data to the staging  , file tittled stg_youtube.sql
6. Create a star schema in the intermidaite folder tittled int_video_fact_data.sql, int_video_dimentional_data.sql, int_date_dimentional_table.sql and also create their yml file for the tables full descriptions
7. i created a marts file solvin some problems
 -- The query  that retrieve the total views, total comment, and the difference between total views and total comment for each channel from the specified video fact and dimensional data sources, grouping the results by channel_fact_id and ordering them by total views in descending order.



