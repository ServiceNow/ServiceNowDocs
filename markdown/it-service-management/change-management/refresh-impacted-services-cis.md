---
title: Refresh impacted services and CIs for Change
description: The Impacted services and CIs related list refreshes its records based on the affected CIs. Records in the Service Offerings and Business Applications related lists also refresh. Use this information to identify impacted services and CIs and take action.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/refresh-impacted-services-cis.html
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Process a change request, Use, Change Management, IT Service Management]
---

# Refresh impacted services and CIs for Change

The Impacted services and CIs related list refreshes its records based on the affected CIs. Records in the Service Offerings and Business Applications related lists also refresh. Use this information to identify impacted services and CIs and take action.

## Before you begin

Role required: itil, change\_manager, sn\_change\_write, or admin

## About this task

Impacted services on a change request are refreshed in one of the following ways:

-   Conflict detection: When a conflict detection is triggered, refreshing of impacted services may be initiated. The **Automatically include business or application services related to Cis with conflicts in the Impacted Cis/Services related list** property \(**change.conflict.populateimpactedcis**\) controls whether the Impacted Services/CIs related list is refreshed. When this property is set to true, the refreshImpactedServices method of the `ChangeUtils` script include runs for the current change request.
-   Automatically when the change request moves from the new state: Impacted services are refreshed when the change request moves from the new state and when the Affected CIs related list is not modifiable.
-   Manually when selecting the **Refresh Impacted Services** option from the form context menu.

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Open**.

2.  Open the change request whose related lists you want to refresh.

3.  Select the Additional actions icon \[Omitted image "AdditionalActions.png"\] Alt text:, and then select **Refresh Impacted Services**.

    The records in the Impacted Services/CIs, Business Applications, and Service Offerings related lists are updated according to this flow:

    -   If the **change.refresh\_impacted.include\_affected\_cis** property is set to true, all the services from the svc\_ci\_assoc table are retrieved. If the property is set to false, then services are retrieved from the `CIUtils` script include.
    -   If the **change.conflict.populateimpactedcis** property is set to true, then additional services are retrieved from the `ChangeCollisionHelper` script include and added to the list of services.
    -   If the Service Mapping plugin is active, application services are retrieved where the association type is **Runs On** and the association child is a CI in the affected list.
    After all these services are correlated, the existing items in the related list whose `manually_added` flag is false are removed, and the new list is added. The list of services is then used to populate the Business Applications and Service Offerings if the properties are enabled.


-   **[Refresh impacted services properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/refreshing-impacted-services-properties.md)**  
Use the refresh impacted services properties to turn on or turn off the refresh impacted services capability, and to configure the criteria for additional refresh impacted services properties.

**Parent Topic:**[Process a change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/t_ProcessAChangeRequest.md)

