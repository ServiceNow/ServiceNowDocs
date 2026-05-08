---
title: Use the Analyze potential impact agentic workflow to assess a change request
description: Use the Analyze potential impact agentic workflow to assess the effects of a change request. This workflow highlights the potential impacted servers and suggested services to help you identify risks, benefits, and make any necessary adjustments.
locale: en-US
release: australia
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [installing Now Assist, AI features, AI products, updating Now Assist, solutions, Now Assist, GenAI, generative AI, configure Now Assist]
breadcrumb: [Analyze potential impact agentic workflow, Use agentic AI, Now Assist for ITOM, IT Operations Management]
---

# Use the Analyze potential impact agentic workflow to assess a change request

Use the Analyze potential impact agentic workflow to assess the effects of a change request. This workflow highlights the potential impacted servers and suggested services to help you identify risks, benefits, and make any necessary adjustments.

## Before you begin

Using the Analyze potential impact agentic workflow requires the installation of the following:

-   Service Mapping Plus version 1.16.3.
-   Now Assist for IT Operations Management \(ITOM\) version 2.3.0.
-   Now Assist for IT Service Management \(ITSM\) version 11.1.3.

Role required: sn\_change\_write

## Role masking

Required role:

Agentic workflows and their AI agents use role masking to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see Define security controls for an agentic workflow.

## About this task

The agent verifies the prerequisites at the beginning of the agentic workflow. If any prerequisites aren’t met, the workflow stops, and you’re informed so that you can acquire the prerequisites. For more information about the agentic workflow, see [Analyze potential impact agentic workflow](../concept/now-assist-itom-analyze-potential-impact-workflow.md).

## Procedure

1.  Either initiate the Analyze potential impact agentic workflow using a change request number or from an open change request.

<table id="choicetable_rkr_bbt_3gc"><thead><tr><th align="left" id="d285358e154">

Situation

</th><th align="left" id="d285358e157">

Steps

</th></tr></thead><tbody><tr><td id="d285358e163">

**Change request number is known**

</td><td>

1.  From the header menu, select the Now Assist icon ![](../../../common/image/icon-ai-sparkle.png) to open the Now Assist panel.
2.  Select **Analyze Potential Impact**.
3.  When prompted, enter the change request number.


</td></tr><tr><td id="d285358e195">

**Open change request**

</td><td>

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace** &gt; **.**
2.  Select the list icon ![](../../event-management/image/list-icon-op-ws.png).
3.  Navigate to **Changes** &gt; **All**.
4.  Select the applicable change request from the list.
5.  From the header menu, select the Now Assist icon ![](../../../common/image/icon-ai-sparkle.png) to open the Now Assist panel.
6.  Select **Analyze Potential Impact**.


</td></tr></tbody>
</table>    The Analyze potential impact agentic workflow is initiated and the agent starts with the verification of the prerequisites.


## Result

In the Now Assist panel, the Analyze potential impact agentic workflow generates an analysis of the potentially impacted relevant servers and suggested services.

The impact analysis is updated in the work notes in the change request details.

