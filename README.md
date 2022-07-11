# Hybrid cloud migration phases

     a. Assessment (application, infrastructure, performance assessment)
     
     b. Mobile & mapping (digital asset invectory, application, infrastructure, perfomance discovery mapping, landing zone, vending machine product, migration                 readiness assessment(MRA)  
     
     c. Migration(7R) & modernation (Retain, Retie, relocate, rehost, replatform, repurchase, refactor)
 
 AWS/Azure cloud stacks
 
  1. Cloud Account & Organization structure Design
  2. Cloud user group IAM, Federal SSO
  3. Networking 
  4. Security
  5. Storage
  6. Computing & autoscaling 
  7. Database
  8. Caching
  9. Data Analystics & Machine learning
 
  10.container, microservice, serverless
 
  11.IaC deployment
 
  12.Governance, Monitoring & logging
 
  13.cloud native serverless architecture 
  
  1.  AWS:  organization, structure, cross account, IAM Account roles and permission policy: Service control policy, STS, permission boundary, advanced setting: cross              account management, RAM, shared VPC
      
      AZURE: tenants, organization, Azure AD user, groups Account policy permission RBAC, conditional access policy, identity privilege management

  2. Cloud user group IAM, Federal SSO
       AWS:   SAML2.0, federal sso/Cognito, workspace, hybrid directory service, AD connector, hybrid AD)
       
       AZURE: SAML2.0, federated sso, Azure directory service, AD domain service, identity governance, AD security and health check, Azure AD connector, hybrid AD,                   privilege user identity protection. 

        Note: Federated SSO solution use MS-AD and AFDS to have two-way forest trust is the key solution for multi-cloud strategy.  As premise AD, AWS cloud, Azure all well connect with AD connect and premise AD and directory service 
              Azure AD, AD conditional Access, Connect Health, AD Domain Service, Privilege Identity, Identity governance, Multi-tenants 

  3. Networking 
  
       AWS:  (Region/AZs/subnets, public/private VPC, IGW, NATGW, security VPC, management VPC, transit VPC, NACL, SG, BGP, S2S VPN, Directconnect, DXGW, VGW, TGW,                  pubic/private/tranit VIF, GW & interface end-point, Route53 & Hybrid DNS, AWS private link)

       AZURE: (Region/AZs/subnets, VNet, Vnet peering, application gateway, Azure Bastion, DDOS Protection, ASG and NSG. Azure DNS, Frontdoor, Azure private link, CDN,              Load balancer, Traffic Manager, virtual Network, Virtual Network, VPN gateway, virtual WAN, interface endpoint, privatelink, interface endpoint                        networkwatch
   
             Notes: there is no IGW and NATGW in Azure as all vNet are public/private supportable and Vnet us NATGW as the service 
             Azure VPN GW=AWS TGW, Azure NATGW=AWS IGW+NATGW, Azure ASG support micro segmentation , Azure application GW=AWS WAF+ALB , Hub-spoke deployment, transit                VPC/vnet

  4. Security
      AWS:  (Cloud Directory, Cognito, Directory Service, IAM, GuardDuty, inspector, KMS, Resource Access Manager, cloudHSM, Certificate Manager, Secret Manager, VPC               logs & Packet sniffing, FW, WAF, Firewall manager, security hub, shield, SSO Manager
            IAM, AD SSO, cloudwatch+lambda+SNS, cloudtrail

      AZURE: (Application Gateway, Azure AD, Azure AD domain service, Azure DDoS Protection, key vault, Azure Dedicated HSM, Azure Frontdoor, Azure Information                     Protection, Defender, Sentinel (SIEM), FW, WAF, FW Manager, VPN Gateway)

  5.  Storage
      AWS:  (backup, CloudEndure Disaster Recovery, EFS infrequent Access, EFS standard, EBS, FSx file storage, EBS block, S3 object, S3 Galcier, Snowball, Snowball                Edge, Hybrid storage Gateway)

      AZURE: 
             file storage (Archive Storage, vFXT for Azure file storage, , Azure datalake storage, Azure datashare, Azure files, , Netapp Files, netapp cloud manager)
             object storage( Blob storage)
             volume storage( StorSimple)
             backup(Azure backup, vaeem backup & replication, azure backup as service)

  6.  Computing & autoscaling 
      AWS:  (AMI & Bootscrapping, ALB, NLB, CLB, GWLB, workload auto-scaling, Batch, EC2 auto-scale, Elastic container registry, Elastic Beanstalk, Elastic container                service(ECS), Elastic Kubernetes service(EKS), fargate mode, lambda
 
      AZURE: (VM OS image, Shared Image Gallery, VM storage, VM scale sets, VM disk encryption set, key vault, Azure powershell CLI, Resource Manager, Batch, Disk                 (Managed), function APP, cyclecloud HPC

  7.  Database
      AWS:   (Multi AZ RDS, RDS read-replicas, Elastics Memcached & Redis, Aurora, DynamoDB, ElastiCache, Athena, Neptune, Redshift, Database migration service
 
      AZURE: (Multi AZ SQL, SQL read-replicas, Azure Redis cache, CosmosDB, MariaDB, PostSQL, MYSQL, Data warehouse Elastic Job Agent, Instance pool, Database                       migration service)
 
             note: AWS Aurora=Azure MariaDB
                   AWS Dynamo DB= Azure CosmosDB
                   AWS Redis=Azure Redis

  8.  Caching
      AWS:   Cloudfront, S3, SSL certificate, encryption, caching performance optimization)

      AZURE: Frontdoor, bolb,  SSL certificate, encryption, caching performance optimization)

  9.  Database & server migration
      AWS: (application discovery service, CloudEndure Migration, Server migration service-/VMware/Hyper V/Azure connector, Database migration service(DMS)/schema                 mapping, Hybrid storage migration --storage GW(file GW, Volume GW, Tape GW),  data transfer service- datasync, snowball, snowball Edge, Snowball mobile

      AZURE: (Azure migration service-/VMware/Hyper V/Azure connector, database migration service (DMS)/schema mapping, Azure site recovery, Data Box

  10. Data Analystics
      AWS: Redshift, Athena, cloudsearch, data pipeline, elasticsearch service, EMR, Glue, Kensis data analytics, Kensis data firehose, Kensis data stream, Kensis                video streaming, Kensis, lake formation, quicksights, redshift

      AZURE: Analysis Service, Azure data explorer, powerBI, stream analysis job, Azure Synapse Analysis, DataBricks, Data Factory(ADF), Azure data Lake Analytics
             Note: Azure stream analysis job= AWS kensis firehose

  11. container, microservice, serverless

      AWS: (ECS-docker, EKS-Kubernetes, SNS, SQS, MQ, API GW,  lambda, step function, cloudwatch event integration, serverless application model)
            Microservice/serverless : APPsync, Eventbridge, MQ, SNS, SQS, step functions, fargate, batch 

      AZURE: (API Apps, API Management Service, Logical App, Service Bus, Service Bus Relay, Azure functions, container instances, AKS-Kubernetes, Azure virtual                   desktop, Batch, service fabric/microservices, VM Scale Sets, Service fabric Cluster, Service Fabric Mesh

  12. IaC deployment
      AWS:  Cloudformation , resource manager, System Manager, Patch manager (yalm,json, CFN-INIT, cfn-hup, cross-stack
      AWS DevOps tools: Codecommit, Codepipeline, Codebuilder, Codedeploy, Elastic Beanstalk

      AZURE: resource manager, powershell, CLI, json file
      Azure DevOps Tools: Azure DevOps, Pipeline, Repo, Testplan, DevTest Lab, Lab Service
             Note: IaC solution Terraform VS cloudformation VS ansible VS puppet VS chef

  13.  Governance, Monitoring & logging
      AWS: Auto Scaling, Budgets, Cloudformation, Cloudtrail, Cloudwatch, Config, Control Tower, Cost explorer, License Manager, Opsworks, Organization, System                    manager, Trusted Advisor, Well-architect tool, Cloudwatch, cloud trail

      AZURE: VM monitoring, Advisor, Automation account, Blueprint, Cost Alert, Cost Analysis, Management Group, Policy, AD, VM monitor, AD health check, SQL health                check, update management, 3 party tools Zabbix and solarwind


   14  Machine learning
      AWS: deep learning AMI, deep learning container, DeepLens, DeepRacer, tensorflow, sagemarker

      Azure: Batch AI, Bot Service, Cognitive Search, Cognitive Service, Genomics Account

   16. DR/BCP (cold, warm, politlight, equal, storage, computing, database, networking) 
       Azure: azure backup as service, veeam backup & replication 

17. cloud native serverless architecture 
monnlith application ( Web-logical-DB)

AWS 
APIGW(restful API/HTTP API) + Lambda function(Event Hub) + step function ( state machine)+ RDS+ DynomoDB+ Redis/Elastic inmemory+ cacheSQS/SQS/MQ+ S3/EBS/EFS+ IAM +coundfront CDN

Azure
API Management+ Event Hub+ Function APP(state machine)+ Cosmos DB+ Redis+Azure queue/storage Q+blob+ AD+ frontfoor CDN

Note:
Azure APi Management=AWS APi GW
Azure function APP= AWS step function
