---
title: Help context types and prioritization
description: You can create a help context with the type Form, List, or Record, and link it to a particular table in your ServiceNow instance. If you have multiple help contexts, prioritization determines which help contexts apply to what a user views.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Context-sensitive help, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Help context types and prioritization

You can create a help context with the type **Form**, **List**, or **Record**, and link it to a particular table in your ServiceNow instance. If you have multiple help contexts, prioritization determines which help contexts apply to what a user views.

## Help context types

When a user clicks the help icon, the system analyzes the relevant help contexts to determine which help page to display.

-   Record-level help applies to only one specific record, not the list or form for that table.

    For example, if a **Record** type help context exists for the **Validate Number** record in the Business Rule table, the help icon only directs to the page specified when a user views that record.

-   List-level help applies to the list for a table. If no form-level help is defined, list-level help also applies to the form for the same table.

    For example, if a **List** type but not a **Form** type help context exists for the Business Rule table, the help icon directs to the page specified by the **List** type help context when a user views any list or record \(if record-level help is not defined for it\) in the Business Rule table.

-   Form-level help applies to the form for a table. If no list-level help is defined, the form-level help also applies to the list for the same table.

    For example, if a **Form** type but not a **List** type help context exists for the Business Rule table, the help icon directs to the page specified by the **Form** type help context when you view any record \(if record-level help is not defined for it\) or list in the Business Rule table.

-   If both list- and form-level help are defined for a table, the appropriate help is displayed for the list and the form.

    For example, if a **List** type and a **Form** type help context exist for the Business Rule table, the help icon directs to the page specified by the **List** type help context when a user views the Business Rules list. The help icon directs to the page specified by the **Form** type help context when a user views any record \(if record-level help is not defined for it\) in the Business Rule table.


**Important:** If you create a help context for a base table list or record, the help system opens that target topic for any list or record in a table that extends the base table if no other help context is created in that extended table.

## Help context prioritization

When there are several matching help context records, the following rules determine which help context is used, in descending order of priority.

1.  A customer-created help context is used instead of a default help context provided in the instance for the same table.
2.  A help context that matches the user's language setting is used instead of a help context in the default language of the instance. See the **Language** field on the [Help Context form](../task/t_CreateANewHelpContext.md).
3.  A help context for a closer table in an extended table hierarchy is used instead of a help context for a further table.

    Consider the case of the Linux Server \[cmdb\_ci\_linux\_server\] table, which has the following parentage: cmdbi\_ci &gt; cmdb\_ci\_hardware &gt; cmdb\_ci\_computer &gt; cmdb\_ci\_server &gt; cmdb\_ci\_linux\_server. If help contexts exist for both the cmdb\_ci\_server table and the cmdb\_ci table, the help icon directs to the page specified by the cmdb\_ci\_server help context when you view a record in the cmdb\_ci\_linux\_server table.


**Parent Topic:**[Context-sensitive help](../concept/c_ContextSensitiveHelp.md)

**Related topics**  


[Create a new help context](../task/t_CreateANewHelpContext.md)

