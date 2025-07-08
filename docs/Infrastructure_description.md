This project uses AWS services to host a full-stack application composed of a backend API, a frontend Angular application, and a PostgreSQL database. The infrastructure is cloud-native and follows best practices for scalability and availability.

**Backend (API)**
- Service: AWS Elastic Beanstalk
- Platform: Node.js 14 running on 64bit Amazon Linux 2
- Function: Hosts the RESTful API developed using Express.js.
- Deployment: Managed using Elastic Beanstalk CLI and CircleCI CI/CD pipeline.

**Frontend (Web Application)**
- Service: AWS S3 (Static Website Hosting)
- Function: Hosts the Angular frontend application as a static site.
- Deployment: Deployed via deploy.sh script and CircleCI pipeline.

**Database**
- Service: AWS RDS (PostgreSQL)
- Function: Stores user data, authentication information, and feed metadata.
- Access: Secured with environment variables; not directly accessible from the public internet.

**Other Service**
- IAM: Used to manage permissions for CI/CD deployment via CircleCI.
- S3 Buckets: Store frontend files and potentially images uploaded by users.
- Security Groups: Control access to EC2 instances and RDS.
