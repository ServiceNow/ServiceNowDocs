---
title: Create a change request from Network Inventory Workspace
description: Create, review, update, or close a change request for a change model from the network inventory workspace of the Telecommunications Network Inventory application. You can also analyze the instantiation details of the network instance. Created topic as per DOC1068893 - STRY55011331
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Design &amp; Assign Network, Use, Telecommunications Network Inventory]
---

# Create a change request from Network Inventory Workspace

Create, review, update, or close a change request for a change model from the network inventory workspace of the Telecommunications Network Inventory application. You can also analyze the instantiation details of the network instance.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent, sn\_ni\_core.inventory\_template\_manager, sn\_ni\_core.telco\_inventory\_catalog\_manager

## About this task

You can create, review, update, or close a change request task in the Telecommunications Network Inventory application.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Changes** &gt; **All**.

3.  View the list of your assigned change tasks by selecting **Assigned to me**.

    **Note:** The list view of **Changes** displays the list of all change requests, regardless of the domain. Add a filter to see only the telecommunications network inventory \(TNI\)-related change requests.

4.  Select **New**.

5.  In the search field, use the filter to select any one of the following change models that you want to create a change request for:

    -   Add card
    -   Create Inventory Equipment
    -   Create Logical Connection
    -   Create Physical Connection
    -   Create Rack/Cabinet
    -   Add equipment to Rack/Cabinet
    -   Remove Equipment/Shelf from Rack/Cabinet
    -   IP Address Allocation
    -   Phone Number Allocation
    **Note:** For design assign link aggregation group and GPON broadband service, see [Create a Link Aggregation Group using design and assign function](create_a_change_request_by_using_the_design_assign_link_aggregation_group.md) and [Design your GPON Broadband Service](gpon-broadband-change-model.md).

6.  Select **Next**.

    A record producer or a change request form is displayed depending on the decision table entry. To learn more, see [Assign a record producer form to a change model](create_record_producer_form_for_a_change_request.md).

7.  Select **Save**.

    A change request is created and related tabs appear. To learn more, see [Change request related tabs](../reference/tni-change-request-related-tabs.md).

8.  On the **Overview** tab, do one or more of the following actions:

    -   View or update a summary of this change request.
    -   Add scopes.

        To learn more, see [Scopes](https://servicenow.com/docs/bundle/utah-governance-risk-compliance/page/product/grc-business-continuity-management/task/add-plan-asset-scope-bcp.html).

    -   Assign this change request to a group or a person.

        **Note:** To assign this change request, select **Assign** &gt; **fill in the assignment group and assigned to** &gt; **Save**.

    -   Set a schedule for this change request. To learn more, see [Schedules](https://servicenow.com/docs/bundle/utah-platform-administration/page/administer/time/concept/c_UseSchedules.html).
    -   Calculate the risks for this change request.

        When you select **Calculate Risk**, it analyzes an update in the **Risk** field on the **Details** tab.

    -   View and create the change tasks by selecting **New**.

        To learn more, see [Create and execute a change task in Telecommunications Network Inventory](create-change-task-in-tni.md).

9.  On the **Details** tab, fill in the fields.

    For a description of the field values, see [Change request and change task forms](../concept/change_request_forms.md).

10. Select **Save**.

    A change task is created and based on the details provided. The other related tabs are also updated, such as the Affected CIs, and the Impacted services/CIs.

11. Select a tab to see the impact that it has on the change request.


## What to do next

Create, review, update, or close the change tasks.

For more information, see [Create and execute a change task in Telecommunications Network Inventory](create-change-task-in-tni.md).

**Parent Topic:**[Instantiating your network inventory by using design and assign](../concept/instantiate-asset-using-template-relationship-model.md)

