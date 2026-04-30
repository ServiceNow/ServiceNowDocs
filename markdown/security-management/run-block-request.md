---
title: Run Block Request
description: Blocks communication with observables associated with a security incident.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security Operations Integration- Block Request capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Run Block Request

Blocks communication with observables associated with a security incident.

## Before you begin

Role required: sn\_si.analyst

## About this task

**Note:** If no implementations are available, capability actions are not displayed in product menus.

The **Security Operations Integration - Block Request** flow can be triggered from an observable form, or from the **Security Incident Observables** related list on a security incident.

This example shows a Block Request from a security incident.

## Procedure

1.  Navigate to a security incident.

2.  In the Related Links, select **Show all Related Lists**.

3.  Select **Associated Observables** tab.

4.  Select observables from the list.

5.  Select **Allow/Block Request** in the **Actions on selected rows...** drop-down menu.

    A dialog box appears.

6.  Select **look-up icon** next to the Implementation field.

7.  Select a capability from the list.

    Following fields appear if the capability includes additional runtime parameters. Different integrations may have different parameters.

<table id="table_xxr_blg_q3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Indicator Block Action Type

</td><td>

Option to control how the detection is handled after the block request is submitted.Options include:

-   Block
-   Block, hide detection


</td></tr><tr><td>

Severity

</td><td>

Option to specify the severity assigned to the indicator in CrowdStrike when the block action is submitted.Options include:

-   Informal
-   Low
-   Medium
-   High
-   Critical


</td></tr></tbody>
</table>    ![Allow/Block request](../image/allow:block-obs.png)

8.  Select **Submit**.

    The flow execution audit is displayed in the work notes section.

    ![Block Request work note example](../image/run-block-request-worknote.png)


**Parent Topic:**[Security Operations Integration- Block Request capability](../concept/block-request-capability.md)

