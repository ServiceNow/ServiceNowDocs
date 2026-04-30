---
title: Configuring agentic workflows in Now Assist in Contract Management
description: Configure agentic workflows in Now Assist in Contract Management so that contract fulfillers can use the AI agents to perform specific tasks autonomously.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [Enable agentic workflows in Now Assist in Contract Management]
breadcrumb: [Configure, Now Assist in CM Pro, Contract Management Pro, Employee Service Management]
---

# Configuring agentic workflows in Now Assist in Contract Management

Configure agentic workflows in Now Assist in Contract Management so that contract fulfillers can use the AI agents to perform specific tasks autonomously.

Complete the following steps to configure agentic workflows in Contract Management Pro.

1.  Install the Now Assist in Contract Management plugin \(sn\_cm\_gen\_ai\).
    -   For information about the plugin installation process, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).
    -   For information about the plugin dependencies and plugin activation order, see [Application information](cncore-support-info-na.md#cmpro-na-app-info).
2.  Ensure Now Assist panel is turned on. For more information, see [Activate Now Assist panel standard chat](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).
3.  Ensure **Now Assist Panel - Platform \(default\)** assistant in the CI Admin Experience is turned on. For more information, see [Manage LLM virtual agents on the Assistants screen](https://www.servicenow.com/docs/access?context=manage-llm-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).
4.  Configure the security controls to specify the users who can discover or use the agentic workflow, and provide data permissions for the agentic workflow.

    For more information, see [Configuring user access and data permissions for agentic workflows](cmpro-conf-users-agentic-wf.md).

5.  Configure the security controls to specify the users who can discover or use the agentic workflow, and provide data permissions for AI agents.

    For more information, see [Configuring user access and data permissions for AI agents](cmpro-conf-users-ai-agents.md).

6.  Ensure that Contract metadata extraction and Contract obligation extraction skills are configured and activated in Now Assist Admin console.

    For more information, see [Configuring contract metadata extraction](../task/cncore-conf-metadata-extraction.md) and [Configuring contract obligation extraction](../task/cncore-conf-obligation-extraction.md).

7.  Activate business rules for the agentic workflow to run the AI agents autonomously. For more information, see [Activate business rules for the Manage contract repository agentic workflow](../task/conf-repository-agentic-ai.md).
8.  If you want to modify an agentic workflow, duplicate it and then update it.

    For more information see:

    -   [Duplicate an agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)
    -   [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)
    -   [Modify an agentic workflow](https://www.servicenow.com/docs/access?context=modify-aia-use-case&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)
9.  If you have customized the Manage contract repository agentic workflow, update the script include to run it autonomously.

    For more information, see [Update the contracts AI agents handler script include](../task/cmpro-script-includ-agenticAI.md).

10. Configure system properties to set the notice period for the Manage contract repository agentic workflow that will be used when the contract renewal notice period and termination of contract renewal notice period are not available in a contract.

    For more information, see [Set the default notice period for the Manage contract repository agentic workflow](../task/conf-sys-prop-default-np.md).

11. Enable the email notification for contract metadata and obligation extraction to notify users when metadata extraction is completed.

    For more information, see [Enable notifications for AI extracted metadata and obligations](../task/cmpro-na-me-agentic-ntf.md).


-   **[Activate business rules for the Manage contract repository agentic workflow](../task/conf-repository-agentic-ai.md)**  
Activate the Agentic AI - Set reminders for contract and the Agentic AI Set reminders for Econtract business rules to autonomously run the Manage contract repository agentic workflow.
-   **[Configuring user access and data permissions for agentic workflows](cmpro-conf-users-agentic-wf.md)**  
Configure the security controls to specify the users who can discover or use the agentic workflow, and provide data permissions for the agentic workflow.
-   **[Configuring user access and data permissions for AI agents](cmpro-conf-users-ai-agents.md)**  
Configure the security controls to specify the users who can discover or use the agentic workflow, and provide data permissions for AI agents.
-   **[Set the default notice period for the Manage contract repository agentic workflow](../task/conf-sys-prop-default-np.md)**  
Configure system properties to set the default notice period for the Manage contract repository agentic workflow.
-   **[Update the contracts AI agents handler script include](../task/cmpro-script-includ-agenticAI.md)**  
Update the ContractsAIAgentsHelper script include to add the sys\_id of a customized Manage contract repository agentic workflow to run the agentic workflow autonomously.
-   **[Enable notifications for AI extracted metadata and obligations](../task/cmpro-na-me-agentic-ntf.md)**  
Enable the email notifications for metadata extraction and obligation extraction to notify users when metadata extraction and obligation extraction are complete.

**Parent Topic:**[Configure Now Assist in Contract Management](../task/confg-na-in-cmpro.md)

**Related topics**  


[Select large language models for use cases in Now Assist in Contract Management](../task/cmpro-na-manage-llm.md)

[Configure data permissions for Now Assist skills](../task/cmpro-conf-roles-skills.md)

[Configuring contract metadata extraction](../task/cncore-conf-metadata-extraction.md)

[Configuring contract analysis](cmpro-conf-contract-analysis.md)

[Configuring contract obligation extraction](../task/cncore-conf-obligation-extraction.md)

[Post-upgrade steps for Now Assist in Contract Management](../task/cmpro-na-upgrade-steps.md)

