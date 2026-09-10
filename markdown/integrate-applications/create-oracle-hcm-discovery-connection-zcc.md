---
title: Create an Oracle HCM \(Discovery\) connection
description: Establish a zero copy connection to an external Oracle HCM account in Zero Copy Connector Hub.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/create-oracle-hcm-discovery-connection-zcc.html
release: australia
topic_type: task
last_updated: "2026-08-24"
reading_time_minutes: 1
breadcrumb: [Oracle HCM \(Discovery\), Primary connectors, Zero Copy Connectors, Workflow Data Fabric]
---

# Create an Oracle HCM \(Discovery\) connection

Establish a zero copy connection to an external Oracle HCM account in Zero Copy Connector Hub.

## Before you begin

1.  Check your entitlements to determine whether you have access to the Workflow Data Fabric foundation entitlement, which provides eligibility for the REST Config connector download option.
2.  Install the REST Config Framework plugin.
3.  Install the Oracle HCM plugin.

The Oracle HCM Discovery connector appears in the Zero Copy Connector Hub UI only after both plugins are installed.

Role required: df\_connection\_admin

## About this task

Work with your data source admin to create a connection to Oracle HCM \(Discovery\).

## Procedure

1.  Navigate to the available primary connectors in Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Zero Copy Connector Hub** &gt; **Available connectors** &gt; **Primary connectors**.
    -   Navigate to **Admin** &gt; **Zero Copy Connector Hub** &gt; **Available connectors** &gt; **Primary connectors**.
2.  Find the Oracle HCM \(Discovery\) connector and select **Connect**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name and description|
    |Connection label|Unique name for this connection. This helps in identifying the connection within your system.|
    |Connection name|System-generated name based on the Connection label. This field cannot be modified once the connection is established.|
    |Short description|Description of the connection explaining what it is about.|
    |Connection Details|
    |Connection Alias|The connection alias that identifies the HTTP connection for this connector.|

4.  Select **Connect**.


## Result

A test connection is made to the external data source, verifying that the connection details are correct and the data source is accessible.

## What to do next

If the connection succeeds, configure data steward access on the **Access Control** tab. See [Manage access to an established connection using roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/manage-access-connection-zcc.md).

If the connection fails, verify the connection details with your data source administrator and try again.

