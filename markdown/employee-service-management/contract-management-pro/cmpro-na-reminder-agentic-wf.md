---
title: Manage contract repository agentic workflow
description: Use the Manage contract repository agentic workflow to improve productivity by autonomously creating milestone reminders for the notice period of contract renewals or the notice period for termination of contract renewals.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2025-03-28"
reading_time_minutes: 3
breadcrumb: [Using agentic workflows in Now Assist in Contract Management, Now Assist in Contract Management, Contract Management Pro, Employee Service Management]
---

# Manage contract repository agentic workflow

Use the Manage contract repository agentic workflow to improve productivity by autonomously creating milestone reminders for the notice period of contract renewals or the notice period for termination of contract renewals.

## Manage contract repository overview

**Important:**

-   To run the AI agents autonomously, activate business rules for the agentic workflow. For more information, see [Activate business rules for the Manage contract repository agentic workflow](../task/conf-repository-agentic-ai.md).

    If you have customized the Manage contract repository agentic workflow, update the script include to run it autonomously. For more information, see [Update the contracts AI agents handler script include](../task/cmpro-script-includ-agenticAI.md).

-   To view the agentic workflow in the Now Assist panel, turn on the Now Assist panel. For more information, see [Turn on the Now Assist panel](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

The Manage contract repository agentic workflow can help notify business owners or contract administrators about expiring contracts by automatically creating milestone reminders for the notice period of contract renewals or the notice period for termination of contract renewals. The agentic workflow uses AI agents to retrieve contract details such as the renewal notice period, termination notice period for renewals, or auto-renewal clause information, and determine the average lead time for similar contracts to create the milestone reminders.

**Note:** If the renewal notice period and termination notice period are not available, it uses the default notice period. For more information, see [Set the default notice period for the Manage contract repository agentic workflow](../task/conf-sys-prop-default-np.md).

The agentic workflow for a non-self-served request is triggered when the following conditions are met:

-   The contract repository record is created with a contract end date, or the end date in a contract repository is modified.
-   The **Assigned to** user in the request has the now\_assist\_panel\_user role.

The agentic workflow for a self-served request is triggered when the following conditions are met:

-   The contract repository record is created with a contract end date, or the end date in a contract repository is modified.
-   The group manager of the **Assignment group** has the now\_assist\_panel\_user role.

    If there is no group manager for the **Assignment group**, one of the users in the **Assignment group** has the now\_assist\_panel\_user role.

    If the user requested changes on the contract request, the **Assigned to** user or the group manager in the request has the now\_assist\_panel\_user role.


Contract fulfillers and assignment group managers with the now\_assist\_panel\_user role can view the agentic workflow conversation in the Now Assist panel.

**Note:** The agentic workflow is not supported in the Virtual Agent panel.

## Accessing the agentic workflow

Role required: sn\_aia.admin

If your generative AI service provider is not Now LLM Service, ensure that the API connections and credentials are configured. For more information, see [Configuring API credentials for generative AI capabilities](https://www.servicenow.com/docs/access?context=configuring-api-credentials-for-generative-ai-capabilities&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Set reminders for contract milestones**.

## AI agents used in the Manage contract repository agentic workflow

|Name|Description|
|----|-----------|
|Extract contract metadata AI agent|Extracts the renewal notice period, notice period to terminate the renewals, and auto-renewal clause information from signed contact documents.|
|Calculate contract lead time AI agent|Determines the average lead time for similar contracts.|
|Set contract milestone reminder AI agent|Creates contract renewal reminders.|
|Contract record handler AI agent|Retrieves the contract repository details, such as contract vendor, contract model, contract document's attachment ID, and so on from a specific contract repository record.|

