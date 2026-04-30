---
title: Opt out of data sharing for Now Assist
description: Data sharing improves ServiceNow AI products. You can opt out of data sharing from the Now Assist Admin console Settings page.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-11-18"
reading_time_minutes: 1
keywords: [Opt out, Now Assist, data sharing, Admin console, settings page, account]
breadcrumb: [Review Now Assist account information, Configuring Now Assist settings and features, Now Assist, Enable AI experiences]
---

# Opt out of data sharing for Now Assist

Data sharing improves ServiceNow AI products. You can opt out of data sharing from the Now Assist Admin console Settings page.

## Before you begin

**Important:** Data sharing is not available for GCC or self-hosted instances. You don't need to opt out because data sharing is never enabled. If you have any questions, reach out to your account representative.

If you do not have a data steward, see [Assign the data steward role](assign-data-steward-role.md) documentation.

Role required: sn\_generative\_ai.data\_steward

## About this task

By default, you are opted in for data sharing. By opting out of the ServiceNow customer data sharing program, you can no longer provide data to improve ServiceNow AI products. By sharing data with the ServiceNow AI development program, you provide relevant data to help improve prediction accuracy, user experience, tailor products to your business needs, and reduce hallucinations for your activated Now Assist skills.

You can choose to opt out a ServiceNow instance from data sharing from the Now Assist Admin console if you don't want to participate. Repeat the opt-out process for all instances that use the Now Assist functionality.

Opting out can take up to five business days to process.

## Procedure

1.  Change the current session scope by selecting the Globe icon in the top right next to the search bar and setting Application Scope to Generative AI Controller.

2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Settings**.

    If you’re already in the Now Assist Admin console, select the **Settings** tab.

3.  In the Settings panel, select **Account**.

    ![Account panel in Now Assist Admin Settings that shows the features that are included with your license. It also provides a data sharing opt-out button.](../image/now-assist-account-overview.png)

4.  In the Data sharing section of the panel, select **Opt Out**.

5.  In the confirmation window, select **Opt Out**.


## Result

Your data sharing preference is now saved on the instance. If you wish to opt back in to data sharing, you must consult with your account executive.

**Parent Topic:**[Review Now Assist account information](review-now-assist-account-information.md)

