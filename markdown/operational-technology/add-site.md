---
title: Add a Site
description: Add a site to your Discovery Console for OT.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Sites page, Use the Console pages, Discovery Console for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Add a Site

Add a site to your Discovery Console for OT.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to the Sites page.

2.  Select the add icon![](../../../../msi-console/image/add-icon-msi.jpg).

    The Site creation wizard opens.

3.  In the Identification section, enter a unique name for your site.

    **Note:** The site name must be unique across your Discovery Console instance. Use a descriptive name that clearly identifies the location. For example, "Seattle\_DataCenter" or "NYC\_Office\_Building\_A".

4.  Select **Next**.

5.  In the Address section, add the physical address to your site.

    This information helps identify the site's geographic location for organizational purposes.

6.  Select **Next**.

7.  In the Location section, specify the geographic coordinates using one of these methods:

    1.  Enter the latitude and longitude coordinates directly in the provided fields.

    2.  Click on the interactive map to automatically populate the coordinates.

8.  Select **Next**.

9.  In the Time Zone section, begin entering the zone name in the Search field to quickly filter available time zones.

    The Search filter displays all related Time Zones on the page.

10. Select the button next to the desired Time Zone, and then select **Next**.

11. In the **Network Ranges** option, select at least one range or a Network Zone that has at least one range.

    The Network Ranges configuration determines which IP addresses Discovery Console scans \(including\) and which it ignores during discovery operations for this site.

12. Add IP address ranges to scan:

    1.  Under Include, select the **Begin IP** field and select or enter the starting IP address.

    2.  Select the **End IP** field and select or enter the ending IP address.

    **Note:** The Console automatically prevents you from selecting the same IPs for both the Begin IP and End IP in both the Include and Ignore sections.

13. Add individual IP addresses to scan:

    1.  Under Include, select the **IP Address** field, enter a single IP address, and select the add IP address icon ![](../image/add-ip-address.png).

    2.  To add multiple IP Addresses at once, select the add multiple IP Addresses icon ![](../image/add-multiple.png), and enter or paste the IP addresses separated by commas.

        ![Add multiple IP addresses window](../image/multiple-ip-addresses-window.png)

14. Exclude or ignore IP address ranges to scan:

    1.  Under Ignore, select the **Begin IP** field, and select or enter the starting IP address.

    2.  Select the **End IP** field and select or enter the ending IP address.

15. Exclude or ignore individual IP addresses to scan:

    1.  Under Ignore, select the **IP Address** field, enter a single IP address, and select the Add IP Address icon ![](../image/add-ip-address.png).

    2.  To add multiple IP Addresses to ignore, select the Add Multiple IP Addresses icon ![](../image/add-multiple.png), and enter or paste the IP addresses separated by commas.

        **Note:** You cannot include and ignore the same IP address. If you attempt to do so, the system displays an error.

16. Include network zones:

    1.  Under Include, select the **Network Zone** field.

    2.  Select one of the Network Zones from the drop-down menu.

17. Exclude network zones:

    1.  Under Ignore Network Zones, select the **Ignore Network Zone** field.

    2.  Select one of the Network Zones from the drop-down menu.

    **Note:** The Discovery Console for OT automatically prevents conflicts. When you add a zone to the Include list, it becomes unavailable in the Ignore list, and vice versa. This ensures that each zone is assigned to only one list.

18. If you want to prevent overlapping IP address ranges, select the **Prevent Range Overlap** toggle.

    This option helps avoid configuration errors when multiple ranges are defined.

19. On the Sensors page, select Sensor by checking a box next to their name.

    You can select Sensors in the Allow and Deny sections; but do not select the same Sensor in both sections.

    ![Allow deny Sensors](../image/sensors-allow-deny-site.png)

    **Note:** Sensors are online when the circle next to their name is green. A yellow circle indicates Sensors that are offline.

20. After configuring network ranges and zones, review the summary of information.

21. Review all settings, and then select **Create Shared Site**.


## Result

The system creates the site and returns you to the Sites page where your new site appears in the list.

