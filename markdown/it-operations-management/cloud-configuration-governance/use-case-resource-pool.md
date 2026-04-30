---
title: Example resource pool that limits choices to cost center
description: You can use resource pools with blueprints to limit the choices on the cloud catalog request form.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Pools and Filters for Cloud Provisioning, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Example resource pool that limits choices to cost center

You can use resource pools with blueprints to limit the choices on the cloud catalog request form.

## Use case: Restrict cost center selection

In this example, the cost of the cloud asset is charged against the budget of the cost center of the user. The base-system **UserCostCenter** resource pool ensures that a user can select only resources in their cost center.

## Assumptions

-   The Cost Management \[con.snc.cost\_management\] plugin is active.
-   Cost centers are defined and users are associated with the cost centers.
-   At least one blueprint is defined. This example uses a blueprint named **AWS Virtual Server**.
-   You are assigned the sn\_cmp\_cloud\_admin role and know JavaScript and JSON scripting.

## Components

-   **Review resource pool filter**
    1.  On the Cloud Admin portal navigate to **Manage** &gt; **Resource Pools**.
    2.  Open the **CostCenterPool** and review the related Resource Pool Filters.

        -   **All** is a query filter that returns all cost centers in the table.
        -   **UserCostCenter** is a script filter that looks up the cost center associated with the user who is ordering the item.
        Here is the script for the **UserCostCenter** filter:

        ```
        getFilteredRecords();
        //Do not remove function declaration
        /**
        * @returns filtered records in the format [{"value"="lookupValue",label="displayValue"}]
        */
        function getFilteredRecords() {
        	var filteredRecords = [];
        	var userId = gs.getUserID();
        	var userGr = new GlideRecord('sys_user');
        	if (userGr.get(userId)){
        		var costCenterId = userGr.getValue('cost_center');
        		if (costCenterId){
        			var costCenterGr = new GlideRecord('cmn_cost_center');
        			if (costCenterGr.get(costCenterId)){
        				var costCenter = {};
        				costCenter.value = costCenterGr.getUniqueValue();
        				costCenter.label = costCenterGr.getValue('name');
        				filteredRecords.push(costCenter);
        			}
        		}		
        	}
        
        	//force to string
        	return new global.JSON().encode(filteredRecords);
        }
        ```

-   **Blueprint catalog form parameters**
    1.  Navigate to **Design** &gt; **Blueprints**, and then click the tile for the blueprint you want to open.
    2.  With the blueprint in **Draft** state, click the **Provision** operation tile on the **Catalog** &gt; **Request Operation** tab.

        ![Provision operation](../image/provision-operation-blueprint.png)

    3.  In the Variable sets related list, click the **General Info** variable set. By default, the CostCenter variable is in this variable set.
    4.  In the Cloud Variables related list on the Variable Set form, click the **CostCenter** variable.

        ![CostCenter variable](../image/costcenter-variabe.png)

    5.  On the Cloud Variable form, click the **Type Specifications** tab.
    6.  Look at the **Pool** and **Pool Filter** fields that refer to the resource pool and filter.

        -   **CostCenterPool** is the name of the resource pool.
        -   **UserCostCenter** is the filter script that pulls in the cost center options for the user to select from.
        ![Resource pool and filter used in the datasource value of the cost center catalog property](../image/bp-prop-datasource-pool.png)

    7.  Set the blueprint to **Published**.
-   **Cost center user**

    Identify a user who is a member of a cost center and who has access to the Cloud User Portal.

    ![User who is a member of the sales cost center.](../image/cost-center-user.png)


## Testing the resource pool filter

After reviewing the components that comprise this use case, test the cloud catalog item to verify that users can select only their cost center.

1.  Impersonate the user, **Alene Rabeck** in this example.
2.  On the Cloud User Portal, click **Launch a Stack**, and then select the cloud catalog item \(**AWS Virtual Server** in this example\).
3.  Review the selections in the **Cost Center** list.

    ![Sales is the only selection for this user's cost center.](../image/catalog-item-cost-center-choice.png)


With the **CostCenterPool::UserCostCenter** datasource value for this catalog item, the only option for the **Cost Center** is the cost center the user is a member of.

## Changing the resource pool filter

Test that the resource pool filter is controlling the behavior of the **Cost Center** field by changing it and viewing the results.

1.  On the Cloud Admin Portal, navigate to **Design** &gt; **Blueprints** and then click **AWS Virtual Server**.
2.  Click the **Provision** operation tile.
3.  In the Variable sets related list, click the **General Info** variable set. By default, the CostCenter variable is in this variable set.
4.  In the Cloud Variables related list on the Variable Set form, click the **CostCenter** variable.
5.  On the Cloud Variable form, click the **Type Specifications** tab.
6.  Edit the **Pool filter** field to change the filter from **UserCostCenter** to **All**.

    ![Resource pool and filter used in the datasource value of the cost center catalog property](../image/bp-prop-datasource-pool-all.png)

7.  Click **Update**, then click**Publish.**.
8.  Impersonate the user, **Alene Rabeck** in this example.
9.  On the Cloud User Portal, launch a stack, and then select **AWS Virtual Server**.
10. Verify that all cost centers are listed.

    ![All cost centers are now displayed for selection.](../image/catalog-item-cost-centers.png)


