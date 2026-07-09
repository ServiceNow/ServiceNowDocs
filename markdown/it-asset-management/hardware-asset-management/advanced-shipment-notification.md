---
title: Use Advanced Shipment Notification
description: Use Advanced Shipment Notification \(ASN\) to automate and create asset records when your assets are in transit.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-asset-management/hardware-asset-management/advanced-shipment-notification.html
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 9
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

Role required:

-   Hardware Asset Management version 15.0.0 and later: ham\_admin, ham\_user, procurement\_admin, asset, or admin
-   Hardware Asset Management versions prior to 15.0.0: admin

## About this task

**Note:**

If the asset records that you want to create belong to model categories linked to a CI class with identification rules defined for fields like the Asset tag, Serial number, or MAC address, you must provide details for at least one of these fields in the ASN template. Otherwise, the asset record isn't created. For example, if identification rules are defined for the Serial number and MAC address, you should provide a value for either of these fields.

The identification rules for a CI class are defined in the CMDB Identification and Reconciliation engine \(IRE\). For more details, see [Identification rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/c_IdentificationRules.md) and [Create a CI identification rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/t_CreateCIIdentificationRule.md). These rules help to uniquely identify the asset through these required fields and maintain accurate asset records.

## Procedure

1.  Navigate to ASN import page.

<table id="choicetable_rcm_45c_m3c"><thead><tr><th align="left" id="d288693e116">

HAM version

</th><th align="left" id="d288693e121">

Steps

</th></tr></thead><tbody><tr><td id="d288693e127">

**Version 15.0.0 and later**

</td><td>

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Procurement**.
2.  Select the **Procurement** tab.


</td></tr><tr><td id="d288693e160">

**Versions prior to 15.0.0**

</td><td>

Navigate to **All** &gt; **Procurement** &gt; **Orders** &gt; **Import Shipment Notification**.

</td></tr></tbody>
</table>2.  Attach or upload the ASN template.

    -   HAM version 15.0.0 and later:
        1.  Select **New**.
        2.  On the Create New Shipment Notification Upload page, enter a unique name in the **Name** field.
        3.  Select **Attach file** to upload the updated ASN template \(.xlsx\) that you received from your vendor.

            **Note:** If you do not have a sample ASN template, select **Download template** and share it with the vendor for completion.

    -   HAM versions prior to 15.0.0: Select **Browse files** and select the updated template.

        **Note:** If you don’t have a sample ASN template, on the Import Template page, select the **Download Template File \(.xlsx\)** link to download the template and share it with your vendor for completion.

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
3.  Start the import.

    -   HAM version 15.0.0 and later: Select **Import**.

        The status of the shipment notification upload transitions as follows:

        -   Moves from **Draft** to **Pending** after the import is initiated.
        -   Progresses through the **Extracting Rows** and **Importing** stages as the system processes the data.
        -   Finalizes the process by updating the status to one of the following based on the outcome:
            -   **Completed**: The import finished successfully without issues.

                **Note:** Even if some rows fail validation, the overall import status is marked as Completed. Error details for failed records are displayed in the **Comment** field on the **Shipment Notifications Upload Stagings** tab.

            -   **Failed**: The system couldn’t complete the import process.
        -   The **Shipment Upload Result** section summarizes the import by showing the number of records inserted, ignored, and skipped.
    -   HAM versions prior to 15.0.0: Select **Upload**.

        The upload may take some time as the import process runs asynchronously. Wait for the import process to complete before proceeding.

        Check the status of importing the template in one of the following ways.

        -   Navigate to **Procurement** &gt; **Orders** &gt; **Import Status**.
        -   To open directly the import set record, select the link on the message bar that shows `View import progress here`.
        The Import Sets page shows a list of import set records.

4.  Review the import results.

    -   HAM version 15.0.0 and later: Select the **Shipment Notifications Upload Stagings** tab to view the state all rows included in the ASN template. A row can have any of the following states:

        -   **Inserted**- Indicates that the row passed all validations and was considered for asset creation.
        -   **Ignored**- Indicates that the row failed one or more validations and was excluded from asset creation. Rows containing software licenses are also automatically excluded, as software licenses are not supported through ASN import.
        The **Comment** field displays error details.

    -   HAM versions prior to 15.0.0:
        1.  Select the import set record to view the import status.
        2.  If the import was not successful, select the **Import Set Rows** tab and check the **Comment** field to understand the reason for the failure.

## Result

For rows validated successfully:

-   Asset records are created in the **In Transit** state.
-   Asset records are linked to their corresponding purchase order line items.
-   Purchase order statuses are updated to **Pending Delivery**.

## What to do next

For rows that were ignored or resulted in a failed import, perform the following steps:

1.  Review the **Comment** field to identify errors or details for each row.
2.  Resolve the identified issues in the ASN template.
3.  HAM version 15.0.0 and later: Create a new **Shipment Notification Upload** record to import the updated template.
4.  HAM versions prior to 15.0.0: Import the updated template again.

**Parent Topic:**[Using Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/hardware-asset-management/using-ham-classic.md)

**Related topics**  


[Work with hardware normalization]()

[Manage asset bundles from your inventory]()

[Manage your inventory through pallet assets]()

[Manage loaner assets]()

[Donate assets to charity organizations]()

[Manage RMA requests]()

[Create an inventory stock order request]()

[Create a disposal order]()

[Use a hardware asset request flow]()

[Audit hardware asset inventory]()

[Request a Hardware Asset Refresh]()

[Manage your expiring contracts for leased hardware assets]()

[Reclaim hardware assets]()

[View RFID information of assets]()

[Manage the lifecycle of hardware models with calculated lifecycle templates]()

[Receive asset warranty details from Lenovo]()

[Manage stockrooms]()

[Track shipments using the integration framework]()

[Track asset location using indoor maps]()

[Assess performance of Hardware Asset Management]()

[Manage refresh of assets using Zero Touch Refresh]()

[Configure the Total Cost of Ownership of assets]()

[Manage and monitor hardware asset performance]()

[Manage Hardware Asset Management subscriptions]()

[Manage repair of defective assets in your stockroom in the Hardware Asset Workspace]()

[Manage picking hardware assets within your stockroom for Hardware Asset Management workflows]()

[Manage asset put away using the Hardware Asset Workspace]()

[Manage hardware asset tasks using the Mobile Agent application]()

[Audit your hardware assets by using Asset Attestation]()

[Acknowledge receipt of assets on the Employee Center portal]()

[Update associated Decision tables for HAM flows]()

