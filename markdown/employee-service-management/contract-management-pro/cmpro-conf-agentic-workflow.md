---
title: Configuring agentic workflows in Now Assist in Contract Management
description: Configure agentic workflows in Now Assist in Contract Management so that contract fulfillers can use the AI agents to perform specific tasks autonomously.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/employee-service-management/contract-management-pro/cmpro-conf-agentic-workflow.html
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
    -   For information about the plugin installation process, see .
    -   For information about the plugin dependencies and plugin activation order, see [Application information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/contract-management-pro/cncore-support-info-na.md).
2.  Ensure Now Assist panel is turned on. For more information, see .
3.  Ensure **Now Assist Panel - Platform \(default\)** assistant in the CI Admin Experience is turned on. For more information, see .
4.  Activate business rules for the agentic workflow to run the AI agents autonomously. For more information, see [Activate business rules for the Manage contract repository agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/contract-management-pro/conf-repository-agentic-ai.md).
5.  If you want to modify an agentic workflow, duplicate it and then update it.

    For more information see:

    -   
    -   
    -   
6.  If you have customized the Manage contract repository agentic workflow, update the script include to run it autonomously.

    For more information, see [Update the contracts AI agents handler script include](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/contract-management-pro/cmpro-script-includ-agenticAI.md).

7.  Configure system properties to set the notice period for the Manage contract repository agentic workflow that will be used when the contract renewal notice period and termination of contract renewal notice period are not available in a contract.

    For more information, see [Set the default notice period for the Manage contract repository agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/contract-management-pro/conf-sys-prop-default-np.md).


