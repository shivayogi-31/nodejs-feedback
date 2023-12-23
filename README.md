# nodejs-feedback
Steps:

1. Clone the project using git clone into your local repository
2. To build an image , use docker build -t node:v1 . command to create an image .
3. To push image to AWS ECR
    i. Install AWS CLI on your instance
    ii. Configure AWS CLI using the access key and token key which is generated in AWS IAM
    iii.  Tag the Docker image use following command -->
         docker tag your-image-name:latest <your-ecr-repository-uri>:latest
    iv. Authenticate Docker to your ECR registry use following command -->
         aws ecr get-login-password --region <your-region> | docker login --username AWS --password-stdin <your-ecr-repository-uri>
     v. Push the Docker image to ECR use following command -->
         docker push <your-ecr-repository-uri>:latest
 
