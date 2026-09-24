---
title: Resolve a product non-conformance case playbook
description: Use the guided product non-conformance case playbook to create a case, apply corrections, manage batch containment, and close the case with a resolution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/manufacturing/mco-resolve-a-pnc-case-playbook.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Product non-conformance, MCO workspace, Use, Manufacturing Commercial Operations]
---

# Resolve a product non-conformance case playbook

Use the guided product non-conformance case playbook to create a case, apply corrections, manage batch containment, and close the case with a resolution.

## Before you begin

Role required: Quality Issue Management Admin or Product Non-conformance Resolver \(sn\_mfg\_qm.product\_non\_conformance\_resolver\)

## Procedure

1.  Navigate to **Workspaces** &gt; **CRM Workspace** &gt; **List** &gt; **Product Non Conformance Case** &gt; **All** &gt; **New**.

    The guided Product Non Conformance Case playbook displays.

2.  Create a non-conformance case

    1.  Select **Install Base**.

        The account associated with the install base item is displayed.

    2.  Select **Continue**.

3.  Understand the issue

    1.  Examine the product details

        1.  On the **Product Details** form, fill in the fields.

            For a description of the field values, see [Product details form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/manufacturing/mco-product-non-conformance-case-form.md).

        2.  Select **Assign to me**, to assign the case to self.
            -   If the case is assigned to you and is in the New state, select **Accept**. The case moves from New to In Progress state.
            -   If you need more information from the submitter, select **Request Info**. The Request Information pop-up is displayed and you can add your comments. A notification is sent to the submitter. The case moves to the Awaiting Info state, and the task SLA pauses. It resumes when the state is changed to In Progress.
            -   If you try to mark the current activity complete while the case is in the Awaiting Info state, a message appears. The message states that a submitter response is required before you can proceed.
            -   If more information is not needed from the submitter, select **Info Received**. The case moves to the In Progress state, and you can mark the current activity complete.
        3.  Select **Save &amp; continue**.
    2.  Manage the issue details

        1.  On the **Issue Details** form, fill in the fields.
        2.  Select **Save &amp; continue**.
    3.  Manage the documents

        1.  Select **Add file** and attach the required documents.
        2.  Select **Mark complete**.
    **Note:** You cannot select **Mark complete** for the form if you have requested more \(awaiting status\) information from the submitter.

4.  Apply correction

    1.  Select **Add**.

    2.  Select **Edit** to view and edit the correction actions form.

        You can add [Correction actions form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/manufacturing/mco-correction-actions-form.md) and [CoPQ expense line form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/manufacturing/mco-copq-expense-line-form.md) details.

    3.  Select **Propose Solution**.

        **Note:** **Propose Solution** is enabled when at least one correction action is added and is in the closed state.

        The **State** is updated to Correction Proposed. The PNCC case on the Standard ticket page has two additional options **Accept** or **Reject**.

    4.  Select **Save**.

5.  Complete batch containment

    1.  Identify the impact.

        1.  Select **Add**.
            1.  On the Create New Impact Asset form, fill in the following details.
                -   **Issue**
                -   **Status**
                -   **Asset**
                -   **Install base**
            2.  Select **Save**.
        2.  Select **Import**.

            1.  Select the template to download and use.
            2.  On the Import form, select **Add file**.
            3.  Select the required XLSX file. It contains the following details:
                -   Asset \(Serial number\)
                -   Status \(Optional\)
            4.  Select **Upload**.
            5.  Select **Import**.
            6.  Select **Continue**.
            **Note:** Multiple files can be uploaded. If the same file is re-uploaded without making the changes, then that file is skipped.

        The system displays the status of the import and the number of records created or updated.

    2.  Apply containment

        1.  Select **Recommend containment**.

            The containment actions are displayed. The case moves to the Closed Complete state.

        2.  Select **Use as template**.

            Select the template based on your required correction action template. You can view the record source details.

        3.  Select **Add**.
        4.  Select **Edit** to view and edit the containment actions form.

            You can add [Correction actions form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/manufacturing/mco-correction-actions-form.md) details.

        5.  Select the **Create work order** activity. On the work order form, add the [Work order form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/manufacturing/work-order-form.md) details.
        6.  Select **Add Impacted asset**, to add manually.
        7.  Select **Import asset** to upload the impact asset XLSX file.
        8.  Select **Save**.
6.  Manage outcome

    1.  Manage the Pre-Closure Checklist activity.

        1.  Select **Create quality investigation**.
        2.  Select **Continue**.
    2.  Finish the process.

        1.  Select **State**.
        2.  To close, select **Closed Complete**.
        3.  Select **Resolution code**.
        4.  For the resolution, select **Solved**.
        5.  Enter your resolution details in the **Resolution notes** field.
        6.  Select **Close**.
7.  At any point before the case is closed, select **Summarize** from the ServiceNow Otto context menu on the case.

    This option is available only in the Workspace view.

    The system generates two summaries at the same time:

    -   A brief summary, displayed in the panel. It includes a title, a short description of the case, and highlights such as when the case was opened, severity, and priority. Select the copy icon to copy the summary text.
    -   A detailed summary appears in the report section. This summary remains available even after you close the case.
    **Note:** Selecting **Summarize** again regenerates both summaries and overwrites the previous versions. AI-generated summaries may be inaccurate or incomplete. Review the summaries before relying on them.


**Parent Topic:**[Product non-conformance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/manufacturing/mco-product-non-conformances.md)

