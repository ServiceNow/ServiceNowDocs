---
title: Collect employee input
description: Collect employee input without creating additional case records or adding new fields to existing tables with employee forms.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [HR Administration, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Collect employee input

Collect employee input without creating additional case records or adding new fields to existing tables with employee forms.

Employee forms are questionnaires built using the survey designer that you can use in HR tasks to verify or update information from employees. The information collected can be mapped directly to fields on a target table. You can also use HR criteria to query answers for use in downstream processes, such as for lifecycle event activities.

## How to collect employee input

Employee forms enable you to collect or verify information from employees. To use them, you must first create the employee form. Employee form questionnaires are built using the survey designer, and you can map questions from the employee form to corresponding fields on a target table. The mappings allow you to auto-populate information onto the employee form, and that information can be read-only or editable. If editable, the updated values will be pushed back to the corresponding table fields.

For more information, see [Create an employee form](../task/configure-hr-employee-form.md).

Once created, you can use the employee forms in HR tasks or HR task templates.

**Note:** Make sure that the HR task type is set to **Collect employee input**.

-   [Adding an HR task to an HR case](../task/t_ViewAnHRTask.md)
-   [Configure an HR task template](../task/configure-hr-task-template.md)

You can also use HR criteria records to query collected answers for use in downstream processes, such as for lifecycle event activities. Because questions on the employee form are built using the survey designer, the answers collected are saved to the Metric Result \[asmt\_metric\_result\] table. You can use HR criteria records to query answers from that table to determine whether an activity should trigger for a particular user. For example, if on an invention disclosure form, the new hire answers yes, then you can use that answer to trigger the creation of another task to collect details on the invention.

For more information, see [Create an HR criteria record for an employee form](../task/configure-hr-criteria-record-for-employee-form.md).

## Gathering intellectual property information

As part of the onboarding process, you want to ask new hires if they have any inventions to disclose. If they do, you want to gather details on the invention. To collect this information, you need to create an employee form, which is a questionnaire built using the survey designer. The questionnaire can include:

-   New hire's manager
-   New hire's business unit
-   Do you have inventions to disclose?
-   If yes, provide details on your invention.

After you create the employee form, you can use the form in HR tasks to collect the information you need. The following GIF shows an example of an HR agent creating a collect employee input task for an employee, Eva Seahorn, as part of an HR case.

![An HR agent creating an HR task in an HR task to collect employee input.](../image/employee-form-hr-case-hr-task.gif)

The employee can then provide that information when they receive the to-do. The follow GIF shows an example of the employee, Eva Seahorn, then completing the collect employee input to-do in the Employee Center.

![An employee completing a collect employee input to-do in the Employee Center.](../image/employee-form-esc-to-do.gif)

## Collect employee input error handling

If an error occurs when updating the employee form, a work note will be added to the HR case and HR task forms. Information not updated must be manually updated by the HR agent, and you can navigate to **HR Administration** &gt; **Employee Form Errors** for further details on the error.

-   **[Create an employee form](../task/configure-hr-employee-form.md)**  
Create or modify an employee form so that you can collect employee input. Configuration of the employee form is a three-part process. First, create the employee form record. Second, use the survey designer to build one or more questions for the employee form. Third, you can map questions from the employee form to corresponding fields on a target table.
-   **[Create an HR criteria record for an employee form](../task/configure-hr-criteria-record-for-employee-form.md)**  
Create an HR criteria record for an employee form based on the employee answers stored in the Metric Result \[asmt\_metric\_result\] table.

**Parent Topic:**[HR Administration](c_AdministerHRServiceManagement.md)

