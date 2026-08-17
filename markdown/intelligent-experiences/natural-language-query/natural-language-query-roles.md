---
title: Natural Language Query roles
description: Natural Language Query \(NLQ\) is installed with these roles.The administrator for Natural Language Query.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/natural-language-query/natural-language-query-roles.html
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

To learn more about managing per-user subscriptions, see [Managing per-user subscriptions in Subscription Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/managing-user-subscriptions-v2.md) and contact your account representative.

**Parent Topic:**[Natural Language Query References](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/natural-language-query/nlq-references.md)

**Related topics**  


[NLQ properties]()

## NLQ Admin \[nlq\_admin\]

The administrator for Natural Language Query.

### Module Access

Has full access to the following modules:

-   NLQ Cmdb Implicit Relationships. For more information see [Intelligent Search for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/intelligent-search-cmdb.md).
-   [NLQ Query Logs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/natural-language-query/view-nlq-logs.md)
-   [NLQ Semantic Shortcuts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/natural-language-query/create-nlq-shortcut.md).
-   [NLQ Synonyms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/natural-language-query/create-nlq-synonym.md).

Has read-only access to the following module:

[NLQ Table Guesser Query Logs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/natural-language-query/view-nlq-table-guesser-logs.md).

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

To avoid granting an admin role, use the pa\_analyst role for NLQ Cmdb Implicit Relationships, NLQ Semantic Shortcuts, and NLQ Synonyms.

