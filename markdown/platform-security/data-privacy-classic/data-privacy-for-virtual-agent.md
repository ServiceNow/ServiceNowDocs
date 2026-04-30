---
title: Data Privacy for Virtual Agent
description: You can use Data Privacy to detect and mask the sensitive data and PII during a Virtual Agent conversation.
locale: en-US
release: zurich
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: task
last_updated: "2025-08-20"
reading_time_minutes: 1
breadcrumb: [Data privacy, Data Privacy, Platform Privacy]
---

# Data Privacy for Virtual Agent

You can use Data Privacy to detect and mask the sensitive data and PII during a Virtual Agent conversation.

## Before you begin

Role required: virtual\_agent\_data\_privacy\_admin

## About this task

Use Data Privacy to detect and mask the sensitive data and PII during a Virtual Agent conversation. Data Privacy is replacing the depreciated Sensitive Data Handler, see [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) for more information. The setup process may vary depending on if Sensitive Data Handler was previously installed and configured.

**Note:** If you have previously configured Sensitive Data Handler your settings will be migrated to Data Privacy as a policy. See [Create anonymization policies](dps-create-anonymization-policies.md) for more information.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  Under **Sensitive data detection**, select **View all**.

    If the button reads **Get data privacy**, you will need to install the Data Privacy plugin to continue. See [Activate data privacy \(Classic\)](../../search-administration/task/install-data-privacy.md) for more information

3.  Set the slider to **Active**.

4.  If Data Privacy is not yet installed you will be prompted to install the Data Privacy plugin to continue, see [Activate data privacy \(Classic\)](../../search-administration/task/install-data-privacy.md) for more information.

5.  Select the appropriate conversation flow:

    1.  Requester to agent - detect and mask sensitive data entered by the requester in an Agent Chat conversation.
    2.  Agent to requester - detect and mask sensitive data entered by the agent in an Agent Chat conversation.
    3.  Requester to Virtual Agent - detect and mask sensitive data entered by the requester during a Virtual Agent conversation.
    **Note:** You must select at least one conversation flow.

6.  Select **Manage in Data Privacy**.

    If you have configured Sensitive Data Handler before, your settings will be migrated as a policy to Data Privacy

7.  Create a new Data Privacy policy for Virtual Agent, see [Create anonymization policies](dps-create-anonymization-policies.md) for more information on Data Privacy policies.


