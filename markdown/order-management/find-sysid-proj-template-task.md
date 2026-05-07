---
title: Verify the sys\_id of a project task template
description: Determine if you're using the correct project task template for domain orders or order tasks by checking the sys\_id of the project template task.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Choosing a project template task when duplicates exist, Setting up project oversight conditions and decision rules, Configuring the Strategic Portfolio Management integration, Order Management integration with Strategic Portfolio Management, Integrate, Sales Customer Relationship Management]
---

# Verify the sys\_id of a project task template

Determine if you're using the correct project task template for domain orders or order tasks by checking the sys\_id of the project template task.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All**, and in the filter enter `project_template_task.list`.

2.  Select the record for the project template task to be verified.

    ![Project template task record to be verified](../image/proj-template-task-decision-table.png)

    For example, in the Project Template Task record for Product Order for SD-WAN Security, which belongs to the SD-WAN Package project template, the sys\_id is 183910354fcd2110c5ff2624b2ce0b49.

3.  Check the value of the sys\_id in the associated Decisions table entry.

    1.  Navigate to **All** and in the filter, enter `sys_decision_question.list`.

    2.  In the Decisions \[sys\_decision\_question\] table, locate the record of the corresponding decision table entry, for example Project Management Oversight for Domain Order.

    3.  In the record for the project template task, select the **Answer** column.

    ![List of decision tables for project oversight](../image/sys-decision-question-table.png)

    The resulting record for the **Answer** field opens.

4.  In the resulting record for the Decision Table Multiple Result, view the XML output by right-clicking the header bar of the record and selecting **Show XML**.

5.  Review the XML and locate the sys\_id value in the file.

    ![XML that shows the sys_id value of the project template task](../image/proj-task-template-xml-value.png)

    The sys\_id value should match the sys\_id of the project template task determined in Step 1. If the sys\_id doesn't match, proceed to the next step.

6.  In the Decision Table Multiple Result record, select the **u\_project\_template\_task** and check the XML view of another project template task to verify the sys\_id of the project task template.

    ![Pop-up list of Project Template Tasks to verify](../image/verify-xml-u-project-template.png)


