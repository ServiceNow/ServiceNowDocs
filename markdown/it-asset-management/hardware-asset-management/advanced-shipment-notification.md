---
title: Use Advanced Shipment Notification
description: Use Advanced Shipment Notification \(ASN\) to automate and create asset records when your assets are in transit.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/advanced-shipment-notification.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Use, Hardware Asset Management, IT Asset Management]
---

# Use Advanced Shipment Notification

Use Advanced Shipment Notification \(ASN\) to automate and create asset records when your assets are in transit.

## Before you begin

-   Download the ASN template and share it with the vendor for completion.
-   Before importing asset records using the ASN template, validate the following data requirements:

    -   The model ID provided in the template is defined in your ServiceNow instance.
    -   The shipping address in the template matches the shipping address in the Location \[cmn\_location\] table.
    -   The shipping carrier in the template is available in the Shipping carrier \[sn\_itam\_common\_shipping\_carrier\] table.
    For more details on all ASN data validations, see [Advanced Shipment Notification \(ASN\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/asn-for-ham.md).


Role required: ham\_admin, ham\_user, procurement\_admin, asset, sn\_hamp.ham\_asn\_admin, or admin

## About this task

**Note:**

If the asset records that you want to create belong to model categories linked to a CI class with identification rules defined for fields like the Asset tag, Serial number, or MAC address, you must provide details for at least one of these fields in the ASN template. Otherwise, the asset record isn't created. For example, if identification rules are defined for the Serial number and MAC address, you should provide a value for either of these fields.

The identification rules for a CI class are defined in the CMDB Identification and Reconciliation engine \(IRE\). For more details, see [Identification rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_IdentificationRules.md) and [Create a CI identification rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_CreateCIIdentificationRule.md). These rules help to uniquely identify the asset through these required fields and maintain accurate asset records.

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

**Parent Topic:**[Using Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/using-ham-classic.md)

**Related topics**  


[Analyze hardware assets using the Generate hardware asset insights generative AI skill]()

[Work with hardware normalization]()

[Manage asset bundles from your inventory]()

[Manage your inventory through pallet assets]()

[Manage loaner assets]()

[Donate assets to charity organizations]()

[Manage RMA requests]()

[Create an inventory stock order request]()

[Create a disposal order]()

[Fulfilling hardware asset requests]()

[Audit hardware asset inventory]()

[Request a Hardware Asset Refresh]()

[Manage your expiring contracts for leased hardware assets]()

[Reclaim hardware assets]()

[View RFID information of assets]()

[Manage the lifecycle of hardware models with calculated lifecycle templates]()

[Create an internal lifecycle in the Hardware Asset Workspace]()

[Receive asset warranty details from Lenovo]()

[Manage stockrooms]()

[Track shipments using the integration framework]()

[Track asset location using indoor maps]()

[Assess performance of Hardware Asset Management]()

[Manage refresh of assets using Zero Touch Refresh]()

[Configure the Total Cost of Ownership of assets]()

[Manage Hardware Asset Management subscriptions]()

[Manage repair of defective assets in your stockroom in the Hardware Asset Workspace]()

[Manage picking hardware assets within your stockroom for Hardware Asset Management workflows]()

[Manage hardware asset tasks using the Mobile Agent application]()

[Manage asset put away using the Hardware Asset Workspace]()

[Audit your hardware assets by using Asset Attestation]()

[Acknowledge receipt of assets on the Employee Center portal]()

[Update associated Decision tables for HAM flows]()

