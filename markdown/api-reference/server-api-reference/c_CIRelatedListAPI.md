---
title: CIRelatedList - Global
description: The CIRelatedList script include is a utility class that provides methods for working with configuration item \(CI\) related lists.Adds the specified record to the related list.Sets the given records to the related list.Appends an XML child to a field.Appends an XML child to a record.Checks to see if this is a SysCollection table. If it is, sets the target table name and reference field name.Checks to see if this is a Sys many-to-many table. If it is, sets the target table name and reference field name.Creates an instance of the CIRelatedList class. With no arguments, simply constructs an empty instance.Initializes this instance from the specified XML element.Populates the this.records field of this instance.Makes a string representation of this instance, pushing each line onto the end of the given result array.Serializes this instance to XML in the given document and &lt;rl&gt; element.Removes all the related list items.Converts a related list from XML to record format.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CIRelatedList- Global

The CIRelatedList script include is a utility class that provides methods for working with configuration item \(CI\) related lists.

Each instance of this script include contains the details of a single list that is related to a particular CI. The details of this list and the contents of the list are included.

Use with any server-side discovery script.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CIRelatedList - addRec\(Object record\)

Adds the specified record to the related list.

<table id="table_bzv_mlh_rt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

record

</td><td>

Object

</td><td>

Each member in the object is a column name in the associated table. For example, if referencing the cmdb\_serial\_number table this value may contain something similar to the following:`{"serial_number_type":"bios","serial_number":"1BC5E4z89246","valid":"true"}`

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example shows how to add a record to a CI related list.

```
var ciDataObj = new CIData(); // Instantiate a new CIData class object

// sys_id of the CI to which the related list is attached.
var rl = new CIRelatedList('cmdb_serial_number', 'cmdb_ci','0c43b0f5c6112275019abd2bb3dcd78f','true');

// Create an object and add the serial numbers
var sr = {"serial_number_type":"bios","serial_number":"1BC5E4z89246","valid":"true"};
rl.addRec(sr); // Add the related list. Sets the given records to the related list.
ciDataObj.addRelatedList(rl); // Adding the related list to the cidata
gs.info(JSON.stringify(rl, null, 4)); // Display the added related list
```

Output:

```
{
  "GlideRecordUtil": {},
  "ignoreFields": {
    "sys_created_by": true,
    "sys_updated_by": true,
    "sys_mod_count": true
  },
  "records": [
    {
      "serial_number_type": "bios",
      "serial_number": "1BC5E4z89246",
      "valid": "true"
    }
  ],
  "m2m_records": [],
  "table_name": "cmdb_serial_number",
  "field_name": "cmdb_ci",
  "cmdb_ci": "0c43b0f5c6112275019abd2bb3dcd78f",
  "debug_flag": "true",
  "isM2M": false,
  "target_table_name": null,
  "target_ref_field_name": null
}
```

## CIRelatedList - addRecs\(Array records\)

Sets the given records to the related list.

<table id="table_itb_wlh_rt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

records

</td><td>

Array of Objects

</td><td>

Each object represents a record in the associated table. Each member in the object is a column name in that table. For example, if referencing the cmdb\_serial\_number table this value may contain something similar to the following:`[{"serial_number_type":"bios","serial_number":"1BC5E4z89246","valid":"true"},{"serial_number_type":"baseboard","serial_number":"w4z89246","valid":"true"}]`

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example shows how to add multiple records to a CI related list.

```
var ciDataObj = new CIData(); // Instantiate a new CIData class object

// sys_id of the CI to which the related list is attached.
var rl = new CIRelatedList('cmdb_serial_number', 'cmdb_ci','0c43b0f5c6112275019abd2bb3dcd78f','true');

// Create an object and add the serial numbers
var sr = [{"serial_number_type":"bios","serial_number":"1BC5E4z89246","valid":"true"},{"serial_number_type":"baseboard","serial_number":"w4z89246","valid":"true"}];

rl.addRecs(sr); // Add the related list. Sets the given records to the related list.

ciDataObj.addRelatedList(rl); // Adding the related list to the cidata
gs.info(JSON.stringify(rl, null, 4)); // Display the added related list
```

Output:

