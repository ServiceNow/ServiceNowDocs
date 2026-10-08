---
title: HRBP roles
description: Information about the roles installed with HRBP and the additional roles required for using HRBP.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/hr-service-delivery/hrbp-sa-roles.html
release: brazil
product: HR Service Delivery
classification: hr-service-delivery
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 1
breadcrumb: [Reference, HRBP productivity assistant, HR Service Delivery, Employee Service Management]
---

# HRBP roles

Information about the roles installed with HRBP and the additional roles required for using HRBP.

## HRBP productivity assistant roles

The following table lists the roles installed with the HRPB productivity assistant.

|Roles|Description|
|-----|-----------|
|sn\_hrbp\_hub.admin|Provides access to HRBP configuration flow; can create, edit, and delete entries in tables.|
|sn\_hrbp\_hub.user|Provides the non-admin, regular user experience. This role does not give users access to data from other HRSD applications. You must also assign the HRBP roles from respective applications.|

The following table lists the roles that should be assigned to the sn\_hrbp\_hub.user to grant that user access to the data from the applications.

|Roles|Application|
|-----|-----------|
|sn\_lep.hrbp|Learning|
|sn\_ta\_hiring\_core.hrbp|Hiring Core|
|sn\_hr\_core.hrbp|Human Resources: Core|
|sn\_ja.hrbp|Journey Accelerator|
|sn\_egd\_goals.hrbp|Employee Goals|
|sn\_egd\_core.hrbp|Talent Development Core|
|sn\_opp\_market.hrbp|Opportunity Marketplace|
|sn\_lc.hrbp|Learning Core|
|sn\_employee.hrbp|Employee Profile|
|sn\_jny.hrbp|Journey designer|
|sn\_skills\_int.hrbp|Skills foundation|
|sn\_egd\_act.hrbp|Career Conversations|
|sn\_hr\_le.hrbp|Human Resources: Lifecycle Events|

