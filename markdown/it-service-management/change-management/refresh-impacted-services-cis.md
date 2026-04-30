---
title: Refresh impacted services and CIs for Change
description: The Impacted services and CIs related list refreshes its records and also the records listed in the Service Offerings and Business Applications related lists based on the affected CIs. You can identify the impacted services and CIs and take necessary action.
locale: en-US
release: xanadu
product: Change Management
classification: change-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Process a change request, Using Change Management, Change Management, IT Service Management]
---

# Refresh impacted services and CIs for Change

The Impacted services and CIs related list refreshes its records and also the records listed in the Service Offerings and Business Applications related lists based on the affected CIs. You can identify the impacted services and CIs and take necessary action.

## Before you begin

Role required: itil, change\_manager, sn\_change\_write, or admin

## About this task

Refreshing impacted Services on a change request form is executed in one of the following ways:

-   Conflict detection: When a conflict detection is triggered, refreshing of impacted services may be initiated. The **Automatically include business or application services related to Cis with conflicts in the Impacted Cis/Services related list** property \(**change.conflict.populateimpactedcis**\) controls whether the Impacted Services/CIs related list should be refreshed or not. If this property is enabled, then a call is made to the `ChangeUtils` script include calling a refreshImpactedServices method for the current change request.
-   Automatically when the change request moves from the new state: Impacted services are refreshed when the change request moves from the new state and when the Affected CIs related list is not modifiable.
-   Manually when selecting the **Refresh Impacted Services** option from contextual menu.

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Open**.

2.  Open the change record for which you want to refresh the related lists those values are based on affected CIs.

3.  Click the Additional actions icon ![The Additional actions icon](../../incident-management/image/AdditionalActions.png) and then select **Refresh Impacted Services**.

    The records in the Impacted Services/CIs, Business Applications, and Service Offerings related lists are updated according to this flow:

    -   If the **change.refresh\_impacted.include\_affected\_cis** property is set to true, all the services from svc\_ci\_assoc table are retrieved. If the property is set to false, then services are retrieved from `CIUtils` script include.
    -   If the **change.conflict.populateimpactedcis** property is set to true, then additional services are retrieved from ChangeCollisionHelper and added to the list of services.
    -   If the Service Mapping plugin is active, then Application Services are retrieved. These are retrieved, whereby, the association type is **Runs On**, and the association child is one of the CIs in the affected list.
    Once all these services are correlated, a new list is added, and the existing items in the related list are removed, where the **manually\_added** flag is set to false. The list of services is then used to populate the Business Applications and Service Offerings if the properties are enabled.


-   **[Refresh impacted services properties](../reference/refreshing-impacted-services-properties.md)**  
Use the refresh impacted services properties to enable or disable the refresh impacted services capability, and to configure the criteria for additional refresh impacted services properties.

**Parent Topic:**[Process a change request](t_ProcessAChangeRequest.md)

