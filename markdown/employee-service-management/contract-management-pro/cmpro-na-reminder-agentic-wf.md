---
title: Manage contract repository agentic workflow
description: Use the manage contract repository agentic workflow to improve productivity by extracting metadata and obligations automatically from signed contracts and setting the contract reminder dates for contract renewal or termination.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Use agentic workflows, Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Manage contract repository agentic workflow

Use the manage contract repository agentic workflow to improve productivity by extracting metadata and obligations automatically from signed contracts and setting the contract reminder dates for contract renewal or termination.

## Manage contract repository overview

**Important:**

-   To use the agentic workflow for your workspace, your role must be configured to use the agentic workflow, and the data access permissions must be set for the AI agents and the agentic workflow.

    For more information, see [Configuring user access and data permissions for agentic workflows](cmpro-conf-users-agentic-wf.md) and [Configuring user access and data permissions for AI agents](cmpro-conf-users-ai-agents.md).

-   The data access permissions must be set for the Now Assist skills, contract metadata extraction, and contract obligation extraction.

    For more information, see [Configure data permissions for Now Assist skills](../task/cmpro-conf-roles-skills.md).

-   To run the AI agents autonomously, ensure that the business rules for the agentic workflow are activated. For more information, see [Activate business rules for the Manage contract repository agentic workflow](../task/conf-repository-agentic-ai.md).

    If you have customized the manage contract repository agentic workflow, make sure to update the script include to run it autonomously. For more information, see [Update the contracts AI agents handler script include](../task/cmpro-script-includ-agenticAI.md).

-   To view the agentic workflow in the Now Assist panel, turn on the Now Assist panel. For more information, see [Activate the Now Assist panel standard chat](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

The manage contract repository agentic workflow uses an AI agent to do the following sequentially.

-   Extract metadata from signed contracts.
-   Calculate the contract reminder date for renewal and termination.
-   Extract obligations from signed contracts.

## Metadata extraction and contract reminders

The AI agent uses Now Assist contract metadata extraction skill to extract key metadata from signed contracts. Once the metadata extraction is complete, you can open the playbook to review the extracted information and set the contract reminder date.

The following workflow explains the metadata extraction and contract reminder setup process.

1.  As a Contract Admin with the AI role, activate the contract metadata extraction skill in the Now Assist Admin console.

    For more information, see [Configure Now Assist in Contract Management](../task/confg-na-in-cmpro.md).

2.  As a Contract Admin, activate the business rules.
3.  The metadata extraction process is automatically initiated when a contract record is created.
4.  Once the extraction is complete, the Contract Manager with the AI role receives a notification indicating that the metadata is ready for review.
5.  The Contract Manager reviews the extracted metadata and submits it to update the contract repository.
6.  The contract reminder date is then calculated based on the following factors:
    -   Contract end date
    -   Presence of auto-renewal clause
    -   Notice period for contract renewal or termination

        **Note:** If the renewal notice period and termination notice period aren’t available, it uses the configured default notice period. For more information, see [Set the default notice period for the Manage contract repository agentic workflow](../task/conf-sys-prop-default-np.md).

7.  The Contract Manager sets the contract reminders in the playbook by reviewing the calculated date and configuring the recipient list for the reminders.

For more information, see [Review AI-extracted metadata and contract reminder date](../task/cmpro-na-review-ai-metadata.md).

## Obligation extraction

The AI agent uses Now Assist contract obligation extraction skill to extract key contractual obligations from contracts. Once extracted, you can review the obligations within the contract playbook and choose to accept or reject them. Accepted obligations are added as records in the **Obligations** tab of the contract record.

The following workflow explains the obligation extraction process.

1.  As a Contract Admin with the AI role, activate the contract obligation extraction skill in the Now Assist Admin console.

    For more information, see [Configure Now Assist in Contract Management](../task/confg-na-in-cmpro.md).

2.  As a Contract Admin, activate the business rules.
3.  The obligation extraction process is automatically initiated when a contract record is created.
4.  Once the extraction is complete, the Contract Manager with the AI role receives a notification indicating that obligations are ready for review.
5.  The Contract Manager reviews the extracted obligations within the contract playbook. Each obligation can be accepted or rejected based on relevance.
6.  Approved obligations are automatically added as obligation records in the **Obligations** tab of the contract record.
7.  Obligation tasks are created.
    -   For a recurring schedule, the obligation tasks are automatically created for the obligation record based on the defined schedule.
    -   For an ad hoc schedule, the contract manager creates an obligation task from the **Obligation tasks** tab in the contract record.
8.  The assigned user is notified when the obligation task is created.
9.  The assigned user works on the obligation task and submits it for review.

    The state of the obligation task changes from Open to Awaiting approval.

10. The Obligation Fulfiller reviews the task and approves or rejects it.
    -   If the obligation task is rejected, the state of the task changes to Open, and the assigned user continues to work on it.
    -   If the obligation task is approved, the state of the task changes to Completed.

For more information, see [Review AI-extracted obligations](../task/cmpro-na-review-obligations.md).

## Conditions for the agentic workflow to trigger

The manage contract repository agentic workflow for a non-self-served request is triggered as soon as the contract repository record is created and the Assigned to user in the request has the sn\_cm\_gen\_ai.ai\_contract\_fulfiller and now\_assist\_panel\_user role.

The manage contract repository agentic workflow for a self-served request is triggered as soon as the contract repository record is created and the following conditions are met:

-   The group manager of the Assignment group has the now\_assist\_panel\_user role.
-   If there’s no group manager for the Assignment group, one of the users in the Assignment group has the now\_assist\_panel\_user role.
-   If the user requested changes on the contract request, the Assigned to user or the group manager in the request has the sn\_cm\_gen\_ai.ai\_contract\_fulfiller and now\_assist\_panel\_user role.

Contract fulfillers and assignment group managers with the now\_assist\_panel\_user role can view the agentic workflow conversation in the Now Assist panel.

**Note:** The agentic workflow isn’t supported in the Virtual Agent panel.

## Accessing the agentic workflow

Role required: sn\_aia.admin

If your generative AI service provider isn’t Now LLM Service, ensure that the API connections and credentials are configured. For more information, see [Configuring API credentials for generative AI capabilities](https://www.servicenow.com/docs/access?context=configuring-api-credentials-for-generative-ai-capabilities&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Manage contract repository**.

## AI agents used in the manage contract repository agentic workflow

<table id="table_rpx_swm_v2c"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Contract Repository AI agent

</td><td>

Uses various tools to perform the following:-   Retrieves the contract repository details, such as contract vendor, contract model, contract document's attachment ID, and so on from a specific contract repository record.
-   Extracts metadata from signed contact documents based on the applicable use case in the contract metadata extraction skill.
-   Extracts obligations from signed contact documents based on the applicable use case in the contract obligation extraction skill.
-   Calculates the average lead time for similar contracts.

</td></tr></tbody>
</table>