---
title: Additional features within the Service Graph Connector for AWS
description: Use the additional features available within the Service Graph Connector for AWS to maximize its use for importing data.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2025-04-27"
reading_time_minutes: 2
breadcrumb: [AWS, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Additional features within the Service Graph Connector for AWS

Use the additional features available within the Service Graph Connector for AWS to maximize its use for importing data.

The following features are available within the Service Graph Connector for AWS:

-   **[Enabling optimized deletion of retired CIs in AWS](../task/sgc-cmdb-aws-delete-cis.md)**

    Enable the **sn\_aws\_integ.enableOptimizedDeletion** system property for the optimized deletion of retired configuration items \(CIs\) in AWS during delta import of data.

-   **[Enabling optimized SG-AWS-SendCommand data source performance](../task/sgc-cmdb-aws-ssm-prop.md)**

    When using the SG-AWS-Software-Inventory data source, enable the **sn\_aws\_integ.is\_software\_inventory\_enabled** system property for optimizing the performance of the SG-AWS-SendCommand and SG-AWS-SSM-GetS3Object data sources.

-   **[Handling import failures for large AWS resources](sgc-cmdb-aws-large-data-vol.md)**

    Manage the data source failure when importing resources from AWS.

-   **[Handling memory utilization errors for Service Graph Connector for AWS](sgc-cmdb-aws-memory.md)**

    Avoid the memory utilization errors when using the Service Graph Connector for AWS to import a large number of CIs from an AWS instance.


-   **[Setting up partition size with parallel loading enabled](../task/sgc-aws-partition-size-prop.md)**

    Optimize the performance of the SG-AWS-Image-Private, SG-AWS-Tags, SG-AWS-SendCommand, and AWS-SSM-GetS3Object data sources by configuring the partition size setting in the **aws\_account\_partition\_size** connection property.

-   **[Disable parallel loading for Service Graph Connector for AWS data sources](../task/sgc-aws-disable-parallel-loading.md)**

    Disable parallel loading for specific data sources in the Service Graph Connector for AWS.

-   **[Handling parallel deletion of CIs in Service Graph Connector for AWS](sgc-cmdb-aws-parallel-deletion.md)**

    Optimize performance when using the Service Graph Connector for AWS by enabling the parallel deletion of CIs.

-   **[Enable mapping for Cloud Os Image in AWS](../task/sgc-cmdb-aws-map-cloud-data.md)**

    Enable mapping of AWS Cloud Os Image data to the Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table.


