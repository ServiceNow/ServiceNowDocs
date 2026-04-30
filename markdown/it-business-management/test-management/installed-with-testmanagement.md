---
title: Components installed with Test Management
description: Several types of components are installed with activation of the Test Management plugin, including tables and user roles.
locale: en-US
release: xanadu
product: Test Management
classification: test-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Activate Test Management, Test Management 1.0, Test Management applications, Strategic Portfolio Management]
---

# Components installed with Test Management

Several types of components are installed with activation of the Test Management plugin, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Roles installed

<table id="roles_TestMgmt"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Test manager\[tm\_test\_manager\]

</td><td>

Manages test plans and test suites \(metadata\). Has all privileges within test management, including planning, execution, and administration.

</td><td>

tm\_tester

</td></tr><tr><td>

Tester\[tm\_tester\]

</td><td>

Executes test cases and tests.

</td><td>

feature\_user

</td></tr></tbody>
</table>## Tables installed

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