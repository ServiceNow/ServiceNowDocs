---
title: IPAddressFixup - Global
description: The IPAddressFixup script include provides methods that ensure that no other device has the same IP address, after a device has been successfully discovered. If any duplicates are found, the IP address field is cleared.Removes duplicates of the specified IP address in the specified table.Removes all duplicate IP addresses from the tables.Removes all duplicate IP addresses and ensures that the parent ip\_address record is set to one of the network interface card's \(NIC\) IP addresses.Returns the parent IP address for the current device.Sets the parent IP address field for the current CI.Ensures that the parent ip\_address record is set to one of the NIC's IP addresses, or leaves it alone if there were no NICs.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# IPAddressFixup- Global

The IPAddressFixup script include provides methods that ensure that no other device has the same IP address, after a device has been successfully discovered. If any duplicates are found, the IP address field is cleared.

Use with any server-side Discovery script to validate IP addresses.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## IPAddressFixup - dedupe\(String tableName, String ip\)

Removes duplicates of the specified IP address in the specified table.

After a device has been successfully discovered, you can use the dedupe\(\) method to remove the duplicate IP addresses for that device.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Table to check for duplicates.|
|ip|String|IP address to check for.|

|Type|Description|
|----|-----------|
|void| |

The following example shows how to use dedupe\(\) in a background script to remove duplicate IP addresses for the specified IP address within the cmdb\_ci\_hardware table.

```
var grDiscovery=new GlideRecord("discovery_device_history");
grDiscovery.addQuery('sys_id','<sys id of the record>'); // sys_id of the device discovery_device_history
grDiscovery.query();
if(grDiscovery.next())
  {
    var fx=new IPAddressFixup(grDiscovery.cmdb_ci); // Instantiate IPAddressFixup - pass cmdb reference 
    fx.dedupe('cmdb_ci_hardware','192.161.1.1'); // Pass the IP address and table which removes duplicates of the specified IP address in the specified table.
  }
```

The following example shows how to use dedupe\(\) in a business rule to remove duplicate IP addresses for the specified IP address within the cmdb\_ci\_hardware table.

```
(function executeRule(current, previous /*null when async*/) {

var cmdb_ci = current.cmdb_ci + '';
if (cmdb_ci) 
  {
    var ipf = new IPAddressFixup(cmdb_ci); // Instantiate IPAddressFixup - pass cmdb reference
    ipf.dedupe('cmdb_ci_hardware','168.128.1.1'); // Removes duplicates of the specified IP address in the specified table.
  }
})(current, previous);
```

## IPAddressFixup - dedupeAll\(\)

Removes all duplicate IP addresses from the tables.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

The following example shows how to use dedupeAll\(\) in a background script to remove all duplicate IP addresses.

```
var grDiscovery=new GlideRecord("discovery_device_history"); 
grDiscovery.addQuery('sys_id','<sys id of the record>'); // sys_id of the device discovery_device_history
grDiscovery.query();
if(grDiscovery.next())
{
  var fx=new IPAddressFixup(grDiscovery.cmdb_ci); // Call script include IPAddressFixup and pass cmdb reference
  fx.dedupeAll(); //Removes all duplicate IP addresses from the tables.
}
```

The following example shows how to use dedupeAll\(\) in a business rule to remove all duplicate IP addresses.

```
(function executeRule(current, previous /*null when async*/) {

var cmdb_ci = current.cmdb_ci + '';
if (cmdb_ci) 
{
  var ipf = new IPAddressFixup(cmdb_ci); //call script include IPAddressFixup and pass cmdb reference
  ipf.dedupeAll(); //Removes all duplicate IP addresses from the tables.
})(current, previous);
```

## IPAddressFixup - fix\(\)

Removes all duplicate IP addresses and ensures that the parent ip\_address record is set to one of the network interface card's \(NIC\) IP addresses.

After a device has been successfully discovered, you can use the dedupe\(\) method to remove the duplicate IP addresses for that device and set the parent ip\_address record value.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

The following example shows how to use fix\(\) in a background script to remove duplicate IP addresses and set the parent IP address.

```
var grDiscovery=new GlideRecord("discovery_device_history"); 
grDiscovery.addQuery('sys_id','<sys id of the the record>'); // sys_id of the device discovery_device_history
grDiscovery.query();
if(grDiscovery.next())
  {
    var fx=new IPAddressFixup(grDiscovery.cmdb_ci); // Instantiate IPAddressFixup - pass cmdb reference
    fx.fix(); // Remove all duplicate IP addresses and ensure that the parent ip_address record is set to one of the NIC's IP addresses.
  }
```

