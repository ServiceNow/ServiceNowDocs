---
title: Remove CIs not belonging to application services
description: Remove CIs erroneously mapped as part of an application service by Service Mapping. Unnecessary CIs included in the map can generate irrelevant alerts in Event Management. For example, when creating an application service for a web portal, Service Mapping might automatically discover a connection to unaffiliated external services, such as PayPal.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Fine-tune application services to implement owner requests, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Remove CIs not belonging to application services

Remove CIs erroneously mapped as part of an application service by Service Mapping. Unnecessary CIs included in the map can generate irrelevant alerts in Event Management. For example, when creating an application service for a web portal, Service Mapping might automatically discover a connection to unaffiliated external services, such as PayPal.

## Before you begin

You remove CIs only from application services discovered by Service Mapping.

**Important:** You cannot fine-tune or edit tag-based and dynamic services from the map.

Role required: service\_mapping\_admin

## About this task

Removing CIs from the map also removes all their connections. For example, if you remove a CI of the second tier on the map, all CIs of the third tier connected to it through outgoing connections, get removed too.

Depending on why Service Mapping mapped an unwanted CI, you can remove it by the following methods:

-   Add mapping boundaries to remove the unnecessary CIs. A boundary makes Service Mapping stop discovery from this point and not follow outgoing connections. Use this method to remove CIs that Service Mapping discovered using patterns or using traffic-based discovery.

-   Tweak traffic-based discovery. Service Mapping can discover and map configuration items \(CIs\) following their traffic-based connections. This method is referred to as traffic-based mapping and complements pattern-based mapping. Service Mapping generates connection suggestions based on traffic-based connections and on Predictive Intelligence analysis of application fingerprints. If the connection suggestions feature is enabled, Service Mapping doesn't automatically add any traffic-based connections to application services, providing suggestions. Review the suggestions and choose which CIs to add or to remove.

    If the connection suggestions feature is disabled, Service Mapping automatically adds traffic-based connections and CIs to application services. Remove connections that lead to irrelevant CIs to declutter application services.


## Procedure

1.  Open the service instance map.

    1.  Navigate to **All** &gt; **CSDM** &gt; **Manage Technology Management Services** &gt; **Service Instance**.

    2.  Select the needed service instance.

    3.  On the service instance page, select **View Map**.

2.  Remove CIs that do not belong to this service instance by completing the following actions.

<table id="choicetable_rsk_cnk_hnb"><thead><tr><th align="left" id="d579338e172">

Action

</th><th align="left" id="d579338e175">

Steps

</th></tr></thead><tbody><tr><td id="d579338e181">

**Add mapping boundaries**

</td><td>

1.  Right-click the connector leading to the CI you want to remove.
2.  Select **Mark boundary**.

The CI is marked as boundary on the map \(![The boundary icon](../image/MapBoundaryIcon.png)\).

 **Note:** Ensure that you are looking at the map in Edit view.

</td></tr><tr><td id="d579338e213">

**\(If the connection suggestions feature is disabled\) Remove CIs discovered using traffic-based connections**

</td><td>

1.  Right-click the CI on the map.

**Note:** You can see traffic-based connections for a CI, even if you disabled the traffic-based discovery for an service instance the CI is part of.

2.  Select **Show traffic based connections**.

The Traffic Based Connections List opens. See [Traffic-based connections list](../reference/traffic-based-connections-list.md).

3.  In the **Traffic Based Connections List**, identify the connection used to discover the unwanted CI.
4.  Select `Remove` from the **User decision** field for this connection.
5.  Click **Close**.


</td></tr><tr><td id="d579338e269">

**\(If the connection suggestions feature is enabled\) Remove CIs discovered using traffic-based connections**

</td><td>

Perform the procedure described in [Add or remove CIs for single application services using connection suggestions](add-remove-ci-connections-services.md).

</td></tr></tbody>
</table>
**Parent Topic:**[Fine-tune application services to implement owner requests](review-implement-business-service-maps.md)

**Related topics**  


[Enable traffic-based discovery for CI types or specific CIs](t_CreateATrafficBasedDiscoveryRule.md)

