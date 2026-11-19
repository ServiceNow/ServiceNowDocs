---
title: Run a model with the Explore ERP models agentic workflow
description: ServiceNow Otto finds the ERP model that you name, asks for any required inputs, and runs the model for you.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erpc-run-a-model-with-explore-erp-models.html
release: brazil
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-11-03"
reading_time_minutes: 2
keywords: [erp, zero, copy, connector, sap, ai, otto, agentic, ai agent, explore, model, run, content pack]
breadcrumb: [ERP models, Using, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Run a model with the Explore ERP models agentic workflow

ServiceNow Otto finds the ERP model that you name, asks for any required inputs, and runs the model for you.

## Before you begin

Role required: sn\_erp\_integration.erp\_ai\_user

The ServiceNow Otto for Zero Copy Connector and Knowledge Graph plugins are installed. For more information, see [Requirements for using AI in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-prereqs-for-ai.md).

ServiceNow Otto is set up for agentic workflows. For more information, see [Prepare ServiceNow Otto for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-prepare-otto-for-erp-agentic-workflows.md).

## About this task

The Explore ERP models agentic workflow uses a team of AI agents to answer questions about configured ERP database tables and models, including models in ERP content packs. In this task, you use it to run a model that you name.

## Procedure

1.  Select the Otto icon \(\[Omitted image "bus-ai-otto.svg"\] Alt text:\) from anywhere in your instance to open the ServiceNow Otto panel.

2.  Name the model that you want to run in plain language.

    For example, `I want to run the Order Details model`.

3.  Select **Explore ERP models**.

4.  Select **Go to the ERP Model**.

5.  If the model has mandatory fields, enter values in the format shown.

    You can also fill in optional fields.

    ServiceNow Otto runs the model and shows the results.


## Result

Your conversation is saved until you start a new chat. If the conversation ends unexpectedly, start a new chat by selecting the New chat icon \(\[Omitted image "icon-zoom-in.png"\]\).

## What to do next

To change what the model returns, manage its inputs and outputs. For more information, see [Managing Zero Copy Connector for ERP model inputs, outputs, and field mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-canvas-manage-models.md).

**Parent Topic:**[Building and managing models to work with ERP data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/work-with-erp-data-models.md)

**Related topics**  


[Skills, agentic workflows, and AI agents in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-ai-skills-workflows-and-agents.md)

[Exploring Zero Copy Connector for ERP models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/exploring-erp-models.md)

