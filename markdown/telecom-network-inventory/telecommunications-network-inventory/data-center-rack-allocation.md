---
title: Data center infra allocation
description: Data center infra allocation change request reserves rack unit using the rack allocation agentic workflow. The rack allocation agentic workflow handles change requests and finds racks that can accommodate the capacity requirement based on specific physical and logical constraints.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/data-center-rack-allocation.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-07-23"
reading_time_minutes: 2
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# Data center infra allocation

Data center infra allocation change request reserves rack unit using the rack allocation agentic workflow. The rack allocation agentic workflow handles change requests and finds racks that can accommodate the capacity requirement based on specific physical and logical constraints.

## Data center infrastructure allocation overview

Data center infrastructure allocation reserves rack unit space in a data center based on the requirements specified in a change request and the placement policies you have configured.

\[Omitted image "data-center-infra-allocation-process-diagram.png"\] Alt text: Data center infrastructure allocation process diagram

When a data center infrastructure allocation change request is submitted, the target data center, rack units, power, weight, temperature constraints, and any equipment specifications in **Short description**, **Description**, and **Work notes** fields, are taken as input for rack allocation analysis.

Selecting the **Find Allocation** button initiates the rack allocation agentic workflow. It handles change requests and finds racks that can accommodate the capacity requirement based on specific physical and logical constraints. The workflow processes change requests that require rack unit allocation and creates Affected CI records. To learn more see [Rack allocation workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/rack-allocation-workflow.md)

After data center infrastructure allocation completes, the change request is updated in the following areas:

-   **Work notes**: the Placements and Decisions sections list the placement result, which racks were selected, which were excluded, and the reason for each decision.
-   **Review output panel** displays the rack placement recommendation and a structured summary of the requirements as interpreted from your change request.
-   **Affected CIs tab** shows the allocated slot and rack created automatically.

In the rack view, reserved slots display the change request number. Select the number to view change request details, including the short description, requested by, scheduled dates, and current state, without leaving the rack view.

\[Omitted image "rack-allocation.png"\] Alt text: Rack allocation using change request

When allocation fails, the Close Code field displays **Unsuccessful** as the status and the Close Notes field displays the reason for the failure.

\[Omitted image "close-notes.png"\] Alt text: Close Notes field showing the reason for rack allocation failure

## Re-initiating rack allocation

When you re-initiate the **Find Allocation** action on a change request with the same or slightly modified short description that already contains Affected CIs, a dialog appears asking whether to continue or finish without changes.

-   **Continue**: The system treats slots marked as reserved from the previous run as occupied. This reduces available contiguous space and may affect which racks are eligible for the new run.
-   **Finish**: The system exits without making changes.

\[Omitted image "re-run-allocation.png"\] Alt text: Dialog asking whether to continue or finish a rack allocation re-run

**Parent Topic:**[Telecommunications Network Inventory reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-reference.md)

**Related topics**  


[Data center infrastructure allocation placement policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/data-center-infra-allocation-placement-policies.md)

[Data center infrastructure allocation failure cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/data-center-infra-allocation-failure-cases.md)

[Data center infrastructure rack allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/data-center-infra-rack-allocation.md)

