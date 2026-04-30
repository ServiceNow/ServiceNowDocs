---
title: Configure a workplace task signing template
description: Configure a signing template that you want to make available for signing the completed Workplace Core workplace tasks. You can configure the default signing template available with the application or create a new template.
locale: en-US
release: zurich
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Managing workplace tasks, Manage, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Configure a workplace task signing template

Configure a signing template that you want to make available for signing the completed Workplace Core workplace tasks. You can configure the default signing template available with the application or create a new template.

## Before you begin

Role required: sn\_wsd\_core.admin

## About this task

When a workplace manager signs a completed task, an e-signature PDF document is generated using a signing template and is attached to the task. For information about signing a workplace task, see [Sign a completed workplace task](sign-completed-task-wsd.md).

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Administration** &gt; **HTML templates**.

2.  Select **New** or open an existing signing template to edit it.

    The application provides a default template called **Task Signing Template**.

3.  On the form, fill in or modify the fields.

<table id="table_k3p_qpr_qlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Acknowledgment text

</td><td>

Text clarifying the meaning of the signature.For example, "I acknowledge that this information is true".

</td></tr><tr><td>

Name

</td><td>

Name of the signing template.

</td></tr><tr><td>

Table

</td><td>

Table associated with the template. The selected table determines the available variables in the **Select variables** field.

</td></tr><tr><td>

Body

</td><td>

Placeholder for HTML text and variables. The variables are resolved when the PDF is generated.You can select fields from the **Select variables** option to add them as variables to the HTML body.

</td></tr></tbody>
</table>4.  Customize the body of the signing template in the **Body** field.

    1.  Enter and format the text to design the body of the template.

        Use the formatting tools to apply formatting options, such as bold, italic, underline, or font styling.

    2.  Insert variables by locating your cursor at the desired location and selecting the variable under **Fields**.

        For example, to indicate which location to clean, you might insert the text `Cleaning finished for the Workplace location:` and, after a space, select **Workplace location** under **Select variables**. The variable in the **Body** field text would appear as follows:

        ```
        Cleaning finished for the Workplace location: ${workplace_location}
        ```

        The variable is replaced with the actual location when the PDF is generated.

5.  At the desired location in the **Body** field, enter the following variables:

    -   `${Checklist}`: Adds the checklist variable.
    -   `${Signature}`: Adds the signature variable.
    ![Signature and checklist variables in signing template body](../../../reuse/workplace-safety-mgmt/images/signing-template-body.png)

    In the signed PDF document, the signature and checklist are embedded at the same location where you entered these variables into the template body.

6.  Select **Submit**.

7.  Review the look of the PDF document by impersonating a workplace manager and signing a closed task.


**Parent Topic:**[Managing workplace tasks](../concept/managing-workplace-maintenance-tasks.md)

