---
title: Data lookup rules
description: Data lookup rules offer a generic way to change any field value, not just assignment fields.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/table-administration-and-data-management/c\_DataLookupRules.html
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Assignment rules, Working with Task table, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Data lookup rules

Data lookup rules offer a generic way to change any field value, not just assignment fields.

[Data lookup and record matching support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_DataLookRecMatchSupport.md) offer the following improvements over the Assignment module:

-   Ability to change any field value not just an assignment field
-   More options to define when a rule runs:
    -   On form change \(Allows assignment rules to apply to unsaved changes on a form\)
    -   On record insert
    -   On record update
-   Option to replace existing values \(including default values\)

**Note:** You can define data lookup and Assignment rules at the same time. The system ignores any duplicate rules after an incident has been assigned unless you are using a data lookup definition option to replace existing values.

**Parent Topic:**[Defining assignment rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_DefineAssignmentRules.md)

**Related topics**  


[Assignment rules module]()

[Precedence between data lookup, assignment, and business rules]()

[Workflow assignments]()

[Baseline assignment rules example]()

[Create an assignment rule]()

[Create an assignment data lookup rule]()

[Precedence between data lookup, assignment, and business rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_PrecBetweenAssignmentAndBusRules.md)

