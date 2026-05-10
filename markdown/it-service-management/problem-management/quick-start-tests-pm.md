---
title: Quick start tests for Problem Management
description: Validate that Problem Management still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: australia
product: Problem Management
classification: problem-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Reference section for Problem Management, Problem Management, IT Service Management]
---

# Quick start tests for Problem Management

Validate that Problem Management still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.

Problem Management quick start tests require activating the Problem Management Best Practice — Madrid plugin \(com.snc.best\_practice.problem.madrid\) and the Problem Management — ATF Tests plugin \(com.snc.problem.atf\). For all state related test, the Problem Management State Model \(com.snc.best\_practice.problem.madrid.state\_model\) plugin needs to be active.

<table id="table_bjf_nfg_h1c"><thead><tr><th>

Test

</th><th>

Description

</th><th class="filter">

Release version

</th></tr></thead><tbody><tr><td>

PRB MGMT: Cancel a Problem when the state of the Problem is Assess

</td><td>

Verify that when a Problem in the **Assess** state is canceled, the state of the Problem changes to **Closed** with **Resolution code** as **Canceled**.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Cancel a Problem when the state of the Problem is Root Cause Analysis

</td><td>

Verify that when a Problem is in the **Root Cause Analysis** state and is canceled, the state of the Problem changes to **Closed** with **Resolution code** as **Canceled**.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Mark a Problem as Duplicate when the state of the Problem is Assess

</td><td>

Verify that when a Problem is in the **Assess** state and is marked as duplicate, the state of the Problem changes to **Closed** with **Resolution code** as **Duplicate**.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Mark a Problem as Duplicate when the state of the Problem is Root Cause analysis

</td><td>

Verify that when a Problem is in the **Root Cause Analysis** state and is marked as duplicate, the state of the Problem changes to **Closed** with **Resolution code** as **Duplicate**.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Accept Risk of Problem \(problem.acceptrisk.move\_to\_closed:false,state:Fix in Progress\)

</td><td>

Verify that when a Problem state is **Fix in Progress** and the risk is accepted, then the Problem state changes to **Resolved** with **Resolution code** as **Risk Accepted**. **Note:** The test is valid when Problem property **Accept Risk moves the Problem to Closed state instead of Resolved state** **\(problem.acceptrisk.move\_to\_closed\)** is false.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Accept Risk of Problem \(problem.acceptrisk.move\_to\_closed:true,state:Fix in Progress\)

</td><td>

Verify that when a Problem state is **Fix in Progress** and the risk is accepted, then the Problem state changes to **Closed** with **Resolution code** as **Risk Accepted**. **Note:** The test is valid when Problem property **Accept Risk moves the Problem to Closed state instead of Resolved state** **\(problem.acceptrisk.move\_to\_closed\)** is true.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Accept Risk of Problem \(problem.acceptrisk.move\_to\_closed:false,state:Root Cause Analysis\)

</td><td>

Verify that when a Problem state is **Root Cause Analysis** and the risk is accepted, then the Problem state changes to **Resolved** with **Resolution code** as **Risk Accepted**. **Note:** The test is valid when Problem property **Accept Risk moves the Problem to Closed state instead of Resolved state** **\(problem.acceptrisk.move\_to\_closed\)** is false.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Accept Risk of Problem\(problem.acceptrisk.move\_to\_closed:true,state:Root Cause Analysis\)

</td><td>

Verify that when a Problem state is **Root Cause Analysis** and the risk is accepted, then the Problem state changes to **Closed** with **Resolution code** as **Risk Accepted**. **Note:** The test is valid when Problem property **Accept Risk moves the Problem to Closed state instead of Resolved state** **\(problem.acceptrisk.move\_to\_closed\)** is true.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Reanalyze Problem which is closed-Risk Accepted from state Root Cause Analysis

</td><td>

Verify that when a Problem is reanalyzed after it is **Closed** with the **Resolution code** as **Risk Accepted**, Problem state changes to **Root Cause Analysis**.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Create Emergency Change from Problem

</td><td>

Verify the creation of Emergency Change from a Problem.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Create Normal Change from Problem

</td><td>

Verify the creation of Normal Change from a Problem.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Problem State Management

</td><td>

Verify problem state management.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Reanalyze a Problem from Complete

</td><td>

Verify that when a Problem is reanalyzed after it is **Closed** with the **Resolution code** as **Fix Applied**, Problem state changes to **Root Cause Analysis**.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Reanalyze a Problem which is canceled from state Assess

</td><td>

Verify that when a Problem is reanalyzed after it is **Closed** with the **Resolution code** as **Canceled**, Problem state changes to **Root Cause Analysis**.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Reanalyze a Problem which is canceled from state Root Cause Analysis

</td><td>

Verify that when a Problem is reanalyzed after it is **Closed** with the **Resolution code** as **Canceled**, Problem state changes to **Root Cause Analysis**.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Reanalyze Problem which is closed-Risk Accepted from state Fix in progress

</td><td>

Verify that when a Problem is reanalyzed after it is **Closed** with the **Resolution code** as **Risk Accepted**, Problem state changes to **Root Cause Analysis**.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Create a Known Error article from Problem

</td><td>

Verify creation of Known Error article from a Problem.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Risk Accept reason on Incident

</td><td>

Verify the **Risk Accepted reason** is copied to the Incidents which are awaiting resolution of a Problem.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Communicate Fix

</td><td>

Verify the communicate fix functionality.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Communicate Workaround

</td><td>

Verify the communicate workaround functionality.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Fix information on Incident

</td><td>

Verify that when a Problem is resolved, the state of the Incidents that are awaiting resolution of the Problem changes to **Resolved**. The fix notes of the Problem are copied to the Incidents.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Problem task \(Type:General\) state management

</td><td>

Verify Problem task state management of a general type Problem.

</td><td>

Madrid

</td></tr></tbody>
</table>**Parent Topic:**[Reference section for Problem Management](../../../product/problem-management/concept/reference-section-for-problem-management.md)

**Related topics**  


[Quick start tests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/quick-start-tests.md)

