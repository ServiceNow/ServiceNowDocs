---
title: Customize job requisition state management workflow
description: Add new job requisition states or customize the job requisition state management workflow according to your organizational needs.
locale: en-US
release: australia
product: Recruiter Workspace
classification: recruiter-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Recruitment Workspace, Hiring Experiences, HR Service Delivery, Employee Service Management]
---

# Customize job requisition state management workflow

Add new job requisition states or customize the job requisition state management workflow according to your organizational needs.

Customize the job requisition state management workflow to add modifications to the predefined workflow. For more information, see [Customize job requisition state management workflow \[KB1700566\]](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=43f8feb19318da10080af35d6cba1045).

To add a new job requisition state:

1.  Open the job requisition table\(sn\_ta\_hiring\_core\_job\_requisition\).
2.  Right-click and select **Configure** &gt; **Table**.
3.  In the **Columns** tab, search for and select the State column.
4.  In the **Choices** tab, select **New**.
5.  In the **Label** field, enter the name of the new state.
6.  In the **Value** field, enter a numerical value for the new state.

    **Note:** The value must be a unique number that determines the order of the state and enables proper sequencing. For example, to add a new state between two existing ones, enter a number that falls between their respective values.

7.  Select **Submit**.

**Parent Topic:**[Configuring Recruitment Workspace](../concept/config-recruitment.md)

