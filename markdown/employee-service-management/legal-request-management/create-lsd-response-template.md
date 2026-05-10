---
title: Create or modify a response template for legal services
description: Create or modify a response template with a reusable message that legal fulfillers can use to send users quick and consistent messages. They can use these reusable messages in their assigned legal requests or legal matter forms, as well as in chat sessions or emails.
locale: en-US
release: australia
product: Legal Request Management
classification: legal-request-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Legal Request Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Create or modify a response template for legal services

Create or modify a response template with a reusable message that legal fulfillers can use to send users quick and consistent messages. They can use these reusable messages in their assigned legal requests or legal matter forms, as well as in chat sessions or emails.

## Before you begin

Ensure that the Templated Response plugin \(com.sn\_templated\_snip\) is installed.

Role required: sn\_lg\_ops.legal\_config

## About this task

Response templates are reusable messages that can be used by the legal fulfillers to respond to stakeholders of a legal request or legal matter. For more information, see [Response templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/response-templates-templated-snippets.md).

## Procedure

1.  Navigate to **All** &gt; **Legal Administration** &gt; **Response Template Configuration**.

2.  Create or modify a response template.

    -   To create a response template, click **New**.
    -   To modify an existing response template, open it from the list.
3.  On the form, fill in the fields.

    For field descriptions, see [Response Template form](../reference/response-template-fields.md).

4.  Save the response template.

    -   Save a new response template by clicking **Submit**.
    -   Save the changes to an existing response template by clicking **Update**.
    The response template is created and the Channels related list appears.

5.  Associate one or more channels through which the response template can be used.

    A response template is only available through the channels that you select. You can provide different messages by creating response templates for each channel, such as chat, email, or form.

    1.  In the Channels related list, click **Edit**.

    2.  On the Edit Members form, select one or more channels from the **Collection** list and click **&gt;** to add them to the **Channels List**.

    3.  Click **Save**.

        The selected channels are added to the Channels related list.


## Result

The response template is ready to be used by the legal fulfiller through the configured channels.

**Parent Topic:**[Configuring Legal Request Management](../concept/legal-ops-administration.md)

