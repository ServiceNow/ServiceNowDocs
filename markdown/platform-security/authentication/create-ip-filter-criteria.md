---
title: Create IP filter criteria
description: IP filter criteria allows you to filter users based on the user's IP addresses. You can configure an authentication policy to allow or deny access to a specific address or range of addresses.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [IP Filter, Filter criteria, Adaptive authentication, Authentication, Access Management]
---

# Create IP filter criteria

IP filter criteria allows you to filter users based on the user's IP addresses. You can configure an authentication policy to allow or deny access to a specific address or range of addresses.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **Filter Criteria** &gt; **IP Filter Criteria**.

2.  Click **New**.

3.  On the form, fill in these fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the IP network.|
    |Description|Short description of the IP network.|
    |Application|Scope of the application.|

    ![IP filter criteria form](../images/ip-filter-criteria.png "Example IP filter criteria record")

4.  Right-click the form header and click **Save**.

5.  From the **IP Range** tab, double-click **Insert a new row**.

    You can enter a single IP address or multiple ranges of IP addresses. For example, for a range of IP addresses enter `192.0.2.0` in the **Start IP** column and `192.0.2.255` in the **End IP** column.

    **Note:** For a single IP addresses, make sure that you enter the same IP address in the **Start IP** address and **End IP** columns. When you enter an IP address in the **Start IP** column, leave the **End IP** column blank and then save the record. The **End IP** column is auto-populated with the same **Start IP** address.

6.  From the **Subnet \(CIDR\)** tab, double-click **Insert a new row**.

    Enter the Network IP address and Netmask in the Classless Inter-Domain Routing \(CIDR\) format. For example, enter `255.255.255.0` as Network IP and `25` as Netmask.

    ![Sample Subnet in IP filter criteria](../images/subnet-ip-filter-sample.png)


