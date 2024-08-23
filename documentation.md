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
            - Created root and korifi namespaces
            - Created a personal access token on dockerhub
            - Created a secret for the root-namespace named "image-registry-credentials"
            - Installed Contour as Gateway Provisioner with gateway API experimental channel
            - Created a GatewayClass and a Gateway
            - Installed cert-manager and kpack via kubectl
            - Installed Korifi via Helm
            - ELB: {"hostname":"adeb1d6b8f22a4a96a416fdb577ecbf7-1057529710.eu-west-1.elb.amazonaws.com"}  // kubectl get service envoy-korifi -n korifi-namespace-gateway -ojsonpath='{.status.loadBalancer.ingress[0]}'

## II. Install a8s PostgreSQL Service
https://github.com/anynines/pt2-postgres-data-service-test/tree/develop
Control Plane name prefix: `pcf-ws-2-`

Required steps:
 - Provision a PostgreSQL Instance
 - Bind an application to the PostgreSQL Instance
 - Take a backup of the PostgreSQL Instance
 - Visualize the Logs of the PostgreSQL Instance
 - Visualize the Metrics of the PostgreSQL Instance

 