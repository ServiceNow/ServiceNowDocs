---
title: Sensitive Data Handler
description: The Sensitive Data Handler detects and masks sensitive data entered in Agent Chat or Virtual Agent conversations. It can also collect sensitive data for processes such as user authentication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/conversational-interfaces/agent-chat/ac-sensitive-data-overview.html
release: australia
product: Agent Chat
classification: agent-chat
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Sensitive Data Handler, Agent Chat, Virtual Agent]
breadcrumb: [Explore, Agent Chat, Conversational Interfaces]
---

# Sensitive Data Handler

The Sensitive Data Handler detects and masks sensitive data entered in Agent Chat or Virtual Agent conversations. It can also collect sensitive data for processes such as user authentication.

**Note:** This feature is being prepared for future deprecation. It will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

Install the Data Privacy application as a replacement. For more information, see [Data Privacy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/data-privacy-landing.md).

Possible situations when the Sensitive Data Handler might detect and mask sensitive data include:

-   A requester enters sensitive data, such as a Social Security number, during a conversation with a live agent or virtual agent.
-   An agent enters company information, such as a manager's confidential email address, that the requester should not have access to.
-   A requester enters sensitive data in a pre-chat or post-chat survey.

The Sensitive Data Handler detects and masks sensitive data when the requester is conversing through the chat widget, mobile apps \(iOS or Android\), or any supported adapter channel \(SMS, Slack, Microsoft Teams, or Workplace\).

You can configure the following:

-   Regular expressions for each type of sensitive data \(for example, Social Security number or credit card number\).
-   Whether sensitive data handling works only for inbound \(from a requester\) messages, outbound \(from a live agent\) messages, or both.
-   Messages that display to the requester or agent informing them that sensitive data has been masked.

If the requester sends a message containing sensitive data to an agent, the system notifies both the requester and the agent that the message contained sensitive data. The system masks the sensitive data in the transcript and marks it as sensitive in the internal transcript.

If an agent tries to send a message containing sensitive data to a requester, the system doesn't send the message. Instead, the agent sees an error, and the system tags the message as sensitive in the internal transcript.

You can configure the Sensitive Data Handler to pass user authentication information to another entity. The requester might provide sensitive data during a conversation to prove their identity \(for example, a Social Security number, date of birth, or email address\).

You can install the Sensitive Data Handler plugin \(com.glide.sensitive\_data\_handling\) by itself, without a Glide Virtual Agent or Agent Chat plugin. You can add, edit, and delete regular expressions in the Sensitive Data Handling module.

## Regular expressions

The Sensitive Data Handler includes predefined regular expressions for credit card numbers, debit card numbers, Social Security numbers, and email addresses. When the Sensitive Data Handler detects a regular expression, it uses the defined masking pattern to mask sensitive data. To define your own regular expressions and patterns to mask other sensitive data, see [Configure Sensitive Data Handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/agent-chat/ac-configure-sensitive-data-handling.md). If a regular expression isn't configured correctly, the system might stall while matching the regular expression against the message. To help avoid this issue, the system times out after one second.

<table id="table_r1n_gdm_gsb"><thead><tr><th>

Name

</th><th>

Regular expression

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Credit Card - Visa

</td><td>

\\b4\[0-9\]\{12\}\(?:\[0-9\]\{3\}\)?\\b

</td><td>

-   Card number starts with 4.
-   Current card numbers have 16 digits, and older card numbers have 13 digits.

</td></tr><tr><td>

Credit Card - American Express

</td><td>

\\b3\[47\]\[0-9\]\{13\}\\b

</td><td>

-   Card number starts with 34 or 37.
-   Card number has 15 digits.

</td></tr><tr><td>

Credit Card - Mastercard

</td><td>

\\b\(?:5\[1-5\]\[0-9\]\{2\}\|222\[1-9\]\|22\[3-9\]\[0-9\]\|2\[3-6\]\[0-9\]\{2\}\|27\[01\]\[0-9\]\|2720\)\[0-9\]\{12\}\\b

</td><td>

-   Card number starts with a number between 51-55 or 2221-2720.
-   Card number has 16 digits.

</td></tr><tr><td>

Credit Card - Diners Club

</td><td>

\\b3\(?:0\[0-5\]\|\[68\]\[0-9\]\)\[0-9\]\{11\}\\b

</td><td>

-   Card number starts with 36, 38, or 300-305.
-   Card number has 14 digits.
-   Cards that start with 5 and have 16 digits should be processed like a Mastercard.

</td></tr><tr><td>

Credit Card - Discover

</td><td>

\\b6\(?:011\|5\[0-9\]\{2\}\)\[0-9\]\{12\}\\b

</td><td>

-   Card number starts with 65 or 6011.
-   Card number has 16 digits.

</td></tr><tr><td>

Social Security number

</td><td>

\\b\(?!666\|000\|9\\d\{2\}\)\\d\{3\}-\(?!00\)\\d\{2\}-\(?!0\{4\}\)\\d\{4\}\\b

</td><td>

-   First 3 digits cannot be 000, 666, or 900-999.
-   Hyphen \(-\)
-   Middle 2 digits are 01-99 and cannot be 00.
-   Hyphen \(-\)
-   Last 4 digits should be 0001-9999 and cannot be 0000.

</td></tr><tr><td>

Email

</td><td>

\\b\[\\w!\#$%&amp;'\*+/=?\`\{\|\}~^-\]+\(?:\\.\[\\w!\#$%&amp;'\*+/=?\`\{\|\}~^-\]+\)\*@\(?:\[a-zA-Z0-9-\]+\\.\)+\[a-zA-Z\]\{2,6\}\\b

</td><td>

-   Word
-   Period \(.\)
-   Word
-   @ symbol
-   String of alphanumeric characters at least one character long.
-   Period \(.\)
-   Alphabetical string 2-6 characters long.

</td></tr></tbody>
</table>