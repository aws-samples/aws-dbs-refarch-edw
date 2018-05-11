# Integration with Amazon Quicksight

## Overview

[Amazon Quicksight](https://aws.amazon.com/quicksight) is a fast, cloud-powered business analytics service that makes it easy to build visualizations, perform ad-hoc analysis, and quickly get business insights from your data.

Quicksight natively integrates with Redshift [(and other data sources)](https://docs.aws.amazon.com/quicksight/latest/user/supported-data-sources.html) clusters in the same account as you've provisioned 

![quicksight integration](quicksight-viz.png)

## Walkthrough of the Architecture

1. The deployment architecture used for Quicksight integration is the same as for [public routing](../public-routing). Redshift is deployed into a Public Subnet in your VPC, with a Cluster Subnet Group that spans all Public Subnets in your VPC.
2. Redshift's Cluster Security Group is extended to include the [CIDR block range for Quicksight in the Region](https://docs.aws.amazon.com/quicksight/latest/user/regions.html).

## Learn More

You can learn more by following this [step-by-step guide](https://docs.aws.amazon.com/quicksight/latest/user/enabling-access-redshift.html).
