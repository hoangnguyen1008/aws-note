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
VPC