The following example shows how to use fix\(\) in a business rule to remove duplicate IP addresses and set the parent IP address.

```
(function executeRule(current, previous /*null when async*/) {

var cmdb_ci = current.cmdb_ci + '';
if (cmdb_ci) 
  {
    var ipf = new IPAddressFixup(cmdb_ci); // Instantiate IPAddressFixup - pass cmdb reference
    ipf.fix(); /// Remove all duplicate IP addresses and ensure that the parent ip_address record is set to one of the NIC's IP addresses.
  }
})(current, previous);
```

## IPAddressFixup - getParentIP\(\)

Returns the parent IP address for the current device.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Parent IP address|

The following example shows how to use getParentIP\(\) in a background script to obtain the parent IP address.

```
var grDiscovery=new GlideRecord("discovery_device_history"); // current.cmdb_ci can be used in case of Business rule on discovery_device_history table
grDiscovery.addQuery('sys_id','<sys id of the the record>'); // sys_id of the device discovery_device_history
grDiscovery.query();
if(grDiscovery.next())
  {
    var fx=new IPAddressFixup(grDiscovery.cmdb_ci); // Instantiate IPAddressFixup - pass cmdb reference
    gs.info(fx.getParentIP()); // Display the parent IP address of the device 
  }
```

Output:

```
172.21.12.11
```

The following example shows how to use getParentIP\(\) in a business rule to obtain the parent IP address.

```
((function executeRule(current, previous /*null when async*/) {

var cmdb_ci = current.cmdb_ci + '';
if (cmdb_ci) 
  {
    var ipf = new IPAddressFixup(cmdb_ci); // Instantiate IPAddressFixup - pass cmdb reference
    gs.log(ipf.getParentIP()); // Log the parent IP address of the device. Located in the system logs table 
  }
})(current, previous);
```

## IPAddressFixup - setParentIP\(String ip\)

Sets the parent IP address field for the current CI.

|Name|Type|Description|
|----|----|-----------|
|ip|String|Parent IP address for the current CI.|

|Type|Description|
|----|-----------|
|void| |

The following example shows how to use setParentIP\(\) in a background script to store the parent IP address.

```
var grDiscover=new GlideRecord("discovery_device_history"); 
grDiscover.addQuery('sys_id','a14e43b31bb4051070cb96c6b04bcb23'); // sys_id of the device in discovery_device_history table. Put your own sys_id here.
grDiscover.query();
if(grDiscover.next())
  {
    var fx=new IPAddressFixup(grDiscover.cmdb_ci); // Instantiate IPAddressFixup - pass cmdb reference.
    fx.setParentIP('197.111.1.1'); // Pass IP address to set as new IP on current mentioned CI.
  }
```

The following example shows how to use setParentIP\(\) in a business rule to store the parent IP address.

```
((function executeRule(current, previous /*null when async*/) {

var cmdb_ci = current.cmdb_ci + '';
if (cmdb_ci) 
  {
    var ipf = new IPAddressFixup(cmdb_ci); // Instantiate IPAddressFixup - pass cmdb reference
    fx.setParentIP('195.11.1.1'); // Set the new IP address of the CI 
  }
})(current, previous);
```

## IPAddressFixup - syncIP\(\)

Ensures that the parent ip\_address record is set to one of the NIC's IP addresses, or leaves it alone if there were no NICs.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

This shows an example of using the syncIP\(\) method in a background script.

```
var grDevHistory=new GlideRecord("discovery_device_history");
grDevHistory.addQuery('sys_id','a14e43b31bb4051070cb96c6b04bcb23'); // Sys_id of the device in discovery_device_history table. Put your own sys_id here.
grDevHistory.query();
if(grDevHistory.next())
  {
    var fx=new IPAddressFixup(grDevHistory.cmdb_ci); // Call the script include IPAddressFixup and pass cmdb reference
    fx.syncIP(); // Ensures that the parent ip_address record is set to one of the NIC's IP addresses, or leaves it alone if there were no NICs.
  }
```

This shows an example of using the syncIP\(\) method in a business rule.

```
(function executeRule(current, previous /*null when async*/) {

var cmdb_ci = current.cmdb_ci + '';
if (cmdb_ci) 
  {
    var ipf = new IPAddressFixup(cmdb_ci); // Call script include IPAddressFixup and pass cmdb reference
    ipf.syncIP(); // Ensures that the parent ip_address record is set to one of the NIC's IP addresses, or leaves it alone if there were no NICs.
  }
})(current, previous);

```

