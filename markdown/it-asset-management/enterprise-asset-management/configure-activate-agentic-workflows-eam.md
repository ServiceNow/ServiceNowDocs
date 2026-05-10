---
title: Configure and activate agentic workflows for Enterprise Asset Management
description: Configure and activate the agentic workflows that you want to use in the Enterprise Asset Workspace.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-18"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Enterprise Asset Management, IT Asset Management]
---

# Configure and activate agentic workflows for Enterprise Asset Management

Configure and activate the agentic workflows that you want to use in the Enterprise Asset Workspace.

## Before you begin

Role required: sn.aia\_admin role or an appropriate role that is defined in your [security controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aw.md)

## Procedure

1.  If you want to use a customized agentic workflow, configure it through one of the following options:

    -   Create a new workflow and configure the settings according to your requirements.

        For detailed instructions, see [Create an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-use-case-ai-agents.md).

    -   Duplicate an existing workflow and adjust the settings according to your requirements.

        For detailed instructions, see [Duplicate an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md).

    -   Modify an existing workflow according to your requirements.

        For detailed instructions, see [Modify an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/modify-aia-use-case.md).

    **Note:** If you want to run an existing agentic workflow as is, skip this step and proceed directly to [step 3](configure-activate-agentic-workflows-eam.md#trigger).

2.  Test the customized agentic workflow to analyze its performance while it executes the instructions that you have defined.

    -   To test the agentic workflow manually, see [Manually test the execution of an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-aia-use-case.md).
    -   To test the agentic workflow automatically against various execution log datasets, see [Execute an agentic evaluation run](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/execute-aia-eval.md).
3.  Activate the trigger to invoke the agentic workflow automatically.

    For detailed instructions, see [Activate an agentic workflow template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-aia-use-case.md).

    **Note:** If you do not activate the trigger, you must invoke the agentic workflow manually.


