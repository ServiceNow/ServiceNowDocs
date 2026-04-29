---
title: Set up the Socure spoke
description: Integrate the ServiceNow instance and Socure account using an API key to authenticate ServiceNow requests.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Socure Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Socure spoke

Integrate the ServiceNow instance and Socure account using an API key to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Socure spoke.
-   Contact the Socure support team and obtain the connection URL to connect to Socure account.
-   Role required: admin.

## Procedure

1.  Obtain the IP addresses of your ServiceNow instance.

    1.  Log in to [ServiceNow - NOW Support](https://support.servicenow.com/now).

    2.  Search for the **My IP Information** service catalog item.

        ![Search for the service catalog item.](../image/socure-ip-instance.png)

    3.  Click the service catalog item.

    4.  Provide your instance name in **Select the instance**.

        ![Provide the instance name.](../image/socure-ip-instance-num.png)

    5.  Click **Submit**.

        The IP addresses are displayed.

    6.  Copy and record the IP addresses for later use.

        ![Copy the IP addresses.](../image/snow-ip-addresses.png)

2.  Obtain the value of token from your Socure admin account.

    1.  Log in to your [Socure admin account](https://admin.socure.com/) with your admin credentials.

    2.  Click the **Settings** tab.

    3.  In the **Account Settings** tab, provide these values.

        -   Select **Production** from the **Environment** list.
        -   In **Allowed Domains**, specify the IP addresses of your ServiceNow instance. Separate multiple IP addresses using comma \(,\).
        -   Copy and record the value of **ID+key** for later use.
3.  Create credential record for the Socure spoke in your ServiceNow instance.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Credentials**.

    2.  Click **New**.

        The system displays the message **What type of Credentials would you like to create?**.

    3.  Select **API Key Credentials**.

        A blank API Key Credentials form displays.

    4.  Enter these values.

<table id="table_lwy_g1z_4fb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, enter `Socure Credentials`.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the credential record.

</td></tr><tr><td>

API Key

</td><td>

Socure token in this format: `SocureApiKey <Value of ID+key>`.

</td></tr><tr><td>

Applies to

</td><td>

**Note:** This option is not applicable to this spoke.

</td></tr><tr><td>

Order

</td><td>

Order to apply this credential. For example, enter `100`.

</td></tr></tbody>
</table>    5.  Click **Submit**.

4.  Create connection record for the Socure spoke in your ServiceNow instance.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    2.  Open for the record for **Socure**.

    3.  From the **Connections** tab, click **New**.

        The system displays a blank HTTP\(s\) Connection form.

    4.  Enter these values.

        |Field|Value required|
        |-----|--------------|
        |Name|Name to uniquely identify the connection record. For example, enter `Socure Connection`.|
        |Credential|Select the Credential record you created for Socure. For example, select **Socure Credentials**.|
        |Connection URL|Connection URL to connect to Socure account.|

    5.  Click **Submit**.


