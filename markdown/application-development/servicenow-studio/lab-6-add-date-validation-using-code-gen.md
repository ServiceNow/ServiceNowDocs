---
title: Tutorial part 6: Add date validation using code generation
description: Currently, there is no validation for date fields in event records, allowing events to be created with a start date after the end date. This section shows how to use code generation to create a business rule preventing this issue. While date validations can be time-consuming, Now Assist streamlines the process with code generation.
locale: en-US
release: yokohama
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ServiceNow Studio tutorial, Exploring ServiceNow Studio, Building applications with ServiceNow Studio, Developing your application, Building applications]
---

# Tutorial part 6: Add date validation using code generation

Currently, there is no validation for date fields in event records, allowing events to be created with a start date after the end date. This section shows how to use code generation to create a business rule preventing this issue. While date validations can be time-consuming, Now Assist streamlines the process with code generation.

## Before you begin

Role required: admin or delegated\_developer

## Procedure

1.  From the We Volunteer app dashboard, select **Create** &gt; **File**.

2.  Enter **Global** in the Application field.

3.  Under the Server Development category, select **Business Rule**.

4.  Select **Continue**.

5.  Add the following specifications to the new business rule:

    -   Name: Date validation
    -   Table: Event \[x\_snc\_we\_volunteer\]
    -   Advanced: true \(select the check box\)
    -   When: before
    -   Insert: true \(select the check box\)
    -   Update: true \(select the check box\)
6.  Select **Add Filter Condition**.

7.  Add the following specifications to the filter condition:

    -   Starts: changes
    -   OR
    -   Ends: changes
8.  On the Advanced tab, click into the third line in the script editor.

9.  Open the Now Assist code generator by pressing **Command + Enter** \(on Mac\) or **Ctrl + Enter** \(on Windows\).

10. Enter the following text: `Get value of start date(starts) & end date (ends) from the current record, using GlideDateTime() check if start date is greater than end date, abort if true, check if start date is past due, abort if true`.

11. Select the Submit icon \(![submit icon](../image/sn-studio-na-submit-icon.png)\) and wait a few moments for Now Assist to generate a code snippet.

12. Select **Accept**.

13. Select **Submit**.


**Parent Topic:**[ServiceNow Studio tutorial](../concept/lab-sns-lab-guide.md)

