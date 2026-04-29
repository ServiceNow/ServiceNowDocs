---
title: Set up the BigFix Inventory spoke
description: Integrate the ServiceNow instance and the BigFix Inventory using an API key for authenticating ServiceNow requests.Generate an API key that enables your ServiceNow instance to request access to the BigFix Inventory instance.Configure the connection and credential record that contains the information to request access to the BigFix Inventory instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [BigFix Inventory Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the BigFix Inventory spoke

Integrate the ServiceNow instance and the BigFix Inventory using an API key for authenticating ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the BigFix Inventory spoke.
-   BigFix Inventory administrator access to the BigFix Inventory portal.
-   Role required: admin.

## Generate an API key

Generate an API key that enables your ServiceNow instance to request access to the BigFix Inventory instance.

### Before you begin

BigFix Inventory requirements:

-   BigFix Inventory account
-   Role required: BigFix Inventory administrator

Complete these steps from your BigFix Inventory environment. For more information on installation and configuration, see [BigFix V9.5 Inventory Documentation](https://help.hcltechsw.com/bigfix/9.5/inventory/welcome/BigFix_Inventory_welcome.html).

### Procedure

1.  Log in to your BigFix Inventory portal.

2.  On the Overview page, select the Profile icon \(![Profile icon.](../image/bigfix-inventory-spoke-profile-icon.png)\).![BigFix Inventory portal Overview page.](../image/bigfix-inventory-spoke-overview-page.png)

3.  Select Profile.

4.  On the Edit User page, select the Show token link in the API Token field.![Show token link in the API Token field.](../image/bigfix-inventory-spoke-api-token-link.png)

5.  Copy the API token and store at a secure place.

6.  Navigate to **Management** &gt; **Configuration** &gt; **Mail Setting**.

7.  Configure the mail settings.

    ![Mail settings.](../image/bigfix-mailsettings.png)

8.  Schedule exports of the required reports.

    1.  Navigate to the required report under **Reports**, for example, **Computers**.

        ![BigFix reports.](../image/bigfix-report.png)

    2.  Select **Schedule Export**.

        ![Schedule export.](../image/bigfix-comp-rep.png)

    3.  On the form, specify the ServiceNow instance email address to which the report must be sent and the frequency and time at which the report must be emailed.

        ![Schedule Export configurations.](../image/bigfix-scheduleexp.png)

    4.  Save the configurations.


## Configure the connection and credential record

Configure the connection and credential record that contains the information to request access to the BigFix Inventory instance.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select Connections.

3.  Turn on the Outbound tab.

4.  In the Search all connections field, enter `BigFix Inventory`.

5.  On the BigFix\_Inventory card, select **View Details**.

6.  Select **Configure**.

7.  Fill the form.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name of the connection established with the BigFix Inventory instance. The first connection's default name is automatically assigned to match the name specified in the Connections and Credentials form on the Connection &amp; Credential Aliases page. To provide your custom name, create a connection record by selecting **Add Connection**.|
    |Connection URL|The URL your ServiceNow instance uses to connect to the BigFix Inventory instance.|
    |API Key|The key that your ServiceNow instance requires to access the BigFix Inventory instance. Enter the API key that you had generated in the BigFix Inventory portal. To learn how to generate an API key, see [Generate an API key](setup-bigfix.md#).|

8.  Select **Configure Connection**.

    The connection and credential record is created.


