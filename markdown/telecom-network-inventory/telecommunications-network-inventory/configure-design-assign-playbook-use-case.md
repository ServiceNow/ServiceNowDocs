---
title: Configure a Design and Assign function example
description: This example demonstrates how you can create and configure a playbook to design and assign a network service in the Telecommunications Network Inventory application.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Design and Assign function, Configure, Telecommunications Network Inventory]
---

# Configure a Design and Assign function example

This example demonstrates how you can create and configure a playbook to design and assign a network service in the Telecommunications Network Inventory application.

## Example overview

Consider you have an order requests from a customer to fulfill a network service that must create Optical Network Terminals \(ONT\) for a specified location. To design and assign this network service, you must capture the ONT details such as an ONT site and equipment template details. By creating and configuring a playbook for the Design and Assign function, you can automate these tasks by following step-by-step guidance for designing the network service.

As a playbook admin, you create and configure the playbook to design and assign your inventory for the network service. The playbook contains the following activities to create the ONT device.

1.  Setup Network Service - Collects service details of your design request.
2.  Capture ONT Details - Capture the ONT site and inventory template details to instantiate the equipment.
3.  Review and Submit - You review the activity details and creates the ONT devices for the specific location according to the template.

As a part of this playbook workflow, you automate the following.

-   Creates a change request for the ONT design.
-   Creates change tasks for the activities such as capturing ONT details.
-   Execute the change tasks to instantiate the equipment using an inventory template.

As a playbook agent, you can fulfill your customer orders and requests for the network service by using this Design and Assign function.

## Prerequisites

Prior to creating a playbook, as an inventory core admin, you create and configure the following.

1.  Create a Change model and add model states.

<table id="table_mqg_b1g_tdc"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Change model name

</td><td>

Set name as **Network Service Automated Flow**.

</td></tr><tr><td>

Model state

</td><td>

Add the following model states and set the model state transitions.-   **Design in progress**

Set model state transition to **Design complete**.

-   **Design complete**

Set model state transition to **Closed**.

-   **Closed**

Don't set any model state transition for this state.

**Note:** You must add Allow CI Modification attribute to the **Design in progress** and **Design complete** model states.

</td></tr></tbody>
</table>    To learn more about the detailed steps, see [Create a Change Model for Design and Assign function](../task/create-change-model-design-assign-playbook.md).

2.  Create a record producer to capture the ONT input details such as ONT site and inventory template. This record producer is used in the second activity in the playbook.

<table id="table_qtd_lfg_tdc"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Record producer

</td><td>

-   Set the record producer name as **Capture ONT Details**.
-   Set the **Table** field as **Change Task**.


</td></tr></tbody>
</table>    To learn more about the detailed steps, see [Create a record producer for the Design and Assign function](../task/create-record-producer-design-assign-playbook.md).

3.  Add variables to the record producer.

<table id="table_yrl_rhg_tdc"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Variable 1

</td><td>

Set the following details for Variable 1.-   Set the **Type** field as **Reference**.
-   On the **Question** tab, set the **Question** field as **ONT site**.
-   On the **Specification** tab, set **Reference** field as **Network Site \[cmdb\_ci\_ni\_site\]**.


</td></tr><tr><td>

Variable 2

</td><td>

Set the following details for Variable 1.-   Set the **Type** field as **Reference**.
-   On the **Question** tab, set the **ONT Template** field as **ONT site**.
-   On the **Specification** tab, set **Reference** field as **Inventory Template \[sn\_ni\_core\_inventory\_template\]**.


</td></tr></tbody>
</table>    To learn more about the detailed steps, see [Create variables for Design and Assign function](../task/create-variables-record-producer-design-assign-playbook.md).

4.  Select **DA common variables** as a variable set to the record producer.

    To learn more about the detailed steps, see [Add variable set to the record producer for Design and Assign function](../task/add-variable-set-record-producer-design-assign-playbook.md).

5.  Create a subflow for the request definition that you use to configure the second activity in the playbook.

<table id="table_kbc_rkg_tdc"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Subflow name

</td><td>

Set the subflow name as **Capture ONT Details**.

</td></tr><tr><td>

Input fields

</td><td>

Add the following input fields for the subflow.-   Set Label as **Ignore Validation Error** and the Type as **true/false** for input 1.
-   Set Label as **Change task** and the Type as **Reference.Change Task** for input 2.


</td></tr><tr><td>

Actions

</td><td>

Add the following actions to the subflow.-   Add the **Get Catalog Variable** action to read the details from the record producer.
-   Add the **TNI Create CI from Template** action to create the equipment from the inventory template.
-   Add the **Update Record** action to update the equipment to the affected Configuration Items \(CI\)


</td></tr></tbody>
</table>    To learn more about the detailed steps, see [Create subflow for Design and Assign function](../task/create-subflow-design-assign-playbook.md).

6.  Create a request definition that you use to configure the second activity in the playbook.

<table id="table_mty_qmg_tdc"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Request definition name

</td><td>

Set the following details for the request definition.-   Set the request definition name as **Capture ONT Details**.
-   Set the **Task type** field as **Change Task**.


</td></tr></tbody>
</table>    To learn more about the detailed steps, see [Create subflow for Design and Assign function](../task/create-subflow-design-assign-playbook.md).


