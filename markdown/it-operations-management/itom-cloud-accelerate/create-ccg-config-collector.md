---
title: Create a configuration collector
description: Create a configuration collector to set up how Cloud Configuration Governance imports the configuration data from the cloud. The configuration collector uses Integration Hub subflows to import the configuration data from the cloud.
locale: en-US
release: zurich
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Cloud Configuration Governance policies, Using Cloud Configuration Governance, Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create a configuration collector

Create a configuration collector to set up how Cloud Configuration Governance imports the configuration data from the cloud. The configuration collector uses Integration Hub subflows to import the configuration data from the cloud.

## Before you begin

-   Ensure that Cloud Configuration Governance contains suitable configuration keys for all the configuration values that you want to import from the cloud. Create a configuration key if it is not available in the application. For more information, see [Create a configuration key](create-ccg-config-key.md).

Role required: sn\_itom\_ccg.governor

## About this task

For some cloud resources, the required configuration data is available at the cloud resource level. Therefore, create a configuration collector only if the required configuration data is not available at the cloud resource level.

For example, most of the configuration data of the **Virtual Machine Instance** resource type are available at the cloud resource level. Therefore, a configuration collector is not implemented to import these configurations.

Refer to a base system configuration collector as an example for creating the configuration collectors.

## Procedure

1.  Create an Integration Hub subflow for the configuration collector.

    1.  Copy the **CCG – Collector Template** subflow.

        For more information on copying templates, see [Copy an Integration Hub subflow template](copy-ih-subflow-template.md).

    2.  Add the **CCG - Get Resources** action and fill in the fields.

    3.  Add the appropriate Cloud Action Library \(CAL\) action and flow logic to read the configuration data.

        **Note:**

        For more information on the available CAL actions, see [Cloud Action Library actions reference](../reference/ccg-cal-actions.md).

        If CAL doesn’t have the required action, you can refer to an existing CAL action and use the Integration Hub REST step to implement the custom action. For more information, see [REST step](https://www.servicenow.com/docs/access?context=rest-request-action-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

    4.  Add the **CCG – Insert Configuration Settings** action to insert the configuration data to the Configuration Management Database \(CMDB\).

    5.  Select **Publish**.

2.  Navigate to **Cloud Configuration Governance** &gt; **Configuration Collector**.

3.  Select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Provider type|Cloud that hosts the resources to be scanned through the policies.|
    |Flow|Configuration collector that can import the configuration data from the cloud.|
    |Resource type|Cloud resource type whose configuration you want to import|
    |Name|Name of the configuration collector.|
    |Description|Brief description of the configuration collector.|

5.  Select **Submit**.


