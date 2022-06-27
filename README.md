# Hosting a Full-Stack Application on the Cloud and Automate deployment 

## Infrastructure description 

- The application contains frontend , backend and relational database 

- The frontend is Angular - ionic application and is hosted on S3 bucket on AWS cloud

- Link for the frontEnd App : 
---

```  http://mo-udagram-bucket1.s3-website-us-east-1.amazonaws.com  ```

---

- The backend api is a node.js Typescript application using express framework and hosted on AWS Elastic beanstalk service 

- The relational database is using postgreSQL as a database engine and hosted on AWS RDS service on the cloud 

- The three services of the aws infrastructure is communicating to host the application


### More info can be found in the Infrastructure-description.md file in docs/diagrams directory


## App dependencies 

```
- Node v14.15.1 (LTS) or more recent. While older versions can work it is advisable to keep node to latest LTS version

- npm 6.14.8 (LTS) or more recent

- AWS CLI v2, v1 can work but was not tested for this project

- A RDS database running Postgres

- A S3 bucket for hosting frontend application

```

- The frontend app dependencies can be installed using ``` npm install ``` command in the udagram-frontend directory 


- The backend app dependencies can be installed using ``` npm install ``` command in the udagram-api directory

- Elastic beanstalk hosting the Backend-api should have a these env variables

1. POSTGRES_HOST="database link goes here"

2. DB_PORT=port here

3. POSTGRES_USERNAME="username"

4. POSTGRES_PASSWORD=password-here

5. POSTGRES_DB="Database name"


### More info can be found in the App-depenedencies.md file in docs/diagrams directory

## Pipeline Process 

- The pipeline as a service platform used for CICD is CircleCi 

- The config.yml file exist in .circleci directory and it holds the pipeline configuration for the cicd

- The code pushed to github triggers the pipeline to execute since CircleCi detects config.yml file , builds the code and deploys on the aws infrastructure . The CircleCi also holds env variable for the aws access keys 

### More info can be found in the Pipeline-process.md file in docs/diagrams directory


### Diagrams for the aws infrastructure exist in docs directory

### ScreenShots for CircleCi and AWS Console exists in docs directory

### More info can be found in the md files in docs/diagrams directory


