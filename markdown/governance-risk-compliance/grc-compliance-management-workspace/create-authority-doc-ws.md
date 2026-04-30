---
title: Create an authority document using the Compliance Workspace
description: Authority documents manage a process, and citations are created within them to manage the points of the process. For example, the process called Building Security contains a citation for Entry Control.
locale: en-US
release: yokohama
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Manage control objectives and policies using the Compliance Workspace, Using the Compliance Workspace, Performing compliance tasks in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Create an authority document using the Compliance Workspace

Authority documents manage a process, and citations are created within them to manage the points of the process. For example, the process called Building Security contains a citation for Entry Control.

## Before you begin

Role required: sn\_compliance\_ws.corporate\_compliance\_analyst, sn\_compliance\_ws.corporate\_compliance\_manager, sn\_compliance\_ws.it\_compliance\_manager

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  Select the **Create** list and select **Authority document**.

3.  On the form, fill in the fields.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the document.

</td></tr><tr><td>

Number

</td><td>

Read-only field that is automatically populated with a unique identification number.

</td></tr><tr><td>

Source

</td><td>

A non-editable field with the source of the policy. For example, if the statement is from the UCF import, the source is UCF.

</td></tr><tr><td>

Source ID

</td><td>

The unique identification number used by the source to catalog this authority document.

</td></tr><tr><td>

Version

</td><td>

The unique version number used by the source to identify this authority document.

</td></tr><tr><td>

Common name

</td><td>

Abbreviated version of the **Name** field.

</td></tr><tr><td>

Category

</td><td>

Category for this authority document.

</td></tr><tr><td>

Type

</td><td>

The document type: -   Audit Guideline
-   Best Practice Guideline
-   Bill or Act
-   Contractual Obligation
-   International or National Standard
-   Not Set
-   Organizational Directive
-   Regulation of Statute
-   Safe Harbor
-   Self-Regulatory Body Requirement
-   Vendor Documentation


</td></tr><tr><td>

Valid From

</td><td>

The date and time for which the policy becomes valid.

</td></tr><tr><td>

Valid To

</td><td>

The date and time for which the policy is no longer valid.

</td></tr><tr><td>

Url

</td><td>

The URL of the stored authority document.

</td></tr><tr><td>

Description

</td><td>

More information about the authority document.

</td></tr></tbody>
</table>4.  Select **Save**.

    The authority document is created and all its related lists are available for your view. By default, the Overview page opens up to display the **Description** of the authority document record and highlights the record details in the sidebar of the page.

5.  From the **Overview** page, select the **Issues**.

    You can add existing one or more related issues to the authority document that you created. By mapping the existing issues to the authority document, you can reduce the count of open issues on the document.

    1.  Select the **Add** button.

    2.  Select the related issue or issues from the Issues pop-up.

    3.  Select **Add**.

        The selected issues are added to the authority document as related issues. You can also create an issue for the authority document by selecting the **New** button.

    4.  To remove an issue that is mapped to an authority document, select the issue and click **Remove**.

        The remove action only removes the mapping between the authority document and the issue, and doesn’t delete the issue record.

        **Note:** The UI action buttons such as New, Add, Remove aren’t available if the authority document is in Retired state.


