---
title: CimCIData - Global
description: The CimCIData script include provides a wrapper for Common Information Model \(CIM\) configuration item \(CI\) data manipulation.Adds a serial number to the current configuration item \(CI\), by type.Creates a new serial record.Sets the make and model for the current configuration item \(CI\).
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CimCIData- Global

The CimCIData script include provides a wrapper for Common Information Model \(CIM\) configuration item \(CI\) data manipulation.

Use with any server-side discovery script.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CimCIData - addSerial\(String type, String serial\)

Adds a serial number to the current configuration item \(CI\), by type.

|Name|Type|Description|
|----|----|-----------|
|type|String|Serial number type. For the base system, use the CimCIData.serialType enum.|
|serial|String|Serial number to add.|

|Type|Description|
|----|-----------|
|String|Current CI|

The following example loads the CI data from current CI and passes the data object to the CimCIData.addSerial\(\) method which adds the serial number to CimCIData and CIData.

```
var cidata = new CIData();  //Instantiate a new CIData class object
cidata.loadFromCI('0c43b0f5c6112275019abd2bb3dcd78f');  // Load the current data from a CI record. use sys_id or ci name
var cimcidata = new CimCIData(cidata);  // Instantiate a new CimCIData class object and pass the CIdata 
var cimdata = cimcidata.addSerial('baseboard','XK0HKSN6');  // Add serial number to the CIData and CimCIData
gs.info(JSON.stringify(cimdata, null ,4));  // The JSON payload in string format with added serial number and serial number type
gs.info("serial number : "+cimdata.serials.records[1].serial_number);  // Display serial number which is added
gs.info("serial type : "+ cimdata.serials.records[1].serial_number_type);  // Display serial type which is added
```

Output:

