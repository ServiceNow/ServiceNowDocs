---
title: Enable optimized SG-AWS-SendCommand data source performance
description: When the SG-AWS-Software-Inventory data source is being used, enable the sn\_aws\_integ.is\_software\_inventory\_enabled system property for optimizing the performance of the SG-AWS-SendCommand and SG-AWS-SSM-GetS3Object data sources.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-03"
reading_time_minutes: 1
breadcrumb: [Additional features, AWS, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Enable optimized SG-AWS-SendCommand data source performance

When the SG-AWS-Software-Inventory data source is being used, enable the **sn\_aws\_integ.is\_software\_inventory\_enabled** system property for optimizing the performance of the SG-AWS-SendCommand and SG-AWS-SSM-GetS3Object data sources.

## Before you begin

**Important:** The **sn\_aws\_integ.is\_software\_inventory\_enabled** system property is not supported in Service Graph Connector for AWS version 2.10.0 and later.

Set the application scope to Service Graph Connector for AWS using the application picker. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

Role required: admin

## About this task

The SG-AWS-SendCommand and SG-AWS-SSM-GetS3Object data sources use SSM GetInventory API calls for importing software data, impacting performance. To enhance the performance of the SG-AWS-SendCommand and SG-AWS-SSM-GetS3Object data sources, consider leveraging the SG-AWS-Software-Inventory data source by enabling the **sn\_aws\_integ.is\_software\_inventory\_enabled** system property.

This optimization skips a substantial number of SSM GetInventory API calls, enhancing the performance of the SG-AWS-SendCommand and SG-AWS-SSM-GetS3Object data sources. However, the SG-AWS-SendCommand and SG-AWS-SSM-GetS3Object data sources import data from the same servers that are configured for the SG-AWS-Software-Inventory data source.

By default, the **sn\_aws\_integ.is\_software\_inventory\_enabled** property is set to `false`. To enhance the performance of the SG-AWS-SendCommand and SG-AWS-SSM-GetS3Object data sources, set the **sn\_aws\_integ.is\_software\_inventory\_enabled** property to `true`.

## Procedure

1.  Enter `sys_properties.list` in the navigation filter, and then open the **sn\_aws\_integ.is\_software\_inventory\_enabled** property.

2.  In the **Value** field, enter `true`.

3.  Select **Update**.


