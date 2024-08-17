# Worksample for DevOps

## Introduction
As the practical part of the anynines recruiting process we created a work sample for you. 
The work sample is divided into two parts. Please stick to the given order and solve the tasks.

The work sample is split into two parts:
  
1. set up Korifi and push an app via the CF CLI (Part I) 
3. set up the a8s PostgreSQL Dataservice and perform various actions with it (Part II)
 
|https://919830305524.signin.aws.amazon.com/console

Create a document about what you did to solve the tasks. After you finished keep your solution online so we can review it.

Please make sure that you are in the right Amazon Web Services (AWS) region. Please choose Ireland in the upper right corner.
 
## I Deploy Korifi to an EKS Cluster
Korifi is an implementation of the CF API on K8S.

Please use the installation information that can be found [here](https://github.com/cloudfoundry/korifi) to roll out Korifi.

Be aware of the installation and naming conventions stated below:
 
- do not use ECR but a public Dockerhub account 
- if you create roles, user, cluster make sure to prefix them with pcf-ws-2
- use the following base_domain: ws2.a9s-ops.de

During Post-Install Configuration you should create a CNAME entry. Please let us know the ELB ID so we can create that entry for you.

After you finished the installation please use the CF CLI and push a sample app to CF. 

## II. Install a8s PostgreSQL Service
Please follow [these](https://github.com/anynines/pt2-postgres-data-service-test/tree/develop) instruction on how to rollout the a8s PostgreSQL Service to your existing EKS cluster.

Which means first setup the Control Plane, use a bucket name prefixed with `pcf-ws-2-` for that.
Afterwards perform the following steps:
 - Provision a PostgreSQL Instance
 - Bind an application to the PostgreSQL Instance
 - Take a backup of the PostgreSQL Instance
 - Visualize the Logs of the PostgreSQL Instance
 - Visualize the Metrics of the PostgreSQL Instance