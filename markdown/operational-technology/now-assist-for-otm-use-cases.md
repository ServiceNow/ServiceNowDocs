---
title: Use agentic AI for Now Assist for Operational Technology Manager \(OTM\)
description: Use the Operational Technology Manager \(OTM\) AI agent within an agentic workflow to complete tasks autonomously.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/operational-technology/now-assist-for-otm-use-cases.html
release: zurich
product: Operational Technology
classification: operational-technology
topic_type: concept
last_updated: "2025-11-21"
reading_time_minutes: 2
breadcrumb: [Now Assist for OTM, Operational Technology]
---

# Use agentic AI for Now Assist for Operational Technology Manager \(OTM\)

Use the Operational Technology Manager \(OTM\) AI agent within an agentic workflow to complete tasks autonomously.

<table id="table_ofm_rf1_l2c"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Import OT device spreadsheet into OT CMDB

</td><td>

With the Import OT device spreadsheet into OT CMDB agentic workflow, you can do the following:-   Import the device inventory spreadsheet and map data to the OT staging table
-   Validate OT staging table records, remediate invalid records, and import all validated records into the Configuration Management Database \(CMDB\)

</td><td>

OT Excel import task AI agent

</td></tr></tbody>
</table>**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. For more information, see .

## Supported Large Language Models

**Note:**

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in AI Control Tower to define which options are available, then set the skill-level preferences in the Now Assist Admin console. For more information, see .

## Security implementation considerations

Enable security implementation to execute AI agents and agentic workflows through Access Control Lists \(ACLs\) and user identities. For more information, see 

## Considerations for running the autonomous AI agents

**Important:** By default, all agent workflow and AI agent records are read-only.

To run the AI agents autonomously, you must first duplicate the agentic workflow, and then proceed with the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. The triggers for each agentic workflow must be unique. If you prefer to invoke it manually, activating the trigger isn’t necessary.

## Standalone AI agents

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see Find AI agents.
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

## Role masking

Role masking enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see Define security controls for an agentic workflow.

-   **[Import the OT device spreadsheet into OT CMDB agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/now-assist-otm-aiagents-import-ot-device-workflow.md)**  
Use the Import OT device spreadsheet into OT CMDB agentic workflow to automate the upload, validation, and import of your OT device data into the OT CMDB.

**Parent Topic:**[Now Assist for Operational Technology Manager \(OTM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/now-assist-for-otm-landing.md)

