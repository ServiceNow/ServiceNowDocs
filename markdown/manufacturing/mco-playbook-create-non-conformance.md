---
title: Create a product non-conformance case
description: Create a non-conformance case for the products that have issue.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Product non-conformance, Agent management, Use, Manufacturing Commercial Operations]
---

# Create a product non-conformance case

Create a non-conformance case for the products that have issue.

## Before you begin

Role required: Quality Issue Management Admin, product non-conformance resolver \(sn\_mfg\_qm.product\_non\_conformance\_resolver\) or product Non-conformance Submitter \(sn\_mfg\_qm.product\_non\_conformance\_submitter\)

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** &gt; **List** &gt; **Product Non Conformance Case** &gt; **All** &gt; **New**.

    The guided Product Non Conformance Case playbook displays.

2.  Create a non-conformance case.

    1.  Select **Install Base**.

        The account associated with the install base item is displayed.

    2.  Select **Continue**.

3.  **Understand the issue**

    1.  Examine the product details.

        1.  On the Product Details form, fill in the fields.

            For a description of the field values, see [Product details form](../reference/mco-product-non-conformance-case-form.md)

        2.  Select **Save**, to save the product details.
        3.  Select **Assign to me**, to assign the case to self.
        4.  Select **Continue**.
        The Issue Details activity window displays.

    2.  Manage the issue details.

        1.  On the Issue Details form, fill in the following fields.

            |Field|Description|
            |-----|-----------|
            |What|Description of the problem or incident in clear, concise terms.|
            |Where|Location of the issue.|
            |When|Timeline of the issue. This includes when it was first detected, when it occurred, and the duration of its impact.|
            |Why|Underlying causes of the issue.|
            |How|Details of how the issue occurred and how it was resolved.|
            |How much|Number of parts or customers affected.|

        2.  Select **Save** to save these values.
        3.  Select **Continue**.
    3.  Manage the documents.

        1.  Select **Add file** to attach documents.
        2.  Select **Mark Complete**.
        When you select **Mark Complete**, all activities in Understand the Issue are marked complete. The Apply correction and Batch containment activities display simultaneous.

4.  Apply a correction.

    1.  Select the **Apply Correction** Activity.

    2.  Select **Add** to add new correction action.

    3.  Select edit to view and edit the correction actions form.

        You can [Create a correction action](mco-correction-actions.md) and

    4.  Select **Continue**&gt;**Mark complete**.

5.  If there are similar issues that are in the same location, apply a batch containment.

    1.  Identify the impact.

        1.  Select **Add**.
        2.  On the Create new Impact asset, fill in the following details.
            -   Issue
            -   Status
            -   Asset
            -   Install base
        3.  Select **Save**.
        4.  Select **Continue**.
    2.  Apply the containment.

        1.  Select **Add**.
        2.  On the Containment actions form, fill in the [Containment action form](../reference/mco-containment-actions-form.md) details.
        3.  Add the Expense line details.
            -   Description
            -   CoPQ Type
            -   Asset
            -   Amount
        4.  Select the **Map impacted assets**.
        5.  Select **Add file**, to add any attachments.
        6.  Select **Save**.
        7.  Select **Mark Complete**.
6.  Manage the outcome.

    On per-closure checklist, review all the details. It shows the activities that are completed or pending.

    **Note:** You can edit any activity, if it is pending. All the pending activities will be in red.

    1.  Manage the Pre-Closure Checklist activity.

        1.  Select **Create quality investigation**.
        2.  Select **Continue**.
    2.  Finish the process.

        1.  Select **State**.
        2.  To close, select **Closed complete**.
        3.  Select **Resolution code**.
        4.  To close, select **Solved**.
        5.  Add **Resolution notes**.
        6.  Select **Close**.

-   **[Related lists for Non-conformance](mco-related-lists-product-non-conformance.md)**  
In the workspace, you can use the product non-conformance related list to log the report.

**Parent Topic:**[Product non-conformance](../concept/mco-product-non-conformances.md)

**Related topics**  


[Create a correction action](mco-correction-actions.md)

[Create an impacted asset](mco-impacted-asset.md)

[Impacted asset action](mco-impacted-asset-action.md)

[Create a containment action](mco-containment-actions.md)

[Create a CoPQ expense line](mco-copq-expense-line.md)

[Create a product quality investigation](mco-create-product-quality-investigation.md)

