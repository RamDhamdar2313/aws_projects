# AWS Network Load Balancer (NLB) with Custom Health Checks

Author: Me  

## Architecture Overview

I implemented an AWS Network Load Balancer (NLB) with customized health checks and tuned target group attributes to ensure low latency, high availability, and predictable failover.

# First Create an Instances

- create 3 instances with the sam econfiguration and using a user-data-script 
- user-data-script 
  
#!/bin/bash
apt update -y
apt install nginx -y 
echo "<h1> NLB Practicals </h1> <p> This is launched from </u>$(hostname)</u> </p>" > /var/www/html/inex.html
echo "This is health check" > /var/www/html/hc.txt
systemctl enable nginx
systemctl restart nginx

    
![](images/media/image1.png)


## Step 2: Target Group Creation

- Target type: Instance
- Protocol: TCP
- Port: 80
- VPC: Default
- We are creating a Halth Check for The Target Group here itself so here are the steps of it
- Settings for the Health Check
    - Protocol: TCP / HTTP
    - Path: /health (HTTP)
    - Interval: 30s
    - Timeout: 10s
    - Healthy threshold: 3
    - Unhealthy threshold: 3
Each service has its own target group for independent health management.

![Target Group](images/media/image2.png)

## Step 3: Registering Targets

EC2 instances were registered and monitored continuously via health checks.

![Target Group](images/media/image3.png)
![Target Group](images/media/image4.png)



## Step 1: Creating the Network Load Balancer

I created a Network Load Balancer with:
- Type: Network
- Scheme: Internet-facing
- IP type: IPv4
- VPC: Default VPC
- AZs: All enabled

Why NLB:
- Layer 4 (TCP)
- Preserves client IP
- Static IPs per AZ
- Extremely high throughput

![Network Load Balancers](images/media/image5.png)

## Step 4: Check if everything is working fine 

- Copy th DNS name of the nlb provided after the status of netowrk load balancer is turned active
- hit the address in the browser and keep pressing Refresh 
  
![Hitting one](images/media/image6.png)
![Hitting one](images/media/image7.png)
![Hitting one](images/media/image8.png)
- You can see three different ips loading 






## Step 5: Target Group Attributes

I modified the following:
- Deregistration delay (reduced)
- Preserve client IP (enabled)
- Proxy protocol v2 (enabled when required)

This prevents dropped connections during deployments.

![Attributes](images/media/image9.png)

## Step 6: Verify by Forcefully stopping one instance

I did ssh to one of the instanes and forcefully stopped the nginx

![SSH to Instance](images/media/image10.png)
![Stop the ssh](images/media/image11.png)

## What Happens After the nginx stopped one one server
- The instances is declared Unhealthy
- and now the Load Balncer is not routing the traffic to it 
![Healthy Targets](images/media/image12.png)



Unhealthy instances are immediately removed, traffic shifts automatically, and recovered instances rejoin without manual action.

## Final Outcome

A production-ready, low-latency, fault-tolerant NLB configuration.
Unhealthy instances are immediately removed, traffic shifts automatically, and recovered instances rejoin without manual action.