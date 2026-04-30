---
title: CIData - Global
description: The CIData script include is a utility class that provides methods for working with configuration item \(CI\) data structures in JavaScript.Creates an instance of the CIData class.Adds the specified related list to this instance.Converts the specified related list to a related list in a given sensor.Initializes the current CIData instance from the specified XML string.Gets the data map in the base CI record.Returns an array of data maps in the given many-to-many list \(to this CI\).Gets an array of maps of data in the given related list \(to this CI\).Returns the instance of CIRelatedList for the given list.Initializes this instance in preparation for loading a new CI.Loads the current data from a specified sys\_id.Converts the name of this CIData instance to a string.Returns an XML string containing a serialized version of this instance \(including any related lists\).
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CIData- Global

The CIData script include is a utility class that provides methods for working with configuration item \(CI\) data structures in JavaScript.

This script include requires the Discovery \(com.snc.discovery.core\) plugin. You can use it in any server-side Discovery script.

Instances of this class represent a CI \(both its base record and any related lists\), and the provided methods allow loading from or storing both the base record and related lists.

This class acts as a container for simple classes acting as maps of property name/value pairs. This class contains three kinds of such maps.

-   A single map representing the base CI table entry \(such as one row cmdb\_ci\_linux\_server and its superclasses\). You can retrieve this map using the [CIData - getData\(\)](c_CIDataAPI.md#) method.
-   Arrays of maps representing the instances of related lists, with each array representing a single related list and each element of such an array representing a single row of that related list. These arrays can be retrieved with the [CIData - getRelatedList\(String table, String refField\)](c_CIDataAPI.md#) method.
-   Arrays of maps representing the instances of many-to-many tables, with each array representing a single many-to-many table and each element of such an array representing a single row of that many-to-many table. These arrays can be retrieved with the [CIData - getM2MTable\(String table, String refField\)](c_CIDataAPI.md#) method.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CIData - CIData\(String debugFlag\)

Creates an instance of the CIData class.

<table id="table_sjx_wn1_rt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

debugFlag

</td><td>

String

</td><td>

Flag that indicates whether to enable debug logging.Valid values:

-   True: Debug logging is enabled.
-   False: Debug logging is not enabled.

</td></tr></tbody>
</table>This example creates and adds a related list to the CIData object.

```
var ciDataObj = new CIData();
var rl = new CIRelatedList('cmdb_serial_number', 'cmdb_ci');
var sr = {};
sr['serial_number_type'] = "bios";
sr['serial_number'] = "1BC5E4z89246";
sr['valid'] =  "true";
rl.addRec(sr);
ciDataObj.addRelatedList(rl);
```

## CIData - addRelatedList\(Array relatedList\)

Adds the specified related list to this instance.

|Name|Type|Description|
|----|----|-----------|
|relatedList|Array|Related list to add.|

|Type|Description|
|----|-----------|
|void| |

This example creates and adds a related list to the CIData object.

```
var ciDataObj = new CIData();
var rl = new CIRelatedList('cmdb_serial_number', 'cmdb_ci');
var sr = {};
sr['serial_number_type'] = "bios";
sr['serial_number'] = "1BC5E4z89246";
sr['valid'] =  "true";
rl.addRec(sr);
ciDataObj.addRelatedList(rl);
```

## CIData - convertRelatedList\(String sensor, String tableName, String refField, String keyName\)

Converts the specified related list to a related list in a given sensor.

|Name|Type|Description|
|----|----|-----------|
|sensor|String|The sensor|
|tableName|String|The table name|
|refField|String|The reference field|
|keyName|String|The key name|

|Type|Description|
|----|-----------|
|void| |

## CIData - fromXML\(String xml\)

Initializes the current CIData instance from the specified XML string.

|Name|Type|Description|
|----|----|-----------|
|xml|String|An XML string.|

|Type|Description|
|----|-----------|
|void| |

The following example shows how to get test XML-formatted CI Data collected during discovery.

```
var xmlCIData = '<CIData><data><fld name="cpu_name">Intel(R) Xeon(R) CPU E5-2686 v4 @ 2.30GHz</fld><fld name="host_name">ip-172-31-19-95</fld><fld name="kernel_release">3.10.0-1160.45.1.el7.x86_64</fld><fld name="os">Linux CentOS</fld></data></CIData>';

var ciData = new CIData();

ciData.fromXML(xmlCIData);
gs.log(ciData);
```

Output:

```
CIData instance:
  cpu_name: Intel(R) Xeon(R) CPU E5-2686 v4 @ 2.30GHz
  host_name: ip-172-31-19-95
  kernel_release: 3.10.0-1160.45.1.el7.x86_64
  os: Linux CentOS
[object Object]
```

## CIData - getData\(\)

Gets the data map in the base CI record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|The data map|

## CIData - getM2MTable\(String table, String refField\)

Returns an array of data maps in the given many-to-many list \(to this CI\).

|Name|Type|Description|
|----|----|-----------|
|table|String|Name of the table containing the related list. In the case of a many-to-many list, this is the name of the many-to-many table, not the target table.|
|refField|String|Name of the field in the related list that refers to this CI. In the case of a many-to-many list, this is the name of the referring field in the many-to-many table, not in the target table.|

<table id="table_rzb_hv1_rt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array

</td><td>

List of data maps in the given many-to-many list. The list is not in any particular order.If this is not a many-to-many list, returns an empty array.

</td></tr></tbody>
</table>This example shows how to get the many-to-many relationships for the installed\_on field of the cmdb\_software\_instance table.

```
function () {
  //Instantiate a new CIData class object
  var cdta = new CIData();

  //Load the current data from a CI record.
  cdta.loadFromCI('b4fd7c8437201000deeabfc8bcbe5dc1');

  // Returns an Array of Objects (records) of a given M2M related list
  var records = cdta.getM2MTable('cmdb_software_instance', 'installed_on');

  gs.info(JSON.stringify(records, null, 4));

})();
```

Output:

```
[
  {
    "sys_id": "208983661b3330106cdf0f26624bcb4b",
    "software": "46c1ec3ca9fe198100beafe77332be9a",
    "sys_updated_on": "2021-11-16 18:32:35",
    "sys_created_on": "2021-11-16 18:32:35",
    "name": "3D Groove Playback Engine-*ANNIE-IBM",
    "installed_on": "b4fd7c8437201000deeabfc8bcbe5dc1"
  },
  {
    "sys_id": "288983661b3330106cdf0f26624bcb4a",
    "software": "0c43bc5fc61122750182c13269a7a3ef",
    "sys_updated_on": "2021-11-16 18:32:35",
    "sys_created_on": "2021-11-16 18:32:35",
    "name": ".NET SDK 2003-*ANNIE-IBM",
    "installed_on": "b4fd7c8437201000deeabfc8bcbe5dc1"
  }
]
```

## CIData - getRelatedList\(String table, String refField\)

Gets an array of maps of data in the given related list \(to this CI\).

The array is not in any particular order. In the case of a many-to-many list, this will be an array of instances of the target table, not the many-to-many table. For example, given 'cmdb\_software\_instance' and 'installed\_on' \(a many-to-many table and the field that refers to a CI\), this method will return an array of maps representing cmdb\_ci\_spkg \(the target table\) instances.

|Name|Type|Description|
|----|----|-----------|
|table|String|Name of the table containing the related list. In the case of a many-to-many list, this is the name of the many-to-many table, not the target table.|
|refField|String|Name of the field in the related list that refers to this CI. In the case of a many-to-many list, this is the name of the referring field in the many-to-many table, not in the target table.|

|Type|Description|
|----|-----------|
|Array|An array of maps of data in the specified related list.|

## CIData - getRelatedListInstance\(String table, String refField\)

Returns the instance of CIRelatedList for the given list.

|Name|Type|Description|
|----|----|-----------|
|table|String|Name of the table containing the related list. In the case of a many-to-many list, this is the name of the many-to-many table, not the target table.|
|refField|String|Name of the field in the related list that refers to this CI. In the case of a many-to-many list, this is the name of the referring field in the many-to-many table, not in the target table.|

|Type|Description|
|----|-----------|
|Object|Instance of the `CIRelatedList` for the specified list.|

The following code example uses the getRelatedListInstance\(\) method to find the related list relationships to remove.

```
removeAllRelatedList: function(ci_id) {
  var cdta = new CIData('false');
  cdta.init();
  cdta.loadFromCI(ci_id); // Get a Computer CI Instance
  var cirelatedlist = cdta.getRelatedListInstance('cmdb_rel_ci', 'parent'); // Get the CIRelatedList instance holding all relationships of the above CI.
  cirelatedlist.remove(); // Remove all the CI Relationships
}
```

## CIData - init\(\)

Initializes this instance in preparation for loading a new CI.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var cdta = CIData('false');
cdta.init();
```

## CIData - loadFromCI\(String cmdb\_ci\)

Loads the current data from a specified sys\_id.

|Name|Type|Description|
|----|----|-----------|
|cmdb\_ci|String|The sys\_id of the CI|

|Type|Description|
|----|-----------|
|Object|The current data from the specified CI.|

```
var cdta = CIData('false');
cdta.init();
cdta.loadFromCI('ccaf9c0a8016400b98a06818d57c7');
```

## CIData - toString\(\)

Converts the name of this CIData instance to a string.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the instance|

This example loads the CIData from the current CI and converts this new CIData instance into string format.

```
var cidata = new CIData(); // Instantiate a new CIData class object
cidata.loadFromCI('0c43b0f5c6112275019abd2bb3dcd78f'); // Load the current data from a CI record. Use sys_id or ci name.
cidata.toString(); // Convert the name of this CIData instance to a string.
gs.info(cidata); // Display name value pairs of the current CI
```

Output:

```
CIData instance:
  sys_id: 0c43b0f5c6112275019abd2bb3dcd78f
  operational_status: 1
  os_service_pack: Service Pack 1
  cpu_manufacturer: 0c43b088c6112275011a4bd46a4e6cc4
  sys_updated_on: 2022-01-11 07:44:05
  discovery_source: Other Automated
  ram: 503
  cpu_speed: 1993
  sys_domain_path: /
  disk_space: 37.26
  cost_center: d9d07bddc0a80a647cf932056ed24652
  assigned: 2020-08-31 08:00:00
  cd_speed: -1
  can_print: 0
  sys_class_name: cmdb_ci_computer
  manufacturer: add7b97737e3100044e0bfc8bcbe5d96
  cpu_count: 1
  vendor: adb3d8ce37413000158bbfc8bcbe5d15
  assigned_to: 5137153cc611227c000bbd1bd8cd2007
  os_version: 5.1.2600
  cd_rom: 0
  unverified: 0
  asset: aac1ba8837f3100044e0bfc8bcbe5d3b
  skip_sync: 0
  sys_created_on: 2005-05-24 01:14:19
  sys_domain: global
  cpu_type: GenuineIntel
  install_date: 2020-05-19 07:00:00
  asset_tag: P1000143
  install_status: 1
  name: ANDREWDWXP
  subcategory: Computer
  virtual: 0
  sys_class_path: /!!/!2/!(
  company: 31bea3d53790200044e0bfc8bcbe5dec
  department: 221f3db5c6112284009f4becd3039cc9
  cost: 1299.99
  os: Windows XP Professional
  attestation_status: Not Yet Reviewed
  monitor: 0
  ip_address: 195.11.1.1
  cost_cc: USD
  location: db9a923c0a0a0a6501068d6eaec25ee0
  category: Hardware
  fault_count: 0
[object Object]

```

## CIData - toXML\(\)

Returns an XML string containing a serialized version of this instance \(including any related lists\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The XML string containing a serialized version of this instance and any related lists.|

```
var cdta = CIData();
cdta.toXML();
```

