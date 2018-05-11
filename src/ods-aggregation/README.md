# Operational Data Store Consolidation and Aggregation

## Overview

Many data warehouses will bring operational system data into a single environment using the same structure as the source, and then collapse this data into a format which is more suitable for querying in aggregated form.

![ODS & Aggregation](ods-aggregation.png | width=750)

## Walkthrough of the Architecture

1. Source databases, whether on-premises or on AWS are replicated to Amazon Redshift using the [Database Migration Service](https://aws.amazon.com/dms). This service connects to the source system [Change Data Capture logs](https://aws.amazon.com/blogs/database/migrate-postgresql-databases-and-perform-ongoing-replication-with-the-aws-database-migration-service), or uses [SCT Extraction Agents](https://aws.amazon.com/blogs/database/introducing-data-extractors-in-aws-schema-conversion-tool-version-1-0-602) to extract data from the source systems
2. Source data is placed into schemas on Amazon Redshift that are mirror copies of the source systems. DMS replicates not just the data changes, but also any schema structure changes (for sources which support CDC replication).
3. Aggregation tables for raw events may be created within each source schema in Redshift, or alternatively a [Star Schema](../star-schema) may be used to create a more structured analytical system
4. Data is transformed from the source schemas to the target tables using a third-party ETL tool or pushdown SQL transformation.
