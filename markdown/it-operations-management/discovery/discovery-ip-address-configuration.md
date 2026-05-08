---
title: Discovery IP address configuration
description: Use one or more of these methods in any combination to define the network or network segment for Discovery to query. You can include or exclude specific IP ranges from your query.You can use system properties to control the selection of IP address for specified configuration item \(CI\) classes.Quick ranges allow administrators to define IP addresses to scan in a single comma-delimited string without creating separate records.One method of entering large numbers of IP networks into Discovery schedules is by using import sets.You can specify a range of IP addresses that you want to exclude from your Discovery query.Global Excludes List allows administrators to define global IP exclusions lists that work across Discovery schedules that discover configuration items, IP addresses, or networks. The list helps to prevent access to sensitive IPs as it blocks discovery when the IP is on the exclusion list. This feature is only applicable for Horizontal Discovery starting in the Rome release.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery IP address configuration

Use one or more of these methods in any combination to define the network or network segment for Discovery to query. You can include or exclude specific IP ranges from your query.

**Note:** If you do not know the IP addresses in the network, run [Network discovery](../concept/c_NetworkDiscovery.md#) first to determine the IP networks. Then, convert the IP networks into IP address range sets.

If you have integrations which populate sys\_metadata and sys\_update\_xml tables, make sure to clear the update and metadata records after the discovery\_range\_item or discovery\_range\_item\_ip import occurs.

**Important:** IPv6 addresses are not supported for IP address range or IP network.

There are three types of IP collections:

<table id="table_qqv_ll3_1y"><thead><tr><th>

IP collection type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

IP address list

</td><td>

Use IP address lists to add individual addresses to query. These addresses are not included in any existing IP range or IP network. You can enter the IP address of the device or a host name \(DNS name\). If you enter a host name, it must be mapped to an IP address.

</td></tr><tr><td>

IP address range

</td><td>

You can define arbitrary ranges of IP addresses to query. This process is a good way to include selected segments of a network or subnet. However, Discovery has no way of knowing if the IP range includes addresses for private networks or broadcast addresses, and scans all the addresses in the range. If the network and broadcast addresses are included, then the results are inaccurate. Discoveries configured to detect IP networks are more accurate than discoveries configured for IP address ranges. Only those IP addresses in your range that are reserved for manageable devices on the public network should be included.

 **Note:** To avoid performance issues, limit Discovery schedules to a maximum range of /16 \(approximately 65,536 IPs\). For better performance, consider splitting the range into smaller segments.

</td></tr><tr><td>

IP network

</td><td>

You can also scan an entire IP network. [An IP network](../concept/c_NetworkDiscovery.md#) includes the range of available IP addresses in that network. The scan also includes the network address \(the lowest address in the range\) and the broadcast address \(the highest address in the range\). After you [run network discovery](../concept/c_NetworkDiscovery.md#), [convert the IP networks that were found into range sets](../concept/c_NetworkDiscovery.md#)for use in discovering other devices.

 IP networks are represented in CIDR notation. Examples of CIDR notation include:

-   192.168.0.0/24
-   10.11.128.192/26

 Discovery will not scan the network or broadcast addresses for a network. The equivalent ranges for the two networks are:

-   192.168.0.1 – 192.168.254
-   10.11.128.193 – 10.11.128.254

 To avoid introducing errors from broadcast addresses, configure Discovery to exclude them by using IP network definitions in CIDR notation. Discovery automatically avoids scanning network and broadcast addresses when using IP networks.

 Including broadcast addresses in Discovery scans can lead to significant errors in the data, such as redundant or invalid device entries. By excluding broadcast addresses, Discovery helps prevent these errors.

 This built-in control makes IP networks the best method of defining which IP address ranges to query.

</td></tr></tbody>
</table>After you define your IP collections, you can use Discovery generic attributes to automatically set field values on CIs discovered within a schedule, range set, or IP address range. For example, you can assign different locations to CIs based on which IP range they were discovered in. For more information, see [Define CI field attributes](../task/define-ci-attributes.md).

## IP address selection properties

You can use system properties to control the selection of IP address for specified configuration item \(CI\) classes.

Use these properties to determine if the system should replace the IP address returned by Discovery in a device's CI record if the address does not match that of a network interface \(NIC\) on the device. This is important for the discovery of devices with management IP addresses that differ from IP addresses associated with one or more NICs on the device. Because a device's management IP is used in the Discovery schedule for that device, this is the address that Discovery returns. Use these properties to determine which IP address to use for CIs of any class.

<table id="table_pty_hpq_hhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.discovery.exclude\_ip\_sync\_classes

</td><td>

Defines CI classes whose IP addresses shouldn’t be substituted if the address returned by Discovery doesn’t match one of the devices' NICs. Use a comma-separated list to define multiple classes. By default, the system uses the management IP of a load balancer returned by Discovery in the CI record, rather than substituting it for the IP address of one of the load balancer's NICs.-   Type: string
-   Default value: cmdb\_ci\_lb

</td></tr><tr><td>

glide.discovery.enforce\_unique\_ips

</td><td>

Enforce unique IP addresses: Ignores the IP address after Discovery encounters subsequent devices that use the same IP address. Each time a computer, printer, or network gear with a valid IP address is discovered, any other devices with the same IP address have their IP address field cleared. If inactive, stores the IP address for each device.

 -   Type: true \| false
-   Default value false

</td></tr></tbody>
</table>**Note:** After you define your IP collections, you can use Discovery generic attributes to automatically set field values on CIs discovered within a schedule, range set, or IP address range. For example, you can assign different locations to CIs based on which IP range they were discovered in. For more information, see [Define CI field attributes](../task/define-ci-attributes.md).

## Create a Quick IP range for a Discovery schedule

Quick ranges allow administrators to define IP addresses to scan in a single comma-delimited string without creating separate records.

### Before you begin

Only MID Servers that are up and validated are used with quick ranges. The MID Servers must specify the Discovery application \(or ALL applications\) and have IP ranges configured if you use the auto-select feature on the [Discovery schedule](../task/t_CreateADiscoverySchedule.md#).

Role required: discovery\_admin

### About this task

You can enter IP addresses in one of the following formats:

-   An IP range defined by a slash and the number of bits in the subnetwork. For example, the string 10.10.10.0/24 scans 24 bits of IP addresses from 10.10.10.0 to 10.10.10.254.
-   An IP range defined by a dash. For example, the string 10.10.11.0-10.10.11.165 scans the IP addresses from 10.10.11.0 to 10.10.11.165.
-   A comma-separated list of specific IP addresses. For example, the string 10.0.2.1,10.0.2.15 scans the IP addresses 10.0.2.1 and 110.0.2.15.

**Note:** IPv6 address ranges and networks are not supported and will be ignored. Any other entries that cannot be interpreted will also be ignored.

### Procedure

1.  Click the **Quick Ranges** related link on the Discovery Schedule form.

2.  Enter the IP ranges and specific IP addresses to scan.

3.  Click **Make Ranges**.

    **Note:** The Quick Range interface is for entering IP addresses only and cannot be used to edit IP addresses that have already been submitted.

    ![Entering a quick range](../image/DiscoveryQuickRanges.png "Entering a quick range from a Discovery schedule")

    The instance automatically displays the entries in the proper format.

4.  For changes to IP address ranges, select the IP address records in the **Discovery Range Sets** related list.

    **Note:** Overriding behavior is not applicable on Discovery range sets.


## Import IP ranges into Discovery schedules with import sets

One method of entering large numbers of IP networks into Discovery schedules is by using import sets.

### Before you begin

Role required: discovery\_admin

### About this task

Common groups of IP addresses, known as [ranges](discovery-ip-address-configuration.md#) can be used in Advanced Discovery schedules.

**Note:** You can also use IPAM integration for entering large numbers of IP networks into Discovery schedules. See [IPAM Integration](../../cloud-management-v2/concept/IPAM-integration.md) for more information.

Use a data source that can be mapped. Include these fields:

-   Start IP: the first IP address in the range \(inclusive\).
-   End IP: the last IP address in the range \(inclusive\).

### Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Load Data**.

2.  Identify the file or data source that contains the desired information.

3.  Create a table name, such as `ipnetworks`.

4.  Select **Upload an Excel file** and browse to the source file.

5.  Click **Go** to import the file.

    ![Data Sources](../image/DataSource.png "Data Source")

6.  Navigate to **System Import Sets** &gt; **Create Transform Map** and map the items in the Excel spreadsheet to the fields of the CMDB in the target table IP Range `[ip_address_range]` table.

7.  Give the Transform Map a unique and descriptive name.

8.  Submit the form, and then click **New** in the **Field Maps** Related List.

9.  Map the fields from the Excel spreadsheet to the fields in the IP Range `[ip_address_range]` table.

    The fields you need values for are the **Start IP** and **End IP** addresses.

10. Click the **Mapping Assist** Related Link and use the lists that appear to resolve the fields between the table and the data source \(the Excel spreadsheet in this example\).

11. Click **Save**.

    The view returns to the Table Transform Map form.

12. Click **Transform** in the Related Links to move the data into the proper fields in the IP Range `[ip_address_range]` table.

    The imported IP ranges are available now for use in any advanced Discovery schedule.


## Exclude IP ranges from a Discovery range set

You can specify a range of IP addresses that you want to exclude from your Discovery query.

### Before you begin

Before a Discovery schedule is run, the number of excluded IP addresses is totaled. If there are more than 500,000 excluded IP addresses, the Discovery is cancelled and an error is logged through DiscoveryLogger regarding its status.

**Note:** Exclude IPs is not supported for IPv6 ranges or subnets.

Role required: discovery\_admin or agent\_admin

### Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Discovery Range Sets**.

2.  Select one of the range sets.

3.  Select one of the types from the **Discovery IP ranges** related list.

4.  Click **New** from the **Discovery Range Item Excludes** related list.

5.  Choose one of the following options from the **Type** drop-down list.

<table id="choicetable_vp2_g1m_dgc"><thead><tr><th align="left" id="d343435e927">

Option

</th><th align="left" id="d343435e930">

Description

</th></tr></thead><tbody><tr><td id="d343435e936">

**IP Address List**

</td><td>

Enables you to exclude non-consecutive IP addresses by listing individual IP addresses in the **Discovery Range Item IPs** related list.**Note:** After you select **IP Address List** as the **Type**, you must right-click the header and select **Save** before you can begin adding IPs to the related list.

</td></tr><tr><td id="d343435e959">

**IP Address Range**

</td><td>

Enables you to exclude a range of IPs by providing the starting and ending IP addresses.

</td></tr><tr><td id="d343435e968">

**IP Network**

</td><td>

Enables you to exclude an IP network by providing the Network IP and Network mask.

</td></tr></tbody>
</table>6.  Click **Submit**.


## Use Global Excludes List for IP addresses and ranges

Global Excludes List allows administrators to define global IP exclusions lists that work across Discovery schedules that discover configuration items, IP addresses, or networks. The list helps to prevent access to sensitive IPs as it blocks discovery when the IP is on the exclusion list. This feature is only applicable for Horizontal Discovery starting in the Rome release.

### Before you begin

Global IP exclude ranges are active by default. To deactivate, uncheck the **Active** check box. This makes the records inactive and the entries aren't excluded from Discovery. You can add a single IP or an IP range to the Global Excludes list. The IP exclusion list \[ip\_exclusion\] table references existing IP collection tables and supports three types of collections: IP address list, IP address subnet, and IP address range.

**Note:** Use of Global Excludes List for IP addresses and ranges is not supported for IPv6 addresses. While the UI still allows users to add IPv6 addresses to the list, these addresses get ignored and are skipped from the exclusion process during Discovery.

Role required: discovery\_admin or agent\_admin role

### Procedure

1.  Navigate to **All** &gt; **Global IP Exclusion** &gt; **IP Exclusion**.

2.  Click **New** to create a new IP exclusion record.

3.  In the IP Excluded box, click the search icon to bring up the IP collections window.

4.  Select one of the IP collections listed or click **New** to bring up the IP Collections wizard.

5.  From the IP Collections wizard, select one of the three types of collections you want to create and fill in the necessary details.

    For each type, you can add a description on why you want to exclude particular IPs or which IPs are excluded.

    -   IP Address Range

        Fill in the details and then click **Submit**. This new range is added to the IP Exclusion list.

    -   IP Address Subnet

        Fill in the details and then click **Submit**. This new subnet is added to the IP Exclusion list.

    -   IP Address List

        Enter the name and then **Save**. The related list then shows at the bottom of the page. From the collections list, pick an existing item or click **New** to create a new list. Click **Update**. Remember the name you created. This new name is added to the collection list. Select this name from the list and click **Submit** again. This address list is added to the IP Exclusion list.

6.  Navigate to **Discovery** &gt; **Discovery Schedules** and select a schedule.

7.  If the schedule is for discovering configuration items, IP addresses, or networks, you can view the Global IP Exclusion tab at the bottom of the page.


### Result

When the scheduled Discovery runs, it skips the discovery of all IPs that are part of the active Global IP Exclusion record. All the rest of the IPs should be discovered.

**Note:** Overriding behavior is not applicable when the Discovery schedule has active Global IP exclusions.

If you try to run a Quick Discovery that includes an excluded IP, you will see an error message and Discovery will not be triggered.

