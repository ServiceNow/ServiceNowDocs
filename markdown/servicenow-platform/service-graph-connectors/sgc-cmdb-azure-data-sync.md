---
title: Configuring data synchronization in Service Graph Connector for Microsoft Azure
description: You can configure the system property for synchronizing only delta data from an Azure instance.Disable delta synchronization to import all the Microsoft Azure data.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2025-10-14"
reading_time_minutes: 2
breadcrumb: [Additional features, Microsoft Azure, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configuring data synchronization in Service Graph Connector for Microsoft Azure

You can configure the system property for synchronizing only delta data from an Azure instance.

The connector provides the ability to import only delta data from an Azure instance. With delta synchronization enabled, the importing process of Azure data is quicker because the connector imports the changes in Azure data only.

For data sources discovered by a software connection, the **Last Run Datetime** field displays the timestamp of the most recent delta pull run. The **Last Run Datetime** field is updated only when the last delta pull run was a success. An empty **Last Run Datetime** field indicates no previous delta pull run for the data source, but either a full pull run or no run at all. The delta pull period is calculated by subtracting the last run date and time from the current date and time; that is, Delta period = Current date timestamp - Last run date timestamp.

For data sources discovered by a hardware connection, the **Last Success Import Time** field displays the timestamp of the most recent delta pull run. The **Last Success Import Time** field is updated only when the last delta pull run was a success. An empty **Last Success Import Time** field indicates no previous delta pull run for the data source, but either a full pull run or no run at all. The delta pull period is calculated by subtracting the last successful import date and time from the current date and time; that is, Delta period = Current date timestamp - Last success import date timestamp.

The application includes the **sn\_sg\_azure\_integ.is\_delta\_sync\_enabled** system property to enable delta synchronization. By default, the property is set to `true`. To import full data from your Azure instance, disable the **sn\_sg\_azure\_integ.is\_delta\_sync\_enabled** property. See [Disable delta synchronization](sgc-cmdb-azure-data-sync.md#).

For a delta pull, you can also configure the grace time, page size, preceding time period, and API call duration using system properties. For more information, see [Service Graph Connector for Microsoft Azure properties](../reference/cmdb-sgc-azure-props.md).

## Disable delta synchronization

Disable delta synchronization to import all the Microsoft Azure data.

### Before you begin

Set the application scope to Service Graph Connector for Microsoft Azure using the application picker. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

Role required: admin

### Procedure

1.  Enter `sys_properties.list` in the navigation filter, and then open the **sn\_sg\_azure\_integ.is\_delta\_sync\_enabled** property.

2.  In the **Value** field, enter `false`.

3.  Select **Update**.


