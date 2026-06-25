---
title: Domain-separate a custom table
description: You may need to create custom tables in separate domains. This topic covers both the procedure and the concept behind domain-separating a custom table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/bp-ds-custom-table.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
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

**Parent Topic:**[Domain separation recommended practices for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-domain-sep-recommended.md)

**Related topics**  


[Domain separation explained]()

[Domain separation hierarchies]()

[Context and domain separation]()

[Segregating and securing data with domain separation]()

[Alternatives to domain separation]()

[Evaluating the need for domain separation]()

[Benefits of domain separation]()

[How a database query works with domain separation]()

[Domain separation levels of support]()

[Service provider reference architecture]()

[Domain separation terms]()

[Customizing domain properties and themes]()

[Managing domain separation for specific uses]()

[Configuring domain separation with the domain picker]()

[Domain separation performance considerations]()

[Setting up domain hierarchies]()

[Checking domain logs for errors and warnings]()

[Importance of the Default domain]()

[Contains queries and domain access]()

[Domain paths query method]()

[Slow queries and SQL debugging]()

[Before Query business rules]()

[Avoiding domain path in scripts]()

[Domain assignments]()

[Domain separation and the Customer Service Management \(CSM\) plugin]()

