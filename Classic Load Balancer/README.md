# Classic Load Balancer

Classic Load Balancer provides basic load balancing across multiple Amazon EC2 instances and operates at both the request level and connection level

### Steps to Launch an Instance:
    1. Go to EC2->instance.
    2. Click on launch instance
    3. Give the name of the instance, select the AMI of the instance, and instance type accordingly
    4. Select or create new key-pair if you haven't already.
    5. Create or select the security group accordingly.
    6. Click on Launch Instance

### Steps to Configure Classic Load Balancer
    1. Go to Load Balacners -> Create Load Balancer
    2. Select Classic load balancer and click on Create.
    3. Give the name of the load balancer
    4. Give the LB protocol, port and Instances protocol and port. Now click on assign security groups.
    5. Create a new security group for Load balancer and set its inbound rules such that it allows Your IP request.
    6. Configure health check and set the ping path according to yout application then click on Add EC2 instance.
    7. Add the EC2 instance created earlier.
    8. Now create the Load balancer.

### Configure Security Groups
    
1. First Configure Load balancer securtiy groups:
    
    1. Edit Inboud rule so that any traffic from your IP is allowed.
    2.  Copy your load balancer security group ID.

2. Now configure Instance's security group:
    
    1. Edit inbound rules and paste the security group ID of the load balancer.
    2. select the same protocol and port number as select in load balancer security group.

Now you can connect to your instance and deploy your web application and run it on your web browser by copying the DNS name of the load balancer and paste it on your browser.

`Note - If your project doesn't pass the health check, then cross-check IP of the security group and also check the ping path that you've specified in health check path.`