---
title: Create an Auto Query ignore list
description: Create an Auto Query to exclude specified asset IP addresses from receiving scanning traffic.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Auto Query page, Use the Console pages, Discovery Console for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Create an Auto Query ignore list

Create an Auto Query to exclude specified asset IP addresses from receiving scanning traffic.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to the Auto Query page.

2.  Select the add icon ![](../../../../msi-console/image/add-icon-msi.jpg).

3.  In the Identification section, add the Auto Query name in the **Auto Query Name** field or use the generated name.

4.  Select **Next**

5.  In the Assets section, select the desired assets and targets.

    The Assets section displays a choice of All Assets, New Assets Only, Incremental, Asset Discovery, and Asset Discovery &amp; Query.

    When the Query is set to use **All Assets**, then the Assets that are marked as ignored, are excluded from the list of targets.

    The Targets section lists All Sensors, Specific Sensors, and Auto Targeting.

6.  Select **Next**

7.  Specify any filters in the Filters selection.

    You can specify Sites, Ports, Ethernet Vendors, Brands, Inbound and Outbound Protocols, Networks, Ignore Networks, and Hostnames.

8.  To create the ignore list, select the Ignore Networks filter.

    -   To ignore an IP Address Range, enter an IP Range in the IP Address Range section, and select the add icon ![Add IP](../image/add-ip-address.png).
    -   To ignore one individual IP address, enter an IP address in the Ignore IP Address section.
    -   To ignore multiple IP addresses, select the multiple selection icon ![Add Multiple IPs](../image/add-multiIP-icon.png) in the Ignore IP Address section, and use commas to separate the entries.
    ![Displaying selections](../image/ignore-list.png)

9.  Select **Next**

10. In the Query Types section, select as many types needed from one or both the Simplified Query list or the Advanced Query list.

11. In the Classification section, if you choose to, you can select from the following.

    -   **Console Hostname Look up**: Attempts to determine an Asset's hostname based on its IP address.
    -   **Location**: Sets a label and the location field with Site name.
    -   **Unknown**: Marks the Asset brand and category Unknown.
12. Select **Next**

13. In the **Confirmation** section, set the schedule, recursion, and duration.

    ![Confirmation settings](../../../images/auto-query-confirmation.png)

14. Select the **Create Auto Query** button to create the Auto Query ignore list.


## Result

The Auto Query results are added to the Auto Query page. The **Ignored** column displays the number of IP addresses that were ignored.

![Number of ignored IP addresses](../../../images/auto-query-ignore-columns.png)

