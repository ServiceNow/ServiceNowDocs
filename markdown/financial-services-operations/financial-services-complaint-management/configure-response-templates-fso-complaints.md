---
title: Define response templates for Financial Services Complaint Management
description: Create or modify a response template to define a reusable message that can be copied to complaint case or task forms to provide quick and consistent messages to customers.
locale: en-US
release: australia
product: Financial Services Complaint Management
classification: financial-services-complaint-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Complaint Management, Common applications, Financial Services Operations \(FSO\)]
---

# Define response templates for Financial Services Complaint Management

Create or modify a response template to define a reusable message that can be copied to complaint case or task forms to provide quick and consistent messages to customers.

## Before you begin

Ensure that the scope is selected for the Financial Services Complaint Management application. For more information, see [Application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_ApplicationPicker.md).

Role required: sn\_bom\_compl.admin and sn\_templated\_snip.template\_snippet\_admin

## About this task

Each template is associated with the Complaint Case \[sn\_bom\_compl\_service\] table of Financial Services Complaint Management. The template can be configured to include variables pulled from that table. Also, use condition builder to define when a case meets the criteria for a template, such as for a specific service definition.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Response Template Configuration**.

2.  Create a response template.

    For more information, see [Create or modify a response template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/create-modify-templated-snippet.md).

    The Channels related list appears.

3.  In the Channels related list, associate a channel with the response template.

    Channels limit the response template to only the channels that you associate, for example, chats, emails, or form. A response template without a channel will not be available to use.

    -   Click **New** to create a new channel that gets added to the response template.

        **Note:** For information on Response Template Channel form fields, see [Create a response template channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/hr-templated-snippets.md).

    -   Click **Edit** to access and add an existing channel to the response template.
    The Response Template form returns.

4.  Click **Update**.


