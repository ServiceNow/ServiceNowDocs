---
title: Set up the Workfront spoke
description: Set up an outbound integration between the ServiceNow instance and the Workfront instance.Generate an API key for authenticating Workfront API requests.Create a connection record between the ServiceNow instance and the Workfront instance. The connection record consists of the connection details and the API key.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Workfront Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the Workfront spoke

Set up an outbound integration between the ServiceNow instance and the Workfront instance.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate Workfront plugin.
-   Workfront role required: Administrator
-   Role required: admin

## Generate a Workfront API key

Generate an API key for authenticating Workfront API requests.

### Before you begin

Role required: Workfront administrator

### Procedure

1.  From a web browser, open [Adobe Workfront](https://www.workfront.com).

2.  Log in to the [Adobe Workfront](https://www.workfront.com) instance.

3.  On the page header of your Adobe Workfront instance, select the main Menu icon \(![Main Menu icon.](../image/main-menu-icon.png)\).![Main menu on homepage.](../image/adobe-workfront-main-menu.png)

4.  Select the Setup icon \(![Setup icon.](../image/adobe-workfront-setup.png)\).

5.  From the left navigation menu of the Setup page, navigate to **System** &gt; **Customer Info**.

6.  In the API Key Settings section, select **Generate API Key**.![Generate API Key link.](../image/adobe-workfront-generate-API.png)

    The API key is generated.

7.  Copy the API key and save for later use.

8.  To set an expiry date to the API key, in the **After creation, API keys expire in** list, select the time period.

9.  Click **Save**.


## Create a Workfront connection record

Create a connection record between the ServiceNow instance and the Workfront instance. The connection record consists of the connection details and the API key.

### Before you begin

Role required: admin

### Procedure

1.  Log in to the ServiceNow instance.

2.  Navigate to **Process Automation** &gt; **Flow Designer**.

3.  Select **Connections**.

4.  In the Search all connections field, enter `workfront`.

5.  On the Workfront tile, click **View Details**.![View Details button.](../image/workfront-spoke-view-details.png)

6.  Click **Configure**.![Configure button.](../image/workfront-spoke-configure-button.png)

7.  Fill the form.

<table id="table_xd2_qht_lnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name of the Workfront connection. **Note:** The default name of the first connection record is Workfront and it's read-only. To provide a custom name, you must create another connection record.

</td></tr><tr><td>

Connection URL

</td><td>

URL for the connection. Enter `https://<*domain-name*>.my.workfront.com`, where &lt;*domain-name*&gt; is your company subdomain.

</td></tr><tr><td>

API Key

</td><td>

The API key that you generated from the Workfront instance. To learn how to generate an API key, see [Generate a Workfront API key](setup-workfront.md#).

</td></tr></tbody>
</table>8.  Click **Configure Connection**.


