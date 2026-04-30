---
title: Perform smart assessment on action tasks
description: Use the Tasks page on the Employee Center for a consolidated view of all your tasks, including all assessments, enabling you to access and complete them efficiently.
locale: en-US
release: zurich
product: Compliance Case Management
classification: compliance-case-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Compliance Case Management, Governance, Risk, and Compliance]
---

# Perform smart assessment on action tasks

Use the **Tasks** page on the Employee Center for a consolidated view of all your tasks, including all assessments, enabling you to access and complete them efficiently.

## Before you begin

Ensure that:

-   The **sn\_grc\_case\_mgmt.enable\_smart\_assessments** system property is enabled.
-   The assessment templates are configured and published.

Role required: sn\_comp\_case.compliance\_case\_business\_user

## About this task

When a compliance case action task moves from **Draft** to **Assigned** state, an assessment is initiated. When you perform a smart assessment on an action task that is of type **Assessment**, and the smart assessment property is enabled, the assessments appear on the unified **Tasks** landing page. The tasks that appear on the **Tasks** page are unique to the logged-in user and therefore can help the user complete all tasks assigned to them. If you're not the rightful responder of the assessment, you can reassign the assessment to the correct responder. On the assessment landing page, you have various features such as the option to collaborate with the stakeholders using the **Discuss** feature. If you pause responding to an assessment, you can get back to it using the **Resume** action without losing your responses.

## Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **GRC Tasks** &gt; **My to-dos** &gt; **Open** &gt; **My pending tasks** &gt; **Action tasks**.

2.  Select the action task that you want to assess.

3.  Select **Start**.

4.  Respond to the questionnaire.

    You can view detailed guidance for each question on the side of the screen. The guidance helps you in responding to the questions.

5.  Select **Submit**.

6.  On the success dialog box, select **OK**.

7.  After you submit the assessment, to view the assessment, select **View**.


## Result

After the assessment is submitted, the state of the assessment gets updated to **Review** and the status of the assessment is set to **Completed**. A compliance case analyst reviews the assessment and updates the state of the assessment to **Closed Complete**.

**Parent Topic:**[Using Compliance Case Management](../concept/use-compliance-case-management.md)

