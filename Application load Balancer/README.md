# Application Load Balancer (ALB)

Application Load Balancer operates at the request level (layer 7), routing traffic to targets (EC2 instances, containers, IP addresses, and Lambda functions) based on the content of the request. Ideal for advanced load balancing of HTTP and HTTPS traffic, Application Load Balancer provides advanced request routing targeted at delivery of modern application architectures, including microservices and container-based applications.

### Steps to Launch an Instance:
    1. Go to EC2->instance.
    2. Click on launch instance
    3. Give the name of the instance, select the AMI of the instance, and instance type accordingly
    4. Select or create new key-pair if you haven't already.
    5. Create or select the security group accordingly.
    6. Click on Launch Instance

### Steps to Create Target Group
    1. Go to target group and click on create.
    2. Choose the target type, in our case it is Instances.
    3. Give name to the target group.
    4. Select VPC and Protocol version.
    5. Give the health check protocol and give the health check path accordingly to your project that you're trying to deploy.
    6. Select the available instance which you've created.
    7. Give the port number and review the target group.
    8. Click on create targert group.

### Steps to Create ALB
    1. Go to Load Balancer and click on create and select Application load Balancer
    2. Give the name to the load balancer and select the scheme and IP address type accordingly.
    3. Select the region of your load balancer (Should be the same region as in your EC2 instance)
    4. Select or create a new security group for your load balancer which allows inbound traffic role from your own IP.
    5. Select the target group that you've created.
    6. Click on create load balancer.