---
title: Convert manual services to application services using API
description: You can use a JavaScript API to convert existing manual services to application services. Event Management can use application services to monitor service performance and identify health issues.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Application services in Event Management, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Convert manual services to application services using API

You can use a JavaScript API to convert existing manual services to application services. Event Management can use application services to monitor service performance and identify health issues.

Manual services are no longer supported and this service type, as well as discovered services, have been replaced by application services. Any existing manual services must be converted to application services. Ensure that any automation of manual services \(such as business rules or scheduled jobs\) have been built and tested before converting to application services.

**Note:** Manual services are static and retain their original structure after conversion to application services. To update imported manual services with the existing CMDB state, either populate the original manual services to ensure that all CIs are assigned to the correct service, or run the **update with CMDB changes** option after the conversion.

During the conversion process:

-   The manual service record is moved from the Manual Services \[cmdb\_ci\_service\_manual\] table to the Mapped Application Service \[cmdb\_ci\_service\_discovered\] table by changing the record class.
-   All the original manual service attributes, such as, name, owner, and operational status, are retained in the application services.
-   The configuration items \(CIs\) of the manual service are retained in the application services after the conversion.
-   The system queries the CMDB for the latest CI changes and applies CI impact rules.

The maximum number of CI connections added to application services during this operation is controlled by the sa.service.max\_ci\_service\_population property. By default, the value is 1,000 \(one thousand connections\). Increasing the number of CI connections may cause performance issues. To adjust the maximum number of added CI connections, add the sa.service.max\_ci\_service\_population property, as described in Add a system property.

Attempting to process more CIs than the value specified in the sa.service.max\_ci\_service\_population property causes the operation to fail.

Run the conversion process in small chunks of approximately 10 at a time, to make it easier to pinpoint the problematic service in the event of a conversion problem.

Application services do not support these CI types:

-   cmdb\_ci\_endpoint
-   cmdb\_ci\_translation\_rule
-   cmdb\_ci\_config\_file
-   cmdb\_ci\_qualifier
-   cmdb\_ci\_application\_cluster

If the preceding CI types are used in the manual service that you want to convert, the conversion fails. CIs of this type should be removed before conversion. They can be replaced by adding new CIs to the application services after conversion.

If your ServiceNow instance uses domain separation, the conversion fails if CIs from multiple domains are in the same service. Replace or remove relevant CIs before conversion. The converted application services contains only CIs assigned to the same domain as the application services.

The JavaScript API is:

```
BusinessServiceManager.migrateManualToApplicationService(String service_id)
```

|Name|Type|Description|
|----|----|-----------|
|service\_id|String|sys\_id of the manual service to be converted|

|Type|Description|
|----|-----------|
|Boolean|`true` for a successful conversion, `false` for a conversion that failed|

Where the `sys_id` of an existing manual service is `451047c6c0a8016400de0ae6df9b9d76`, run the following API to convert it to an application services:

```
var bsManager = new SNC.BusinessServiceManager();
var res = bsManager.migrateManualToApplicationService("451047c6c0a8016400de0ae6df9b9d76");
```

**Parent Topic:**[Application services in Event Management](../concept/application-service-event-management.md)

**Related topics**  


[bundle-crapiref.BusinessServiceManagerAPI]