```
{
  "GlideRecordUtil": {},
  "ignoreFields": {
    "sys_created_by": true,
    "sys_updated_by": true,
    "sys_mod_count": true
  },
  "records": [
    {
      "serial_number_type": "bios",
      "serial_number": "1BC5E4z89246",
      "valid": "true"
    },
    {
      "serial_number_type": "baseboard",
      "serial_number": "w4z89246",
      "valid": "true"
    }
  ],
  "m2m_records": [],
  "table_name": "cmdb_serial_number",
  "field_name": "cmdb_ci",
  "cmdb_ci": "0c43b0f5c6112275019abd2bb3dcd78f",
  "debug_flag": "true",
  "isM2M": false,
  "target_table_name": null,
  "target_ref_field_name": null
}
```

## CIRelatedList - appendXMLChildFld\(String parent, String name, String datum\)

Appends an XML child to a field.

|Name|Type|Description|
|----|----|-----------|
|parent|String|The parent element|
|name|String|The element name|
|datum|String|The data to append|

|Type|Description|
|----|-----------|
|void| |

## CIRelatedList - appendXMLChildRecord\(String parent, String name, String record\)

Appends an XML child to a record.

|Name|Type|Description|
|----|----|-----------|
|parent|String|The parent element|
|name|String|The element name|
|record|String|The record|

|Type|Description|
|----|-----------|
|void| |

## CIRelatedList - checkSysCollection\(\)

Checks to see if this is a SysCollection table. If it is, sets the target table name and reference field name.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|CIRelatedList|An instance of CIRelatedList for the specified list.|

## CIRelatedList - checkSysM2M\(\)

Checks to see if this is a Sys many-to-many table. If it is, sets the target table name and reference field name.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if it is a sys many-to-many table; otherwise, false.|

## CIRelatedList - CIRelatedList\(String table, String refField, String cmdb\_ci, String debugFlag\)

Creates an instance of the CIRelatedList class. With no arguments, simply constructs an empty instance.

|Name|Type|Description|
|----|----|-----------|
|table|String|The table containing the related list. If many-to-many, the many-to-many table.|
|refField|String|The reference field in the table for this related list.|
|cmdb\_ci|String|The sys\_id of the CI this list is related to.|
|debugFlag|String|If true, debug logging is enabled.|

## CIRelatedList - fromXML\(String element\)

Initializes this instance from the specified XML element.

|Name|Type|Description|
|----|----|-----------|
|element|String|An XML element|

|Type|Description|
|----|-----------|
|void| |

## CIRelatedList - populate\(\)

Populates the `this.records` field of this instance.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## CIRelatedList - toString\(Array result\)

Makes a string representation of this instance, pushing each line onto the end of the given result array.

This method is called from CIData.toString\(\), and assumes related list lines are to be indented two spaces.

|Name|Type|Description|
|----|----|-----------|
|result|Array|The result to convert|

|Type|Description|
|----|-----------|
|void| |

## CIRelatedList - toXML\(String document, String element\)

Serializes this instance to XML in the given document and &lt;rl&gt; element.

|Name|Type|Description|
|----|----|-----------|
|document|String|The document|
|element|String|The rl element|

|Type|Description|
|----|-----------|
|void| |

## CIRelatedList - remove\(\)

Removes all the related list items.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

This code example deletes the related records mapped with the CI items with the name = \*JEMPLOYEE-IBM. This example is for a non-M2M table.

```
//Get a configuration item record which has a related list. Example:  CI items with the name = *JEMPLOYEE-IBM.
var ciRecord = new GlideRecord("cmdb_ci_computer");
ciRecord.addQuery("name", "*JEMPLOYEE-IBM");
ciRecord.query();
if (ciRecord.next()) {

    var relRecordTable = 'cmdb_ci_network_adapter'; // The table containing the related list (if many-to-many, the many-to-many table)
    var relRecordField = 'cmdb_ci'; // The reference field in the table for this related list
    var cmdb_ciHasRelRecord = ciRecord.sys_id; // The sys_id of the CI this list is related to.
    var debugFlag = 'true'; // True if debug logging is enabled.

    // Get the related record List
    var CIRelatedList = new CIRelatedList(relRecordTable, relRecordField, cmdb_ciHasRelRecord, debugFlag);
    CIRelatedList.remove(); // Delete all related records
}
```

## CIRelatedList - xmlToRecord\(String records, String element\)

Converts a related list from XML to record format.

|Name|Type|Description|
|----|----|-----------|
|records|String|The record to create|
|element|String|The XML element|

|Type|Description|
|----|-----------|
|void| |

