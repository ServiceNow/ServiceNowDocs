---
title: Set up approval levels
description: Assign multiple levels of approvals to users or groups to support each step of your BIA, BCP, or events workflow processes.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Approval configuration, General administration setup for BCM, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Set up approval levels

Assign multiple levels of approvals to users or groups to support each step of your BIA, BCP, or events workflow processes.

## Before you begin

Role required: sn\_bcm.admin

**Note:** Granting this role to a user is equivalent to giving the user the admin role, because workflow script activities bypass access controls and grant access to all tables and database operations. Script activities do not bypass application scope settings.

## Procedure

1.  Navigate to **All** &gt; **Assignment and Approval Configurations** &gt; **Approval Configurations**.

    With the BCM application, these approval configurations are supported with the base system:

    -   `BCP Workflow Configuration`
    -   `BIA Workflow Configuration`
    -   `Crisis Workflow Configuration`
    -   `Exercise Workflow Configuration`
    ![OOTB.](../image/approval-configurations-ootb.png)![BCP config.](../image/approval-config-bcp.png)

    You can update the existing BCP, BIA, Crisis, or Exercise configurations. Additionally, you can set up multiple levels of approval configurations for BCP, BIA, Crisis, or Exercise. The base system supports the Level 1 approval level by default.

2.  To set up multiple approval levels for an existing configuration such as the BCP Workflow Configuration, select the **BCP Workflow Configuration** record from the list and complete the substeps.

    The **BCP Workflow Configuration** record is displayed.

    1.  Select **New** in the related list of the BCP Workflow Configuration record.

        The Approval level new record form is displayed.![Approval level record.](../image/approval-level-level-2-record.png)

    2.  In the form, enter the name for the approval level record such as Level 2 Managers, select the level such as level 2, and select **Submit**.

        The newly created Approval level record such as Level 2 Managers record is displayed in the related list as shown in the example.![Approval level records.](../image/approval-level-records-level-2.png)

3.  To configure an approval rule for the newly configured approval level record, select **New** in the Approval Rules related list of the approval level record and complete the steps.

    1.  Update the approval rule configuration for continuity plans by updating the filter condition and the approver type as shown in the example.

        ![Rule for level 2.](../image/approval-rule-level-2-configuration.png)

        In the filter condition, you can select the source table on which rule the approval rule is evaluated. Optionally, you can apply additional condition on the source table. You can select a field to filter the source records based on the Applies to table of the approval configuration. You can configure for which records, level 1 should trigger level 2.For more information, see [Approval Rule New Record form](../../grc-common/reference/approval-rule-new-record-form.md).

    2.  Select **Submit**.

    The approval rule is now configured for the approval level. When a business continuity plan is created in the BCM Configurable Workspace and later it is sent for a review and an approval, the multiple approval levels are displayed in the **Approval levels** tab of the business continuity plan as shown in the example.![Approval levels in the plan.](../image/approval-levels-tab-of-plan.png)


**Parent Topic:**[Approval configuration](../concept/bcm-approval-configuration.md)

