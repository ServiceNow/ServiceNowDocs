---
title: Data center infrastructure allocation
description: Data center infrastructure allocation reserves rack unit space by evaluating placement policies, capacity metrics, and the requirements specified in a change request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/telecom-network-inventory/telecommunications-network-inventory/data-center-infra-allocation.html
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 2
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# Data center infrastructure allocation

Data center infrastructure allocation reserves rack unit space by evaluating placement policies, capacity metrics, and the requirements specified in a change request.

## Data center infrastructure allocation overview

Data center infrastructure allocation reserves rack unit space in a data center based on the requirements specified in a change request and the placement policies you have configured.

When a data center infrastructure allocation change request is submitted, the target data center, rack units, power, weight, temperature constraints, and any equipment specifications in **Short description**, **Description**, and **Work notes** fields, are taken as input for rack allocation analysis.

Selecting the **Find Allocation** button initiates the rack allocation agentic workflow. It handles change requests and finds racks that can accommodate the capacity requirement based on specific physical and logical constraints. The workflow processes change requests that require rack unit allocation and creates Affected CI records. To learn more see [Rack allocation workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-media-technology/rack-allocation-workflow.md)

After data center infrastructure allocation completes, the change request is updated in the following areas:

-   **Work notes**: the Placements and Decisions sections list the placement result, which racks were selected, which were excluded, and the reason for each decision.
-   **Review output panel** displays the rack placement recommendation and a structured summary of the requirements as interpreted from your change request.
-   **Affected CIs tab** shows the allocated slot and rack created automatically.

In the rack view, reserved slots display the change request number. Select the number to view change request details, including the short description, requested by, scheduled dates, and current state, without leaving the rack view.

When allocation fails, the Close Code field displays **Unsuccessful** as the status and the Close Notes field displays the reason for the failure.

## Re-initiating rack allocation

When you re-initiate the **Find Allocation** action on a change request with the same or slightly modified short description that already contains Affected CIs, a dialog appears asking whether to continue or finish without changes.

-   **Continue**: The system treats slots marked as reserved from the previous run as occupied. This reduces available contiguous space and may affect which racks are eligible for the new run.
-   **Finish**: The system exits without making changes.

**Parent Topic:**[Telecommunications Network Inventory reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-reference.md)

**Related topics**  


[https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/data-center-infra-allocation-placement-policies.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/data-center-infra-allocation-placement-policies.md)

[Data center infrastructure allocation failure cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/data-center-infra-allocation-failure-cases.md)

[Data center infrastructure rack allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/data-center-infra-rack-allocation.md)

