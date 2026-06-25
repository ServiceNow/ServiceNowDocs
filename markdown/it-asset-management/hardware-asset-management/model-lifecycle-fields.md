---
title: Model lifecycle form
description: Fields on the hardware or consumable model lifecycle form and their descriptions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/model-lifecycle-fields.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: reference
last_updated: "2026-05-27"
reading_time_minutes: 2
keywords: [hardware model lifecycle form,consumable model lifecycle form]
breadcrumb: [Reference, Hardware Asset Management, IT Asset Management]
---

# Model lifecycle form

Fields on the hardware or consumable model lifecycle form and their descriptions.

<table id="table_ckb_jm4_gjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Model

</td><td>

Automatically set to the name of the model.

</td></tr><tr><td>

Lifecycle type

</td><td>

Model lifecycle type: -   **Internal**: The lifecycle date is specific to the customer, for example, based on an internal policy or a custom contract with the publisher. This field is automatically set to **Internal**.
-   **Publisher**: The lifecycle date comes from the manufacturer and is not specific to a customer.

</td></tr><tr><td>

Lifecycle phase

</td><td>

Phase of the life cycle for a hardware model.-   **General Availability**: The date when the hardware becomes generally available through the manufacturer's sales channels, including its worldwide subsidiaries, affiliates, and country distributors. The hardware is considered current or active and receiving support from the manufacturer.
-   **End of Sale**: The last date to order the hardware through the manufacturer's sales channels, including its worldwide subsidiaries, affiliates, and country distributors. After the end of sale date, the hardware is no longer available for sale.
-   **End of Support**: The last date upon which the manufacturer provides standard or regular support for the hardware as entitled by active service contracts. After this date, the manufacturer may continue to provide active support for certain issues in a limited capacity, the scope of which may vary across different manufacturers according to their lifecycle or support policies.
-   **End of Extended Support**: Up until this date, the manufacturer extends limited support for the hardware \(after standard/regular support expires\), for a defined period according to manufacturer policy.
-   **End of Life**: The date which indicates the hardware is at the end of its useful life \(from the manufacturer's point of view\). The manufacturer stops marketing, selling, or sustaining the hardware.

</td></tr><tr><td>

Source

</td><td>

Source of the hardware model. Automatically set to **Internal** to identify the entry as a custom entry.

</td></tr><tr><td>

Risk

</td><td>

Risk associated with the lifecycle.

</td></tr><tr><td>

Phase start date

</td><td>

Start date of the lifecycle phase.

</td></tr><tr><td>

Phase end date

</td><td>

End date of the lifecycle phase. **Note:** This field is not used by any models in the Hardware Asset Management application.

</td></tr><tr><td>

Lifecycle code

</td><td>

Not available when manually adding a custom lifecycle record. **Note:** The lifecycle code is only available for lifecycle records that come directly from the ServiceNow Content Library and can't be set for the user-created lifecycle records.

</td></tr><tr><td>

Active

</td><td>

When selected, the lifecycle record is active.

</td></tr><tr><td>

Description

</td><td>

Description of the hardware or consumable model.

</td></tr></tbody>
</table>**Parent Topic:**[Hardware Asset Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/reference-hardware-asset-management.md)

**Related topics**  


[Create an internal lifecycle in the Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/create-internal-lifecycle-hardware-models.md)

