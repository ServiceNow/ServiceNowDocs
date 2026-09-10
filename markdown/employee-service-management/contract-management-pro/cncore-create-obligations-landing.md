---
title: Create obligations using AI
description: Create obligation records for signed contracts to fulfill the responsibilities specified in the contract. You can create obligations manually or use AI to automatically extract obligations from contract documents.Use the contract playbook to review, edit, approve, or reject obligations automatically extracted from contract documents. Approved obligations are added as obligations records in the Obligations tab of the contract repository.Create obligation records for signed contracts in Obligation Management to fulfill the responsibilities specified in the contract through obligation tasks. Recurring obligation tasks are automatically created from the record. You can also add ad hoc obligation tasks that are performed only once or at irregular intervals.Create an obligation task required only once or at irregular intervals to track and fulfill an obligation specified in a contract.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cncore-create-obligations-landing.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2026-08-13"
reading_time_minutes: 6
keywords: [Create obligations, Obligation extraction, AI obligations, Recurring obligation task, Recurring schedule]
breadcrumb: [Obligation Management, Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Create obligations using AI

Create obligation records for signed contracts to fulfill the responsibilities specified in the contract. You can create obligations manually or use AI to automatically extract obligations from contract documents.

You can create obligation records using one of the following methods:

**Parent Topic:**[Obligation Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-obligation-management.md)

## Review AI-extracted obligations

Use the contract playbook to review, edit, approve, or reject obligations automatically extracted from contract documents. Approved obligations are added as obligations records in the **Obligations** tab of the contract repository.

### Before you begin

The Contract Management Pro - Prime plugin \(sn\_cm\_ai\_prime\) must be installed to use AI capabilities.

Role required: sn\_cm\_gen\_ai.ai\_contract\_fulfiller

### About this task

The manage contract repository agentic workflow uses AI agents to extract key contractual obligations from signed contracts. The obligations are extracted based on the applicable use case in the contract obligation extraction skill. After obligation extraction is complete, a message appears on the contract record and an email notification is sent with a link to review the extracted obligations. The playbook provides a step-by-step interface where you can review each obligation, make necessary edits, and decide whether to approve or reject it. Approved obligations are added as actionable records in the **Obligations** tab of the contract repository.

### Procedure

1.  Open a contract repository record where you want to review the extract information.

<table id="choicetable_zst_kcr_5bc"><thead><tr><th align="left" id="d556723e140">

Method

</th><th align="left" id="d556723e143">

Steps

</th></tr></thead><tbody><tr><td id="d556723e149">

**Contract Workspace**

</td><td>

1.  Navigate to **All** &gt; **Contract Workspace**.
2.  Select the list icon \[Omitted image "lsd-lcc-list-icon.png"\] Alt text:.
3.  Select **Executed contracts**.
4.  Select **All**.
5.  Select the contract repository record.


</td></tr><tr><td id="d556723e196">

**Workspace used by your application**

</td><td>

1.  Navigate to your workspace.
2.  Open a contract request that is in the Closed complete or Contract signed state.
3.  Select the **Contract repository** tab.
4.  Select the contract repository record.


</td></tr><tr><td id="d556723e223">

**Email notification**

</td><td>

Select **Review contract** in the email notification that you receive after the obligation extraction is complete.

</td></tr></tbody>
</table>2.  Select the **Playbook** tab.

    The playbook opens displaying a step-by-step interface to review the extracted obligations.

    \[Omitted image "cmpro-na-playbook.png"\] Alt text: Contract playbook displaying extracted obligations details.

3.  In the playbook, navigate to the **Review obligations** step under the AI extracted obligations section.

4.  Select **Review**.

    The extracted obligations are displayed on a new tab.

    \[Omitted image "cmpro-na-ob-extracted.png"\] Alt text: Form displaying the list of extracted obligations.

5.  Select an obligation to review the obligation details.

    -   The **Details** tab displays the extracted obligation details. Use this tab to edit, approve, or reject the obligation.
    -   The **Activity** tab displays a log of key attributes identified during the extraction process. Use this tab to review how the AI agent detected and populated the obligation, including the original text snippets and metadata extracted from the contract. The **Activity** tab helps you validate the extraction accuracy and provides transparency into the decision-making process for each obligation.
    \[Omitted image "cmpro-na-ob-reviewob.png"\] Alt text: Obligation details form displaying the information extracted by AI.

6.  On the **Details** tab, perform the required action.

    -   Edit the obligation details as needed.

        **Note:** Complete all required fields before saving the changes or approving the obligation.

        For more information on the fields, see [Obligation form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-obligation-form.md).

    -   Select **Save** to save the changes.
    -   Select **Approve** to approve the extracted obligation and add it as a record in contract repository.
    -   Select **Reject** to reject the extracted obligation.

        Once an obligation is rejected, it’s deactivated and can’t be reactivated again. If you need to add the obligation later, you must create an obligation record manually. For more information, see [Create obligation records manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-create-obligations-landing.md).

7.  Repeat step 6 for all the extracted obligations.

8.  Navigate to the **Playbook** tab in the contract repository after you have reviewed all the obligations.

9.  Select **Mark as completed**.


### Result

Approved obligations are available as records in the **Obligations** tab of the contract repository. Rejected obligations are deactivated and excluded from further processing.

If the schedule of the obligation is recurring, the obligation tasks are automatically created based on the interval specified in the **Repeats** field.

If the schedule of the obligation is adhoc, you must create obligation tasks manually. For more information see, [Create an ad hoc obligation task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-create-obligations-landing.md).

\[Omitted image "cmpro-na-ob-added.png"\] Alt text: Obligations tab displaying the list of obligations added in the contract repository record.

**Related topics**  


[Obligation Management]()

[Obligation form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-obligation-form.md)

[Create obligations manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-work-on-ob-tasks.md)

[Cancel an obligation task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-cancel-ob-task.md)

[Approve or reject obligation tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-manage-ob-tasks.md)

[Obligation Management notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-ob-mgmt-notification.md)

## Create obligation records manually

Create obligation records for signed contracts in Obligation Management to fulfill the responsibilities specified in the contract through obligation tasks. Recurring obligation tasks are automatically created from the record. You can also add ad hoc obligation tasks that are performed only once or at irregular intervals.

### About this task

**Note:** For more information about adding obligation tasks that are performed only once or at irregular intervals, see [Create an ad hoc obligation task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-create-obligations-landing.md).

### Before you begin

The contract record must be in Active state.

The group managers of the Legal Contract Owners and Obligation Fulfillers groups must also be a member of the respective group.

Role required: sn\_cm\_obligation.obligation\_fulfiller

### Procedure

1.  Open an executed contract from the your workspace.

<table id="choicetable_zst_kcr_5bc"><thead><tr><th align="left" id="d556723e603">

Method

</th><th align="left" id="d556723e606">

Steps

</th></tr></thead><tbody><tr><td id="d556723e612">

**Contract Workspace**

</td><td>

1.  Navigate to **All** &gt; **Contract Workspace**.
2.  Select the list icon \(\[Omitted image "lsd-lcc-list-icon.png"\] Alt text: List icon\).
3.  Select **Executed Contracts**.
4.  Select **All**.
5.  Select an active contract repository record.


</td></tr><tr><td id="d556723e660">

**Workspace used by your application**

</td><td>

1.  Navigate to your workspace.
2.  Open a contract request that is in Closed complete or Contract signed state.
3.  Select the **Contract repository** tab.
4.  Select an active contract repository record.


</td></tr></tbody>
</table>2.  Select the **Obligations** tab.

3.  Select **New**.

    **Note:** If the **New** button is not available, verify that the selected contract is active.

4.  On the form, fill in the fields.

    For more information, see [Obligation form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-obligation-form.md).

5.  Select **Save**.


## Create an ad hoc obligation task

Create an obligation task required only once or at irregular intervals to track and fulfill an obligation specified in a contract.

### Before you begin

The obligation and contract must be in Active state.

The schedule type in the obligation record must be **Adhoc**.

Role required: sn\_cm\_obligation.obligation\_fulfiller

### Procedure

1.  Open an obligation from the workspace that you are using.

<table id="choicetable_zst_kcr_5bc"><thead><tr><th align="left" id="d556723e806">

Method

</th><th align="left" id="d556723e809">

Steps

</th></tr></thead><tbody><tr><td id="d556723e815">

**Contract Workspace**

</td><td>

1.  Navigate to **All** &gt; **Contract Workspace**.
2.  Select the List icon \(\[Omitted image "lsd-lcc-list-icon.png"\] Alt text: List icon\).
3.  Select **Obligations**.
4.  Select **All obligations**.
5.  Select an active obligation record.


</td></tr><tr><td id="d556723e863">

**Workspace used by your application**

</td><td>

1.  Navigate to your workspace.
2.  Open a contract request that is in Closed complete or Contract signed state.
3.  Select the **Contract repository** tab.
4.  Open an active contract record.
5.  Select the **Obligations** tab.
6.  Select an active obligation record.


</td></tr></tbody>
</table>2.  Select the **Obligation tasks** tab.

3.  Select **New**.

4.  On the New obligation task page, in the **Assigned to** field, update the assigned user.

5.  In the **Due date** field, select the due date for the obligation task.

6.  Select **Save**.


### Result

The obligation task is created and the assigned user is notified through email.

