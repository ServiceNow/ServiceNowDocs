---
title: Use Mass Update CI
description: You can use the proposed changes in a change request to apply the same update to a set of CIs for a specific CI class.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Process a change request, Use, Change Management, IT Service Management]
---

# Use Mass Update CI

You can use the proposed changes in a change request to apply the same update to a set of CIs for a specific CI class.

## Before you begin

Role required: itil, sn\_change\_write, or admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Create New** and select **Normal** or **Emergency** change.

2.  Select the **Mass update CI class** check box.

    The **Mass update CI class** tab or form section appears.

3.  On the **Mass update CI class** tab, select the CI class to update.

    The dynamic CI group is not available for selection. When using mass update, a specific CI class must be selected and not a group that may have different CI classes.

    The parent CMDB \[cmdb\_ci\] table is selected by default. Search for the class name, for example, enter `linux` or `email`.

    **Note:** If you have selected a dynamic CI group for the **Configuration item** field, the configuration items that are part of the dynamic group and belong to the selected CI class are updated. For example, if the dynamic CI group that you have selected consists of Linux servers, computers, and network switches, and you select Linux servers for the CI class with proposed changes, only the Linux servers in the dynamic group get updated.

4.  Enter the proposed changes that you want to make to all the affected CIs.

    Each time that you select a field and value, another line appears. If you enter a proposed change in error, click the **X** beside the line to remove it.

5.  Click **Submit**.

6.  Open the change request you submitted.

7.  In the Affected CIs related list, click **Add**.

    The Add Affected Configuration Items window that opens lists only the CIs in the selected CI class.

8.  Select one or more CIs and click **Add Selected**, or click **Add All**.

    If you change the CI class after selecting affected CIs, the list is cleared when you save the record.

9.  Continue with the change management process for this change request.

10. When the record reaches the Implement or Review states, click **Apply Proposed Changes**.

    A message appears informing you that the proposed changes were applied to all the affected CIs.

    **Note:** If you are using the Bulk CI Change without Mass Update CI feature, then the proposed changes are applied when the change request is closed.


**Parent Topic:**[Process a change request](t_ProcessAChangeRequest.md)

**Related topics**  


[Mass Update CI](../concept/bulk-ci-change.md)

[Activate Change Management - Mass Update CI](t_ActivateChangeManagementBulkCI.md)

[Create a change request](t_CreateAChange.md)

