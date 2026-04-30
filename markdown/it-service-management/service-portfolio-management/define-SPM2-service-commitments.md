---
title: Add a commitment to a service offering in Service Portfolio Management
description: Service commitments are specific services that define the unique availability guarantees, scope, and pricing for a service offering.
locale: en-US
release: yokohama
product: Service Portfolio Management
classification: service-portfolio-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Service offerings in Service Portfolio Management, Using Service Portfolio Management, Service Portfolio Management, IT Service Management]
---

# Add a commitment to a service offering in Service Portfolio Management

Service commitments are specific services that define the unique availability guarantees, scope, and pricing for a service offering.

## Before you begin

Role required: service\_editor

## About this task

Service commitments define the expected level of a service. A service offering derives from a service, tailoring the parent service to a specific business need. A service offering consists of a set of service commitments which uniquely define the service offerings.

To create service commitments, each service needs at least one associated service offering.

## Procedure

1.  Navigate to **All** &gt; **Service Portfolio Management** &gt; **Service Offerings**.

    Alternatively, you can navigate to **Service Portfolio Management** &gt; **Commitments**.

2.  Open a service offering record.

3.  In the Service Commitments related list, select **New**.

4.  Give the commitment a descriptive name.

    You can specify any kind of service.

5.  Select the **Type** of commitment from the list.

<table id="choicetable_zjg_yyd_d1b"><tbody><tr><td id="d269265e128">

**Availability or Maintenance Window**

</td><td>

Used in system processing. If you select **Maintenance Window**, the **Schedule** field is required. Creates Availability records for the service offering based on the outages for that offering. If an Availability commitment exists, when an Outage is created against a service offering with the Availability commitment, it will begin tracking down time and availability.

</td></tr><tr><td id="d269265e146">

**Response Time, Delivery or Other**

</td><td>

Display additional information in the service catalog. This information details the type of service commitment the user may expect from a given service offering. These service commitment types do not provide additional functionality or a homepage gauge.

</td></tr><tr><td id="d269265e155">

**Recovery time objective**

</td><td>

Guarantee of how long it takes to recover the system from the recovery point. Set the recovery time in the **Time Amount** field that appears when you select this commitment type. This field is available with vendor ticketing.**Note:** These service commitment types do not provide additional functionality or a homepage gauge.

</td></tr><tr><td id="d269265e170">

**Recovery point objective**

</td><td>

Guarantee of how often backups are performed. Set the backup interval in the **Time amount** field that appears when you select this commitment type. This field is available with vendor ticketing.**Note:** These service commitment types do not provide additional functionality or a homepage gauge.

</td></tr><tr><td id="d269265e185">

**SLA**

</td><td>

Allows commitments defined by a service level agreement \(SLA\) that tracks whether a vendor provides a level of service for a defined percentage of the time. The SLA results are calculated automatically and can be viewed on the My Services - SLAs homepage or by navigating to **Services** &gt; **Service Offering SLAs** &gt; **SLA Results**.

</td></tr></tbody>
</table>6.  Select a **Contract** for this service commitment.

    This information is used when creating vendor credit records.

    **Tip:** If you don't see task \(SLAs for incidents related to service commitments\), then contact your Administrator. When **Contract** is entered in the Reference field of the incident, then the Use reference qualifier field should be set to **Advanced**, and the global business rule **contractFilter** must be entered in the **Reference qual** field.

7.  Enter the information to calculate credit owed by the vendor for any contract breaches.

    These fields are available with vendor ticketing:

    -   **Breach penalty amount**: Amount assessed per unit of time for a breach.
    -   **Per**: Unit of time used to calculate the total credit owed for a breach.
    -   **Breach penalty time**: Amount of free time provided by the vendor per breach.
8.  Complete the form and select **Submit**.

    The Service Offering form opens, and the new commitment appears in the Service Commitment related list.

9.  Select **New** to add another service commitment or select **Edit** to add an existing commitment to this offering.


**Parent Topic:**[Service offerings in Service Portfolio Management](../concept/SPM2-service-offerings.md)

