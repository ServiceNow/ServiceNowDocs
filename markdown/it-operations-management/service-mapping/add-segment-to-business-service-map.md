---
title: Transfer a map segment into another application service
description: You can remove a branch of a service and place it into another application service, either new or existing. Transfer map segments to split large services or when you want to organize services differently from the initial mapping result.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Fine-tune application services to implement owner requests, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Transfer a map segment into another application service

You can remove a branch of a service and place it into another application service, either new or existing. Transfer map segments to split large services or when you want to organize services differently from the initial mapping result.

## Before you begin

You can edit discovered and manually created service instances.

**Important:** You cannot fine-tune or edit tag-based and dynamic services from the map.

Role required: service\_mapping\_admin

## About this task

When you transfer a map segment into another application service, you create a link between the original application service and the application service into which you planted the map segment. The connection to the top CI in the segment becomes an entry point when you transfer it into another, existing or new, application service.

The original service map shows the link to the other application service instead of the map segment. The service that contains the reference, becomes a dependent service. The service that appears as a reference is a contained service.

When you transfer a map segment into another application service, the information about the connection to the top CI in the transferred segment, is updated in the CMDB. If other application services use the same ingoing connection \(endpoint\), the CMDB recognizes it and replaces map segments coming out of the same connection with connected service CIs by analogy.

You can't insert links to multiple application services from the same connection.

If you use Event Management for service monitoring in your organization, dependent application services include alerts generated for their contained services.

## Procedure

1.  Open the application service map containing the segment that you want to transfer:

    1.  Navigate to **Service-Mapping** &gt; **Application Services**.

    2.  Click **View map** next to the relevant service instance.

    3.  Click **Edit** to be in Edit mode.

    4.  If the Host view is on, switch it off by clicking **More Options** and clicking the **Display in Host View** toggle.

        ![Click the More Options menu on the Map page.](../image/MapMoreOptionsHostButton.png)

2.  Identify the segment of the map that you want to transfer.

3.  Right-click the connection leading to the CI at the top of this segment.

    ![Selecting the connector leading into the map segment.](../image/TransferSegment.png)

4.  To transfer the segment into an existing application service map and connect to it:

    1.  Select **Connect to existing service**.

    2.  In the Add To Existing Discovered Service window, select the application service to which you want to transfer the segment.

    3.  Click **Choose**.

        The map displays the contained application service icon instead of the transferred segment. The application service map to which you transferred the segment, shows it under the newly added entry point. For example, the Tomcat application service map includes the Trade application service as its contained service. The Tomcat application service becomes dependent on the Trade service. The Trade application service map shows the segment transferred from the Tomcat application service.

        ![The map displaying connection to an existing service instance.](../image/TransferSegmentExistingBSResult.png)

5.  To transfer the segment into a new service instance map and connect to it:

    1.  Select **Create new service from here**.

    2.  In the Create New Discovered Service window, define attributes for the service instance that you want to create for this segment:

        |Field|Description|
        |-----|-----------|
        |Name|Enter the service instance name. This name must be unique. Use self-explanatory names such as `mailing service` or `printing service`.|
        |Group|\(Optional\) Restrict access to a service instance by adding it to an service instance group. Users must then have the service group role to access the service instance.|
        |Criticality|\(Optional\) Select the option that reflects how important this service instance is to your organization operation. For more information about service instance criticality, see [Define criticality for application services](define-criticality-for-business-services.md).|

    3.  Click **Create**.

        The map displays the contained application service icon instead of the transferred segment. The new application service appears in the list of application services and contains the transferred segment of the map. For example, the Tomcat application service includes the TP rooms service as its contained service. The Tomcat application service becomes a service dependent on the TP rooms service. The TP rooms application service map contains the segment transferred from the Tomcat application service.

        ![The map displaying the new service instance as a contained service.](../image/TransferSegmentNewBSResult.png)


## What to do next

To revert this operation:

1.  On the service instance map containing the connected service CI, click the connection leading to it.
2.  In the Properties pane, note the URL attribute of the connection.

    ![The Properties pane displaying the URL attribute of the connection.](../image/MapConnectedBSendPoint.png)

3.  Double-click the connected service CI.

    The service instance map for the CI containing the transferred segment opens.

4.  Click **Service Map Form**.
5.  Under Entry Points on the left, locate the entry point with the same URL you took note of.
6.  Click **Delete** on the entry point tab, and click **Remove** to confirm.

    This entry point disappears from this service instance form.

    The transferred segment disappears from the map of this service instance.

7.  Navigate to the map that contained the connected service CI.

    This map displays a boundary \(![Boundary icon](../image/MapBoundaryIcon.png)\) instead of the connected service CI.

8.  Click the boundary CI and click **Unmark boundary**.

    The map is refreshed and displays the segment of the service instance.


**Parent Topic:**[Fine-tune application services to implement owner requests](review-implement-business-service-maps.md)

**Related topics**  


[View dependent application services in classic Service Mapping](view-linked-services.md)

[View contained application services in classic Service Mapping](view-contained-services.md)

[Control user access to application services](control-user-access-to-business-services.md)

