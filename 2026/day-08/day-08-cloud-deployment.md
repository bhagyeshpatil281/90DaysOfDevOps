# Deploy a Real Web Server on the Cloud

Step 1 : Launch an instance from AWS console.

Step 2 : Connect to instance using ssh.
    
Command : `ssh -i "udaan-batch-11-server.key.pem" ubuntu@ec2-18-170-219-5.eu-west-2.compute.      amazonaws.co`

Step 3 : Install Nginx

Command : `sudo apt update`

`sudo apt install nginx`
        
Step 3 : Configure security groups for web access.
    From the AWS console, go to the security group and add an inbound rule for port 80 (default for Nginx).
    
Step 4 : Check logs of nginx service

Command : `journalctl -u nginx`

step 5 : save the log file local server save

 command : `sudo tail -n 100 /var/log/nginx/access.log > nginx-access.log`

 command : `scp -i udaan-batch-11-server.key.pem nginx-access.log ubuntu@18.170.219.5:/home/ubuntu/`

# i learned whole assignment 

it the nginx is port no 80 run in word wide http 
is the access.log error .log are stored in your system 
ssh authentication remote ssh connect to your local server
