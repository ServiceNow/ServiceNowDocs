---
title: Handling import failures for large AWS resources
description: Manage the data source failure when importing resources from AWS.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Additional features, AWS, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Handling import failures for large AWS resources

Manage the data source failure when importing resources from AWS.

When importing large AWS resources, the data sources in the Service Graph Connector for AWS might fail because of a Direct REST response exceeding the 1024-MB limit. For more information, see [REST step](https://www.servicenow.com/docs/access?context=rest-request-action-designer&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

You can save the response as an attachment to handle the REST response size limitation error in the Service Graph Connector for AWS.

## Save the response as an attachment

With the save response as an attachment feature, the response of each data source is temporarily stored as an attachment and after the response is read, the attachment is deleted automatically. The save response as an attachment feature is activated by default and is triggered by the **sn\_aws\_integ.save\_payload\_as\_attachment** system property.

As a user with the admin role, you can deactivate the save response as an attachment feature by setting the **sn\_aws\_integ.save\_payload\_as\_attachment** property to `false`. When the feature is deactivated and the response size is within the limit, the data sources run normally.

