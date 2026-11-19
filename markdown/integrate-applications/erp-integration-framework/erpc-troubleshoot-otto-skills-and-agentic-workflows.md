---
title: Troubleshoot ServiceNow Otto agentic workflows
description: Use generative AI logs and Workflow Studio to find out why a ServiceNow Otto agentic workflow in Zero Copy Connector for ERP didn't return what you expected.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erpc-troubleshoot-otto-skills-and-agentic-workflows.html
release: brazil
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-11-03"
reading_time_minutes: 1
keywords: [erp, zero, copy, connector, ai, otto, skill, agentic, troubleshoot, generative ai log, flow debug, workflow studio]
breadcrumb: [Troubleshooting, Using, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Troubleshoot ServiceNow Otto agentic workflows

Use generative AI logs and Workflow Studio to find out why a ServiceNow Otto agentic workflow in Zero Copy Connector for ERP didn't return what you expected.

## Before you begin

Role required: admin

## About this task

Start with the generative AI logs. If you need more detail about how an agentic workflow ran, turn on flow debugging and check the executions in Workflow Studio.

## Procedure

1.  View the generative AI logs.

    1.  Select **All**, enter `sys_generative_ai_log_list.do` in the **Filter**, and press **enter** or **return** on your keyboard.

    2.  Open a record to view its details.

2.  For more detail about an agentic workflow, turn on flow debugging and check its executions.

    The com.glide.oneapi.flow\_debug property turns on debugging for flows built with OneAPI so that you get reporting and insights into flow execution.

    1.  Select **All**, enter `sys_properties.list` in the **Filter**, and press **enter** or **return** on your keyboard.

    2.  Search for and open the property named **com.glide.oneapi.flow\_debug**.

    3.  Set the **Value** to `true`, and save the record.

    4.  Open Workflow Studio and check the executions.

        \[Omitted image "erp-data-explorer-workflow6.png"\] Alt text: Workflow Studio Operations tab, with two executions highlighted.

        For more information, see [Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio.md).


## Result

The log records and flow executions show where the agentic workflow stopped or returned unexpected results.

**Parent Topic:**[Zero Copy Connector for ERP troubleshooting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-canvas-troubleshooting.md)

**Related topics**  


[View and deactivate ERP skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-activate-and-manage-erp-skills.md)

[Prepare ServiceNow Otto for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-prepare-otto-for-erp-agentic-workflows.md)

