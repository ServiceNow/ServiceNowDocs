---
title: Natural Language Query roles
description: Natural Language Query \(NLQ\) is installed with these roles.The administrator for Natural Language Query.
locale: en-US
release: australia
product: Natural Language Query
classification: natural-language-query
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Natural Language Query References, Natural Language Query, Enable AI experiences]
---

# Natural Language Query roles

Natural Language Query \(NLQ\) is installed with these roles.

To learn more about managing per-user subscriptions, see [Managing per-user subscriptions in Subscription Management](https://www.servicenow.com/docs/access?context=managing-user-subscriptions-v2&version=australia&pubname=australia-platform-administration&ft:locale=en-US) and contact your account representative.

**Parent Topic:**[Natural Language Query References](nlq-references.md)

**Related topics**  


[NLQ properties](nlq-properties.md)

## NLQ Admin \[nlq\_admin\]

The administrator for Natural Language Query.

### Module Access

Has full access to the following modules:

-   NLQ Cmdb Implicit Relationships. For more information see [Intelligent Search for CMDB](https://www.servicenow.com/docs/access?context=intelligent-search-cmdb&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).
-   [NLQ Query Logs](../task/view-nlq-logs.md)
-   [NLQ Semantic Shortcuts](../task/create-nlq-shortcut.md).
-   [NLQ Synonyms](../task/create-nlq-synonym.md).

Has read-only access to the following module:

[NLQ Table Guesser Query Logs](../task/view-nlq-table-guesser-logs.md).

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

To avoid granting an admin role, use the pa\_analyst role for NLQ Cmdb Implicit Relationships, NLQ Semantic Shortcuts, and NLQ Synonyms.

