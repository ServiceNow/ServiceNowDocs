---
title: Report an issue
description: Use the Dealer portal to submit non-conformance issues with AI-guided workflows for duplicate detection, assessment, and cost tracking.Report a product non-conformance case using the catalog to describe the issue, identify duplicates, and add correction actions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/manufacturing/mco-report-issue-using-playbook.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 7
keywords: [product non-conformance, Quality Issue Management, correction action]
breadcrumb: [Quality issue management for the dealer, Dealer portal, Use, Manufacturing Commercial Operations]
---

# Report an issue

Use the Dealer portal to submit non-conformance issues with AI-guided workflows for duplicate detection, assessment, and cost tracking.

## Before you begin

Role required: Quality Issue Management Admin or Product Non-conformance Submitter \(sn\_mfg\_qm.product\_non\_conformance\_submitter\)

## Procedure

1.  Navigate to **Dealer Portal** &gt; **Report an issue**.

2.  In the Create New Product Non-conformance Case, select the **Quick start** activity.

    1.  Select **Install Base** from the list.

    2.  Select **Continue**.

        The system retrieves the Account/Service organization/Consumer name for the selected install base item.

    3.  Select **Continue**.

3.  In the **Describe the issue** field, enter the issue description in your own words.

    The description is evaluated for 5W2H — what, where, when, who, why, and how — based on the information provided.

    1.  Select **Suggestions for improvement** to get assistance from ServiceNow Otto \[Omitted image "icon-ai-sparkle.png"\] Alt text:.

    2.  Select + to add the supporting document and work orders.

    3.  Select **Save**.

    4.  Select **Continue**.

4.  Proceed without entering the details in the **Follow-up** activity.

    -   ServiceNow Otto \[Omitted image "icon-ai-sparkle.png"\] Alt text: analyzes the issue description and attachments to auto-populate answers to the follow-up questions.
    -   You can edit the auto-populated answers by selecting the form fields and **Continue**.
5.  In the **Identify duplicate** activity, check if there's any existing non-conformance case \(PNCC\) for the same install base item.

    The system searches the existing PNCCs in the same install base, compares short description and description, and returns the top match based on confidence score. Confidence score is the matching percentage between the existing PNCC and the new submission.

    -   Yes, this is a duplicate: The report exits the flow and this draft is closed as a duplicate. You're redirected to the existing parent PNCC.
    -   No, continue with the new PNCC: The draft report continues.
6.  In the **Add correction action** activity, update whether the correction action is already applied to resolve the issue.

    -   No: It enables you to continue to **Review and Submit**. You can select this option anytime before selecting **Continue**. It deletes the new correction details that you added.
    -   Yes: **Add correction details** and **Expense line** are enabled.

        |Field|Description|
        |-----|-----------|
        |Add Correction details|
        |Short description|Short description of the correction.|
        |Description|Detailed description of the correction.|
        |Expense line|
        |Description|Short description of the expense line|
        |CoPQ type|Cost of poor quality type.|
        |Asset|Type of asset.|
        |Amount|Cost of the labor or administrative, or cost incurred to procure a new item.|

    Add multiple correction actions by selecting **Add**.

7.  Select **Continue** to save your changes.

8.  In the Review and submit section, review all the 5W2H details, correction actions, and the expense lines tagged to the correction actions.

    Review and edit any values. Add additional information if needed, then select **Submit**.

    The system generates an issue reference number for the submitted case.

9.  Check the notification for PNCC updates from the resolver.

    -   If the resolver requests more information, review the record and update the information in the activity stream. The product non-conformance case \(PNCC\) state changes from Awaiting info to In Progress. The SLA pauses when the state changes to "Awaiting info" and resumes once the state returns to "In progress"
    -   If the resolver proposes a correction, review the correction actions for the case.
    -   Select **Accept Solution**, **Reject Solution**, or **Cancel**
        -   **Auto Accept** — automatically accepts the proposed correction after 5 days without submitter action and the case will be moved to In progress.
        -   **Accept Solution** — moves the case to the In Progress state and logs a comment that the submitter accepted the solution.
        -   **Reject Solution** — prompts you for a reason, returns the case to the resolver, and logs a comment with the rejection reason. The existing SLA is completed and new SLA is created.
        -   **Cancel** — cancel the case.
    -   **Auto Accept** — if a submitter does not accept a solution, the system will automatically change the PNC state from "correction proposed" to "in progress" after five days.

## Report a product non-conformance using the catalog

Report a product non-conformance case using the catalog to describe the issue, identify duplicates, and add correction actions.

