---
title: Scripts and engines execution order
description: Scripts, assignment rules, business rules, workflows, escalations, and engines all take effect in relation to a database operation, such as insert or update. In many cases, the order of these events is important.
locale: en-US
release: xanadu
product: Approvals
classification: approvals
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Classic approvals, Build workflows]
---

# Scripts and engines execution order

Scripts, assignment rules, business rules, workflows, escalations, and engines all take effect in relation to a database operation, such as insert or update. In many cases, the order of these events is important.

**Note:** Client-based code that executes in the browser, using Ajax or running as JavaScript, will always execute before the form submission to the server.

The order of execution is as follows:

1.  Before business rules: Scripts configured to execute before the database operation with an order less than 1000.
2.  Before engines. The following are not executed in any specific order:
    -   Approval engine \(for task and sys\_approval\_approver tables\)
    -   Assignment rules engine \(for task tables\)
    -   Escalation engine
    -   Data policy engine
    -   Field normalization engine
    -   Role engine - keeps role changes in sync with sys\_user\_has\_role table \(for sys\_user, sys\_user\_group, sys\_user\_grmember, and sys\_user\_role tables\)
    -   Execution plan engine \(for task tables\)
    -   Update version engine - creates version entry when sys\_update\_xml entry is written \(for sys\_update\_xml table\)
    -   Data lookup engine inserts or updates
    -   Workflow engine \(for default workflows\)
3.  Before business rules: Scripts configured to execute before the database operation with an order greater than or equal to 1000.
4.  The data base operation \(insert, update, delete\).
5.  After business rules: Scripts configured to execute after the database operation with an order less than 1000.
6.  After engines. The following are not executed in any specific order:
    -   Label engine
    -   Listener engine
    -   Table notifications engine
    -   Role engine - keeps role changes in sync with sys\_user\_has\_role table \(for sys\_user, sys\_user\_group, sys\_user\_grmember and sys\_user\_role tables\)
    -   Text indexing engine
    -   Update sync engine
    -   Workflow engine \(for deferred workflows\)
    -   Trigger engine \(for all Workflow Studio flows\)
7.  Email notifications. The following are executed based on the weight of the notification record:
    -   Notifications sent on an insert, update, or delete
    -   Event-based notifications
8.  After business rules \(Only active records\). Scripts configured to execute after the database operation with an order greater than or equal to 1000.

**Note:** Like After business rules, Async business rules execute their logic after a database operation occurs. Unlike After business rules, Async business rules execute asynchronously, running in the background simultaneously with other processes. Async business rules run after the user submits the form and after the scheduler runs the scheduled job created from the business rule. The system creates a scheduled job from the business rule after the user submits the form but before any action is taken on the record in the database.

