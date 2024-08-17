# Worksample for DevOps

## Introduction
The work sample is split into two parts:
  
1. set up Korifi and push an app via the CF CLI (Part I) 
3. set up the a8s PostgreSQL Dataservice and perform various actions with it (Part II)

## I Deploy Korifi to an EKS Cluster
Installation information to roll out Korifi: https://github.com/cloudfoundry/korifi
    
    Steps:
            - Created an access key for my AWS user
            - awscli configuration with the right credentials given by AWS IAM
            - Created korif.env to store Korifi's environment variables
            - Created a cluster with eksctl named "pcf-ws-2-mate-lotti"
