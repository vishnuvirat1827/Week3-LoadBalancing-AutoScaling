# Implement Load Balancing and Auto Scaling on AWS

## Objective
To understand how Elastic Load Balancer distributes traffic across multiple EC2 instances and how Auto Scaling automatically adjusts resources based on demand.

## AWS Services Used
- Amazon EC2
- Elastic Load Balancer (ELB)
- Auto Scaling Group
- CloudWatch

## Architecture

User Requests
      |
      V
Elastic Load Balancer
   /         \
EC2-1      EC2-2
      |
Auto Scaling Group
      |
CloudWatch

## Procedure

### Launch EC2 Instances
Create two EC2 instances.

### Configure Load Balancer
Attach both instances to an Application Load Balancer.

### Create Auto Scaling Group
Minimum: 2 instances
Desired: 2 instances
Maximum: 4 instances

### Configure Scaling Policy
Increase instances when CPU utilization exceeds 70%.

### Monitor with CloudWatch
Monitor CPU utilization and scaling activities.

## Outcome
Traffic is distributed evenly among EC2 instances and the system automatically scales during increased load.

## Learning Outcome
Learned the concepts of load balancing, auto scaling, fault tolerance and cloud scalability.
