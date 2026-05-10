---
title: Fix errors in individual application services using discovery messages
description: Service Mapping does not offer semi-automated resolution options for errors that require advanced resolution. Fix such errors using symptoms and discovery messages.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Fix errors in individual application service maps, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Fix errors in individual application services using discovery messages

Service Mapping does not offer semi-automated resolution options for errors that require advanced resolution. Fix such errors using symptoms and discovery messages.

## Before you begin

Try fixing errors using semi-automated resolution options as described in [Fix errors in individual application service maps](fix-or-ignore-errors-business-service-map.md).

Role required: service\_mapping\_admin

## About this task

You can fix errors in individual application services at any time.

## Procedure

1.  Open the service instance map.

    1.  Navigate to **All** &gt; **CSDM** &gt; **Manage Technology Management Services** &gt; **Service Instance**.

    2.  Select the needed service instance.

    3.  On the service instance page, select **View Map**.

2.  Select **View Map** next to the relevant service instance.

3.  Ensure that the map opens in Edit mode.

    ![Discovery messages appear under the map.](../image/MapEditDiscoveryMessages.png)

    CIs discovered with errors appear with the warning icon \(![The Warning icon](../image/MapWarningIcon.png)\) on the map. Discovery messages on the **Discovery Messages** tab give short error descriptions.

4.  Fix errors based on the symptoms and discovery messages.

<table id="table_c5n_zmf_jz"><thead><tr><th>

Symptom

</th><th>

Resolution

</th></tr></thead><tbody><tr><td>

The following discovery message is displayed: `The map does not display the entire service, because it is too large. The number of CI connections exceeded the allowed maximum.`

</td><td>

Reduce the application service size.-   For an application service mapped using pattern-based and traffic-based discovery, perform the following actions:
    -   If you use customized discovery patterns and mapping results in very large service instances, modify the patterns so that they don't map irrelevant CIs.
    -   [Split the service into smaller services](add-segment-to-business-service-map.md).
-   For an application service converted from an application service, perform the following actions:
    -   Review the converted service instance to identify CI relations irrelevant or redundant for this service. Remove such CI relations in the CMDB.
    -   Decide how many levels of related CIs you must include into this service instance. If necessary, [change the number of levels used in conversion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/update-services-from-cmdb.md) to reduce the service size.


</td></tr><tr><td>

The following discovery message is displayed in a tag-based service instance: **This tag-based service instance reached the maximum number of CIs. For more information, refer to the product documentation.**

</td><td>

Perform the following actions: -   [Modify tag definitions used for mapping](modify-tag-category-family.md) to make sure Service Mapping includes only relevant CIs in the service instance.
-   If necessary, [Tag-based discovery configuration](../concept/tag_discovery_configuration.md) to change which CIs Service Mapping includes in tag-based service instances.


</td></tr><tr><td>

-   The service instance map displays the warning icon \(![The Warning icon](../image/MapWarningIcon.png)\) on top or instead of the configuration item.
-   The following discovery message displays for the configuration item: `Failed to execute command using sudo on host <host IP address>`.


</td><td>

[KB0621669: Resolving failure to execute commands using sudo during Discovery in Service Mapping](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0621669)

</td></tr><tr><td>

The following error message displays for the configuration item: `Access is denied`.

</td><td>

[KB0564283: Resolving an issue of denied access to a Windows Server](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0564283)

</td></tr><tr><td>

-   The service instance map displays the warning icon \(![The Warning icon](../image/MapWarningIcon.png)\) on top or instead of the Windows Server.
-   The following discovery message displays for the Windows Server: `RPC Server unavailable`.


</td><td>

[KB0564282: Resolving issue of RPC Server unavailable during Windows Server discovery in Service Mapping](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0564282)

</td></tr><tr><td>

-   The service instance map displays the warning icon ![The Warning icon](../image/MapWarningIcon.png) instead of the load balancer CI.
-   The following discovery message is displayed: `Service Mapping triggered the horizontal discovery to find the host x.x.x.x, because this host was not in the CMDB. The horizontal discovery failed. See discovery status for more info`.


</td><td>

[KB0610414: Resolving failure to discover operating system for a load balancer](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0610414)

</td></tr><tr><td>

