---
title: IP address selection properties
description: You can use system properties to control the selection of IP address for specified configuration item \(CI\) classes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/r\_CIIPAddressSelection.html
release: zurich
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Discovery IP address configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# IP address selection properties

You can use system properties to control the selection of IP address for specified configuration item \(CI\) classes.

Use these properties to determine whether Discovery should replace the IP address in a device's CI record. Replacement occurs when the returned address doesn't match a network interface \(NIC\) on the device.

This matters for devices whose management IP differs from the IP addresses associated with one or more NICs. Because the management IP is used in the Discovery schedule, that is the address Discovery returns. Use these properties to determine which IP address to use for CIs of any class.

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
</table>