---
title: Create request as manager using the Kronos catalog item
description: Trigger events in Kronos when an item is requested in the Service Catalog.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [UKG Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Create request as manager using the Kronos catalog item

Trigger events in Kronos when an item is requested in the Service Catalog.

## Before you begin

-   [Set up the UKG spoke](setup-kronos.md#)
-   Role required: admin

## About this task

The Kronos spoke adds a catalog item for use with the Kronos spoke sample flows.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Service Catalog**.

2.  Click **Kronos**.

3.  Click **Kronos - Create Time Off Request As Manager \(Super Access\)**.

4.  Provide details of the time off request.

    **Note:** After you have provided a valid **Employee ID** or **Person Number\(Qualifier\)**, the system may take some time to populate the values in the **Subtype Name using Employee ID** and **Symbolic Amount Qualifier By Employee ID**, or **Subtype Name using Person Number** and **Symbolic Amount Qualifier By Person Number** lists.

5.  Click **Order Now**.

    A request item is generated and its generated number is displayed.

6.  Click the request number and change the value of **Approval** to **Requested**, **Approved**, or **Rejected**.

7.  Click **Update**.


## Result

-   The Kronos - Create Manager Time Off Request flow is triggered.
-   A record is created in the Time Off Request Details module. The status of the time off request is updated when the Kronos - Retrieve And Update Manager Time Off Status flow is triggered.

