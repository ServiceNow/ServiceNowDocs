---
title: Set up a bi-directional webhook for the Docusign eSignature spoke
description: Configure the webhook in your Docusign account to enable Docusign to send data to ServiceNow when a recipient signs a document.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Docusign eSignature Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up a bi-directional webhook for the Docusign eSignature spoke

Configure the webhook in your Docusign account to enable Docusign to send data to ServiceNow when a recipient signs a document.

## Before you begin

Role required: admin

## Procedure

1.  Connect a custom configuration to enable your Docusign application to share events and data with your ServiceNow instance.

    1.  Log in to your Docusign account as an admin.

    2.  In the admin dashboard, navigate to **Integrations** &gt; **Connect**.

    3.  Click **Add Configuration**.

        A list of the configuration types is displayed.

    4.  Select **Custom**.

    5.  On the form, fill these values.

<table id="table_br4_rlc_t1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the custom configuration.

</td></tr><tr><td>

URL to Publish

</td><td>

Add your ServiceNow instance URL in this format:-   Under **Event Settings**, if you select **Data Format** as **Legacy**, enter `https://{instance-name}.service-now.com/api/sn_docusign_spoke/docusign_webhook`
-   Under **Event Settings**, if you select **Data Format** as **REST v2.1**, enter, `https://{instance-name}.service-now.com/api/sn_docusign_spoke/docusign_webhook_rest`


</td></tr><tr><td>

Data Format

</td><td>

Select either **Legacy** or **REST v2.1**.**Note:** Ensure that this selection matches is accordance with the URL you provided in **URL to Publish**.

</td></tr></tbody>
</table>        ![Select the Events settings and enter URL to publish.](../image/ds-webhook-event.png)

2.  Under **Trigger Events**, enable Docusign to share envelope events with ServiceNow by selecting these events:

    -   Envelope Sent
    -   Envelope Delivered
    -   Envelope Signed/Completed
    -   Envelope Declined
    -   Envelope Voided
    -   Envelope Deleted
    -   Recipient Sent
    -   Recipient Auto Responded
    -   Recipient Delivered
    -   Recipient Signed/Completed
    -   Recipient Declined
    ![Select the required envelope events.](../image/ds-trigger-events.png)

3.  Under **Include Data**, select the **Recipients** option.

    Select other options as per your requirement.

    ![Select the Recipients option.](../image/include-data.png)

4.  Select the **Include basic authorization** option in the header and provide your ServiceNow instance credentials.

    ![Option to include basic authentiocation header.](../image/ds-basic-auth-header.png)

5.  Click **Add Configuration**.


