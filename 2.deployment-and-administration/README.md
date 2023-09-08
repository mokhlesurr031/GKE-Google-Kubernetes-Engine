# Deployment and Administration


## Section Introduction

Labs:
1. Create our first cluster. 
2. Install kubectl and configure cluster access.
3. Apply labels and tags to GKE clusters. 
4. Configure cluster autoscaling. 
5. Configure and manage monitoring and logging. 


## GKE Modes of Operation. 

Two types:

1. Autopilot
2. Standard


Autopilot: 

![GKE Autopilot](../static/4.png)
Google manages the underlying infrastructure which includes node configuration, auto scaling, auto update, base line security configuration, and networking. The users simple deploy application to GKE, and google takes care of the rest. 


Standard:

![GKE Autopilot](../static/5.png)
Google manages the control plane in a GKE Standard mode while users are responsible for managing the nodes. 

Standard cluster can be created in two way of zone setup:

1. Zonal
2. Regional


Zonal Cluster: A zonal cluster is deployed on a single zone. It means it has only one control plane running in a zone. If that particular zone has an outage, cluster resources will also become unavailable. 

A zonal cluster can be distributed as single zone or multiple zone. 
In a signle zonal cluster, there will only be a singple control plane within the same zone for managing the nodes. 

On the other hand, on a multi-zonal cluster there is still a single replica of control plan running in a zone, managing worked nodes running in multiple zone. 

A multi-zonal cluster is resilient to zonal failures. 


Regional Cluster: 

















