---
title: IPAddress - Scoped, Global
description: The IPAddress API provides methods that enable you to check for various states of a specified IP address, such as whether it is routable, unicast, multicast, public, or reserved. It also enables you to get the canonical \(shortened/standard\) and expanded forms of an IP address.Instantiates an IPAddress object for the specified IP address.Returns the canonical \(shortened/standard\) form of the specified IP address by removing any zero padding from the address.Returns the expanded form of the specified IP addressDetermines whether the specified IPAddress object is a link-local IP address.Determines whether the specified IPAddress object is the loopback IP address.Determines whether the specified IPAddress object is a multicast IP address.Determines whether the specified IPAddress object is a public IP address. An IP address is considered public if it is routable, and it is not a reserved address.Determines whether the specified IPAddress object is a reserved IP address.Determines whether the specified IPAddress object is a routable IP address.Determines whether the passed IPAddress object is the is the same version, IPv4 or IPv6, as the specified IP address.Determines whether the specified IPAddress object is a unicast IP address.Determines whether the specified IP address is a valid IPv4 address.Determines whether the specified IP address is a valid IPv6 address.Determines whether the specified IP address is a valid IPv4 or IPv6 address.Returns the expanded form of an IPAddress object.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 14
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# IPAddress - Scoped, Global

The IPAddress API provides methods that enable you to check for various states of a specified IP address, such as whether it is routable, unicast, multicast, public, or reserved. It also enables you to get the canonical \(shortened/standard\) and expanded forms of an IP address.

Access the global IPAddress class and its associated methods in the `SNC` global namespace.

