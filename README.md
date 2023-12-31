Alias: must be unique
Auth info:
    Console sign-in URL
    https://aws-labs-fpt.signin.aws.amazon.com/console
    User name: Hoang

    CLI
        aws configure

    CloudShell
        online CLI

    Platform as a Service (PaaS)
        chỉ cần upload data + code (không cần config infra)
        - AWS elasstic Beanstack
        - Azure WebApps
        - Compute App Engine

    Data transfer
        - upload data lên aws sẽ không tính phí lưu lượng
        - download data từ aws sẽ tính phí lưu lượng

    AWS Global Infrastructure
        - Region
            AZ: Có nhiều AZ trong Region
                DataCenter: có 1 hoặc nhiều DataCenter trong AZ
        
        AZ
            - Trong mỗi AZ có thể tạo Public Subnet, Private Subnet
            - Các AZ giao tiếp với nhau qua Redundant Networking

        CloudFront
            - Content Delivery network

    Global Infrastructure
        //public-and-private-services.jpg
        https://digitalcloud.training/aws-global-infrastructure/

    AWS Pricing Cheat Sheet
        https://digitalcloud.training/aws-billing-and-pricing/#aws-pricing-calculator


PRACTICE IAM
================================================

https://digitalcloud.training/aws-identity-and-access-management/
    
    IAM

    We have policies that are called identity based policies and resource based policies.
    - Quản lý access đến resource (EC2, S3, IAM)
    - Group: chứa nhiều user
    - Policy: apply cho Group
    - Role

    Root có thể tạo 5000 user
    Mặc định user mới sẽ không có permissions

    Group chứa các thể loại policies để apply permissions cho user

    Roles: chứa permissions đặc biệt. gán cho user, application...
    ví dụ role chỉ cho phép user truy cập S3
        Permission chứa nhiều policies

    Policies: là JSON define permissions
    có thể apply cho user, group, role

    SCPs (Service Control Policies)
        Associated with a service called AWS Organizations.
        SCPs is they don't actually grant permissions,hey control the permissions you're allowed to use.


PRACTICE
================================================
EC2

    - EC2 have an attached with EBS volume
    - Security Group (Firewall): định nghĩa traffic roles (cho phép SSH, cho phép https traffic...allow anywhere ...)
    -Config role và attach vào EC2 để tránh lộ key khi dùng aws configure
    - AWS batch: dịch vụ run job

ECS (Elastic container service)

    - Cluster is group of task (container)
    - Task definition (giống docker-compose)
    - Có 2 cách deploy
        - Run ECS EC2 Cluster với container bên trong. (charge for ec2, tự tạo infra, ..)
        - Serverless: ECS Fargate cluster  (charge for task, không cần quan tâm infra.)

ECR (Elastic container registry)

    - Store Docker Image
