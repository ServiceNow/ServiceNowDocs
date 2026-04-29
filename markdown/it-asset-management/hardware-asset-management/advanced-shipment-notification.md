---
title: Use Advanced Shipment Notification
description: Use Advanced Shipment Notification \(ASN\) to automate and create asset records when your assets are in transit.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Use Advanced Shipment Notification

Use Advanced Shipment Notification \(ASN\) to automate and create asset records when your assets are in transit.

## Before you begin

-   Download the ASN template and share it with the vendor for completion.
-   Before importing asset records using the ASN template, validate the following data requirements:

    -   The model ID provided in the template is defined in your ServiceNow instance.
    -   The shipping address in the template matches the shipping address in the Location \[cmn\_location\] table.
    -   The shipping carrier in the template is available in the Shipping carrier \[sn\_itam\_shipping\_carrier\] table.

    For more details on all ASN data validations, see [Advanced Shipment Notification \(ASN\)](../concept/asn-for-ham.md).


Role required: ham\_admin, ham\_user, procurement\_admin, asset, sn\_hamp.ham\_asn\_admin, or admin

## About this task

**Note:**

If the asset records that you want to create belong to model categories linked to a CI class with identification rules defined for fields like the Asset tag, Serial number, or MAC address, you must provide details for at least one of these fields in the ASN template. Otherwise, the asset record isn't created. For example, if identification rules are defined for the Serial number and MAC address, you should provide a value for either of these fields.

The identification rules for a CI class are defined in the CMDB Identification and Reconciliation engine \(IRE\). For more details, see [Identification rules](https://www.servicenow.com/docs/access?context=c_IdentificationRules&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) and [Create a CI identification rule](https://www.servicenow.com/docs/access?context=t_CreateCIIdentificationRule&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US). These rules help to uniquely identify the asset through these required fields and maintain accurate asset records.

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Procurement**.

2.  Select the **Advance shipment** tab.

3.  Select **New**.

    The Create New Shipment Notification Upload page appears.

4.  In the **Name** field, enter a unique name for the ASN upload.

5.  Select **Attach file** to upload the updated ASN template \(.xlsx\) that you received from your vendor.

    **Note:** If you don't have a sample ASN template, select **Download template** and share it with the vendor for completion.

    The ASN template includes fields such as:

    -   Serial number: Unique identifier for the asset
    -   Asset tag: Alphanumeric tag assigned by your organization for asset tracking
    -   Vendor: Vendor from whom the asset was purchased
    -   PO number: Number associated with the purchase order

        **Note:** This field isn't the vendor PO number.

    -   Model id: Model number of the product
    -   SVC contract end date: Warranty expiration date for the asset
    -   Carrier: Shipping carrier name
    -   Tracking number: Number to track the assets that are in transit
    **Note:** The **OT entity** and **MAC address** columns in the ASN template are used to create Operational Technology \(OT\) assets when the OT Asset Management application is activated.

6.  Select **Import**.

    -   The system performs validations and the status of the shipment notification upload transitions as follows:
        1.  Moves from **Draft** to **Pending** after the import is initiated.
        2.  Progresses through the **Extracting Rows** and **Importing** stages as the system processes the data.
        3.  Finalizes the process by updating the status to one of the following based on the outcome:
            -   **Completed**: The import finished successfully without issues.

                **Note:** Even if some rows fail validation, the overall import status is marked as **Completed**. Error details for failed records are displayed in the **Comment** field on the **Shipment Notifications Upload Stagings** tab.

            -   **Failed**: The system couldn’t complete the import process.
    -   The **Shipment Upload Result** section summarizes the import by showing the number of records inserted, ignored, and skipped.
7.  Select the **Shipment Notifications Upload Stagings** tab to view the state all rows included in the ASN template.

    A row can have any of the following states:

    -   **Inserted**- Indicates that the row passed all validations and was considered for asset creation.
    -   **Ignored**- Indicates that the row failed one or more validations and was excluded from asset creation. Rows containing software licenses are also automatically excluded, as software licenses are not supported through ASN import.
    The **Comment** field displays error details.


## Result

For rows validated successfully:

-   Asset records are created in the **In Transit** state.
-   Asset records are linked to their corresponding purchase order line items.
-   Purchase order statuses are updated to **Pending Delivery**.

## What to do next

For rows that were ignored:

1.  Review the **Comment** field to identify specific errors or details for each ignored row.
2.  Resolve the identified issues within the ASN template.
3.  Create a Shipment Notification Upload record to import the updated template.

**Parent Topic:**[Using Hardware Asset Management](../concept/using-ham-classic.md)

**Related topics**  


[Work with hardware normalization](../concept/Work-with-hardware-normalization.md)

[Manage asset bundles from your inventory](create-bundled-assets.md)

[Manage your inventory through pallet assets](../concept/pallets-for-inventory-management.md)

[Manage loaner assets](manage-loaner-asset.md)

[Donate assets to charity organizations](../concept/donate-asset-to-charity-organizations.md)

[Manage RMA requests](../concept/manage-rma-req.md)

[Create an inventory stock order request](create-inventory-stock-order.md)

[Create a disposal order](create-disposal-order.md)

[Use a hardware asset request flow](hardware-request-flow.md)

[Audit hardware asset inventory](../concept/ham-inventory-audit.md)

[Request a Hardware Asset Refresh](hardware-asset-refresh.md#)

[Manage your expiring contracts for leased hardware assets](manage-your-leased-hw-asts-expiring-contract.md)

[Reclaim hardware assets](../concept/manage-asset-reclaim.md)

[View RFID information of assets](view-rfid-info.md)

[Manage the lifecycle of hardware models with calculated lifecycle templates](../concept/manage-ham-lifecycle-temp.md)

[Receive asset warranty details from Lenovo](../concept/receive-warranty-details-lenovo.md)

[Manage stockrooms](../concept/manage-your-stockrooms.md)

[Track shipments using the integration framework](../concept/tracking-shipments-using-integration-framework.md)

[Track asset location using indoor maps](track-asset-location-using-indoor-maps.md)

[Assess performance of Hardware Asset Management](../concept/suc-goal-act-hw.md)

[Manage refresh of assets using Zero Touch Refresh](../concept/refresh-hardware-uisng-ztr.md)

[Configure the Total Cost of Ownership of assets](../concept/configure-ham-tco.md)

[Manage Hardware Asset Management subscriptions](../concept/managing-ham-subscriptions.md)

[Manage repair of defective assets in your stockroom in the Hardware Asset Workspace](../concept/manage-repair-of-defective-ham-assets.md)

[Manage picking hardware assets within your stockroom for Hardware Asset Management workflows](../concept/manage-asset-picking-stockroom-ham-ws.md)

[Manage hardware asset tasks using the Mobile Agent application](../concept/manage-hardware-asset-tasks-mobile-agent.md)

[Manage asset put away using the Hardware Asset Workspace](../concept/manage-asset-putaway-stockroom-hardware-asset-workspace.md)

[Audit your hardware assets by using Asset Attestation](../concept/audit-hardware-assets-attestation.md)

[Acknowledge receipt of assets on the Employee Center portal](receive-assets-employee-center.md)

[Update associated Decision tables for HAM flows](trigger-flow-ham.md)

