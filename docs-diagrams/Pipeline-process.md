# Pipeline Process

- The pipeline as a service platform used for CI/CD is CircleCi 

- The config.yml file exist in .circleci directory and it holds the pipeline configuration for the cicd

- The code pushed to github triggers the pipeline to execute since CircleCi detects config.yml file , builds the code and deploys on the aws infrastructure . The CircleCi also holds env variable for the aws access keys 

## Pipeline steps 

- The CircleCi CI/CD pipeline starts by setting the required configuration like 
node.js , aws cli and eb cli  

- The build step starts by installing node with it's required version then aws cli 

- The Front-End Dependencies is then installed using the ``` npm run frontend:install ``` command from the root package.json

- API Dependencies is then installed using the ``` npm run api:install  ``` command from the root package.json

- The Front-End is Build into the www folder in udagram-frontend using ``` npm run frontend:build ``` command from the root package.json

- The Backend API is Build into the www folder in udagram-api using ``` npm run api:build ``` command from the root package.json

- The AWS Elastic beanstalk cli is then installed into the pipeline 

- The Front-End and Backend API is then deployed to AWS Infrastructure using ``` npm run deploy ``` command from the root package.json


### WorkFlow 

- The workFlow arranges the order of execution of the above steps so that build step starts first then deploy step 

- The pipeline also is set to detect any change only in the main branch to start the pipeline 
