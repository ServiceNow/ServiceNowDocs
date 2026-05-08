---
title: Review application service maps
description: As the application service owner for the application service map, you receive an email notification that the application service map is assigned to you for review. Review mapping results for correctness and either provide your feedback or approve the application service map. The review and approval process is available only for discovered and manually created service instances.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Review and approval of application service maps, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Review application service maps

As the application service owner for the application service map, you receive an email notification that the application service map is assigned to you for review. Review mapping results for correctness and either provide your feedback or approve the application service map. The review and approval process is available only for discovered and manually created service instances.

## Before you begin

Role required: sm\_app\_owner

## About this task

Ideally, only the application service owner reviews the planned application service, however, users with the sm\_app\_owner or service\_mapping\_admin role can also perform this task.

Reviewing application service maps is part of the [review and approval process](business-service-approval.md). The process of application service review may take some time as it requires making changes and repeatedly running the mapping process on the application service. Typically, it takes several iterations to arrive at the desired result. Once you are satisfied with the discovery result, you approve the application service.

After you request fixes or approve the application service, the service process task assigned to you closes.

To see documentation for another review phase, click the relevant box in the diagram.

![Approval flow for individual application services](../image/ApproveBSFlow.png)

## Procedure

1.  Click the link to the application service map in the email notification.

    The map of the application service opens in the ServiceNow instance.

2.  Alternatively, open to the application service to review from the list of tasks assigned to you.

    1.  Navigate to **Service Mapping** &gt; **Administration** &gt; **My Tasks**.

    2.  Sort the list of service process tasks as required.

    3.  Click the required task.

    4.  Click the application service form link.

    5.  Click **View map**.

3.  On the application service map, check that all essential CIs comprising the application service are discovered and mapped correctly.

<table id="choicetable_zzx_gvd_ht"><thead><tr><th align="left" id="d267263e275">

Purpose

</th><th align="left" id="d267263e278">

Action

</th></tr></thead><tbody><tr><td id="d267263e284">

**Verify that there are no missing CI connections.**

</td><td>

Pay attention to CIs with no connectors from it to other CIs. For example, in the following figure, the Web Server on win2K12 CI is missing connections.![CIs missing connectors](../image/MapMissingConnection.png)

 If connections and CIs to which they lead are missing, the map does not reflect the real state of the service instance and its operation. Inaccurate data can also be transferred to Event Management, causing imprecise monitoring.

</td></tr><tr><td id="d267263e308">

**Verify that there are no CIs that do not belong in the service.**

</td><td>

Check all CIs comprising the application service map to identify CIs not belonging to this application service. Typically, it is applications supporting internal services. For example, Microsoft Internet Information Services \(IIS\) connecting to Active Directory, may be not part of the application service.

</td></tr><tr><td id="d267263e317">

**Check that the connections between CIs are correct.**

</td><td>

[View CI connection attributes in an application service map in classic Service Mapping](view-connector-properties.md).

</td></tr><tr><td id="d267263e333">

**Check that clusters are reflected correctly.**

</td><td>

Click the plus \(+\) icon next to a CI.There are two types of clusters:

-   **Application cluster**

In an application cluster, two or more applications or devices are configured to work together and serve the same purpose. Typically, the clusters provide high availability or load balancing. For example, web servers working behind a load balancer.

This type of cluster appears as a stack of CIs with a label showing the number of CIs in this cluster with the multiplication sign.

![Expanding an application cluster](../image/MapClusterAppCluster.png)

Application clusters can have a cluster within a cluster, but never more than two levels:

![Expanding an application cluster with two levels](../image/MapClusterDouble.png)

-   **OS cluster**

In an OS cluster, a server hosts two identical operating systems. Typically, the cluster provides failover.

This type of cluster appears as a CI with a plus sign and the number of CIs in this cluster.

![OS cluster](../image/MapClustersOSClusters.png)

</td></tr><tr><td id="d267263e388">

**Check that inclusions are reflected correctly.**

</td><td>

Click the plus \(+\) icon next to a CI.In an inclusion, a server hosts applications that are treated as independent objects. For example, IIS Virtual Directory can run on a Windows Service as its host.

 ![Expanding inclusion](../image/MapClusterInclusion.png)

</td></tr></tbody>
</table>4.  To notify the service mapping admin of a necessary change or fix, perform the following steps:

    1.  Click **Actions** above the map.

    2.  Select **Reject Service Map**.

    3.  In the Add Reject Message window, enter your comment, and click **Add**.

        The new comment appears on the **Discovery Messages** tab under the map. The application service status changes to Rejected.

    4.  If necessary, add more comments.

5.  If you are satisfied with the results, approve this application service by clicking **Actions**, and then **Approve service**.

    The application service status changes to Approved and it appears in the list of completed application services on the **Home** page. The operational status changes to Operational. From this point, other applications can use data collected and organized by Service Mapping.


**Parent Topic:**[Review and approval of application service maps](business-service-approval.md)

**Related topics**  


[Fix errors in individual application service maps](fix-or-ignore-errors-business-service-map.md)

