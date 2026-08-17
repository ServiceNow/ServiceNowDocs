---
title: Re-initiate rack allocation
description: Re-initiate the Find Allocation action on a change request to find new racks to reserve when your requirements change or when the initial allocation needs to be revised.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/reinitiate-rack-allocation.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [Data center infrastructure rack allocation, Using Design &amp; Assign Network, Use, Telecommunications Network Inventory]
---

# Re-initiate rack allocation

Re-initiate the **Find Allocation** action on a change request to find new racks to reserve when your requirements change or when the initial allocation needs to be revised.

## Before you begin

Role required: sn\_ni\_core.dc\_ops\_agent or sn\_ni\_core.inventory\_agent

## About this task

When you re-initiate the Find Allocation action, slots reserved from the previous run are treated as occupied. This may reduce available contiguous space and affect which racks are eligible.

## Procedure

1.  Navigate to Service Operations Workspace or Network Inventory Workspace.

2.  Select the list icon \(\[Omitted image "ni-workspace-list-icon.png"\] Alt text: List icon\), and then go to **Changes** &gt; **All**.

3.  Select the change request in which you want to re-initiate the rack allocation.

4.  From the State list, select **New**.

    \[Omitted image "select-new.png"\] Alt text: State list on the change request form set to New

5.  Select **Save**.

6.  Select **Find Allocation**.

    The Racks Allocation Workflow panel opens and displays the progress of the allocation. Status updates appear as the feature evaluates and scores available racks. Monitor the workflow panel until the allocation completes. When the state changes to Design In Progress, rack slots are reserved in the CMDB. When the state changes to Design Complete, the full allocation summary is available in the work notes.

7.  Review the allocation results in the following areas.

    -   Work notes: the Placements and Decisions section lists which racks were selected, which were excluded, and why.
    -   Review output panel: Shows the rack placement recommendation and a structured summary of the requirements as interpreted from your description.
    -   Affected CIs tab: Shows the allocated slot and rack. Base rack-unit slots are marked as Reserved. Device-specific allocations are linked to the device record.
8.  In the **Affected CIs** tab, select the rack to open the rack record.

    Reserved slots display the change request number. Select the number to view change request details without leaving the rack view. \[Omitted image "rack-allocation.png"\] Alt text: Reserved slots in the rack view showing the change request number


**Parent Topic:**[Data center infrastructure rack allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/data-center-infra-rack-allocation.md)

**Related topics**  


[Reserve a rack using data center infrastructure allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/reserve-a-rack-using-data-center-infra-allocation.md)

