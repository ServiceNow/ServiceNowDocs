---
title: Rack allocation workflow
description: The rack allocation agentic workflow reserves rack unit space in a datacenter by evaluating placement policies, capacity metrics, and change request requirements to find suitable rack allocations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/now-assist-for-telecom-media-and-technology/rack-allocation-workflow.html
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2026-07-09"
reading_time_minutes: 1
breadcrumb: [Customer Service Problem Management, Use agentic workflows, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Rack allocation workflow

The rack allocation agentic workflow reserves rack unit space in a datacenter by evaluating placement policies, capacity metrics, and change request requirements to find suitable rack allocations.

## Rack allocation workflow overview

The rack allocation agentic workflow handles change requests and finds racks that can accommodate the capacity requirement based on specific physical and logical constraints. The workflow processes change requests that require rack unit allocation and creates Affected CI records. You can resolve infrastructure requests faster and reduce queue delays. To learn more see [Data center infrastructure rack allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/data-center-infra-rack-allocation.md)

## Role required

Role required: sn\_ni\_core.dc\_ops\_agent or sn\_ni\_core.inventory\_agent

## Access the rack allocation workflow

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Rack Allocation Workflow**.

## Test the agentic workflow

To access the use case testing page:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**.
2.  On the Overview page, select **Rack allocation workflow**.

To test the use case, see [Manually test the execution of an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-aia-use-case.md).

## AI agents in the rack allocation workflow

The Rack Allocation Workflow uses the Rack placement AI agent to execute allocation steps. The LLM matches the agent's name and description to workflow steps to select the appropriate agent.

<table id="table_gzg_pqh_l2c"><thead><tr><th>

AI agent

</th><th>

AI agent role

</th></tr></thead><tbody><tr><td>

Rack placement AI agent

</td><td>

Finds a datacenter rack allocation that fits a change request's capacity requirements. The agent runs autonomously based on the workflow instructions.

Tools used by the agent

-   **find\_rack\_placement** — Finds racks that can accommodate the requested resources. Applies placement policies and capacity constraints. Returns a ranked list of suitable racks.
-   **validate\_change\_request** — Validates the change request. Verifies required fields are present and properly formatted. Returns validation status.
-   **finalize\_allocation** — Finalizes the rack allocation flow: writes a work note summarizing the outcome and moves the change request to Design Complete state.
-   **retrieve\_change\_request** — Reads the change request from CMDB. Extracts target data center, RU, power, weight, temperature, and equipment requirements.
-   **retrieve\_policy** — Retrieves placement policies from published Knowledge Base articles for the target datacenter and individual racks.

</td></tr></tbody>
</table>**Related topics**  


[Data center infrastructure rack allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/data-center-infra-rack-allocation.md)

