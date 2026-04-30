---
title: Configure a restricted caller access privilege
description: Configure a restricted caller access privilege for the document templates application with a global scope to allow the legal matter application to perform read operations.
locale: en-US
release: yokohama
product: Legal Hold Notification
classification: legal-hold-notification
topic_type: task
last_updated: "2025-06-26"
reading_time_minutes: 1
breadcrumb: [Configuring Legal Hold Notification, Legal Hold Notification, Legal Service Delivery Practice Applications, Legal Service Delivery, Employee Service Management]
---

# Configure a restricted caller access privilege

Configure a restricted caller access privilege for the document templates application with a global scope to allow the legal matter application to perform read operations.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **Application Restricted Caller Access**.

2.  Set the application scope.

    1.  Select the Application scope icon \(![Application scope icon](../../workplace-calendar-synchronization/image/application-scope-globe-icon.png)\).

    2.  In the filter navigator, search for and select **Document Templates**.

3.  In the **Restricted Caller Access Privileges** page, select **New**.

4.  Enter the following field values.

    |Field|Value|
    |-----|-----|
    |Source Scope|Global|
    |Application|Document Templates|
    |Source Type|Source Include|
    |Target Scope|Document Templates|
    |Status|Allowed|
    |Target Type|Table: Document Templates|
    |Description|Short description text.|

5.  Select **Submit**.


**Parent Topic:**[Configuring Legal Hold Notification](../concept/config-lg-hold-notif.md)

