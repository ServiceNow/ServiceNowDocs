---
title: Business stakeholder role for Test Management 1.0
description: Use the business stakeholder role to read and retrieve data from any table of the Test Management 1.0 application to generate reports.
locale: en-US
release: yokohama
product: Test Management
classification: test-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Test Management 1.0, Test Management applications, Strategic Portfolio Management]
---

# Business stakeholder role for Test Management 1.0

Use the business stakeholder role to read and retrieve data from any table of the Test Management 1.0 application to generate reports.

When you activate the Business Stakeholder plugin \(com.snc.business\_stakeholder\) in your ServiceNow instance, the Read only roles for Test Management 1.0 plugin \(com.snc.tm1\_read\_roles\) is also activated. This plugin provides a business stakeholder role \(sn\_tm1\_read\) with which you can access all the tables of the Test Management 1.0 application. This role also allows read-only access to the Test Management dashboard. You can assign this role to any user in your organization who is a business stakeholder.

## Plugin availability

If you are a new customer, the Read only roles for Test Management 1.0 plugin \(com.snc.tm1\_read\_roles\) is activated on zBoot. However, the business stakeholder role \(sn\_tm1\_read\) is available only when you activate the Test Management 1.0 plugin \(com.snc.test\_mgmt\).

If you are an upgrade customer, you must manually activate the Read only roles for Test Management 1.0 plugin \(com.snc.tm1\_read\_roles\).

## Test Management 1.0 tables accessible by users with the business stakeholder role

When both the Read only roles for Test Management 1.0 plugin \(com.snc.tm1\_read\_roles\) and Test Management 1.0 plugin \(com.snc.test\_mgmt\) are active in your ServiceNow instance, the user with the business stakeholder role \(sn\_tm1\_read\) has read access to the following tables.

<table id="table_TestManagement"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Test Case \[tm\_test\_case\]

</td><td>

Stores the test cases.

</td></tr><tr><td>

Test Case Instance \[tm\_test\_case\_instance\]

</td><td>

Extends the Planned Task table.

</td></tr><tr><td>

Test Suite \[tm\_test\_suite\]

</td><td>

Stores the test suites.

</td></tr><tr><td>

Test Environment \[tm\_test\_environment\]

</td><td>

Stores the test environments.

</td></tr><tr><td>

Test \[tm\_test\]

</td><td>

Stores the tests.

</td></tr><tr><td>

Test Instance \[tm\_test\_instance\]

</td><td>

Stores the tests under a test plan.

</td></tr><tr><td>

Test Plan \[tm\_test\_plan\]

</td><td>

Stores the test plans. Extends the Planned Task table.

</td></tr><tr><td>

Test Case Defects \[m2m\_tm\_test\_case\_instance\_defect\]

</td><td>

Stores the test case defects that are recorded for failed tests.

</td></tr></tbody>
</table>