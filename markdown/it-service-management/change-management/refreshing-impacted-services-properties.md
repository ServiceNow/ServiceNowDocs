---
title: Refresh impacted services properties
description: Use the refresh impacted services properties to enable or disable the refresh impacted services capability, and to configure the criteria for additional refresh impacted services properties.
locale: en-US
release: zurich
product: Change Management
classification: change-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Refresh impacted services and CIs for Change, Process a change request, Use, Change Management, IT Service Management]
---

# Refresh impacted services properties

Use the refresh impacted services properties to enable or disable the refresh impacted services capability, and to configure the criteria for additional refresh impacted services properties.

By configuring these properties, you can control the capabilities, such as:

-   Include the primary configuration item or all the items in the Affected CIs related list.
-   Processing of refreshing the impacted services as an event.
-   Populate Service Offerings and Business Applications from the Impacted Services related list.

The following properties can be found in sys\_properties.list and on the Change properties page.

<table id="table_ydl_qdx_v4b"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.snc.change\_request.refresh\_impacted.include\_affected\_cis

</td><td>

-   When true, all the configuration items listed in the Affected CIs related list are checked. These configuration items are checked against the Application services mapping table \(svc\_ci\_assoc\) as this is a faster process, and also returns a more concise relationship picture. All the services from svc\_ci\_assoc table are retrieved.
-   If the property is false, only the CI on the change form is used. This uses the method of traversing the cmdb tree structure to find the services. The services are retrieved from `CIUtils` script include.

 **Note:** If dynamic CI groups are used on the Change form, then this property must be set to true as the associations are located in the svc\_ci\_assoc table.

 When a business service is converted to an application service \(as an example\), all the levels included in the svc\_ci\_assoc table are considered at the time of conversion.

</td></tr><tr><td>

change.conflict.populateimpactedcis

</td><td>

If this property is set to true, then the `ChangeCollisionHelper` script include checks the configuration items that have been identified in the list of conflicts against the Application services mapping table \(svc\_ci\_assoc\) and also table \(cmdb\_ci\_service\) to check if there are any business services that are directly impacted.

</td></tr><tr><td>

com.snc.change\_request.refresh\_impacted.event

</td><td>

-   When true, the process of refreshing the impacted services is done through an event. This process is run in the background and you will be notified through a message in Notify that the process has been complete.
-   When false, this is run in your session. As this is not run in background, there is no notification on completion.

</td></tr><tr><td>

com.snc.change\_request.populate\_service\_offering

</td><td>

-   When true, the Service Offerings related list is populated from the Impacted Services/CIs related list.
-   When false, the related list is not populated or amended in any way.

</td></tr><tr><td>

com.snc.change\_request.populate\_business\_application

</td><td>

-   When true, the Business Applications related list is populated from the Impacted Services/CIs related list.
-   When false, the related list is not populated or amended.

</td></tr><tr><td>

com.snc.change\_request.refresh\_impacted\_services.message.show

</td><td>

-   When true, the `Refresh impacted services is initiated` message appears on the Change request form.
-   When false, the `Refresh impacted services is initiated` message doesn't appear.

</td></tr></tbody>
</table>**Parent Topic:**[Refresh impacted services and CIs for Change](../task/refresh-impacted-services-cis.md)

