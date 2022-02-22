# Amazon MSK

| **Component**    | **Modules**           | **Resource Identifiers** | **Binary version** | **Module version** | **Latest Module URI**                                                                            | **Changelog**                                                              |
|------------------|-----------------------|--------------------------|--------------------|--------------------|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| **Amazon MSK**           | `aws_msk_topic_per_broker_cloudwatch`       | `Cluster Name`, `Broker ID`, `Topic`                  | v0.1.0             | v0.0.1             | [Download](https://github.com/last9/openmetrics-registry/releases/download/v0.0.1/aws_topic_per_broker_cloudwatch_msk_msk_v0.0.1.hcl)          | [Changelog](https://github.com/last9/openmetrics-registry/blob/master/aws/cloudwatch/msk/CHANGELOG.md)           |
|               | `aws_msk_topic_per_consumer_grp_cloudwatch` | `Cluster Name`, `Consumer Group`, `Topic`              |                    |                    |                                                                                                                                    |                                                                                                     |
|               | `aws_msk_partition_cloudwatch`              | `Cluster Name`, `Consumer Group`, `Partition`, `Topic` |                    |                    |                                                                                                                                    |                                                                                                     |
|               | `aws_msk_cluster_cloudwatch`                | `Cluster Name`                                         |                    |                    |                                                                                                                                    |                                                                                                     |
|               | `aws_msk_broker_cloudwatch`                 | `Cluster Name`, `Broker ID`                            |                    |                    |                                                                                                                                    |                