In this API, some of the methods are static and some are non-static. The [isV4\(\)](IPAddressAPIBoth.md#) and [isV6\(\)](IPAddressAPIBoth.md#) methods provide both static and non-static implementations. The benefit of the non-static methods is that you don't have to call the [IPAddress\(\)](IPAddressAPIBoth.md#) method to instantiate an IPAddress object.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## IPAddress - IPAddress\(String ipAddress\)

Instantiates an IPAddress object for the specified IP address.

|Name|Type|Description|
|----|----|-----------|
|ipAddress|String|IP address for which to create the IPAddress object.|

The following code example shows how to call the IPAddress constructor when calling a non-static IPAddress method.

```
function() {
  var grDiscover = new GlideRecord('discovery_range_item');
  grDiscover.get("SYS_ID");

  var ip = grDiscover.getValue('network_ip');
  var ip2 = gs.getSession().getClientIP().toString();
  gs.info("ip address 1: " + ip);
  gs.info("ip address 2: " + ip2);
  gs.info("ip address 1 is routable?: " + new SNC.IPAddress(ip).isRoutable());
  gs.info("ip address 2 is routable?: " + new SNC.IPAddress(ip2).isRoutable());
}
```

## IPAddress - canonicalize\(String ipAddress\)

Returns the canonical \(shortened/standard\) form of the specified IP address by removing any zero padding from the address.

For example, the canonical form of the IPv6 address "0000:0000:0000:0000:0000:0000:0000:0001" is "::1". The canonical form of the IPv4 address "192.168.001.002" is "192.268.1.2".

**Note:** This is a static method.

|Name|Type|Description|
|----|----|-----------|
|ipAddress|String or Object|IP address to canonicalize or a scoped IPAddress object that contains the IP address.|

|Type|Description|
|----|-----------|
|String|Canonicalized \(shortened/standardized\) IP address.|

The following example shows how to use the scoped version of this method to canonicalize an IPv6 IP address.

```
function() {
  var grCMDB = new GlideRecord('cmdb_ci');
  grCMDB.get("SYS_ID");
  var ip = grCMDB.getValue('ip_address');
  gs.info("ip address: " + ip);
  gs.info("canonicalized ip: " + SNC.IPAddress.canonicalize(ip));
}
```

Output:

```
ip address: 0000:0000:0000:0000:0000:0000:0000:0001
canonicalized ip: ::1
```

## IPAddress - getExpanded\(String ipAddress\)

Returns the expanded form of the specified IP address

For example, the expanded form of the IPv6 address "::1" is "0000:0000:0000:0000:0000:0000:0000:0001". The expanded form of the IPv4 address "192.268.1.2" is "192.168.001.002".

**Note:** This is a static method.

|Name|Type|Description|
|----|----|-----------|
|ipAddress|String|IP address to expand.|

|Type|Description|
|----|-----------|
|String|Expanded IP address.|

The following example shows how to use the scoped version of this method to expand an IPv6 IP address.

```
function() {
  var grCMDB = new GlideRecord('cmdb_ci');
  grCMDB.get(SYS_ID);
  var ip = grCMDB.getValue('ip_address');
  gs.info("ip address: " + ip);
  gs.info("expanded ip: " + SNC.IPAddress.getExpanded(ip));
}
```

Output:

```
ip address: ::1
expanded ip: 0000:0000:0000:0000:0000:0000:0000:0001
```

## IPAddress - isLinkLocal\(\)

Determines whether the specified IPAddress object is a link-local IP address.

For further information on link-local IP addresses see [RFC 3927](https://datatracker.ietf.org/doc/html/rfc3927) and [RFC 4291](https://datatracker.ietf.org/doc/html/rfc4291).

**Note:** This is a non-static method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_gyr_mg4_htb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the IP address object is a link-local address.

 Valid values:

-   true: IP address is a link-local address.
-   false: IP address is not a link-local address.

</td></tr></tbody>
</table>The following code example shows how to use the scoped version of this method to check if the IP addresses in a record in the Discovery IP Ranges \[discovery\_range\_item\] table are link-local addresses.

```
function() {
  var grDiscover = new GlideRecord('discovery_range_item');
  grDiscover.get("SYS_ID");

  var ip = grDiscover.getValue('network_ip');
  var start_ip = grDiscover.getValue('start_ip_address');
  gs.info("ip address 1: " + ip);
  gs.info("ip address 2: " + start_ip);
  gs.info("ip address 1 is link local?: " + new SNC.IPAddress(ip).isLinkLocal());
  gs.info("ip address 2 is link local?: " + new SNC.IPAddress(start_ip).isLinkLocal());
}
```

Output:

```
ip address 1: ::1
ip address 2: fe80:1::1
ip address 1 is link local?: false
ip address 2 is link local?: true
```

## IPAddress - isLocalhost\(\)

Determines whether the specified IPAddress object is the loopback IP address.

For additional information on the loopback IP address, see [IANA IPv4 Special-Purpose Address Registry](https://www.iana.org/assignments/iana-ipv4-special-registry/iana-ipv4-special-registry.xhtml) and [IANA IPv6 Special-Purpose Address Registry](https://www.iana.org/assignments/iana-ipv6-special-registry/iana-ipv6-special-registry.xml).

**Note:** This is a non-static method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_lgl_g3l_3tb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the IP address object is the loopback IP address.

 Valid values:

-   true: IP address is the loopback IP address.
-   false: IP address is not the loopback IP address.

</td></tr></tbody>
</table>The following code example shows how to use the scoped version of this method to check if the IP addresses in a record in the Discovery IP Ranges \[discovery\_range\_item\] table are the loopback IP address.

```
function() {
  var grDiscover = new GlideRecord('discovery_range_item');
  grDiscover.get("SYS_ID");
  var ip = grDiscover.getValue('network_ip');
  var start_ip = grDiscover.getValue('start_ip_address');
  gs.info("ip address 1: " + ip);
  gs.info("ip address 2: " + start_ip);
  gs.info("ip address 1 is localhost?: " + new SNC.IPAddress(ip).isLocalhost());
  gs.info("ip address 2 is localhost?: " + new SNC.IPAddress(ip2).isLocalhost());
}
```

Output:

```
ip address 1: 127.0.0.1
ip address 2: <current user's public IP Address>
ip address 1 is localhost?: true
ip address 2 is localhost?: false
```

## IPAddress - isMulticast\(\)

Determines whether the specified IPAddress object is a multicast IP address.

For further information on multicast IP addresses see [RFC 2365](https://datatracker.ietf.org/doc/html/rfc2365) and [RFC 3306](https://datatracker.ietf.org/doc/html/rfc3306).

**Note:** This is a non-static method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_rww_sh4_htb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the IP address object is a multicast address.

 Valid values:

-   true: IP address is a multicast address.
-   false: IP address is not a multicast address.

</td></tr></tbody>
</table>The following code example shows how to use the scoped version of this method to check if the IP addresses in a record in the Discovery IP Ranges \[discovery\_range\_item\] table are multicast addresses.

```
function() {
  var grDiscover = new GlideRecord('discovery_range_item');
  grDiscover.get("SYS_ID");
  var ip = grDiscover.getValue('network_ip');
  var start_ip = grDiscover.getValue('start_ip_address');
  gs.info("ip address 1: " + ip);
  gs.info("ip address 2: " + start_ip);
  gs.info("ip address 1 is multicast?: " + new SNC.IPAddress(ip).isMulticast());
  gs.info("ip address 2 is multicast?: " + new SNC.IPAddress(start_ip).isMulticast());
}
```

Output:

```
ip address 1: ::1
ip address 2: 224.0.0.22
ip address 1 is multicast?: false
ip address 2 is multicast?: true
```

## IPAddress - isPublic\(\)

Determines whether the specified IPAddress object is a public IP address. An IP address is considered public if it is routable, and it is not a reserved address.

**Note:** This is a non-static method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_m2f_22l_3tb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the IP address object is a public address.

 Valid values:

-   true: IP address is a public address.
-   false: IP address is not a public address.

</td></tr></tbody>
</table>The following code example shows how to use the scoped version of this method to check if the IP addresses in a record in the Discovery IP Ranges \[discovery\_range\_item\] table are public addresses.

```
function() {
  var grDiscover = new GlideRecord('discovery_range_item');
  grDiscover.get("SYS_ID");
  var ip = grDiscover.getValue('network_ip');
  var ip2 = gs.getSession().getClientIP().toString();
  gs.info("ip address 1: " + ip);
  gs.info("ip address 2: " + ip2);
  gs.info("ip address 1 is public?: " + new SNC.IPAddress(ip).isPublic());
  gs.info("ip address 2 is public?: " + new SNC.IPAddress(ip2).isPublic());
}
```

Output:

```
ip address 1: 2001:1::1
ip address 2: <current user's public IP Address>
ip address 1 is public?: false
ip address 2 is public?: true
```

## IPAddress - isReserved\(\)

Determines whether the specified IPAddress object is a reserved IP address.

For additional information on reserved IP addresses, see [IANA IPv4 Special-Purpose Address Registry](https://www.iana.org/assignments/iana-ipv4-special-registry/iana-ipv4-special-registry.xhtml) and [IANA IPv6 Special-Purpose Address Registry](https://www.iana.org/assignments/iana-ipv6-special-registry/iana-ipv6-special-registry.xml).

**Note:** This is a non-static method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_mpw_ffl_3tb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the IP address object is a reserved address.

 Valid values:

-   true: IP address is a reserved address.
-   false: IP address is not a reserved address.

</td></tr></tbody>
</table>The following code example shows how to use the scoped version of this method to check if the IP addresses in a record in the Discovery IP Ranges \[discovery\_range\_item\] table are reserved addresses.

```
function() {
  var grDiscover = new GlideRecord('discovery_range_item');
  grDiscover.get("SYS_ID");
  var ip = grDiscover.getValue('network_ip');
  var ip2 = gs.getSession().getClientIP().toString();
  gs.info("ip address 1: " + ip);
  gs.info("ip address 2: " + ip2);
  gs.info("ip address 1 is reserved?: " + new SNC.IPAddress(ip).isReserved());
  gs.info("ip address 2 is reserved?: " + new SNC.IPAddress(ip2).isReserved());
}
```

Output:

```
ip address 1: 2001:1::1
ip address 2: <current user's public IP Address>
ip address 1 is reserved?: true
ip address 2 is reserved?: false
```

## IPAddress - isRoutable\(\)

Determines whether the specified IPAddress object is a routable IP address.

An IP Address is considered to be routable if it is not a private address, a link-local address, or the loopback address. For additional information on private addresses, see [RFC 1918](https://datatracker.ietf.org/doc/html/rfc1918) and [RFC 4193](https://datatracker.ietf.org/doc/html/rfc4193).

**Note:** This is a non-static method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_qv3_m34_htb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the IP address object is a routable address.

 Valid values:

-   true: IP address is a routable address.
-   false: IP address is not a routable address.

</td></tr></tbody>
</table>The following code example shows how to use the scoped version of this method to check if the IP addresses in a record in the Discovery IP Ranges \[discovery\_range\_item\] table are routable addresses.

```
function() {
  var grDiscover = new GlideRecord('discovery_range_item');
  grDiscover.get("SYS_ID");
  var ip = grDiscover.getValue('network_ip');
  var ip2 = gs.getSession().getClientIP().toString();
  gs.info("ip address 1: " + ip);
  gs.info("ip address 2: " + ip2);
  gs.info("ip address 1 is routable?: " + new SNC.IPAddress(ip).isRoutable());
  gs.info("ip address 2 is routable?: " + new SNC.IPAddress(ip2).isRoutable());
}
```

Output:

```
ip address 1: ::1
ip address 2: <current user's public IP Address>
ip address 1 is routable?: false
ip address 2 is routable?: true
```

## IPAddress - isSameVersionAs\(String ipAddress\)

Determines whether the passed IPAddress object is the is the same version, IPv4 or IPv6, as the specified IP address.

**Note:** This is a non-static method.

|Name|Type|Description|
|----|----|-----------|
|ipAddress|String|IP address to check against the IP address in the passed IPAddress object.|

<table id="table_y2x_4f4_htb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the specified IP address is the same version as that in the IPAddress object.

 Valid values:

-   true: IP address version is the same.
-   false: IP address version is different.

</td></tr></tbody>
</table>The following code example shows how to use the scoped version of this method to compare whether various IP address are the same version \(IPv4 or IPv6\).

```
function() {
  var grDiscover = new GlideRecord('discovery_range_item');
  grDiscover.get("SYS_ID");
  var ip = grDiscover.getValue('network_ip');
  var start_ip = grDiscover.getValue('start_ip_address');
  var end_ip = grDiscover.getValue('end_ip_address');
  gs.info("ip address 1: "+ ip);
  gs.info("ip address 2: " + start_ip);
  gs.info("ip address 3: " + end_ip);
  var ip1 = new SNC.IPAddress(ip);
  var ip2 = new SNC.IPAddress(start_ip);
  var ip3 = new SNC.IPAddress(end_ip);
  gs.info("ip address 1 is same version as ip address 2?: " + ip1.isSameVersionAs(ip2));
  gs.info("ip address 1 is same version as itself?: " + ip1.isSameVersionAs(ip1));
  gs.info("ip address 2 is same version as ip address 3?: " + ip2.isSameVersionAs(ip3));
}
```

Output:

```
ip address 1: 192.168.0.1
ip address 2: ::2
ip address 3: ::3
ip address 1 is same version as ip address 2?: false
ip address 1 is same version as itself?: true
ip address 2 is same version as ip address 3?: true
```

## IPAddress - isUnicast\(\)

Determines whether the specified IPAddress object is a unicast IP address.

A unicast address is effectively an address that is not multicast.

**Note:** This is a non-static method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_al3_bhl_3tb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the IP address object is a unicast address.

 Valid values:

-   true: IP address is a unicast address.
-   false: IP address is not a unicast address.

</td></tr></tbody>
</table>The following code example shows how to use the scoped version of this method to check if the IP addresses in a record in the Discovery IP Ranges \[discovery\_range\_item\] table are unicast addresses.

```
function() {
  var grDiscover = new GlideRecord('discovery_range_item');
  grDiscover.get("SYS_ID");
  var ip = grDiscover.getValue('network_ip');
  var start_ip = grDiscover.getValue('start_ip_address');
  gs.info("ip address 1: " + ip);
  gs.info("ip address 2: " + start_ip);
  gs.info("ip address 1 is unicast?: " + new SNC.IPAddress(ip).isUnicast());
  gs.info("ip address 2 is unicast?: " + new SNC.IPAddress(ip2).isUnicast());
}
```

Output:

```
ip address 1: 224.0.0.22
ip address 2: <current user's public IP Address>
ip address 1 is unicast?: false
ip address 2 is unicast?: true
```

## IPAddress - isV4\(String ipAddress\)

Determines whether the specified IP address is a valid IPv4 address.

This method has both static and non-static implementations. The way in which you call the two method types is slightly different. For the non-static implementation you don't need to first instantiate an IPAddress object and you pass the IP address in the IPAddress class reference. Both return the same response.

<table id="table_hrb_3gn_htb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ipAddress

</td><td>

String

</td><td>

IP address to validate.For the non-static implementation, the IP address is passed in the IPAddress class reference instead of the method call.

 For example `New SNC.IPAddress("::1").isV4();`.

</td></tr></tbody>
</table><table id="table_irb_3gn_htb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the specified IP address is a valid IPv4 address.

 Valid values:

-   true: IP address is valid.
-   false: IP address is invalid.

</td></tr></tbody>
</table>The following example shows how to use the scoped static version of this method to verify whether IP addresses in a record in the Discovery IP Ranges \[discovery\_range\_item\] table are valid IPv4 addresses.

```
function() {
  var grDiscover = new GlideRecord('discovery_range_item');
  grDiscover.get("SYS_ID");
  var ip = grDiscover.getValue('network_ip');
  var start_ip = grDiscover.getValue('start_ip_address');
  gs.info("ip address 1: " + ip);
  gs.info("ip address 2: " + start_ip);
  gs.info("ip address 1 is v4?: " + SNC.IPAddress.isV4(ip));
  gs.info(("ip address 2 is v4?: " + SNC.IPAddress.isV4(start_ip));
}
```

Output:

```
ip address 1: 192.168.0.1
ip address 2: ::2
ip address 1 is v4?: true
ip address 2 is v4?: false
```

The following example shows how to use the non-static version of this method to verify whether IP addresses in a record in the Discovery IP Ranges \[discovery\_range\_item\] table are valid IPv4 addresses.

```
function() {
  var grDiscover = new GlideRecord('discovery_range_item');
  grDiscover.get("SYS_ID");
  var ip = grDiscover.getValue('network_ip');
  var start_ip = grDiscover.getValue('start_ip_address');
  gs.info("ip address 1: " + ip);
  gs.info("ip address 2: " + start_ip);
  gs.info("ip address 1 is v4?: " + new SNC.IPAddress(ip).isV4());
  gs.info("ip address 2 is v4?: " + new SNC.IPAddress(start_ip).isV4());
}
```

Output:

```
ip address 1: 192.168.0.1
ip address 2: ::2
ip address 1 is v4?: true
ip address 2 is v4?: false
```

## IPAddress - isV6\(String ipAddress\)

Determines whether the specified IP address is a valid IPv6 address.

This method has both static and non-static implementations. The way in which you call the two method types is slightly different. For the non-static implementation you don't need to first instantiate an IPAddress object and you pass the IP address in the IPAddress class reference. Both return the same response.

<table id="table_nkk_sgn_htb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ipAddress

</td><td>

String

</td><td>

IP address to validate. For the non-static implementation, the IP address is passed in the IPAddress class reference instead of the method call.

 For example `New SNC.IPAddress("::1").isV6();`.

</td></tr></tbody>
</table><table id="table_okk_sgn_htb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the specified IP address is a valid IPv6 address.

 Valid values:

-   true: IP address is valid.
-   false: IP address is invalid.

</td></tr></tbody>
</table>The following example shows how to use the scoped static version of this method to verify whether IP addresses in a record in the Discovery IP Ranges \[discovery\_range\_item\] table are valid IPv6 addresses.

```
function() {
  var grDiscover = new GlideRecord('discovery_range_item');
  grDiscover.get(SYS_ID);
  var ip = grDiscover.getValue('network_ip');
  var start_ip = grDiscover.getValue('start_ip_address');
  gs.info("ip address 1: " + ip);
  gs.info("ip address 2: " + start_ip);
  gs.info("ip address 1 is v6?: " + SNC.IPAddress.isV6(ip));
  gs.info(("ip address 2 is v6?: " + SNC.IPAddress.isV6(start_ip));
}
```

Output:

```
ip address 1: 192.168.0.1
ip address 2: ::2
ip address 1 is v6?: false
ip address 2 is v6?: true
```

The following example shows how to use the scoped non-static version of this method to verify whether IP addresses in a record in the Discovery IP Ranges \[discovery\_range\_item\] table are valid IPv6 addresses.

```
function() {
  var grDiscover = new GlideRecord('discovery_range_item');
  grDiscover.get("SYS_ID");

  var ip = grDiscover.getValue('network_ip');
  var start_ip = grDiscover.getValue('start_ip_address');
  gs.info("ip address 1: " + ip);
  gs.info("ip address 2: " + start_ip);

  gs.info("ip address 1 is v6?: " + new SNC.IPAddress(ip).isV6());
  gs.info("ip address 2 is v6?: " + new SNC.IPAddress(start_ip).isV6());

}
```

Output:

```
ip address 1: 192.168.0.1
ip address 2: ::1
ip address 1 is v6?: false
ip address 2 is v6?: true
```

## IPAddress - isValid\(String ipAddress\)

Determines whether the specified IP address is a valid IPv4 or IPv6 address.

**Note:** This is a static method.

|Name|Type|Description|
|----|----|-----------|
|ipAddress|String|IP address to validate.|

<table id="table_pnf_mcn_htb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the specified IP address is a valid IPv4 or IPv6 address.

 Valid values:

-   true: IP address is valid.
-   false: IP address is invalid.

</td></tr></tbody>
</table>The following code example shows how to use the scoped version of this method to check if the IP address in a record within the Configuration Items \[cmdb\_ci\] is valid.

```
function() {
  var grCMDB = new GlideRecord('cmdb_ci');
  grCMDB.get("SYS_ID");
  var ip = grCMDB.getValue('ip_address');
  gs.info("ip address: " + ip)
  var ipAddress = new SNC.IPAddress(ip);
  gs.info("ip is valid?: " + ipAddress.isValid())
}
```

Output:

```
ip address: 127.0.0.1
ip is valid?: true
```

## IPAddress - toExpanded\(\)

Returns the expanded form of an IPAddress object.

**Note:** This is a non-static method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Expanded IP address.|

The following example shows how to use the scoped version of this method to expand an IPv6 IP address.

```
function() {
  var grDiscover = new GlideRecord('cmdb_ci');
  grDiscover.get("SYS_ID");
  var ip = grDiscover.getValue('ip_address');
  gs.info("ip address: " + ip);
  gs.info("expanded ip address: " + new SNC.IPAddress(ip).toExpanded());
}
```

Output:

```
ip address: 2001:41::1
expanded ip address: 2001:0041:0000:0000:0000:0000:0000:0001
```

