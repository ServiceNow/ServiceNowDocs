---
title: Domain-separate a custom table
description: You may need to create custom tables in separate domains. This topic covers both the procedure and the concept behind domain-separating a custom table.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Domain-separate a custom table

You may need to create custom tables in separate domains. This topic covers both the procedure and the concept behind domain-separating a custom table.

## 1. Create a sys\_domain field

**Note:** If a system table or a table has not been domain-separated by the Domain Separation plugin, it's best not to domain-separate it.

Use these points as a guideline to create a sys\_domain field.

-   Create a new field as a **domain\_id** type.
    -   Column Name: sys\_domain
    -   Other attributes: Defined automatically
-   The Sys\_domain\_path is created automatically.

The column name **sys\_domain** is reserved in the ServiceNow AI Platform, which means that the system recognizes it and automatically applies the appropriate field type and attributes for you. This automatic configuration also creates a corresponding **sys\_domain\_path** field.

-   Set the column name to `sys_domain` rather than using the label.
-   Domain separation is not appropriate for every table. In general, if a table is part of the base instance and that table does not have a **sys\_domain** field, you should leave it that way.

A **sys\_domain** field is created automatically when you create a domain\_id type field with the name “sys\_domain."

## 2. Add a business rule to set the domain

-   **Without business rules**

    The domain is set to the current domain of the user who creates the record.

-   **With business rules**

    The domain is assigned using scripted logic, typically based on the Company field.


In addition to a `sys_domain field`, custom tables need a business rule similar to **Domain - Set Domain – Task**to set the value of the domain field. In addition, you will need **Domain – Default – Task**, which moves records without a domain to the default domain if the first rule fails to assign a domain.

On the task table, review the business rules for Domain. Pay particular attention to the Order field. The priority of execution is given by the Order field from low to high.

The first rule that runs, **Domain – Set Domain – Task**, attempts to set the domain of the record based on the record’s Company’s Domain.

If the first rule fails to find an appropriate domain, the second rule, **Domain – Default – Task**, executes. This rule sets the domain of the record to the default domain.

Finally, if the domain of a task record changes, the **Domain – Cascade Domain – Task** business rule changes the domain on all records related to the task, such as workflows, metrics, SLAs, and attachments.

## 3. Add a business rule if Step 2 failed

If the initial business rule fails to set a domain and the domain is still empty or global, a second business rule runs. This rule examines the `task_for` field that is based on the caller or `requested_for` field. This rule is checking to see if you can set the domain of the record based on the user’s domain. If not, the business rule sets the domain to the default domain.

Following is a sample script for the business rule:

```
/* essentially
If (task_for is set)
  set the domain to the user's domain
ELSE
  set the domain to the default domain
*/
```

## 4. Domain – cascade domain – task

Tasks can have many related tables that work together for business objectives. These related records include workflow, SLA, approvals, attachments, and email. If the domain of a task changes, the related records domain must change, too, so they remain visible to users in the new domain.

This Cascade rule is commonly triggered when you clear records out of the default domain.

The related records for a Cascade domain contained in the Script are shown similar to the example:

```
/*
* Keep domains in sync w/related records for:
* workflow context
* workflow history
* approver tables and related workflows
* attachments
* emails
*/
```

**Parent Topic:**[Domain separation recommended practices for service providers](bp-domain-sep-recommended.md)

**Related topics**  


[Domain separation explained](../concept/bp-what-is-domain-separation.md)

[Domain separation hierarchies](bp-domain-sep-hierarchies.md)

[Context and domain separation](../concept/bp-domain-sep-context.md)

[Segregating and securing data with domain separation](bp-segregate-secure.md)

[Alternatives to domain separation](bp-domain-separation-alternatives.md)

[Evaluating the need for domain separation](bp-evaluation-dom-sep.md)

[Benefits of domain separation](bp-advantages-dom-sep.md)

[How a database query works with domain separation](../concept/bp-db-query-with-ds.md)

[Domain separation levels of support](bp-domain-levels.md)

[Service provider reference architecture](bp-sp-reference-arch-ds.md)

[Domain separation terms](bp-terms-conditions.md)

[Customizing domain properties and themes](../concept/bp-domain-prop-themes.md)

[Managing domain separation for specific uses](../concept/bp-emails-catalog-users.md)

[Configuring domain separation with the domain picker](../concept/bp-domain-picker-config-process.md)

[Domain separation performance considerations](../concept/bp-performance-considerations.md)

[Setting up domain hierarchies](../concept/bp-domain-hierarchy.md)

[Checking domain logs for errors and warnings](../concept/bp-domain-logs.md)

[Importance of the Default domain](../concept/bp-default-domain.md)

[Contains queries and domain access](../concept/bp-contains-domain-visibility.md)

[Domain paths query method](../concept/bp-domain-query-method.md)

[Slow queries and SQL debugging](../concept/bp-debug-sql.md)

[Before Query business rules](../concept/bp-before-query-business-rules.md)

[Avoiding domain path in scripts](../concept/bp-no-domain-path-in-scripts.md)

[Domain assignments](bp-domain-assignment.md)

[Domain separation and the Customer Service Management \(CSM\) plugin](../concept/bp-ds-and-csm.md)