## Creating and configuring a playbook

As a playbook admin, you create and configure the playbook for the Design and Assign function in the Workflow Studio. For the detailed information about the following steps, see [Create a playbook for the Design and Assign function](../task/create-playbook-design-assign-function.md).

1.  Create a playbook and set the name as **Design Network Service**.
2.  Add and configure your trigger.

<table id="table_ymd_bpg_tdc"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Additional properties window

</td><td>

On the **Schedule** tab, set the following details for the trigger.-   Set the **Define your own conditions for when your process runs** as **Create Record**.
-   Set trigger condition as **Network Service Automated Flow** Change model.
You configure additional property to trigger the playbook when a change request is created using the **Network Service Automated Flow** Change model.

</td></tr></tbody>
</table>3.  Create a stage and add activities such as Setup Network Service, Capture ONT Details, and Review and Submit.
    1.  Create and configure the Setup Network Service activity.

<table id="table_pv4_drg_tdc"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add activity

</td><td>

Select the **Display Form** default activity.

</td></tr><tr><td>

Details tab

</td><td>

Rename the activity as **Setup Network Service**.

</td></tr><tr><td>

UI Layout tab

</td><td>

Set the following details in the **UI Layout** tab.-   Set the **Associated table** field as **Chang Request**.
-   Set the **Associated record** field as **Flow DataTrigger - change\_request** &gt; **change\_request Record**
-   Set the **Experience Status Table** field as **Flow Data**.
-   Set the **Experience Status Record** field as **Automation plan** &gt; **Create Flow Data** &gt; **Outputs** &gt; **Flow Data Record**.
-   Set the **Form View** field as **Playbook**.


</td></tr></tbody>
</table>    2.  Create and configure the Capture ONT Details activity.

<table id="table_pq1_swg_tdc"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add activity

</td><td>

Select the **Auto Create Change Task** default activity.

</td></tr><tr><td>

Details tab

</td><td>

Rename the activity as **Capture ONT Details**.

</td></tr><tr><td>

Automation tab

</td><td>

Set the following details in the **Automation** tab.-   Set the **Request Type** field as **Capture ONT Details**. The **Capture ONT Details** is the request definition that you created.
-   Set the **Record Producer** field as **Capture ONT Details**.
-   Set the **Change Request** field as **Flow DataTrigger - change\_request** &gt; **change\_request Record**


</td></tr><tr><td>

UI Layout tab

</td><td>

Set the following details in the **UI Layout** tab.-   Set the **Associated table** field as **Chang Task**.
-   Set the **Associated record** field as **Automation plan** &gt; **Create Change Task Data** &gt; **Outputs** &gt; **Change Tasks**.
-   Set the **Experience Status Table** field as **Flow Data**.
-   Set the **Experience Status Record** field as **Automation plan** &gt; **Create Flow Data** &gt; **Outputs** &gt; **Flow Data Record**.
-   Set the **Form View** field as **Playbook**.


</td></tr></tbody>
</table>    3.  Create and configure the Review and Submit activity.

<table id="table_oh2_y5g_tdc"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add activity

</td><td>

Select the **Display Form** default activity.

</td></tr><tr><td>

Details tab

</td><td>

Rename the activity as **Review and Submit**.

</td></tr><tr><td>

UI Layout tab

</td><td>

Set the following details in the **UI Layout** tab.-   Set the **Associated table** field as **Chang Task**.
-   Set the **Associated record** field as **Automation plan** &gt; **Create Change Task Data** &gt; **Outputs** &gt; **Change Tasks**.
-   Set the **Experience Status Table** field as **Flow Data**.
-   Set the **Experience Status Record** field as **Automation plan** &gt; **Create Flow Data** &gt; **Outputs** &gt; **Flow Data Record**.
-   Set the **Form View** field as **Playbook**.


</td></tr></tbody>
</table>    4.  Select **Save and close**.
4.  Select **Activate**.

The following example shows the playbook that you created and configured in the Workflow Studio.

![Playbook in Workflow Studio with the list of activities.](../image/playbook-configure-example.png "Example of the playbook in Workflow Studio")

## Adding playbook to home page

You add the sys\_id of the Network Service Automated Flow Change model in the `sn_ni_ws.tni_design_assign_chg_models` record. To learn more about the detailed steps, see [Update system property to configure the Design and Assign home page](../task/update-system-property-configure-design-assign-home-page.md).

## Using a Design and Assign function

As an agent, you use the playbook for the Design and Assign function to fulfill the requirement of the network service by following the steps.

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.
2.  Select the design and assign icon \(![Design and Assign Icon](../image/icon-design-assign.png)\) to open the Design and Assign home page.
3.  On the Design Assign home page, select **New** &gt; **Network Service Automated Flow**.
4.  Complete the activities on the playbook to design and assign your network service.

This process creates an ONT device based on the template and site that you selected in the playbook activity.

The following example is the Design and Assign function that you created.

![Playbook view with the list of activities](../image/design-assign-playbook-example.png "Example of playbook")

**Parent Topic:**[Design and Assign function for your network services](configure-playbooks-design-assign-function.md)

**Related topics**  


[Design and Assign function for your network services](configure-playbooks-design-assign-function.md)

