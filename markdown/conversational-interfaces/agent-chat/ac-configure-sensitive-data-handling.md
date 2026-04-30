---
title: Configuring Sensitive Data Handler
description: Detect and mask sensitive information that is shared in Agent Chat or Virtual Agent conversations.
locale: en-US
release: zurich
product: Agent Chat
classification: agent-chat
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configuring Agent Chat, Agent Chat, Conversational Interfaces]
---

# Configuring Sensitive Data Handler

Detect and mask sensitive information that is shared in Agent Chat or Virtual Agent conversations.

## Before you begin

**Note:** This feature is being prepared for future deprecation. It will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

Install the Data Privacy application as a replacement. For more information, see [Data Privacy for Virtual Agent](https://www.servicenow.com/docs/access?context=data-privacy-for-virtual-agent&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

Activate the Sensitive Data Handler plugin \(com.glide.sensitive\_data\_handling\).

Role required: admin, virtual\_agent\_admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  Under **Sensitive data detection**, select **View all**.

3.  Slide the **Active** toggle switch to enable sensitive data detection.

4.  Select the appropriate conversation flow:

    1.  Requester to agent - detect and mask sensitive data entered by the requester in an Agent Chat conversation.
    2.  Agent to requester - detect and mask sensitive data entered by the agent in an Agent Chat conversation.
    3.  Requester to Virtual Agent - detect and mask sensitive data entered by the requester during a Virtual Agent conversation.
    **Note:** You must select at least one conversation flow.

5.  The Regular Expressions tab displays the existing expressions:

<table id="table_hzl_rk4_gsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the regular expression.

</td></tr><tr><td>

Regular Expression

</td><td>

Pattern that defines the expression.

</td></tr><tr><td>

Number of characters to mask

</td><td>

Number of characters in the regular expression that are masked.

</td></tr><tr><td>

Start masking from

</td><td>

Direction the regular expression is masked: left to right or right to left.

</td></tr><tr><td>

Status

</td><td>

-   Active - this expression is masked.
-   Inactive - this expression isn't masked.


</td></tr><tr><td>

Order

</td><td>

Order in which the active regular expressions are analyzed against a message to determine if there are any matches.

</td></tr></tbody>
</table>6.  Either select an existing expression to modify or create a new regular expression by selecting **New** and filling in the fields.

<table id="table_xgy_cjs_gsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the regular expression.

</td></tr><tr><td>

Number of characters to mask

</td><td>

Number of characters in the regular expression that are masked.

</td></tr><tr><td>

Masking symbol

</td><td>

Symbol used in place of the sensitive data.

</td></tr><tr><td>

Status

</td><td>

-   Active - this expression is masked.
-   Inactive - this expression isn't masked.


</td></tr><tr><td>

Domain

</td><td>

Name of the domain that this regular expression affects. If you select **Global**, then the regular expression applies to both the agent and requester domains. For the agent and requester to see each other's domain, the administrator must do one of the following:-   Include the domain where the regular expression should be visible as a child domain to the corresponding parent domain.
-   Grant necessary access to the appropriate domain if it's a sister domain.
-   Set the regular expression under a global domain.


</td></tr><tr><td>

Regular Expression

</td><td>

Pattern that defines the expression. Check your regular expression on a regex validation site such as [https://regex101.com/](https://regex101.com/)

</td></tr><tr><td>

Order

</td><td>

Order in which the active regular expressions are analyzed against a message to determine if there are any matches.

</td></tr><tr><td>

Start masking from

</td><td>

Indicates whether the regular expression is processed from left to right or right to left.

</td></tr></tbody>
</table>7.  On the **Agent system messages** tab, enter information for the message that the agent sees if they enter sensitive data:

    |Field|Description|
    |-----|-----------|
    |Description|Description of the system message.|
    |Value|Exact wording of the system message that displays to the agent.|
    |Updated|Date and time the message was most recently updated.|
    |Updated by|Name of the user who most recently updated the message.|

8.  On the **Requester system messages** tab, enter information for the message that the requester sees if they enter sensitive data:

    |Field|Description|
    |-----|-----------|
    |Description|Description of the system message.|
    |Value|Exact wording of the system message that displays to the requester.|
    |Updated|Date and time the message was most recently updated.|
    |Updated by|Name of the user who most recently updated the message.|

9.  Select **Save**.


**Parent Topic:**[Configuring Agent Chat](../concept/ci-agent-chat-configuring.md)

