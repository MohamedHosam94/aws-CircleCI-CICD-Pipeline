# Infrastructure description 

- The application contains frontend , backend and relational database 

- The frontend is Angular - ionic application and is hosted on S3 bucket on AWS cloud

- Link for the frontEnd App : 
---

```  http://mo-udagram-bucket1.s3-website-us-east-1.amazonaws.com  ```

---
- The backend api is a node.js Typescript application using express framework and hosted on AWS Elastic beanstalk service 

- Environment variables for the backend-Api lives in CircleCi and is deployed to aws eb service from CircleCi 

- The relational database is using postgreSQL as a database engine and hosted on AWS RDS service on the cloud 

- The three services of the aws infrastructure is communicating to host the application

- CircleCi is the pipeline as a service used to automate the build and deployment , when any changes pushed to github main branch the pipeline is triggered and CircleCi integrates and delivers code into aws infrastructure