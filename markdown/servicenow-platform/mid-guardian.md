---
title: MID Server Guardian
description: The MID Guardian is an agentic AI feature within the MID Server ecosystem and ITOM Infra Services Workspace. It is designed to proactively assist users in diagnosing and resolving issues related to configuration, connectivity, upgrades, and operations.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use Now Assist agentic workflows for MID Server, Now Assist for MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server Guardian

The MID Guardian is an agentic AI feature within the MID Server ecosystem and ITOM Infra Services Workspace. It is designed to proactively assist users in diagnosing and resolving issues related to configuration, connectivity, upgrades, and operations.

The MID Guardian analyzes logs, signals, and runtime behaviors to offers guided troubleshooting steps, automated fixes, and predictive insights. The agent significantly reduces Mean Time to Repair \(MTTR\) and enhances the reliability and operational efficiency of the MID Server. Features of the MID Guardian include:

-   Root cause analysis \(RCA\) with Agentic AI
-   Correlation of symptoms from various telemetry sources \(logs, errors\)
-   Automated execution of corrective actions \(validating or restarting services\)
-   Playbook-driven or Agentic AI-led remediation strategies
-   Action recommendations for unresolved or partially resolved issues, utilizing web searches
-   Self-learning from previous resolutions and human interventions

## Access MID Guardian

To begin using MID Guardian, open the agentic AI chat and type or select MID Guardian. The MID Guardian provides the options:

-   **Troubleshooting existing MID Server**

    You can provide the name or sys\_id of the MID Server you want to troubleshoot. The MID Guardian checks the MID Server for issues and creates a plan for corrective actions.

-   **Setting up a new MID Server**

    The MID Guardian generates a procedure to set up a MID Server using existing documentation. The MID Guardian takes into account issues like Network connectivity problems and adjusts the procedure accordingly.

-   **Something else**

    You can provide an error message and the MID Guardian searches web resources, such as Knowledge Base articles, to create a troubleshooting procedure.


When you are finished, type `end chat` to stop the agent.

## MID Guardian in ITOM Infra Services Workspace

Using MID Guardian from the ITOM Infra Services Workspace dashboard enables the agent to use the information on the page to inform its suggestions and actions.

If you open a specific MID Server record, opening the Agentic AI chat and selecting MID Guardian automatically assesses the record. If you go to the MID Server Issues section of a record and open the MID Guardian, the MID Guardian focuses on the errors present. The MID Guardian offers diagnosis for issues, such as the MID Server upgrade failed. The MID Guardian can create a procedure to resolve the issue, including suggesting diagnostic scripts for you to run to gather necessary information.

For certain issues, MID Guardian can automatically implement corrective actions. If it detects that current issue can be solved through remediation such as re-keying MID Servers or restarting services, the MID Guardian offers to initiate the action automatically.

## Check MID Server logs

If the MID Guardian checks a MID Server and detects no issues, it provides options to investigate potential issues. You can select **Fetch MID Server Errors and Warnings** to make the MID Guardian call the MID Server, scan its logs, and get the ECC queue record.

The MID Guardian collates a list of most frequent errors. You can choose an error, and the MID Guardian draws from corroborating web data, existing documentation, and Knowledge Base articles to create a troubleshooting procedure.

**Parent Topic:**[Use Now Assist agentic workflows for MID Server](now-assist-mid-use.md)

