---
title: Configure automatic cancellation for draft cases in Social Benefits Playbook
description: An admin can configure auto-cancellation of Social Benefits Playbook cases that remain in the draft state for longer than a set period of time. The number of days that the case can remain in the draft state before it is canceled can be configured by an admin. The default value is five days.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Social Benefits Playbook, Playbooks, Configure Agent Workspaces, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Configure automatic cancellation for draft cases in Social Benefits Playbook

An admin can configure auto-cancellation of Social Benefits Playbook cases that remain in the draft state for longer than a set period of time. The number of days that the case can remain in the draft state before it is canceled can be configured by an admin. The default value is five days.

## About this task

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Script Includes** and search for the `SocialBenefitsConstants` record.

2.  Select the record to open it.

3.  Switch to the Social Benefits Playbook application to edit the record, if prompted.

4.  Locate the `SocialBenefitsConstants.SOCIAL_BENEFITS_MODELS_ARRAY = [` function in the script.

5.  Open a separate tab in your instance.

6.  In the navigation bar, enter `cmdb_model.list` to display a list of all product models in Public Sector Digital Services playbooks.

7.  Right-click on the name of the desired product model record in the Social Benefits Playbook, and in the context menu, select **Copy sys\_id**.

    For example, to close all draft applications submitted for Unemployment Insurance, right click the Unemployment Insurance record and copy the sys\_id.

8.  Paste the copied sys\_id\(s\) into the `SocialBenefitsConstants.SOCIAL_BENEFITS_MODELS_ARRAY = [` function, adding more as needed.

9.  Right click on the top menu bar, and in the context menu, select **Save**.

10. Navigate to **All** &gt; **System Properties** &gt; **All** and search for the `sn_gsm_soc_bnfts.sb_cancel_draft_state` record.

11. Switch to the Social Benefits Playbook application to edit the record, if prompted.

12. Change the number in the **Value** field to set the number of days that a case can remain in the draft state before cancellation, and select **Update**.


## Result

The Social Benefits Playbook is now configured to auto-cancel any draft cases that have remained in the draft state for more than `X` number of days.

