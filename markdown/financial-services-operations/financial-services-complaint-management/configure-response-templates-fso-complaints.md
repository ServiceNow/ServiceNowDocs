---
title: Define response templates for Financial Services Complaint Management
description: Create or modify a response template to define a reusable message that can be copied to complaint case or task forms to provide quick and consistent messages to customers.
locale: en-US
release: yokohama
product: Financial Services Complaint Management
classification: financial-services-complaint-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Financial Services Complaint Management, Setting up Financial Services Complaint Management, Complaint Management, Using common applications, Financial Services Operations \(FSO\)]
---

# Define response templates for Financial Services Complaint Management

Create or modify a response template to define a reusable message that can be copied to complaint case or task forms to provide quick and consistent messages to customers.

## Before you begin

Ensure that the scope is selected for the Financial Services Complaint Management application. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

Role required: sn\_bom\_compl.admin and sn\_templated\_snip.template\_snippet\_admin

## About this task

Each template is associated with the Complaint Case \[sn\_bom\_compl\_service\] table of Financial Services Complaint Management. The template can be configured to include variables pulled from that table. Also, use condition builder to define when a case meets the criteria for a template, such as for a specific service definition.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Response Template Configuration**.

2.  Create a response template.

    For more information, see [Create or modify a response template](https://www.servicenow.com/docs/access?context=create-modify-templated-snippet&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

    The Channels related list appears.

3.  In the Channels related list, associate a channel with the response template.

    Channels limit the response template to only the channels that you associate, for example, chats, emails, or form. A response template without a channel will not be available to use.

    -   Click **New** to create a new channel that gets added to the response template.

        **Note:** For information on Response Template Channel form fields, see [Create a response template channel](https://www.servicenow.com/docs/access?context=hr-templated-snippets&version=yokohama&pubname=yokohama-employee-service-management&section=response-template-channel&ft:locale=en-US).

    -   Click **Edit** to access and add an existing channel to the response template.
    The Response Template form returns.

4.  Click **Update**.


