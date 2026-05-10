---
title: Enable mapping for Cloud Os Image in AWS
description: Enable the sn\_cmdb\_ci\_class.use\_single\_cloud\_os\_image system property to add Cloud Os Image data to the Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table instead of adding the data to the Image \[cmdb\_ci\_os\_template\] table.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Additional features, AWS, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Enable mapping for Cloud Os Image in AWS

Enable the **sn\_cmdb\_ci\_class.use\_single\_cloud\_os\_image** system property to add Cloud Os Image data to the Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table instead of adding the data to the Image \[cmdb\_ci\_os\_template\] table.

## Before you begin

Set the application scope to Service Graph Connector for AWS using the application picker. For more information, see [Application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_ApplicationPicker.md).

Role required: admin

## About this task

In Service Graph Connector for AWS version 2.9.1 and earlier, the Cloud Os Image data was added to the Image \[cmdb\_ci\_os\_template\] table. Multiple records were created for the same image because the Image \[cmdb\_ci\_os\_template\] table is a dependent class. In Service Graph Connector for AWS version 2.10.0 and later, Cloud Os Image data is added to the Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table, which is an independent class, when the **sn\_cmdb\_ci\_class.use\_single\_cloud\_os\_image** system property is enabled.

## Procedure

1.  Enter `sys_properties.list` in the navigation filter, and then open the **sn\_cmdb\_ci\_class.use\_single\_cloud\_os\_image** property.

2.  In the **Value** field, enter `true`.

3.  Select **Update**.


