---
title: Create additional incident data fields
description: Create Additional Incident Data Fields for the DLP incidents. You can create different types of fields such as string, number, check box, choice, date and time, and use them in the DLP incident forms.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/data-loss-prevention/create-custom-fields-dlp.html
release: australia
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Administer, Data Loss Prevention Incident Response, Security Operations]
---

# Create additional incident data fields

Create Additional Incident Data Fields for the DLP incidents. You can create different types of fields such as string, number, check box, choice, date and time, and use them in the DLP incident forms.

## Before you begin

Role required:

-   sn\_dlir.admin
-   sn\_dlir.analyst and sn\_dlir.analyst\_read

**Important:** Additional incident data fields for DLP incidents are supported only on the San Diego version or later.

## About this task

Additional Incident Data Fields are not stored as columns on the DLP incident table. Unlike standard table-level fields, they cannot be queried directly through list views, reports, or scripts that reference incident table fields.

Additional Incident Data Fields view differs by role. DLP Analysts can view and set field values in the DLP Ops portal. DLP End Users can set field values, but fields that contain no value are hidden from them in the DLP Workspace. For example, an unchecked **Check box** or a **Choice** field with no selection is not displayed to end users.

## Procedure

1.  Navigate to **All** &gt; **DLP Administration** &gt; **Additional Incident Data Fields**.

2.  Create an Additional Incident Data Fields by clicking **New**.

3.  On the form, fill in the fields.

<table id="table_mzl_mbl_zrd"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the Additional Incident Data Fields.

</td></tr><tr><td>

Type

</td><td>

Option to select the type of Additional Incident Data Fields. You can choose one of the following types:-   **String**
-   **Number**
-   **Check box**
-   **Choice**

If you select the Additional Incident Data Fields type as **Choice**, then after creating the Additional Incident Data Fields you can define the Additional Incident Data Fields choice options.

To create an Additional Incident Data Fields choice option:

    1.  Open the required Additional Incident Data Fields.
    2.  In the Custom Choice Field Options section, select **New**.
    3.  In the Option Name field, define the required option name.
    4.  Select **Submit**.
-   **Date**
-   **Date/Time**
 **Note:** After you select a type for your new Additional Incident Data Fields, you can't modify it. If you want to modify the type, you must create a new Additional Incident Data Fields again with the required type. For **Check box** and **Choice** field types, DLP end users will not see the field in the DLP Workspace unless it contains a value \(a checked box or a selected choice\).

</td></tr><tr><td>

Order

</td><td>

Option to choose the order in which the Additional Incident Data Fields should be displayed. You can define the order value for each Additional Incident Data Fields. The Additional Incident Data Fields are sorted based on the order values that you define.By default, the Additional Incident Data Fields are sorted in ascending order. You can sort the Additional Incident Data Fields in descending order by clicking on the **Order** column.

</td></tr><tr><td>

Active

</td><td>

Option to indicate whether the Additional Incident Data Fields is active.

</td></tr><tr><td>

Description

</td><td>

Description for the Additional Incident Data Fields you created.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[DLP Incident Response Administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/data-loss-prevention/data-loss-prevention-administration.md)

**Related topics**  


[DLP default configuration settings]()

[Create end user lookup rules]()

[Create assignment rules]()

[Create incident consolidation rules]()

[Create response due date rules]()

[Create Approval Rules]()

[Create user instructions templates]()

[Create email templates]()

[Create a Data Loss Prevention Incident Response SLA trigger]()

[Create a Data Loss Prevention Incident Response SLA definition]()

[Create assessments]()

[Configure response option for your DLP incidents]()

[Create incident response option rules]()

[Create age chart configurations]()

[Create user delegate configurations]()

[Create repeat offender identification rules]()

[DLP SLA Definition form]()

[Configure advanced settings]()

[Monitor DLP Integration Run process]()

[DLP Incident Access Restrictions]()

[DLP Incidents Archival]()

