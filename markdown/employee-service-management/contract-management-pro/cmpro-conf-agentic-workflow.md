---
title: Configuring agentic workflows in Now Assist in Contract Management
description: Configure agentic workflows in Now Assist in Contract Management so that contract fulfillers can use the AI agents to perform specific tasks autonomously.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2025-04-16"
reading_time_minutes: 1
breadcrumb: [Now Assist in Contract Management, Contract Management Pro, Employee Service Management]
---

# Configuring agentic workflows in Now Assist in Contract Management

Configure agentic workflows in Now Assist in Contract Management so that contract fulfillers can use the AI agents to perform specific tasks autonomously.

Complete the following steps to configure agentic workflows in Contract Management Pro.

1.  Install the Now Assist in Contract Management plugin \(sn\_cm\_gen\_ai\).
    -   For information about the plugin installation process, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
    -   For information about the plugin dependencies and plugin activation order, see [Application information](cncore-support-info-na.md#cmpro-na-app-info).
2.  Ensure Now Assist panel is turned on. For more information, see [Turn on the Now Assist panel](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
3.  Ensure **Now Assist Panel - Platform \(default\)** assistant in the CI Admin Experience is turned on. For more information, see [Manage LLM virtual agents on the Assistants screen](https://www.servicenow.com/docs/access?context=manage-llm-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).
4.  Activate business rules for the agentic workflow to run the AI agents autonomously. For more information, see [Activate business rules for the Manage contract repository agentic workflow](../task/conf-repository-agentic-ai.md).
5.  If you want to modify an agentic workflow, duplicate it and then update it.

    For more information see:

    -   [Duplicate an agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)
    -   [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)
    -   [Modify an agentic workflow](https://www.servicenow.com/docs/access?context=modify-aia-use-case&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)
6.  If you have customized the Manage contract repository agentic workflow, update the script include to run it autonomously.

    For more information, see [Update the contracts AI agents handler script include](../task/cmpro-script-includ-agenticAI.md).

7.  Configure system properties to set the notice period for the Manage contract repository agentic workflow that will be used when the contract renewal notice period and termination of contract renewal notice period are not available in a contract.

    For more information, see [Set the default notice period for the Manage contract repository agentic workflow](../task/conf-sys-prop-default-np.md).


