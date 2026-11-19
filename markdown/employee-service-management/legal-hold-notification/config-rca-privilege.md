---
title: Configure a restricted caller access privilege
description: Configure a restricted caller access privilege for the document templates application with a global scope to allow the legal matter application to perform read operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/legal-hold-notification/config-rca-privilege.html
release: zurich
product: Legal Hold Notification
classification: legal-hold-notification
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Legal Hold Notification, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Configure a restricted caller access privilege

Configure a restricted caller access privilege for the document templates application with a global scope to allow the legal matter application to perform read operations.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **Application Restricted Caller Access**.

2.  Set the application scope.

    1.  Select the Application scope icon \(\[Omitted image "application-scope-globe-icon.png"\] Alt text: Application scope icon\).

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


**Parent Topic:**[Configure Legal Hold Notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/legal-hold-notification/config-lg-hold-notif.md)

