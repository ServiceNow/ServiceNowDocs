---
title: Set up the Dun and Bradstreet DirectPlus spoke
description: Integrate the ServiceNow instance and Dun and Bradstreet Direct+ by using the client ID and client secret credentials to authenticate ServiceNow requests.Add and configure a Dun and Bradstreet DirectPlus connection to authenticate ServiceNow requests.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Dun and Bradstreet DirectPlus Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Dun and Bradstreet DirectPlus spoke

Integrate the ServiceNow instance and Dun and Bradstreet Direct+ by using the client ID and client secret credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate Dun and Bradstreet DirectPlus spoke.
-   Role required: admin

## Configure a connection for Dun and Bradstreet DirectPlus spoke

Add and configure a Dun and Bradstreet DirectPlus connection to authenticate ServiceNow requests.

### Before you begin

-   Get the client ID and client secret of your Dun and Bradstreet account from the account administrator.
-   Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **DunAndBradstreet** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Dun and Bradstreet DirectPlus spoke, click **View Details**.![Dun and Bradstreet connection template](../image/d-and-b-spoke-conn-template.png)
    -   To manage more than one Dun and Bradstreet DirectPlus connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    ![Dun and bradstreet spoke connection configuration](../image/d-and-b-conn-temp-config.png)

5.  On the **Configure Connection** form, fill in the fields:

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the connection record. For example, `Dun and Bradstreet Directplus connection`|
    |Connection URL|URL of the Dun and Bradstree Direct+ instance. Enter `https://plus.dnb.com`.|
    |Client ID|Client ID of your Dun and Bradstreet DirectPlus account.|
    |Client Secret|Client secret of your Dun and Bradstreet DirectPlus account.|

    ![Dun and bradstreet connection template form](../image/d-and-b-connection-form.png)

6.  Click **Configure Configure and Get OAuth Token**.


### Result

The spoke connection is configured and ready to be used.