```
{
  "cidata": {
    "ignoreFields": {
      "sys_created_by": true,
      "sys_updated_by": true,
      "sys_mod_count": true
    },
    "GlideRecordUtil": {},
      "debug_flag": false,
      "data": {
        "sys_id": "0c43b0f5c6112275019abd2bb3dcd78f",
        "operational_status": "1",
        "os_service_pack": "Service Pack 1",
        "cpu_manufacturer": "0c43b088c6112275011a4bd46a4e6cc4",
        "sys_updated_on": "2021-07-05 18:03:59",
        "discovery_source": "Other Automated",
        "ram": "503",
        "cpu_speed": "1993",
        "sys_domain_path": "/",
        "disk_space": "37.26",
        "cost_center": "d9d07bddc0a80a647cf932056ed24652",
        "assigned": "2020-08-31 08:00:00",
        "cd_speed": "-1",
        "can_print": "0",
        "sys_class_name": "cmdb_ci_computer",
        "manufacturer": "add7b97737e3100044e0bfc8bcbe5d96",
        "cpu_count": "1",
        "vendor": "adb3d8ce37413000158bbfc8bcbe5d15",
        "assigned_to": "5137153cc611227c000bbd1bd8cd2007",
        "os_version": "5.1.2600",
        "cd_rom": "0",
        "unverified": "0",
        "asset": "aac1ba8837f3100044e0bfc8bcbe5d3b",
        "skip_sync": "0",
        "sys_created_on": "2005-05-24 01:14:19",
        "sys_domain": "global",
        "cpu_type": "GenuineIntel",
        "install_date": "2020-05-19 07:00:00",
        "asset_tag": "P1000143",
        "install_status": "1",
        "name": "ANDREWDWXP",
        "subcategory": "Computer",
        "virtual": "0",
        "sys_class_path": "/!!/!2/!(",
        "company": "31bea3d53790200044e0bfc8bcbe5dec",
        "department": "221f3db5c6112284009f4becd3039cc9",
        "cost": "1299.99",
        "os": "Windows XP Professional",
        "monitor": "0",
        "model_id": "0c43b0c6c611227501522de2b64679ac",
        "cost_cc": "USD",
        "location": "db9a923c0a0a0a6501068d6eaec25ee0",
        "category": "Hardware",
        "fault_count": "0",
        "serial_number": "XK0HKSN6"
      },
      "rl_map": {
        "cmdb_serial_number:cmdb_ci": {
          "GlideRecordUtil": {},
          "ignoreFields": {
            "sys_created_by": true,
            "sys_updated_by": true,
            "sys_mod_count": true
          },
          "records": [
            {
              "serial_number_type": "baseboard",
              "serial_number": "XK0HKSN6",
              "valid": true
            }
          ],
          "m2m_records": [],
          "table_name": "cmdb_serial_number",
          "field_name": "cmdb_ci",
          "cmdb_ci": "ANDREWDWXP",
          "debug_flag": false,
          "isM2M": false,
          "target_table_name": null,
          "target_ref_field_name": null
        }
      },
      "cmdb_ci": "ANDREWDWXP",
      "related": {}
    },
    "data": {
      "sys_id": "0c43b0f5c6112275019abd2bb3dcd78f",
      "operational_status": "1",
      "os_service_pack": "Service Pack 1",
      "cpu_manufacturer": "0c43b088c6112275011a4bd46a4e6cc4",
      "sys_updated_on": "2021-07-05 18:03:59",
      "discovery_source": "Other Automated",
      "ram": "503",
      "cpu_speed": "1993",
      "sys_domain_path": "/",
      "disk_space": "37.26",
      "cost_center": "d9d07bddc0a80a647cf932056ed24652",
      "assigned": "2020-08-31 08:00:00",
      "cd_speed": "-1",
      "can_print": "0",
      "sys_class_name": "cmdb_ci_computer",
      "manufacturer": "add7b97737e3100044e0bfc8bcbe5d96",
      "cpu_count": "1",
      "vendor": "adb3d8ce37413000158bbfc8bcbe5d15",
      "assigned_to": "5137153cc611227c000bbd1bd8cd2007",
      "os_version": "5.1.2600",
      "cd_rom": "0",
      "unverified": "0",
      "asset": "aac1ba8837f3100044e0bfc8bcbe5d3b",
      "skip_sync": "0",
      "sys_created_on": "2005-05-24 01:14:19",
      "sys_domain": "global",
      "cpu_type": "GenuineIntel",
      "install_date": "2020-05-19 07:00:00",
      "asset_tag": "P1000143",
      "install_status": "1",
      "name": "ANDREWDWXP",
      "subcategory": "Computer",
      "virtual": "0",
      "sys_class_path": "/!!/!2/!(",
      "company": "31bea3d53790200044e0bfc8bcbe5dec",
      "department": "221f3db5c6112284009f4becd3039cc9",
      "cost": "1299.99",
      "os": "Windows XP Professional",
      "monitor": "0",
      "model_id": "0c43b0c6c611227501522de2b64679ac",
      "cost_cc": "USD",
      "location": "db9a923c0a0a0a6501068d6eaec25ee0",
      "category": "Hardware",
      "fault_count": "0",
      "serial_number": "XK0HKSN6"
    },
    "serials": {
      "GlideRecordUtil": {},
      "ignoreFields": {
        "sys_created_by": true,
        "sys_updated_by": true,
        "sys_mod_count": true
      },
      "records": [
        {
          "serial_number_type": "baseboard",
          "serial_number": "XK0HKSN6",
          "valid": true
        }
      ],
      "m2m_records": [],
      "table_name": "cmdb_serial_number",
      "field_name": "cmdb_ci",
      "cmdb_ci": "ANDREWDWXP",
      "debug_flag": false,
      "isM2M": false,
      "target_table_name": null,
      "target_ref_field_name": null
    },
    "serialMap": {
      "baseboard": {
        "XK0HKSN6": true
      }
    }
  }

serial number : XK0HKSN6
serial type : baseboard
```

## CimCIData - SerialRecord\(String type, String serial\)

Creates a new serial record.

|Name|Type|Description|
|----|----|-----------|
|type|String|The serial type to assign to the CI. If out-of-box, uses the CimCIData.serialType enum.|
|serial|String|The serial number to assign.|

|Type|Description|
|----|-----------|
|void| |

## CimCIData - setMakeAndModel\(String make, String model\)

Sets the make and model for the current configuration item \(CI\).

|Name|Type|Description|
|----|----|-----------|
|make|String|Name of the manufacturer to set for the CI.|
|model|String|Name of the model to set for the CI.|

|Type|Description|
|----|-----------|
|void| |

The following example shows how to use the setMakeAndModel\(\) method to set the make and model of the specified CI.

```
var cidata = new CIData(); // Instantiate a new CIData class object
cidata.loadFromCI('0c43b0f5c6112275019abd2bb3dcd78f'); // Load the current data from a CI record. Use sys_id or CI name
var cimcidata = new CimCIData(cidata); // Instantiate a new CimCIData class object and pass the CIdata 
cimcidata.setMakeAndModel('IBM','Thinkpad T20'); // Set make(manufacturer) and model in the CIData and CimCIData
gs.info(JSON.stringify(cimcidata, null, 4)); // Display JSON payload in string format with added manufacturer sys_id
gs.info("model= "+cimcidata.data.model_id); // Display model sys_id which is added from cmdb_hardware_product_model table
```

Output:

```
{
    "cidata": {
        "ignoreFields": {
            "sys_created_by": true,
            "sys_updated_by": true,
            "sys_mod_count": true
        },
        "GlideRecordUtil": {},
        "debug_flag": false,
        "data": {
            "sys_id": "0c43b0f5c6112275019abd2bb3dcd78f",
            "operational_status": "1",
            "os_service_pack": "Service Pack 1",
            "cpu_manufacturer": "0c43b088c6112275011a4bd46a4e6cc4",
            "sys_updated_on": "2022-01-06 18:07:50",
            "discovery_source": "Other Automated",
            "ram": "503",
            "cpu_speed": "1993",
            "sys_domain_path": "/",
            "disk_space": "37.26",
            "cost_center": "d9d07bddc0a80a647cf932056ed24652",
            "assigned": "2020-08-31 08:00:00",
            "cd_speed": "-1",
            "can_print": "0",
            "sys_class_name": "cmdb_ci_computer",
            "manufacturer": "b7e7c073c0a801690143e7b7d29eb408",
            "cpu_count": "1",
            "vendor": "adb3d8ce37413000158bbfc8bcbe5d15",
            "assigned_to": "5137153cc611227c000bbd1bd8cd2007",
            "os_version": "5.1.2600",
            "cd_rom": "0",
            "unverified": "0",
            "asset": "aac1ba8837f3100044e0bfc8bcbe5d3b",
            "skip_sync": "0",
            "sys_created_on": "2005-05-24 01:14:19",
            "sys_domain": "global",
            "cpu_type": "GenuineIntel",
            "install_date": "2020-05-19 07:00:00",
            "asset_tag": "P1000143",
            "install_status": "1",
            "name": "ANDREWDWXP",
            "subcategory": "Computer",
            "virtual": "0",
            "sys_class_path": "/!!/!2/!(",
            "company": "31bea3d53790200044e0bfc8bcbe5dec",
            "department": "221f3db5c6112284009f4becd3039cc9",
            "cost": "1299.99",
            "os": "Windows XP Professional",
            "monitor": "0",
            "ip_address": "198.11.23.111",
            "cost_cc": "USD",
            "location": "db9a923c0a0a0a6501068d6eaec25ee0",
            "category": "Hardware",
            "fault_count": "0",
            "model_id": "0c43b124c611227501522de2a381613e"
        },
        "rl_map": {},
        "cmdb_ci": "0c43b0f5c6112275019abd2bb3dcd78f",
        "related": {}
    },
    "data": {
        "sys_id": "0c43b0f5c6112275019abd2bb3dcd78f",
        "operational_status": "1",
        "os_service_pack": "Service Pack 1",
        "cpu_manufacturer": "0c43b088c6112275011a4bd46a4e6cc4",
        "sys_updated_on": "2022-01-06 18:07:50",
        "discovery_source": "Other Automated",
        "ram": "503",
        "cpu_speed": "1993",
        "sys_domain_path": "/",
        "disk_space": "37.26",
        "cost_center": "d9d07bddc0a80a647cf932056ed24652",
        "assigned": "2020-08-31 08:00:00",
        "cd_speed": "-1",
        "can_print": "0",
        "sys_class_name": "cmdb_ci_computer",
        "manufacturer": "b7e7c073c0a801690143e7b7d29eb408",
        "cpu_count": "1",
        "vendor": "adb3d8ce37413000158bbfc8bcbe5d15",
        "assigned_to": "5137153cc611227c000bbd1bd8cd2007",
        "os_version": "5.1.2600",
        "cd_rom": "0",
        "unverified": "0",
        "asset": "aac1ba8837f3100044e0bfc8bcbe5d3b",
        "skip_sync": "0",
        "sys_created_on": "2005-05-24 01:14:19",
        "sys_domain": "global",
        "cpu_type": "GenuineIntel",
        "install_date": "2020-05-19 07:00:00",
        "asset_tag": "P1000143",
        "install_status": "1",
        "name": "ANDREWDWXP",
        "subcategory": "Computer",
        "virtual": "0",
        "sys_class_path": "/!!/!2/!(",
        "company": "31bea3d53790200044e0bfc8bcbe5dec",
        "department": "221f3db5c6112284009f4becd3039cc9",
        "cost": "1299.99",
        "os": "Windows XP Professional",
        "monitor": "0",
        "ip_address": "198.11.23.111",
        "cost_cc": "USD",
        "location": "db9a923c0a0a0a6501068d6eaec25ee0",
        "category": "Hardware",
        "fault_count": "0",
        "model_id": "0c43b124c611227501522de2a381613e"
    },
    "serials": null,
    "serialMap": {}
}
model= 0c43b124c611227501522de2a381613e
```

