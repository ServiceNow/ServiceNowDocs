---
title: Associate a new post incident report
description: Create your own post incident report and associate the UI page with the View Complete Report button under the Post Incident Report tab. Using the customized report, you can add information that is specific to your organization.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Major incident workbench, Managing major incidents, Incident Management, IT Service Management]
---

# Associate a new post incident report

Create your own post incident report and associate the UI page with the **View Complete Report** button under the **Post Incident Report** tab. Using the customized report, you can add information that is specific to your organization.

## Before you begin

Role required: itil, major\_incident\_manager, or admin

## About this task

For associating the **View Complete Report** button with your customized post incident report page, set the value of the **PIR export ui page url** major incident property to the new UI page.

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **UI Pages** and click **New**.

2.  Create a UI page.

    For information on how to create a UI page, refer UI pages.

3.  Navigate to **Incident** &gt; **Major Incident Properties**.

4.  In the **PIR export ui page url** \(**sn\_major\_inc\_mgmt.pir\_export\_pdf\_ui\_page**\) property, enter the link of the new UI page.

5.  Click **Save**.

    When you click the **View Complete Report** button, the new UI page opens.


**Parent Topic:**[Major incident workbench](../concept/major-incident-workbench.md)

