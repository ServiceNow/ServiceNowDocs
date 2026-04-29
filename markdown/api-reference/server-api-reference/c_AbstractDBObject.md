---
title: AbstractDBObject - Global
description: The AbstractDBObject script include provides common methods for classes based on records in the database.Determines if the current database record is valid.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# AbstractDBObject- Global

The AbstractDBObject script include provides common methods for classes based on records in the database.

Use this script include as a base class to create your own database object class.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## AbstractDBObject - isValid\(\)

Determines if the current database record is valid.

See also [IPService - Global](../../IPService/concept/c_IPServiceAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_bxq_zpc_pt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

True if the database record is valid, false otherwise.Flag that indicates whether the database record is valid.

 Valid values:

-   true: The database record is valid.
-   false: The database record is invalid.

</td></tr></tbody>
</table>The following example shows how to get a list of valid instances using the IPService\(\) class from the IP Services \[cmdb\_ip\_service\] table. The IPService class extends the AbstractDBObject\(\) class.

```
/**
 * IPService class Encapsulates the notion of an IP Service. Instances in which isValid() returns true have the 
 * following properties initialized: 
 *  sysID:       sys_id of this record
 *  port:        the TCP or UDP port used by the service
 *  protocol:    protocol used by the service ("UDP", "TCP", or "TCP/UDP")
 *  name:        short name or handle
 *  serviceName: long, descriptive English name
 *  creates:     table that this service creates entries in
 *  description: description
 */

var result = [];
// Array of sys_id's from the IP Service class which we want to get the abstract details
var list = ['db9840e10ab3015500f5e3fe8f78da42', 'a1505ebc7782330099808d1168106179', 'abc05ebc7782330099808d1168106112'];

// query for the records on the list
var ipservice = new GlideRecord('cmdb_ip_service');
ipservice.addQuery('sys_id', 'IN', list.toString());
ipservice.query();
while (ipservice.next()) {
    var ip = new IPService(ipservice); // IPService class extends AbstractDBObject class and this class 
    if (ip.isValid())      // check whether the record is valid or not
        result.push(ip);   // if valid get the properties for 
}

gs.info(JSON.stringify(result, null, 2));
```

Output:

```
[
  {
    "valid": true,
    "sysID": "a1505ebc7782330099808d1168106179",
    "port": "8882",
    "protocol": "TCP",
    "name": "blkbry-uem-enroll",
    "serviceName": "Blackberry Enrollment Request",
    "creates": null,
    "description": null
  },
  {
    "valid": true,
    "sysID": "db9840e10ab3015500f5e3fe8f78da42",
    "port": "548",
    "protocol": "TCP",
    "name": "afp",
    "serviceName": "Apple File Protocol",
    "creates": null,
    "description": null
  }
]
```

