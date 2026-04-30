---
title: Convert manual services to application services
description: You can convert existing manual services to application services. Event Management can use application services to monitor service performance and identify health issues.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Application services in Event Management, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Convert manual services to application services

You can convert existing manual services to application services. Event Management can use application services to monitor service performance and identify health issues.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

Manual services are no longer supported and this service type, as well as discovered services, have been replaced by application services. Any existing manual services must be converted to application services.

During the conversion process:

-   The manual service record is moved from the Manual Services \[cmdb\_ci\_service\_manual\] table to the Mapped Application Service \[cmdb\_ci\_service\_discovered\] table by changing the record class.
-   All the original manual service attributes, such as, name, owner, and operational status, are retained in the application services.
-   The configuration items \(CIs\) of the manual service are retained in the application services after the conversion.
-   The system queries the CMDB for the latest CI changes and applies CI impact rules.

Application service does not support these CI types:

-   cmdb\_ci\_endpoint
-   cmdb\_ci\_translation\_rule
-   cmdb\_ci\_config\_file
-   cmdb\_ci\_qualifier
-   cmdb\_ci\_application\_cluster

If the preceding CI types are used in the manual service that you want to convert, the conversion fails. CIs of this type should be removed before conversion. They can be replaced by adding new CIs to the application services after conversion.

If your ServiceNow instance uses domain separation, the conversion fails if CIs from multiple domains are in the same service. Replace or remove relevant CIs before conversion. The converted application services contains only CIs assigned to the same domain as the application services.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Services** &gt; **Manual Services**.

    ![Manual service in the list](../image/manual-service-in-list.png)

2.  Select the manual service that you want to convert to an application services.

    ![Convert manual service to application service](../image/migrate-manual-2-application.png)

3.  Click **Migrate to Application Service**.

4.  Click **OK**.


## Result

-   The CIs from the manual service are added to the converted application services.
-   After the conversion process is complete, the application services form opens.

**Parent Topic:**[Application services in Event Management](../concept/application-service-event-management.md)

