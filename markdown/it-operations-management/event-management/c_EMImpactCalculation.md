---
title: Alert impact calculation
description: Impact calculation shows the magnitude of an outage on CIs, services, alerts, and alert groups. The system uses factors such as impact rules and CI relationships to calculate the severity of a generated alert. The severity appears on the impact tree, application services maps, and dashboards.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 11
breadcrumb: [Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Alert impact calculation

Impact calculation shows the magnitude of an outage on CIs, services, alerts, and alert groups. The system uses factors such as impact rules and CI relationships to calculate the severity of a generated alert. The severity appears on the impact tree, application services maps, and dashboards.

Impact calculations are available for application services alert groups. The following factors are used to calculate the overall impact of an outage.

-   Impact rules.
-   Number of related active alerts.
-   Past history of the affected CI.
-   Relationships between CIs for a particular application service or application services.
-   If the CI element includes a network or storage devices.
-   Alerts on CIs in the maintenance state are excluded from impact calculation.

    **Note:**

    -   CIs are considered to be in maintenance not only when an active change request is scheduled, but also when the **Status** field of the CI is set to **In Maintenance**.
    -   When a child CI is put in maintenance, it also places the parent CI in maintenance.
-   By default, impact is calculated for all operational application services. However, the system allows you to filter impact calculation by service class or by individual application service. For more information, see [Add CMDB tables or classes for impact calculation](../task/add-cmdb-tables-impact-cal.md) and [Add application services for impact calculation](../task/add-impact-cal-services.md).

If there is a connection between services, the impact of one service on the other is also calculated.

![Factors that affect impact status](../image/EventManagementArchitecture.png "Impact calculations use information from various sources to set the alert severity")

## How impact is calculated

Impact calculation varies depending on the CI relationships for a application service or application services. Additional factors, such as change requests, network paths, storage paths, and related CIs all affect impact calculation.

-   **Services**

    The following impact calculation flow operates for alerts where the outage does not affect a network or network storage. Event Management performs the following steps:

    1.  Create a service map. Use the Service Configuration Item Associations \[svc\_ci\_assoc\] and CI Relationships \[cmdb\_rel\_ci\] tables to create child-parent relationships in the application service or application services.
    2.  If there is no CMDB path from the service to the CI but an association appears in the svc\_ci\_assoc table, show a Depends-on relationship between the application service and the CI. Otherwise, show no connection.
    3.  For an application services, if the CIs assigned to the service are also connected to the service in the CMDB, the map keeps the hierarchy between CIs as they appear in CMDB. The CI service assignments appear in the Service Configuration Item Associations section of the Application service form. If there is no connection to the service in the CMDB, the CIs appear directly under the application services in the map.
    4.  Create the impact tree. Mark the magnitude of an outage by 100% down, 60% affected, 40% impaired, or 20% impaired. If the items in two or more clusters are affected, the impact is 100% down.
-   **Change requests and the In Maintenance status**

    If an active change request is scheduled for the CI or if the **Install Status** of the CI is **In Maintenance**, all alerts on the affected CI are excluded from impact calculation. The Alerts tab also temporarily hides all corresponding alerts. The impact tree shows the CI in green with a note of **\(In Maintenance\)**. The impact tree and the service map temporarily show CIs in green.

    **Note:**

    -   CIs are considered to be in maintenance not only when an active change request is scheduled, but also when the **Status** field of the CI is set to **In Maintenance**.
    -   When a child CI is put in maintenance, it also places the parent CI in maintenance.
    For a service, all alerts on CIs in the service are also hidden from the Alerts tab. The entire service is shown in green on the impact tree. For a host with an active change request, the host applications are considered as one unit. All child applications are treated in the same manner as the host until the change request is no longer active. For additional information, see [How alerts work with CIs in maintenance](c_EMHowImpactTree.md).

-   **Network paths**

    To account for network redundancy, Event Management uses a separate impact calculation. You can see network topology or path changes in the application service. The following impact calculation flow operates for alerts where a network path is affected. Event Management performs the following steps:

    1.  Create a application service map for the affected network.
        -   Use the host ID and target IP information from the alert and the network path from the Network Paths \[sa\_network\_paths\] table.
        -   Use the elements in the network path that derive from the Configuration Item \[cmdb\_ci\] table. Also, use the elements that are associated to the path, from the Infra Path To Elements \[sa\_infra\_path\_assoc\] table.
        -   Set the relationships. The application CI has a Depends on::Used by relationship on an element in the path that is defined in the CI Relationship \[cmdb\_rel\_ci\] table. In the relationship, the application CI is the parent and the element in the network path is the child.
    2.  Calculate a separate severity for each regular element in the path. Each regular element in the path contributes its own severity to its ancestors up to the application CI where the path originated from.
    3.  Calculate all redundant elements in the path with the redundancy rule by reducing the severity on the impacted CIs by one level. For example, if the severity is **Critical**, the redundancy rule decreases severity by one level to **Major**.
    4.  Create the impact tree. Mark the magnitude of an outage by 100% down, 60% affected, 40% impaired, or 20% impaired. If the items in two or more clusters are affected, the impact is 100% down.
-   **Storage paths**

    To account for storage device redundancy, Event Management uses a separate impact calculation. You can see impact tree updates when the network storage topology changes from the application service. Event Management performs the following steps for alerts that contain storage CIs:

    1.  Create a application service map for the affected storage device:
        -   Use the storage device in the sa\_fs\_to\_storage\_path table. The storage device definition uses the file system information in the path.
        -   Use the elements in the storage path that derive from the Configuration Item \[cmdb\_ci\] table. Also, use the elements that are associated to the path from the Infra Path To Elements \[sa\_infra\_path\_assoc\] table.
        -   Set the relationships. The application CI has a Depends on::Used by relationship on an element in the path that is defined in the CI Relationship \[cmdb\_rel\_ci\] table. In the relationship, the application CI is the parent and the element in the storage path is the child.
    2.  Calculate a separate severity for each regular element in the path. Each regular element in the path contributes its own severity to its ancestors up to the original application CI the path.
    3.  Use the redundancy rule to calculate redundant elements in the path by reducing the severity on the impacted CIs by one level. For example, if the severity is **Critical**, the redundancy rule decreases by one level to **Major**.
    4.  Create the impact tree. Mark the magnitude of an outage by 100% down, 60% affected, 40% impaired, or 20% impaired. If the items in two or more clusters are affected, the impact is 100% down.
-   **Related CIs**

    As alerts generate for a CI, additional impact calculations run for related CIs. For example additional impact calculations run for a application service dependency to a CI that is not actually part of the application service. These related CIs are not discovered as part of the service. Instead, the related CIs are specified by an infrastructure relationship definition.

    The following impact calculation flow operates for alerts with CIs that have a dependency to related CIs which are considered outside the application service. Event Management performs the following steps:

    1.  Derive relationships between the application service CIs and related CIs. Use the relationships, impact rules, and other data from the Infrastructure Relations \[em\_impact\_infra\_rel\_def\] table.
    2.  Add related CIs to the impact tree and alert list on the Event Management dashboard.
        -   Use data from the Infrastructure Relationship \[em\_impact\_infra\_rel\_def\] table to show containment links to the host.
        -   Use the Impact Status \[em\_impact\_status\] and Alert History \[em\_alert\_history\] tables to determine the status.

## Impact rules

Impact rules, which are used for impact calculation, estimate the magnitude or severity of an outage based on affected CIs.

The Impact Rule \[em\_impact\_rule\] table contains impact rules that show the applicable CIs, application services, and settings for impact. The following default impact rules are available.

-   **Application Cluster Member**

    Determines how application cluster members affect the overall impact of the cluster. For example, if a three-member cluster requires **90% Influence** to set the severity for the entire cluster to **Major**, each member has **30% Influence** \(90% divided by 3\). The severity of the entire cluster can only change to **Major** when all three members have a severity of **Major**.

    You can configure different impact rules per cluster and thus the child CI impact propagation to the parent \(for the same child CI\) will be different. Therefore, you can manually create groups of Cis \(aka manual clusters\) and configure the impact rule at the cluster level for downstream towards the cluster children.

    ![child CI severity is propagated differently to each parent service](../image/manual-cluster.png "Example where the same child CI will propagate its impact to its parent cluster differently to each cluster")

    In the above example, there are two entry points. The Osaka cluster on the right-hand side has three CIs. The Tokyo cluster on the left-hand side has two CIs. The Tokyo and Osaka backup server has shared parents - Tokyo cluster and Osaka cluster. On the right-hand panel you can see the Impact Tree where the Tokyo cluster has two Application Cluster Members with 50% influence each and the Osaka cluster has three with 34% influence each.

    For manual cluster configuration there are two rows: Application Impact and Application Cluster Member. The children are displayed since the Impact On field was selected as Parent and not Application Service. In the Application Cluster Member row the Influence field is configured to two. This implies that the minimum amount of children who fail \(and that they propagate the failure upwards to their parents\) are two. The Osaka cluster is configured to three. The percentage is different for the Tokyo and Osaka backup server for each cluster \(50% and 34%\). As you can see, even though the Tokyo and Osaka backup server failure is Red Critical, it influences the parents differently. The Osaka cluster remains green even though the Tokyo cluster failure is Orange Major.

    Click a service or CI to see the alerts that are associated with it. For example, if you click the high-level application service, the alerts that are associated with it are displayed in the alert area under the Map View when you select **Alerts**. The alerts listed are those of the selected service. Alerts of child-services are listed when those services are selected.

    The following impact fields are displayed when you select **Impact**.

-   **Inclusion**

    Determines the impact on entities with a Contains relationship. This rule is read-only.

-   **Infrastructure Dependencies**

    Determines the definition of impact propagation for CIs in infrastructure relationships.

-   **CI application service**

    Determines how impact applies to parent or child entities that are part of an application service.

-   **CI Impact**

    Applies to application services. Determines the relationship between service members. The impact from child to parent CIs is always 100%. For example, the parent impact severity is derived from the child CI with the highest severity.

-   **CI Parent in Application**

    Sets impact only on the parent entity.

-   **Network Path**

    Determines how impact applies to parent or child entities that are part of a traditional network.

-   **OS Cluster Member**

    Determines how host cluster members affect the overall cluster status based on a percentage or number of cluster members. For example, if a three-host cluster requires **60% Influence** to set the severity of **Major**, each member has **20% Influence** \(60% divided by 3\). The severity of the entire cluster can only change to **Major** when two or more cluster members have a severity of **Major**. The entire cluster is also considered to be down.

-   **Storage Path**

    Determines how impact applies to parent or child entities that are part of a storage network.


## Properties

In addition to configuring impact rules, you can configure properties for impact calculation.

Configure these properties, as appropriate:

<table id="table_qw1_xh5_drb"><thead><tr><th>

Property Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`evt_mgmt.impact_calculation.alert_group_support`

</td><td>

Enable alert group support.

</td></tr><tr><td>

`evt_mgmt.impact_maintenance.sleep_time_sec`

</td><td>

Minimum time in seconds for checking CI maintenance: checks both the Status field on the CI and any change request schedule for the CI.

</td></tr><tr><td>

`evt_mgmt.impact_calculation.alert_copy_delay`

</td><td>

The delay after creating or updating an alert, before it is used for impact calculation and grouping. Used to compensate for the late arrivals or slow business rules defined on the em\_alert table. Default = 2000 msec. Used when alerts and events are processed one at a time \(when the `evt_mgmt.max_objs_in_alert_query` property is not defined or is set to **1**\).

</td></tr><tr><td>

`evt_mgmt.impact_calculation.alert_copy_delay_when_alerts_are_processed_in_batch_msec`

</td><td>

The delay after creating or updating an alert, before it is used for impact calculation and grouping. Used to compensate the late arrivals or slow business rules defined on em\_alert table. Default = 30000 msec.Used in large customer environments with high traffic, when alerts and events are processed in batches \(when the `evt_mgmt.max_objs_in_alert_query` property is set to a value greater than **1**\).

</td></tr></tbody>
</table>For more information, see [Event Management - Impact calculation \[KB1157218\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1157218).

