# Openmetrics-registry
Modules to be used by Openmetrics-exporter.

## What is Openmetrics-exporter?
Openmetrics-exporter is an Observability-as-Code software tool that reduces the toil of finding-and-combining useful metrics from layers and hundreds of components involved in modern Cloud-native systems. Every source, component, or metric is just a simple configuration file because the only “code” you should focus on is for your customers.

## What are Opemetrics-exporter modules?
Openmetrics-exporter modules are the reusable building blocks that scrape the information for standard cloud components, in the above case AWS components. Modules help organize, encapsulate and re-use configurations along with maintaining consistency. 

## How do I find the right module?
Please refer the tables below to find the right module for system components you want to Observe. 

### AWS Cloudwatch

| **Component** | **Modules**                               | **Resource Identifiers**                               | **Binary version** | **Module version** | **Latst Module URI**                                                                                                                | **Changelog**                                                                                       |
|---------------|-------------------------------------------|--------------------------------------------------------|--------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| **AWS ALB**           | `aws_alb_cloudwatch`                        | `LoadBalancer`                                           | v0.1.0             | v0.0.1             | [Download](https://github.com/last9/openmetrics-registry/releases/download/v0.0.1/aws_cloudwatch_alb_alb_v0.0.1.hcl)                           | [Changelog](https://github.com/last9/openmetrics-registry/blob/master/aws/cloudwatch/alb/CHANGELOG.md)           |
|               | `aws_alb_target_group_cloudwatch`           | `LoadBalancer`, `TargetGroup`                              |                    |                    |                                                                                                                                    |                                                                                                     |
| **Amazon API Gateway**  | `aws_apigateway_cloudwatch`                 | `ApiName`, `Stage`                                         | v0.1.0             | v0.0.1             | [Download](https://github.com/last9/openmetrics-registry/releases/download/v0.0.1/aws_cloudwatch_apigateway_apigateway_v0.0.1.hcl)             | [Changelog](https://github.com/last9/openmetrics-registry/blob/master/aws/cloudwatch/apigateway/CHANGELOG.md)    |
| **Amazon Aurora**        | `aws_aurora_instance_logical_cloudwatch `   | `DBInstanceIdentifier`                                   | v0.1.0             | v0.0.1             | [Download](https://github.com/last9/openmetrics-registry/releases/download/v0.0.1/aws_instance_logical_cloudwatch_aurora_aurora_v0.0.1.hcl)    | [Changelog](https://github.com/last9/openmetrics-registry/blob/master/aws/cloudwatch/aurora/CHANGELOG.md)        |
|               | `aws_aurora_instance_physical_cloudwatch`   | `DBInstanceIdentifier`                                   |                    |                    |                                                                                                                                    |                                                                                                     |
| **AWS Cloudfront**    | `aws_cloudfront_cloudwatch`                 | `DistributionId`, `Region`                             | v0.1.0             | v0.0.1             | [Download](https://github.com/last9/openmetrics-registry/releases/download/v0.0.1/aws_cloudwatch_cloudfront_cloudfront_v0.0.1.hcl)             | [Changelog](https://github.com/last9/openmetrics-registry/blob/master/aws/cloudwatch/cloudfront/CHANGELOG.md)    |
| **Amazon DAX**           | `aws_dax_cloudwatch`                        | `ClusterId`, `NodeId`                                      | v0.1.0             | v0.0.1             | [Download](https://github.com/last9/openmetrics-registry/releases/download/v0.0.1/aws_cloudwatch_dax_dax_v0.0.1.hcl)                           | [Changelog](https://github.com/last9/openmetrics-registry/blob/master/aws/cloudwatch/dax/CHANGELOG.md)           |
| **Amazon DynamoDb**      | `aws_dynamodb_table_operation_cloudwatch`   | `TableName`, `Operation`                                   | v0.1.0             | v0.0.1             | [Download](https://github.com/last9/openmetrics-registry/releases/download/v0.0.1/aws_cloudwatch_dynamodb_dynamodb_v0.0.1.hcl) | [Changelog](https://github.com/last9/openmetrics-registry/blob/master/aws/cloudwatch/dynamodb/CHANGELOG.md)      |
|               | `aws_dynamodb_table_cloudwatch`             | `TableName`                                              |                    |                    |                                                                                                                                    |                                                                                                     |
| **AWS EC2**           | `aws_ec2_cloudwatch`                        | `InstanceId`                                             | v0.1.0             | v0.0.1             | [Download](https://github.com/last9/openmetrics-registry/releases/download/v0.0.1/aws_cloudwatch_ec2_ec2_v0.0.1.hcl)                           | [Changelog](https://github.com/last9/openmetrics-registry/blob/master/aws/cloudwatch/ec2/CHANGELOG.md)           |
| **Amazon EKS**           | `aws_eks_cluster_cloudwatch`                | `ClusterName`                                            | v0.1.0             | v0.0.1             | [Download](https://github.com/last9/openmetrics-registry/releases/download/v0.0.1/aws_cloudwatch_eks_eks_v0.0.1.hcl)                   | [Changelog](https://github.com/last9/openmetrics-registry/blob/master/aws/cloudwatch/eks/CHANGELOG.md)           |
|               | `aws_eks_service_cloudwatch`                | `ClusterName`, `Namespace`, `Service`                        |                    |                    |                                                                                                                                    |                                                                                                     |
|               | `aws_eks_pod_cloudwatch`                    | `ClusterName`, `Namespace`, `PodName`                        |                    |                    |                                                                                                                                    |                                                                                                     |
|               | `aws_eks_node_cloudwatch `                  | `ClusterName`, `NodeName`, `InstanceId`                     |                    |                    |                                                                                                                                    |                                                                                                     |
| **Amazon ElastiCache** | `aws_elasticache_redis_cloudwatch`          | `CacheClusterId`                                         | v0.1.0             | v0.0.1             | [Download](https://github.com/last9/openmetrics-registry/releases/download/v0.0.1/aws_cloudwatch_elasticache_elasticache_v0.0.1.hcl)     | [Changelog](https://github.com/last9/openmetrics-registry/blob/master/aws/cloudwatch/elasticache/CHANGELOG.md)   |
|               | `aws_elasticache_cluster_cloudwatch`        | `CacheClusterId`                                         |                    |                    |                                                                                                                                    |                                                                                                     |
| **Amazon Elasticsearch** | `aws_elasticsearch_cloudwatch`              | `ClientId`, `DomainName`                               | v0.1.0             | v0.0.1             |[Download](https://github.com/last9/openmetrics-registry/releases/download/v0.0.1/aws_cloudwatch_elasticsearch_elasticsearch_v0.0.1.hcl)       | [Changelog](https://github.com/last9/openmetrics-registry/blob/master/aws/cloudwatch/elasticsearch/CHANGELOG.md) |
|               | `aws_elasticsearch_master_cloudwatch`       | `ClientId`, `DomainName`                              |                    |                    |                                                                                                                                    |                                                                                                     |
| **Amazon ELB**           | `aws_elb_cloudwatch`                        | `LoadBalancerName`                                       | v0.1.0             | v0.0.1             | [Download](https://github.com/last9/openmetrics-registry/releases/download/v0.0.1/aws_cloudwatch_elb_elb_v0.0.1.hcl)                           | [Changelog](https://github.com/last9/openmetrics-registry/blob/master/aws/cloudwatch/elb/CHANGELOG.md)           |
| **AWS Lambda**        | `aws_lambda_cloudwatch`                     | `FunctionName`                                           | v0.1.0             | v0.0.1             | [Download](https://github.com/last9/openmetrics-registry/releases/download/v0.0.1/aws_cloudwatch_lambda_lambda_v0.0.1.hcl)                     | [Changelog](https://github.com/last9/openmetrics-registry/blob/master/aws/cloudwatch/lambda/CHANGELOG.md)        |
| **Amazon MSK**           | `aws_msk_topic_per_broker_cloudwatch`       | `Cluster Name`, `Broker ID`, `Topic`                  | v0.1.0             | v0.0.1             | [Download](https://github.com/last9/openmetrics-registry/releases/download/v0.0.1/aws_cloudwatch_msk_msk_v0.0.1.hcl)          | [Changelog](https://github.com/last9/openmetrics-registry/blob/master/aws/cloudwatch/msk/CHANGELOG.md)           |
|               | `aws_msk_topic_per_consumer_grp_cloudwatch` | `Cluster Name`, `Consumer Group`, `Topic`              |                    |                    |                                                                                                                                    |                                                                                                     |
|               | `aws_msk_partition_cloudwatch`              | `Cluster Name`, `Consumer Group`, `Partition`, `Topic` |                    |                    |                                                                                                                                    |                                                                                                     |
|               | `aws_msk_cluster_cloudwatch`                | `Cluster Name`                                         |                    |                    |                                                                                                                                    |                                                                                                     |
|               | `aws_msk_broker_cloudwatch`                 | `Cluster Name`, `Broker ID`                            |                    |                    |                                                                                                                                    |                                                                                                     |
| **AWS NLB**           | `aws_nlb_cloudwatch`                        | `LoadBalancer`                                           | v0.1.0             | v0.0.1             | [Download](https://github.com/last9/openmetrics-registry/releases/download/v0.0.1/aws_cloudwatch_nlb_nlb_v0.0.1.hcl)                           | [Changelog](https://github.com/last9/openmetrics-registry/blob/master/aws/cloudwatch/nlb/CHANGELOG.md)           |
| **Amazon RDS**           | `aws_rds_cloudwatch`                        | `DBInstanceIdentifier`                                   | v0.1.0             | v0.0.1             | [Download](https://github.com/last9/openmetrics-registry/releases/download/v0.0.1/aws_cloudwatch_rds_rds_v0.0.1.hcl)                         | [Changelog](https://github.com/last9/openmetrics-registry/blob/master/aws/cloudwatch/rds/CHANGELOG.md)           |
| **Amazon SQS**           | `aws_sqs_cloudwatch`                        | `QueueName`                                              | v0.1.0             | v0.0.1             | [Download](https://github.com/last9/openmetrics-registry/releases/download/v0.0.1/aws_cloudwatch_sqs_sqs_v0.0.1.hcl)                           | [Changelog](https://github.com/last9/openmetrics-registry/blob/master/aws/cloudwatch/sqs/CHANGELOG.md)           |


### GCP Stackdriver

| **Component**    | **Modules**           | **Resource Identifiers** | **Binary version** | **Module version** | **Latest Module URI**                                                                            | **Changelog**                                                              |
|------------------|-----------------------|--------------------------|--------------------|--------------------|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| **Google Cloud SQL** | `gcp_cloudsql_logical`  | NA                       | v0.1.0             | v0.0.1             | [Download](https://github.com/last9/openmetrics-registry/releases/download/v0.0.1/gcp_cloudsql_v0.0.1.hcl) | [Changelog](https://github.com/last9/openmetrics-registry/blob/master/gcp/CHANGELOG.md) |
|                  | `gcp_cloudsql_physical` |


## Learn more about Openmetrics-exporter
- [What is Openmetrics-exporter?](https://last9.notion.site/openmetrics-exporter-06e2b2f0ae404968b4238c32257acc0c)


