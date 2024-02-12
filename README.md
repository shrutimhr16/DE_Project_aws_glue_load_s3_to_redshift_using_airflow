# DE_Project_aws_glue_load_s3_to_redshift_using_airflow
aws_glue_load_s3_to_redshift_airflow

<h3> Problem Statement </h3>
In this project, dataset is kept on landing zone on Amazon S3 bucket. Some basic transformations are performed like datatypechange , column selection etc using AWS glue job. The data is then loaded into Redshift using AWS Glue job. The process is automated using Airflow which triggers the glue job. Finally redshift is connected to Power BI to perform analytics on data.

<h3>DataSet</h3>: For this project, we are going to use the 
<h3>Tech Stack / Skill used:</h3>
Python
Airflow
AWS Redshift
AWS Glue
Power BI

<h3>Dags</h3>
Step 1 --> Create a landing zone bucket on S3 on which csv files will arrive.
![image](https://github.com/shrutimhr16/DE_Project_aws_glue_load_s3_to_redshift_using_airflow/assets/42519482/dcc3f7fc-ce7e-400b-816d-1880c64c5001)

Step 2 --> Create crawlers which crawls amazon s3 and another which crawls redshift tables and loads data accordingly to catalog tables.
<img width="1119" alt="Screenshot 2024-02-12 at 7 33 14 PM" src="https://github.com/shrutimhr16/DE_Project_aws_glue_load_s3_to_redshift_using_airflow/assets/42519482/5f805175-c563-4ba4-9c0f-bfe76cc54b20">

Step 3 --> Create ETL job using AWS glue with source as S3 , transform (change schema,update datatype, select columns) and destination as Redshift tables.
<img width="755" alt="Screenshot 2024-02-12 at 11 28 21 PM" src="https://github.com/shrutimhr16/DE_Project_aws_glue_load_s3_to_redshift_using_airflow/assets/42519482/6e109c29-f6bc-4be3-b17a-c5f0db168806">
![image](https://github.com/shrutimhr16/DE_Project_aws_glue_load_s3_to_redshift_using_airflow/assets/42519482/4f0edcc6-33e5-4cf6-9193-2529226fb7ab)


Step 4 --> Launch an EC2 instance and download Airflow. Place dag file in airflow/dags.
<img width="1271" alt="Screenshot 2024-02-12 at 7 08 28 PM" src="https://github.com/shrutimhr16/DE_Project_aws_glue_load_s3_to_redshift_using_airflow/assets/42519482/f7360501-1eea-46ba-b42f-3ead2dbcf6f7">

 Final Output:
 ![Uploading Screenshot 2024-02-12 at 7.09.26 PM.png…]()


