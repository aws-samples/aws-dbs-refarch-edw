# AWS Reference Architectures - Amazon Redshift

Amazon Redshift is a fast, fully managed data warehouse that makes it simple and cost-effective to analyze all your data using standard SQL and your existing Business Intelligence (BI) tools. It allows you to run complex analytic queries against petabytes of structured data, using sophisticated query optimization, columnar storage on high-performance local disks, and massively parallel query execution.

This project provides you with an overview of the most common deployment models and reference architectures that we see built by customers with the Redshift service. Redshift is extremely flexible, and able to be run both within VPC and in EC2 Classic networking environments. These reference architectures only assume that you run the service within VPC, which offers significant security, simplicity, and performance benefits over non-VPC deployments. We start with simple deployment models, and then move to other types of use cases and data integrations.

## Data Architectures

## Deployment Architectures

Because AWS Services are designed to work together, the service is largely consistent in how it's deployed, and you don't have to make many architectural decisions. However, you do have to decide how to deploy them within your VPC. The following architectures provide common patterns for how customers deploy 

### [Simple, Single Cluster with Public Routing](public-routing)

<table><tr><td><a href="https://github.com/aws-samples/aws-dbs-refarch-redshift/tree/master/public-routing"><img src="https://github.com/aws-samples/aws-dbs-refarch-redshift/blob/master/public-routing/thumbnail.png"/></a></td><td>

This the most basic architecture that we recommend to be used with Amazon Redshift. It uses simple public routing, and enables high availability. Click the thumbnail for more information.

</td></tr></table>

### [Single Cluster with Private (DirectConnect) Routing](private-routing)

<table><tr><td><a href="https://github.com/aws-samples/aws-dbs-refarch-redshift/tree/master/private-routing"><img src="https://github.com/aws-samples/aws-dbs-refarch-redshift/blob/master/private-routing/thumbnail.png"/></a></td><td>

This is perhaps the most common deployment architecture for Redshift clusters - deployed within private subnets in VPC that are only accessible over DirectConnect.

</td></tr></table>

## Architectures for Scaling

### [Multiple Business Line Clusters](business-line-clusters)

<table><tr><td><a href="https://github.com/aws-samples/aws-dbs-refarch-redshift/tree/master/business-line-clusters"><img src="https://github.com/aws-samples/aws-dbs-refarch-redshift/blob/master/business-line-clusters/thumbnail.png"/></a></td><td>

This the most basic architecture that we recommend to be used with Amazon Redshift. It uses simple public routing, and enables high availability. Click the thumbnail for more information.

</td></tr></table>

### [Redshift Spectrum based Multi-Cluster](spectrum-multicluster)

<table><tr><td><a href="https://github.com/aws-samples/aws-dbs-refarch-redshift/tree/master/spectrum-multicluster"><img src="https://github.com/aws-samples/aws-dbs-refarch-redshift/blob/master/spectrum-multicluster/thumbnail.png"/></a></td><td>

This the most basic architecture that we recommend to be used with Amazon Redshift. It uses simple public routing, and enables high availability. Click the thumbnail for more information.

</td></tr></table>

### [Low Latency Hybrid Architecture](high-performance-hybrid)

<table><tr><td><a href="https://github.com/aws-samples/aws-dbs-refarch-redshift/tree/master/high-performance-hybrid"><img src="https://github.com/aws-samples/aws-dbs-refarch-redshift/blob/master/high-performance-hybrid/thumbnail.png"/></a></td><td>

This the most basic architecture that we recommend to be used with Amazon Redshift. It uses simple public routing, and enables high availability. Click the thumbnail for more information.

</td></tr></table>

## Integrating with Other AWS Services

### [Connecting with AWS Lambda](lambda-connections)

<table><tr><td><a href="https://github.com/aws-samples/aws-dbs-refarch-redshift/tree/master/lambda-connections"><img src="https://github.com/aws-samples/aws-dbs-refarch-redshift/blob/master/lambda-connections/thumbnail.png"/></a></td><td>

This the most basic architecture that we recommend to be used with Amazon Redshift. It uses simple public routing, and enables high availability. Click the thumbnail for more information.

</td></tr></table>

### Loading data with Kinesis Firehose

### [Access from Amazon Quicksight](quicksight-connections)

<table><tr><td><a href="https://github.com/aws-samples/aws-dbs-refarch-redshift/tree/master/quicksight-connections"><img src="https://github.com/aws-samples/aws-dbs-refarch-redshift/blob/master/quicksight-connections/thumbnail.png"/></a></td><td>

This the most basic architecture that we recommend to be used with Amazon Redshift. It uses simple public routing, and enables high availability. Click the thumbnail for more information.

</td></tr></table>

## License Summary

This sample code is made available under a modified MIT license. See the LICENSE file.
