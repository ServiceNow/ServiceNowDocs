---
title: Create a service credit in Vendor Management Workspace
description: Create a service credit record each time the vendor breaches the agreement. The breaches are typically associated with an outage, incident, or SLA breaches.
locale: en-US
release: yokohama
product: Vendor Management Workspace
classification: vendor-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Vendor Management Workspace, Vendor Management Workspace, IT Service Management]
---

# Create a service credit in Vendor Management Workspace

Create a service credit record each time the vendor breaches the agreement. The breaches are typically associated with an outage, incident, or SLA breaches.

## Before you begin

From Vendor Management Workspace, you can create service credits from an incident, outage, or service availability record based on the conditions listed in the table below.

<table id="table_whf_lqv_1pb"><thead><tr><th>

Record

</th><th>

Conditions for creating a service credit

</th></tr></thead><tbody><tr><td>

Incident

</td><td>

-   The incident state is **On Hold**.
-   The on hold reason is **Awaiting Vendor**.

</td></tr><tr><td>

Outage

</td><td>

The configuration item field in the outage record must be configured to a service offering.

</td></tr><tr><td>

Service availability

</td><td>

The service offering must be configured in the service availability record.

</td></tr></tbody>
</table>Role required: sn\_vlm.vendor\_manager

You must have the sn\_incident\_read role enabled to view service credit reports.

## Procedure

1.  Navigate to **All** &gt; **Vendor Management** &gt; **Workspace**.

2.  Click the Vendor Home icon.

3.  Create a service credit from a vendor, incident, outage, or a service offering.

<table id="choicetable_qb5_n35_1pb"><thead><tr><th align="left" id="d157649e147">

To create a service credit

</th><th align="left" id="d157649e150">

Do this

</th></tr></thead><tbody><tr><td id="d157649e156">

**From a vendor**

</td><td>

1.  Click the **Lists** tab.
2.  Click All Vendors.
3.  Select a vendor to create the service credit.
4.  Click the **Service Credit** tab.


</td></tr><tr><td id="d157649e186">

**From an incident, outage, or service availability**

</td><td>

1.  Click the **Lists** tab.
2.  Select the incident, outage, or service availability list to create the service credit.
3.  Select an record for which you want to create a service credit.
4.  Click the overflow icon and select **Create Service Credit**.


</td></tr></tbody>
</table>4.  Click **New**.

    Fill in the following fields as required:

    |Field|Description|
    |-----|-----------|
    |Number|System generated reference number for this credit record.|
    |Vendor|Name of the vendor.|
    |Service offering|Service offering related to this vendor.|
    |Service commitment|Specific service commitment that affects this vendor credit.|
    |Service availability|Business service availability commitment that affects this vendor credit.|
    |Related incident|Number of any incidents related to these vendor products.|
    |Related outage|Actual outage that created the vendor credit. The value in this field is from the **Short description** in the outage record.|
    |Vendor contract|Contract for this vendor, if any. Choose a contract for the specified vendor. These contracts can be in any state.|
    |Reference number|Any reference that pertains to this credit, for example, a confirmation number from the vendor or the name of a contact.|
    |Breach penalty time|Duration of the breach. This value is the elapsed time of the credit-generating event and is inherited from the **Service commitment** selected.|
    |Breach penalty amount|Total amount of credit due from this event, inherited from the **Service commitment** selected.|
    |Per|Unit for calculating the breach penalty amount, inherited from the **Service commitment** selected.|
    |Credit used|Check box indicating that credit from this vendor has been recovered.|
    |Notes|Notes pertaining to this credit record, for example, to keep track of recovered credit.|

5.  Click **Save**.


