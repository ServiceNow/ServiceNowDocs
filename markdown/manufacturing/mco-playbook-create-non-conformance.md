---
title: Create a product non-conformance case using playbook
description: Create a non-conformance case for the products that have issue using the playbook experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/manufacturing/mco-playbook-create-non-conformance.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Product non-conformance, Agent management, Use, Manufacturing Commercial Operations]
---

# Create a product non-conformance case using playbook

Create a non-conformance case for the products that have issue using the playbook experience.

## Before you begin

Role required: Product Non-conformance Submitter \(sn\_mfg\_qm.product\_non\_conformance\_submitter\) or Product Non-conformance Triager \(sn\_mfg\_qm.product\_non\_conformance\_case\_triager\)

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** &gt; **List** &gt; **Product Non Conformance Case** &gt; **All** &gt; **New**.

    The guided Product Non Conformance Case playbook displays.

2.  **Quick start**.

    1.  Select **Install Base**.

        The account associated with the install base item is displayed.

    2.  Select **Continue**.

3.  **Describe the issue**

    1.  Enter the **Issue description**.

    2.  Select **Add file**, to add supporting documents.

    3.  Select **Continue**.

4.  **Follow-up**

    1.  On the Issue Details form, fill in the following fields.

        |Field|Description|
        |-----|-----------|
        |What is the problem?|Description of the problem or incident in clear, concise terms.|
        |Where is the problem observed?|Location of the issue.|
        |When did this problem happen or get identified?|Timeline of the issue. This includes when it was first detected, when it occurred, and the duration of its impact.|
        |Who is involved, responsible, or affected by the problem?|Details of the customer facing the problem.|
        |Why is this problem important?|Underlying causes of the issue.|
        |How will the problem be resolved?|Details of how the issue will be resolved.|
        |How much will it cost to fix the problem?|Number of parts or customers affected.|

    2.  Select **Back** to return to the previous form.
    3.  Select **Save**.
    4.  Select **Continue**.
    **Note:** Select **Restart** to clear all the form data entry and start over without leaving the form.

5.  **Identify duplicate**

    Duplicate non-conformance details are displayed. You can open the record and verify if the record is duplicate or not. If the record is confirmed as duplicate, then it is marked as **Closed Duplicate**.

    Select **Submit**.

6.  **Add correction action**

    1.  Select **Log or select a correct** to add correction action.

        1.  Select **Recommend corrections**.

            The correction action recommendations are displayed.

        2.  Select **Add**.
        3.  In the **Add correction details** form, fill in the following details:

            |Field|Description|
            |-----|-----------|
            |Short description|Short note.|
            |Description|Detailed description of the correction action.|

        4.  Select **Add Expense**.
        5.  In the **Expense line** form, fill in the following details:

<table id="id_sxf_nqh_jjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Description

</td><td>

Short note on the expense line.

</td></tr><tr><td>

CoPQ type

</td><td>

CoPQ type:-   Part
-   Labor
-   Service
-   Material
-   Rework


</td></tr><tr><td>

Amount

</td><td>

Amount of CoPQ expense line.

</td></tr><tr><td>

Asset

</td><td>

Identification number of the asset associated with the expense line, if any.

</td></tr></tbody>
</table>            **Note:** You can add multiple expense lines.

        6.  Select **Save** to save the expense line.
        7.  Select **Back** to return to the previous form.
        8.  Select **Continue**.
    2.  Select **Create remediation action plan**.

        **Note:** If you have already created correction action for this case, a notification is displayed to remove the correction action.

        1.  Select **Add**.
        2.  In the **Remediation action plan details** form, fill in the following details:

            |Field|Description|
            |-----|-----------|
            |Plan name|Name of the remediation action plan.|
            |Description|Detailed description of the remediation action plan.|

        3.  Select **Add planned line charges**.

<table id="id_oqw_hsh_jjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CoPQ type

