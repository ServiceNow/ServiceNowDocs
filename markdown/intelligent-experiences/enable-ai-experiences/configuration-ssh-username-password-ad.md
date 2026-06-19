---
title: Create a Desktop action parameter record
description: Create a Desktop action parameter record to store a name that an AI agent references when accessing credentials or other values during desktop action execution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/enable-ai-experiences/configuration-ssh-username-password-ad.html
release: australia
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: task
last_updated: "2026-05-25"
reading_time_minutes: 1
breadcrumb: [Enable AI agents to securely access parameters, Defined desktop actions, Configure, AI Desktop Actions, Enable AI experiences]
---

# Create a Desktop action parameter record

Create a Desktop action parameter record to store a name that an AI agent references when accessing credentials or other values during desktop action execution.

## Before you begin

Perform this task in the ServiceNow instance.

For SSH connector desktop actions, verify that you have an active SSH server.

Role required: sn\_aia.admin

## About this task

Parameter records are supported for on-screen tasks and SSH background tasks. Use them to replace fixed values with configured ones for on-screen tasks and username and password for SSH.

## Procedure

1.  Navigate to **All** &gt; **AI Desktop Actions** &gt; **Desktop Action Parameters**.

2.  Select **New**.

3.  Fill in the following fields.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a unique name for the parameter. The AI agent references this name when retrieving the stored value. For example, `un_username_group` or `un_password_group`.|
    |Description|Enter a description of what value this parameter stores.|
    |Shared|Option to make this parameter available to all users. When selected, only one Desktop action parameter value record can be created under this parameter, and only a user with the sn\_aia.admin role can create it. During execution, the AI agent uses this single value regardless of which user triggered the agent.|
    |Mark As Sensitive|Option to encrypt all associated Desktop action parameter value records. The agent decrypts the value at execution time.|

    **Important:**

    **Shared** and **Mark As Sensitive** can only be edited when there are no associated parameter value records.

4.  Select **Submit**.


## Result

The Desktop action parameter record is created and appears in the Desktop Action Parameters list. You can now create Desktop action parameter value records under this parameter. For more information, see [Create a parameter value record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/configure-parameter-value-record.md).

