---
title: Create a catalog item for an SCCM application
description: Using the applications discovered on the SCCM server, create a catalog item for an application you want to offer for distribution from the service catalog.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configuring SCCM, Client software distribution from SCCM, Client Software Distribution, Orchestration applications, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a catalog item for an SCCM application

Using the applications discovered on the SCCM server, create a catalog item for an application you want to offer for distribution from the service catalog.

## Before you begin

Role required: sn\_client\_sf\_dist.csd\_admin or admin

Before creating a catalog item, you must link the application to a software model and create at least one software configuration.

## Procedure

1.  Navigate to **All** &gt; **Client Software Distribution** &gt; **SCCM** &gt; **SCCM Applications**.

    A list of applications discovered on the SCCM server appears.

2.  Open a record for an SCCM application.

3.  Under **Related Links**, click **Create Catalog Item**.

    A new SCCM Application Catalog Item record appears with preconfigured information. .

    ![SCCM application catalog item](../image/SCCMCatalogItem.png "SCCM application catalog item")

4.  Add price information and complete the following fields added to the Client Software Distribution Catalog Item \[sn\_client\_sf\_dist\_cat\_item\] table by the Orchestration - Client Software Distribution plugin:

<table id="table_jd5_54r_wt"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Skip approval \(skip\_approval\)

</td><td>

Check box that allows skipping approval for this item by the requester's manager when a user orders it from the service catalog. Use this field in conjunction with the **Order on behalf of** field to ensure that software ordered by a logged in user on behalf of another user is subject to approval. By default, this check box is cleared, requiring manager approval for all new catalog items.**Note:** There are two levels of approval possible. By default, all category items require group approval for items in excess of $1000. If that approval is given or skipped, the system evaluates the **Skip approval** check box to determine if the software item requires approval by the requester's manager.

</td></tr><tr><td>

Check license compliance \(check\_license\_compliance\)

</td><td>

Check box that forces the system to determine if deploying this item is allowed under the current license.

</td></tr><tr><td>

Order on behalf of

</td><td>

Check box that allows the logged-in user to order this software from the service catalog for another user. This permits service desk personnel to order SCCM deployments for other users in the system. By default, this feature is enabled. To prevent unauthorized users from ordering software, ensure that approvals are required for this type of deployment by clearing the **Skip approval** check box.If an approval is required for software ordered on behalf of a user, the system automatically sends an approval request to the manager of the user receiving the software. The approval is skipped if the requestor is the named user's manager.

 Software items requested from the service catalog on behalf of a different user require the following information:

-   **User**: User selected for deployment. This field is automatically populated with the name of the logged in user. You can select another user from the list.
-   **Device to install this sofware on**: Device belonging to the selected user on which to deploy the software. Only devices belonging to that user appear in the choice list.
-   **Lease start**: Date and time to deploy the software. This is the start time for the lease. A lease can be open-ended or have a lease end time.


</td></tr><tr><td>

SCCM configuration

</td><td>

Name of the [SCCM configuration record](t_ConfigureSCCMCollections.md) for this application. This record defines the collection and uninstall collection for this application. This configuration is required for all deployments, revocations, and leases performed by the SCCM server.

</td></tr></tbody>
</table>5.  If the catalog item requires approval because of cost, be sure to configure an approval group in the**Approved By Group** related list.

    By default, the Service Catalog Request workflow runs when an item costing more than $1000 is ordered and looks for an appropriate approval group. If no approval group is configured for the item, this workflow skips approval altogether and ends. The system then runs the Order Client Software workflow, which evaluates the **Skip approval** check box to determine if approval by the requester's manager is required.

6.  Click **Update**.

    The view returns to the SCCM Applications list.

7.  To see all client software distribution \(CSD\) catalog items, navigate to **Client Software Distribution** &gt; **Maintain Items** &gt; **Software Items**.


**Parent Topic:**[Configuring SCCM](../concept/configuring-sccm.md)

