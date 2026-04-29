---
title: Set up a bidirectional webhook
description: Configure a webhook to subscribe to Salesforce events with a ServiceNow callback URL.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Salesforce Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up a bidirectional webhook

Configure a webhook to subscribe to Salesforce events with a ServiceNow callback URL.

## Before you begin

-   Role required: admin

## Procedure

1.  Log in as an administrator to your Salesforce instance.

2.  Obtain the Salesforce instance details.

    For more information, see the [View instance information for your Salesforce Organization](https://help.salesforce.com/articleView?id=000322728&language=en_US&type=1&mode=1) knowledge article in [Salesforce Trailblazer forum](https://success.salesforce.com/).

    1.  If you don't have Salesforce custom domains, obtain the Salesforce instance name from the Company Information page.

    2.  If you have custom domains, navigate to **Domain Management** &gt; **My Domain** and copy the domain name.

        For example, if the complete domain name on the page is **newdomain-customdomain.my.salesforce.com**, copy and record the value `newdomain-customdomain`.

3.  Obtain the 18-digit Organization ID of your Salesforce instance.

    1.  Navigate to the Developer Console in your Salesforce instance and run this query:

        ```
        Select Id from Organization
        ```

    2.  Copy and record the value of the 18-digit Organization ID.

4.  Log in to your ServiceNow instance.

5.  Create a webhook registry.

    1.  Navigate to **Salesforce Webhook Registry** &gt; **Salesforce Webhook Registries**.

    2.  Click **New**.

    3.  On the form, fill these values:

        |Field|Description|
        |-----|-----------|
        |Organization ID|18-digit Organization ID of your Salesforce instance.|
        |Instance Name|Name of the Salesforce instance obtained from the Company Information page or custom domain of the Salesforce instance obtained from **Domain Management** &gt; **My Domain**.|

    4.  Right-click the form header and click **Save**.

6.  Obtain the resource path from your ServiceNow instance.

    1.  Navigate to **System Web Services** &gt; **Scripted Web Services** &gt; **Scripted REST APIs**.

    2.  Open the record, **Salesforce Webhook Callbacks**.

    3.  In the **Resources** tab, click the **Default Callback** record.

    4.  Copy and record the value of **Resource path**.

        The required ServiceNow endpoint URL is: `https://<intance-name>.service-now.com/<resource-path>`

7.  Configure the default subflows or create customsubflows.

    These subflows are triggered when the required events occur in Salesforce instance. For more information, see [Building subflows](https://www.servicenow.com/docs/access?context=subflows&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

8.  Configure the webhook routing policy.

    1.  Navigate to **System Definition** &gt; **Decision Tables**.

    2.  Open the record, **Salesforce Decision Webhook Policy**.

    3.  In the **Decisions** tab, click **New**.

    4.  On the form, fill these values:

        |Field|Description|
        |-----|-----------|
        |Label|Unique label to identify the routing policy.|
        |Answer|Subflow that must be triggered when the specified conditions are met.|
        |Default Answer|Option to specify if this is the default answer.|
        |Condition|Conditions to be met when the required events occur in Salesforce.|

        **Note:** By default, these Salesforce objects are supported in the webhook routing policies:

        -   Account
        -   Case
        -   Contract
        -   Opportunity
        You can configure the default decision table to support other Salesforce objects as per your requirement.

    5.  Click **Save**.

9.  From your Salesforce instance, create outbound message.

    For information about creating the outbound message, see [Outbound Message Actions](https://help.salesforce.com/articleView?id=workflow_managing_outbound_messages.htm&type=5) in [Salesforce Trailblazer forum](https://success.salesforce.com/).

10. In the Endpoint URL, enter the endpoint URL in this format: https://&lt;intance-name&gt;.service-now.com/&lt;resource-path&gt;.