### Before you begin

Role required: Quality Issue Management Admin or Product Non-conformance Submitter \(sn\_mfg\_qm.product\_non\_conformance\_submitter\)

### Procedure

1.  Navigate to **Dealer Portal** &gt; **Catalogs** &gt; **Categories** &gt; **Quality issues** &gt; **Report a product non-conformance**.

2.  Select **Quick start**.

    1.  Select **Install Base**.

        The Buyer organization associated with the install base item is displayed.

    2.  Select **Continue**.

3.  Select **Describe the issue**.

    1.  Enter the **Issue description**.

    2.  Select **Add file** to add supporting documents.

    3.  Select **Continue**.

4.  Select **Follow-up**.

    1.  On the Issue details form, fill in the following fields.

        |Field|Description|
        |-----|-----------|
        |What is the problem?|Description of the problem or incident in clear, concise terms.|
        |Where is the problem observed?|Location of the issue.|
        |When did this problem happen or get identified?|Timeline of the issue. This includes when it was first detected, when it occurred, and the duration of its impact.|
        |Who is involved, responsible, or affected by the problem?|Details of the customer facing the problem.|
        |Why is this problem important?|Underlying causes of the issue.|
        |How will the problem be resolved?|Details of how the issue is resolved.|
        |How much will it cost to fix the problem?|Number of parts or customers affected.|

    2.  Select **Back** to return to the previous form.
    3.  Select **Save**.
    4.  Select **Continue**.
5.  Select **Identify duplicate**.

    The system displays duplicate non-conformance details. You can open the record and verify whether the record is a duplicate. If the record is confirmed as a duplicate, then it is marked as **Closed Duplicate**.

    Select **Submit**.

6.  Select **Add correction action**.

    1.  Select **Log or select a correction** to add a correction action.

        1.  Select **Recommend corrections**.

            The correction action recommendations are displayed.

        2.  Select **Add**.
        3.  In the **Add correction details** form, fill in the following details.

            |Field|Description|
            |-----|-----------|
            |Short description|Short note.|
            |Description|Detailed description of the correction action.|

        4.  Select **Add Expense**.
        5.  In the **Expense line** form, fill in the following details.

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

Cost of poor quality \(CoPQ\) type:-   Part
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

Identification number of the asset associated with the expense line.

</td></tr></tbody>
</table>            **Note:** You can add multiple expense lines.

        6.  Select **Save** to save the expense line.
        7.  Select **Back** to return to the previous form.
        8.  Select **Continue**.
    2.  Select **Create remediation action plan**.

        **Note:** If you have already created a correction action for this case, a notification prompts you to remove it.

        1.  Select **Add**.
        2.  In the **Remediation action plan details** form, fill in the following details.

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

Model of the product to use.

</td></tr><tr><td>

Unit of measure

</td><td>

Unit used to measure the quantity.

</td></tr><tr><td>

Planned cost

</td><td>

Planned cost is auto-calculated based on the `quantity * unit cost * unit of measure`.

</td></tr></tbody>
</table>            **Note:** You can add multiple planned line charges.

        4.  Select **Save**.
        5.  Select **Continue**.
    3.  Select **No action at this time**.

        **Note:** If you have already created a correction action or a remediation action plan for this case, a notification prompts you to remove it.

        Select **Continue**.

7.  Select **Review and Submit**.

    On the Review and submit form, review all the details.

    **Note:** You can edit any activity if it is pending.

    **Review issue details and support document** provides all the required information for this case.

8.  Select **Submit**.

    The product non-conformance case \(PNCC\) is submitted for review.

9.  Check the notification for PNCC updates from the resolver.

    -   If the resolver requests more information, review the record and update the information in the activity stream. The product non-conformance case \(PNCC\) state changes from Awaiting info to In Progress. The SLA pauses when the state changes to "Awaiting info" and resumes once the state returns to "In progress"
    -   If the resolver proposes a correction, review the correction actions for the case.
    -   Select **Accept Solution**, **Reject Solution**, or **Cancel**
        -   **Auto Accept** — automatically accepts the proposed correction after 5 days without submitter action and the case will be moved to In progress.
        -   **Accept Solution** — moves the case to the In Progress state and logs a comment that the submitter accepted the solution.
        -   **Reject Solution** — prompts you for a reason, returns the case to the resolver, and logs a comment with the rejection reason. The existing SLA is completed and new SLA is created.
        -   **Cancel** — cancel the case.
    -   **Auto Accept** — if a submitter does not accept a solution, the system will automatically change the PNC state from "correction proposed" to "in progress" after five days.

