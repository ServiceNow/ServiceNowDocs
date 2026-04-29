---
title: Create an SAP ECC connection
description: Establish a zero copy connection to an SAP ECC system in Zero Copy Connector Hub.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SAP ECC, Primary connectors, Zero Copy Connectors, Workflow Data Fabric]
---

# Create an SAP ECC connection

Establish a zero copy connection to an SAP ECC system in Zero Copy Connector Hub.

## Before you begin

Role required: df\_connection\_admin

## Procedure

1.  Navigate to the available primary connectors in Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Workflow Data Fabric Hub** &gt; **Available connectors** &gt; **Primary connectors**.
    -   Navigate to **Admin** &gt; **Workflow Data Fabric Hub** &gt; **Available connectors** &gt; **Primary connectors**.
2.  Find the SAP ECC connector and select **Connect**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name and description|
    |Connection label|Unique name for this connection. This helps in identifying the connection within your system.|
    |Connection name|System-generated name based on the Connection label. This field cannot be modified once the connection is established.|
    |Short description|Description of the connection explaining what it is about.|
    |Connection attributes|
    |Instance URL|URL of your local instance.|
    |Authentication methods|
    |ServiceNow username|Username of the current user accessing your local instance.|
    |ServiceNow user password|Password of the current user accessing your local instance.|

4.  Select **Connect**.


## Result

A test connection is made to the external data source, verifying that the connection details are correct and the data source is accessible.

## What to do next

If the connection succeeds, configure data steward access on the **Access Control** tab. See .

If the connection fails, verify the connection details with your data source administrator and try again.

