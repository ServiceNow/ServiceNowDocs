---
title: Set up approval configuration
description: Set up approval configuration to enable multiple levels of approvals and select approvers for each level based on approval rules.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Approval configuration, General administration setup for BCM, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Set up approval configuration

Set up approval configuration to enable multiple levels of approvals and select approvers for each level based on approval rules.

## Before you begin

You must install GRC: Approver Configurator \(sn\_grc\_appr\) application for approval configurations.

Role required: sn\_bcm.admin

**Note:** Granting this role to a user is equivalent to giving the user the admin role, because workflow script activities bypass access controls and grant access to all tables and database operations. Script activities do not bypass application scope settings.

## Procedure

1.  Navigate to **All** &gt; **Assignment and Approval Configurations** &gt; **Approval Configurations**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_oyj_52z_hrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the approval configuration.

</td></tr><tr><td>

Applies to

</td><td>

Table such as a business impact analysis, business continuity plan, events, or any table from which a record is submitted for approval.

</td></tr><tr><td>

Priority

</td><td>

Preference of approval configuration with higher priority.

</td></tr><tr><td>

Filter condition

</td><td>

Condition applied on the table with reference to the **Applies to** field.The approval configuration with higher priority that matches the filter condition for the business document is selected for approver evaluation.

</td></tr><tr><td>

Active

</td><td>

Option to enable the approval configuration as active.

</td></tr></tbody>
</table>    **Note:** You cannot have more than one approval configuration applying to the table with the same priority.

4.  Click **Submit**.


**Parent Topic:**[Approval configuration](../concept/bcm-approval-configuration.md)

