---
title: Set up the Craft spoke
description: Integrate the ServiceNow instance and Craft spoke by using the basic authentication to authenticate ServiceNow requests.Add and configure a Craft spoke connection to authenticate ServiceNow requests.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-11-04"
reading_time_minutes: 1
breadcrumb: [Craft spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the Craft spoke

Integrate the ServiceNow instance and Craft spoke by using the basic authentication to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate Craft spoke.
-   Role required: admin

## Configure a connection for Craft spoke

Add and configure a Craft spoke connection to authenticate ServiceNow requests.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio.**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **sn\_craft\_spoke** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Azure DevOps Boards spoke, click **View Details**.![Craft spoke connection template details](../image/craft-spoke-conn-template.png)
    -   To manage more than one Azure DevOps Boards spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    ![Craft spoke connection template configuration for the first time](../image/craft-spoke-conn-temp-config.png)

5.  On the **Configure Connection** form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection name|Name to uniquely identify the connection record. For example, `Craft connection`.|
    |Connection URL|URL of the Craft instance. For example, enter the URL in this format: `https:://api.craft.co/`|
    |API Key|API key from your Craft account.|

    ![Craft spoke connection template configuration form](../image/craft-spoke-conn-temp-form.png)

6.  Click **Configure Connection**.


### Result

The spoke connection is configured and ready to be used.

