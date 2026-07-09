---
title: Reserve a rack using data center infrastructure allocation
description: Reserve rack unit space in a data center by creating a data center infrastructure allocation change request and running the allocation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/telecom-network-inventory/telecommunications-network-inventory/reserve-a-rack-using-data-center-infra-allocation.html
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-07-09"
reading_time_minutes: 2
breadcrumb: [Data center infrastructure rack allocation, Using Design &amp; Assign Network, Use, Telecommunications Network Inventory]
---

# Reserve a rack using data center infrastructure allocation

Reserve rack unit space in a data center by creating a data center infrastructure allocation change request and running the allocation.

## Before you begin

To use custom policies, the Knowledge Base article must be published and set as the latest version.

Role required: sn\_ni\_core.dc\_ops\_agent or sn\_ni\_core.inventory\_agent

## About this task

Data center infrastructure allocation reserves rack unit space in a data center based on the requirements you provide in a change request and the placement policies you have defined.

## Procedure

1.  Navigate to Service Operations Workspace or Network Inventory Workspace.

2.  Select the list icon \(\[Omitted image "ni-workspace-list-icon.png"\] Alt text: List icon\), and then go to **Changes** &gt; **All**.

3.  Select the **New** button.

4.  Select **Data Center Infra allocation**.

5.  Select **Continue**.

6.  Select **Next**.

    Create Change Request form opens.

7.  Enter a brief summary of your allocation request in the **Short description** field.

8.  Enter your allocation requirements in plain text in the **Description** field.

    -   Target site or data center
    -   Rack units required
    -   Power required \(in watts\)
    -   Weight \(in kilograms\)
    -   Temperature constraint
    -   Equipment or devices \(optional\)
    -   Whether to allow split across racks
9.  Select **Save**.

10. Select **Find Allocation**.

    Status updates appear as data center infrastructure allocation evaluates and scores available racks. When the state changes to Design In Progress, rack slots are reserved in the CMDB. When the state changes to Design Complete, the full allocation summary is available in the work notes.

11. Review the allocation results in the following areas.

    -   **Work notes**: the Placements and Decisions section lists which racks were selected, which were excluded, and why.
    -   **Review output panel** shows the rack placement recommendation and a structured summary of the requirements as interpreted from your description.
    -   **Affected CIs tab** shows the allocated slot and rack. Base rack-unit slots are marked as Reserved. Device-specific allocations are linked to the device record.
12. Select the rack in the Affected CIs tab to open the rack record.

    Reserved slots display the change request number. Select the number to view change request details without leaving the rack view. \[Omitted image "image.rack-allocation"\] Alt text: Reserved slots in the rack view showing the change request number

13. If the change request already has Affected CIs, review the dialog and select an option.

    \[Omitted image "image.re-run-allocation"\] Alt text: Dialog asking whether to continue or finish when Affected CIs already exist

    **Note:** Selecting **Continue** treats the slots marked as reserved from the previous run as occupied. This reduces available contiguous space and may affect which racks are eligible for the new run. Selecting **Finish** exits without making changes. You can update your requirements and re-run to find a new allocation.


**Parent Topic:**[Data center infrastructure rack allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/data-center-infra-rack-allocation.md)