</td><td>

CoPQ type:-   Part
-   Labor
-   Service
-   Material
-   Rework


</td></tr><tr><td>

Quantity

</td><td>

Number of units.

</td></tr><tr><td>

Unit cost

</td><td>

Cost per unit.

</td></tr><tr><td>

Product model

</td><td>

Select the product model.

</td></tr><tr><td>

Unit of measure

</td><td>

Select the unit of measure

</td></tr><tr><td>

Planned cost

</td><td>

Planned cost will be auto calculated based on the `quantity * unit cost * unit` of measure.

</td></tr></tbody>
</table>            **Note:** You can add multiple planned line charges.

        4.  Select **Save**.
        5.  Select **Continue**.
    3.  Select **No action at this time**.

        **Note:** If you have already created correction action or remediation action for this case, a notification is displayed to remove them.

        Select **Continue**.

7.  **Review and Submit**.

    On the Review and submit form, review all the details.

    **Note:** You can edit any activity if it is pending.

    **Review issue details and support document** provides all the required information for this case.

8.  Select **Submit**.

    The PNCC case is submitted for review.


**Parent Topic:**[Product non-conformance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-product-non-conformances.md)

## Create a product non-conformance case as resolver

### Before you begin

Role required: Quality Issue Management Admin or product non-conformance resolver \(sn\_mfg\_qm.product\_non\_conformance\_resolver\)

### Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** &gt; **List** &gt; **Product Non Conformance Case** &gt; **All** &gt; **New**.

    The guided Product Non Conformance Case playbook displays.

2.  Create a non-conformance case

    1.  Select **Install Base**.

        The account associated with the install base item is displayed.

    2.  Select **Continue**.

3.  **Understand the issue**

    1.  Examine the product details

        1.  On the **Product Details** form, fill in the fields.

            For a description of the field values, see [Product details form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-product-non-conformance-case-form.md).

        2.  Select **Assign to me,** to assign the case to self.
        3.  Select **Save &amp; continue**.
    2.  Manage the issue details

        1.  On the **Issue Details** form, fill in the fields.
        2.  Select **Save &amp; continue**.
    3.  Manage the documents

        1.  Select **Add file** and attache the required documents.
        2.  Select **Mark complete**.
4.  **Apply correction**

    1.  Select **Recommend corrections**.

        The correction action recommendations are displayed and it will be in close complete state.

    2.  Select **Use as template**.

        Select the template based on your required correction action template. You can view the record source details.

    3.  Select **Add**.

    4.  Select edit to view and edit the correction actions form.

        You can add [Correction actions form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-correction-actions-form.md) and [CoPQ expense line form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-copq-expense-line-form.md) details.

    5.  Select **Create work order** activity.

        On the work order form, add the [Work order form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/work-order-form.md) details.

    6.  Select **Save**.

5.  **Batch containment**

    1.  Identify impact.

        1.  Select **Add**.
        2.  On the Create new Impact asset, fill in the following details.
            -   Issue
            -   Status
            -   Asset
            -   Install base
        3.  Select **Save**.
        4.  Select **Continue**.
    2.  **Apply Containment**

        1.  Select **Recommend containment**.

            The containment actions are displayed and it will be in close complete state.

        2.  Select **Use as template**.

            Select the template based on your required correction action template. You can view the record source details.

        3.  Select **Add**.
        4.  Select edit to view and edit the containment actions form.

            You can add [Correction actions form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-correction-actions-form.md) details.

        5.  Select **Save**.
6.  **Manage outcome**

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

**Related topics**  


[Create a root cause analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-root-cause-analysis-task.md)

[Create a correction action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-correction-actions.md)

[Create an impacted asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-impacted-asset.md)

[Create a containment action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-containment-actions.md)

[Task SLA](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-task-sla.md)

[Create a parent-child relationship](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-relationships.md)

[Remediation action plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-remediation-action-plans.md)

