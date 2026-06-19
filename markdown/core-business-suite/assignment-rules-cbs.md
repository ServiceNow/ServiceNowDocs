---
title: Assignment rule form
description: Field descriptions for the Edit assignment rule form, used to define when and how tasks are assigned to a group or user in Core Business Suite.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/core-business-suite/assignment-rules-cbs.html
release: australia
product: Core Business Suite
classification: core-business-suite
topic_type: reference
last_updated: "2026-06-08"
reading_time_minutes: 1
keywords: [assignment rule, form fields, CBS]
breadcrumb: [Reference, Core Business Suite]
---

# Assignment rule form

Field descriptions for the Edit assignment rule form, used to define when and how tasks are assigned to a group or user in Core Business Suite.

|Field|Description|
|-----|-----------|
|Name|Name of the assignment rule. For example, `HR General Case`.|
|Execution order|Numeric value that determines the order in which this rule runs relative to other assignment rules. Lower values run first.|
|Set to active|When selected, the assignment rule is active and applied to incoming tasks.|
|When to assign|
|Table|Table that the assignment rule applies to. For example, `HR Case`.|
|Show labels|When enabled, displays field labels in the condition builder.|
|Field|Field on the selected table used to evaluate the assignment condition. For example, `Assigned to`.|
|Operator|Comparison operator applied to the selected field. For example, `Is empty`.|
|AND/OR|Toggle that controls how multiple conditions are combined. Select **AND** to require all conditions to be met, or **OR** to require any one condition to be met.|
|Who to assign|
|Group|Group to assign the task to when the assignment conditions are met. For example, `HR Request managers`.|
|User|User to assign the task to when the assignment conditions are met. Can be used with or without a group assignment.|

**Parent Topic:**[Core Business Suite reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/cbs-reference-parent.md)

