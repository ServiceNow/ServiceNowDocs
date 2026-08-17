---
title: Work notes for incident field updates with DEX
description: When a configuration item \(CI\), Business Service, or Service Offering on an incident record is set to an item monitored by DEX, a work note is added automatically. Service desk agents use these notes to view monitoring context on the incident record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/ci-update-work-notes.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-07-24"
reading_time_minutes: 3
keywords: [CI update work note, CI update, incident, device health, configuration item, business service, service offering]
breadcrumb: [Incident diagnostics and suggested resolutions, DEX for service desk agents, Digital End-User Experience, IT Service Management]
---

# Work notes for incident field updates with DEX

When a configuration item \(CI\), Business Service, or Service Offering on an incident record is set to an item monitored by DEX, a work note is added automatically. Service desk agents use these notes to view monitoring context on the incident record.

When the CI, Business Service, or Service Offering field on an incident record changes, the platform determines whether the associated item is monitored by Digital End-user Experience Self-service \(DEX\). The system checks the following:

-   For a device CI, whether the device has a DEX agent connected
-   For an application CI, whether the application is monitored by DEX
-   For a Business Service, whether the business service is monitored by DEX
-   For a Service Offering, whether the service offering is monitored by DEX

If the item is monitored, the system automatically posts a work note on the incident. The work note includes a message and a link to view more details in DEX. Service desk agents can select the link to view more details. For link destinations by field type, see [Link destination by field type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/ci-update-work-notes.md).

**Tip:** This automatic work note is separate from the incident diagnostics and suggested resolutions available from the **Investigation** tab. For more information, see [Incident investigation with DEX](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/dex-diagnostics-guided-resolutions.md).

## When the work note is posted

The system posts a work note in the following cases:

-   When a CI, Business Service, or Service Offering is set on a new incident.
-   When the CI, Business Service, or Service Offering on an existing incident is changed to a different value.

The work note wording depends on the field type, the CI type \(device or application\), and whether the value was set at incident creation or changed afterward.

|Field type|Set on a new incident|Changed on an existing incident|
|----------|---------------------|-------------------------------|
|Application CI|`The Configuration Item on this incident is *CI name*. This CI is monitored by DEX. Click the link below to view more details in DEX.`|`The Configuration Item on this incident has been updated to *CI name*. This CI is monitored by DEX. Click the link below to view more details in DEX.`|
|Device CI|`The Configuration Item on this incident is *CI name*. This CI has a DEX agent connected. Click the link below to view more details in DEX.`|`The Configuration Item on this incident has been updated to *CI name*. This CI has a DEX agent connected. Click the link below to view more details in DEX.`|
|Business Service|`The Business Service on this incident is *service name*. This service is monitored by DEX. Click the link below to view more details in DEX.`|`The Business Service on this incident has been updated to *service name*. This service is monitored by DEX. Click the link below to view more details in DEX.`|
|Service Offering|`The Service Offering on this incident is *offering name*. This offering is monitored by DEX. Click the link below to view more details in DEX.`|`The Service Offering on this incident has been updated to *offering name*. This offering is monitored by DEX. Click the link below to view more details in DEX.`|

## Link destination

Selecting the link in the work note opens the following page in the Service Operations Workspace, depending on the field type:

-   For a device CI, the **Device health overview** tab of the device page.
-   For an application CI, the **Overview** tab of the installed application or web application page, depending on the application type.
-   For a Business Service, the corresponding business service page.
-   For a Service Offering, the corresponding service offering page.

