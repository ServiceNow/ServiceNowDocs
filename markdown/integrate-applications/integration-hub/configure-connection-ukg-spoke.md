---
title: Configure a connection for the UKG spoke
description: Add and configure a connection using the UKG spoke connection template in Flow Designer to authenticate ServiceNow requests to your Kronos instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/configure-connection-ukg-spoke.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [UKG Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Configure a connection for the UKG spoke

Add and configure a connection using the UKG spoke connection template in Flow Designer to authenticate ServiceNow requests to your Kronos instance.

## Before you begin

Request an Integration Hub subscription.

Activate the UKG Spoke.

Role required: admin

**Note:** If you're updating from a previous version \(before version 3.3.0\) of the spoke, first you must remove the current connection record, credentials record, and Kronos user credentials. Then, you can set up the connection.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select the **Connections** tab.

3.  Locate the **UKG connection** alias and select **View Details**.

    **Note:** Don't select **Add Connection**.

    \[Omitted image "ukg-spoke-conn-template.png"\] Alt text: Connection template for UKG spoke.

4.  Select **Edit**.

    If you're configuring the spoke for the first time, select **Configure**.\[Omitted image "ukg-spoke-config-conn.png"\] Alt text: Configure a connection for the UKG spoke

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to uniquely identify the connection record. For example, enter Kronos Conn.|
    |Connection URL|URL of the Kronos instance.|
    |App Key|Application key of the Kronos instance.|
    |OAuth Entity Name|Unique name to identify the OAuth entity profile of the UKG spoke. For example, select `UKG OAuth entity`.|
    |OAuth Client ID|Client ID created during the application configuration in Kronos.|
    |OAuth Client Secret|Client Secret created during the application configuration in Kronos.|
    |Token URL|OAuth server token endpoint. For example, `https://<Kronos-Instance>.com/api/authentication/access_token`.|

6.  Select **Configure and Get OAuth Token**.

    A modal page displays to enter your Kronos credentials.

7.  Enter your Kronos username and password and select **Get OAuth Token**.


## Result

Once your OAuth token has been successfully fetched, you can begin using your UKG spoke connection.

