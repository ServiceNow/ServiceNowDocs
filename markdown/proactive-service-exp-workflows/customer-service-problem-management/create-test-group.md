---
title: Create a test group
description: Create a test group to combine various tests that can assist in troubleshooting issues encountered by specific types of services or product models. For instance, grouping a speed test and a ping test together can effectively help in diagnosing internet-related problems.
locale: en-US
release: zurich
product: Customer Service Problem Management
classification: customer-service-problem-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up a test group, Configure, Customer Service Problem Management]
---

# Create a test group

Create a test group to combine various tests that can assist in troubleshooting issues encountered by specific types of services or product models. For instance, grouping a speed test and a ping test together can effectively help in diagnosing internet-related problems.

## Before you begin

Role required: sn\_st\_mgmt.test\_def\_creator

## Procedure

1.  Navigate to **All** &gt; **Service Test Management** &gt; **Test Groups** &gt; **All**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_ndt_z23_4fc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto-generated ID for the test group.

</td></tr><tr><td>

Name

</td><td>

Name of the test group.

</td></tr><tr><td>

State

</td><td>

State of the test group.-   **Draft**

Unpublished draft service test group that is assigned when you first create the group record.

-   **Published**

Published service test group that is assigned when you formally publish it for use.

The service test group and the related tables can’t be modified in the published state.

-   **Retired**

Service test group that is retired.

</td></tr><tr><td>

Execution Type

</td><td>

Execution type of the test group.-   **Manual**

The test definitions can be mapped to the test group in the related list.

-   **Automated**

A subflow has to be created and mapped to the automated test group.

</td></tr><tr><td>

Description

</td><td>

Description for the test group.

</td></tr></tbody>
</table>4.  Select **Submit**.


