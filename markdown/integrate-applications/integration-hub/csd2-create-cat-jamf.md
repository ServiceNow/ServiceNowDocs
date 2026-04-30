---
title: Create a catalog item for the Jamf application
description: Create a catalog item for an application you want to offer for distribution from the service catalog using the applications discovered on the Jamf server.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [CSD 2.0 for Jamf, Client Software Distribution 2.0 application, Integration Hub solutions, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Create a catalog item for the Jamf application

Create a catalog item for an application you want to offer for distribution from the service catalog using the applications discovered on the Jamf server.

## Before you begin

Role required: Ensure that the user has one of the two mentioned set of roles.

-   sn\_jamf\_spoke.jamf\_admin, catalog\_admin, and sn\_csd.CSD Admin
-   admin

Before creating a catalog item, you must link the application to a software model and create at least one software configuration.

Perform these steps for the Jamf applications and policies.

## Procedure

1.  Create a catalog item for the application or the policy.

    -   If you are creating a catalog item for the Jamf application, navigate to **Jamf** &gt; **Applications**.
    -   If you are creating a catalog item for the Jamf policy, navigate to **Jamf** &gt; **Policies**.
    A list of applications or policies discovered on the Jamf server appears.

2.  Open the required record.

3.  Click the **Create Catalog Item** related link.

4.  On the form, fill the required values.

<table id="table_ld5_9kr_wt"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the record.

</td></tr><tr><td>

Access Type

</td><td>

If **Delegated** is selected, enables the logged-in user to order this software from the service catalog for another user. This permits service desk personnel to order Jamf deployments for other users in the system. By default, this feature is disabled. To prevent unauthorized users from ordering software, ensure that approvals are required for this type of deployment by clearing the **Skip approval** check box.If an approval is required for software ordered on behalf of a user, the system automatically sends an approval request to the manager of the user receiving the software. The approval is skipped if the requestor is the named user's manager.

 Software items requested from the service catalog on behalf of a different user require the following information:

-   **User**: User selected for deployment. This field is automatically populated with the name of the logged in user. You can select another user from the list.
-   **Device to install this software on**: Device belonging to the selected user on which to deploy the software. Only devices belonging to that user appear in the choice list.
-   **Lease start**: Date and time to deploy the software. This is the start time for the lease. A lease can be open-ended or have a lease end time.
If **Restricted** is selected, the **User** field is not displayed on the order form.

</td></tr></tbody>
</table>5.  Right-click the form header and click **Save**.

6.  In the **CSD Catalog Item Fulfillment Configuration** tab, open the default record and provide these values.

<table id="table_d5l_213_fsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Software configuration

</td><td>

Name of the configuration record for this application. This record defines the collection and uninstall collection for this application. This configuration is required for all deployments, revocations, and leases performed by the Jamf server.

</td></tr><tr><td>

Skip approval \(skip\_approval\)

</td><td>

Check box that allows skipping approval for this item by the requester's manager when a user orders it from the service catalog. Use this field in conjunction with the **Access Type** field to ensure that software ordered by a logged in user on behalf of another user is subject to approval. By default, this check box is cleared, requiring manager approval for all new catalog items.**Note:** There are two levels of approval possible. By default, all category items require group approval for items in excess of $1000. If that approval is given or skipped, the system evaluates the **Skip approval** check box to determine if the software item requires approval by the requester's manager.

</td></tr><tr><td>

Check license compliance \(check\_license\_compliance\)

</td><td>

Check box that forces the system to determine if deploying this item is allowed under the current license.

</td></tr></tbody>
</table>    **Note:** If the catalog item requires approval because of cost, be sure to configure an approval group in the**Approved By Group** related list. By default, the Service Catalog Request flow runs when an item costing more than $1000 is ordered and looks for an appropriate approval group. If no approval group is configured for the item, this flow skips approval altogether and ends. The system then runs the Order Client Software flow, which evaluates the **Skip approval** check box to determine if approval by the requester's manager is required.

7.  Click **Update**.

    Catalog item is created and is available for ordering from Service Catalog.

8.  To see all CSD 2.0 catalog items, navigate to **Client Software Distribution 2.0** &gt; **Software Items**.

    **Note:** If you are unable to see any of the above fields or tabs, configure the table's form view or related lists accordingly.


**Parent Topic:**[CSD 2.0 for Jamf](../concept/csd2-jamf-tsk.md)

