---
title: Certify an account
description: A certification task represents the work of verifying and certifying the data associated with a record. The certifier reviews tasks created after data validation against the published policy. Account certification helps resolve issues like outdated ownership, inactive user profiles, and improper permissions in cloud accounts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/cloud-account-management/certify-account.html
release: brazil
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Use, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Certify an account

A certification task represents the work of verifying and certifying the data associated with a record. The certifier reviews tasks created after data validation against the published policy. Account certification helps resolve issues like outdated ownership, inactive user profiles, and improper permissions in cloud accounts.

## Before you begin

Make sure that the admin has reviewed the Cloud Account Management default policy. Optionally, the admin can customize or add new policies based on the organization requirement. For more information, see [Review default Cloud Account Management certification policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/policy-setup.md). The ITOM CW Certifier Group must contain at least one user.

**Note:** Cloud Account Management admin can add users to the ITOM CW Certifier Group by navigating to **All** &gt; **Account Certification** &gt; **ITOM CW Certifier Group** &gt; **Group Members**.

Role required: sn\_itom\_cam.cw\_certifier

## About this task

## Procedure

1.  Navigate to **All** &gt; **Cloud Workspace** &gt; **Manage and Configure** &gt; **Policy center** &gt; **Account certification**.

    It opens the CMDB Workspace where you can access and update your certificate tasks.

2.  In the **My Work** section select the **Certification tasks tab**.

3.  Select the certification task that you want to review.

4.  Review the details of the certification task, then select **Review records to certify**.

5.  Select the records that you want to conclude the review for in the **Review not completed** tab, and then select **Certify** or **Fail**.

    \[Omitted image "cw-certification-tasks.png"\] Alt text: Cloud Workspace Certification tasks

    **Note:** If you select **Fail**, the task is moved to the registry and Cloud Account Management admin will take the next action. You can also reassign the ownership of a task.

6.  Select the records that you want to review in details and then select **Review records**.

7.  Select **Submit** when all the records have been reviewed.

    The **Submit** button isn't available until all the records in the task are reviewed and the task is complete.

8.  Assign owners \(if they’re empty\) by select and hold \(or right-click\) on the **Owned By** entry and selecting the name from the lookup.

    **Note:**

    The account certification state changes to pending if it meets the admin's policy conditions for recertification.


## What to do next

For more information on certifying a task, see [Review certification tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/data-certific-review-tasks.md)

**Parent Topic:**[Using Cloud Account Management in Cloud Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/using-cam.md)

