# DC/OS Blog App Tutorial

## Motivation
DC/OS 1.8 comes with a large number of new features.
This tutorial aims at giving developers and operators hands-on guidance towards using these new features.

## Target audience
This tutorial will be targeted at a number of distinct personas with different outcomes:

* Service Developer
    How to utilize DC/OS features while developing a new service
* Operators
    Best practice service deployment, e.g., Security
* Operators
    Best practice 2nd day operations
        * Monitoring
        * Upgrading, etc
* (DC/OS) Developers
    CI tests ensuring the used features/demo will still work 


## Relevant Features
DC/OS features which should be covered/explained by the tutorial
* DC/OS 1.8
    * Security
    * IP per Container 
    * VIPS
    * Subnet isolation
    * Persistent Storage
    * Infinity services (Kafka, Cassandra, Spark)

## Target Operations
Best practices which should be covered by the tutorial
    * Service Discovery
    * Viewing logs
    * Installing packages
    * Resource Requirements
    * Docker vs. Mesos/Unified Containers
    * Monitoring
    * High Availability
    * External Loadbalancing
    * Developing applications


# Blog as a Service App
	
We will develop a Blog as a service (BaaS) application.
Multiple users can host theirs blogs -each consisting of the actual blogging app 
using ghost,  each user can control/restart scale his own blog instance(s)

## Step 1: Setup
1. Check Cluster is healthy
    1. UI
    1. Logs
1. Install CLI
1. Install Marathon-lb
    1. Via CLI/UI
1. Deploy MYSQL as persistence layer
    1. Unified/Mesos Containerizer
    1. Using named VIPs
    1. Show and discuss different storage options
        1. Persistent volumes
        1. External volumes
1. Deploy Ghost blog container
    1. Exposed via marathon-lb
1. Deploy second user (i.e., repeat steps 4 and 5)
1. Configure security to isolate users
     Each user can see/scale own containers