Instead of the map, the following discovery message displays: `Cannot display the map. Topology too large`.

</td><td>

[KB0596671: Resolving a large topology issue in service instance maps](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0596671)

</td></tr><tr><td>

A Virtual IP \(VIP\) for a load balancer service CI is sometimes updated with the IP addresses of another load balancer.

</td><td>

[KB0610412: Resolving load balancers merging into one CI in Service Mapping](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0610412)

</td></tr><tr><td>

The map displays incorrect virtual IP names for load balancers.

</td><td>

[KB0610413: Resolving incorrect virtual IP names of load balancers in Service Mapping](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0610413)

</td></tr><tr><td>

The service instance map consists of different CIs every time you run the mapping process on the same entry points to discover the same service instance.

</td><td>

[KB0595227: Troubleshooting inconsistent mapping results](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0595227)

</td></tr><tr><td>

There is no load balancer CI on the service instance map. There are connections going directly from the entry point of the service instance to the next tier CIs. The rest of the CIs also disappear from the map.

</td><td>

[KB0621529: Resolving the issue of a load balancer disappearing from the application service map](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0621529)

</td></tr><tr><td>

-   The service instance map displays the warning icon \(![The Warning icon](../image/MapWarningIcon.png)\) on top or instead of the configuration item.
-   The following discovery message displays for the configuration item: `SSH command timed out on host`.


</td><td>

[KB0621670: Resolving the issue of SSH command time-out during discovery in Service Mapping](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0621670)

</td></tr><tr><td>

A cluster CI appears detached from all CIs in map tiers above or below it.

</td><td>

[KB0621531: Resolving disconnected cluster CIs on the service instance map](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0621531)

</td></tr><tr><td>

-   The map displays either the load balancer configuration item \(CI\) with a warning icon or just the warning icon ![The Warning icon](../image/MapWarningIcon.png)
-   The following discovery message appears for the CI that is expected to be the load balancer in the service instance: `Failed to recognize application. See the discovery log for more details.`

</td><td>

[KB0621576: Resolving failure to discover VIP for a load balancer](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0621576)

</td></tr><tr><td>

The service instance map shows a different load balancer from the one you expected to see in this application service.

</td><td>

[KB0621616: Business service map displays a wrong load balancer in Service Mapping](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0621616)

</td></tr><tr><td>

-   The service instance map displays the warning icon \(![The Warning icon](../image/MapWarningIcon.png)\) on top or instead of the configuration item.
-   The following discovery message displays for the configuration item: `SSH command timed out on host`.


</td><td>

[KB0621670: Resolving the issue of SSH command time out during discovery in Service Mapping](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0621670)

</td></tr><tr><td>

-   The service instance map displays the warning icon \(![The Warning icon](../image/MapWarningIcon.png)\) on top or instead of the configuration item.
-   The following discovery message displays for the configuration item: `No active MID Server found for IP X.X.X.X.`


</td><td>

[KB0622808: Resolving a failure to find a MID Server for an IP address](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0622808)

</td></tr><tr><td>

-   The service instance map displays the warning icon \(![The Warning icon](../image/MapWarningIcon.png)\) on top or instead of the configuration item.
-   The following discovery message displays for the configuration item: `'64\rctrlx' is not recognized as an internal or external command, operable program or batch file.`


</td><td>

Perform the procedure described in [Upload the rctrlx.exe file to MID Servers](upload-rctrlx-file.md).

</td></tr><tr><td>

A CI or a segment of the map is grayed out after Service Mapping runs the top-down discovery on a previously mapped service instance.In this application service Service Mapping failed to rediscover the CI or connections leading to this CI.

</td><td>

Perform the following steps:1.  \(Optional for grayed out segments\) Identify the faulty CI that causes the segment to be grayed out.
2.  Use the discovery message associated with this faulty CI to resolve the problem.


</td></tr></tbody>
</table>5.  Click **Run Discovery**.


**Parent Topic:**[Fix errors in individual application service maps](fix-or-ignore-errors-business-service-map.md)

**Related topics**  


[Skip errors to continue discovering an application service](skip-errors-continue-discovery-individual-services.md)

[Resolve pattern-related mapping errors](t_TBSMapProcess.md)

