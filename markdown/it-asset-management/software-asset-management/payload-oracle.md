---
title: Sample payload for Oracle software install records
description: A sample payload for Oracle publisher pack that populates the Oracle Instance \[cmdb\_ci\_db\_ora\_instance\] table with software install records from third-party discovery sources.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [References, Software Asset Management, IT Asset Management]
---

# Sample payload for Oracle software install records

A sample payload for Oracle publisher pack that populates the Oracle Instance \[cmdb\_ci\_db\_ora\_instance\] table with software install records from third-party discovery sources.

After you discover Oracle software installs via your discovery source, send a payload that contains the Oracle Instance and the Oracle options associated with the Oracle Instance.

**Note:** In the Properties page, make sure to select the Enable scheduled jobs when using third party Datasource Integration Framework \[com.snc.samp.ire.datasource.integration\] property.

When the schedule job, SAM- Software Asset Connections, runs, it looks for records with null software installs, populates the software install field in the Oracle Instance table and creates the software install record associated to the instance.

The following is a sample payload to create software install records for Oracle in the Oracle Instance \[cmdb\_ci\_db\_ora\_instance\] table. The sample input contains a list of CIs and relationships that exist between these CIs. The payload states that there is an Oracle database server, Dev development 1969 with a standard edition. The Oracle database server has many Oracle options enabled such as Armstrong, Aldrin, Collins and runs on a Linux server.

```
{
  'items': [
    {
      'className': 'cmdb_ci_db_ora_instance',
      'related': [
        {
          'className': 'samp_oracle_options',
          'values': {
            "option": "Armstrong",
            "currently_used": "true"
          }
        },
        {
          'className': 'samp_oracle_options',
          'values': {
            "option": "Aldrin",
            "currently_used": "true"
          }
        },
        {
          'className': 'samp_oracle_options',
          'values': {
            "option": "Collins",
            "currently_used": "true"
          }
        }
      ],
      'values': {
        'name': 'Dev development 1969',
        'edition': 'Standard',
        'sid': '1-2-569',
        'version': '11.2'
      }
    },
    {
      'className': 'cmdb_ci_linux_server',
      'values': {
        'name': 'CI DATAI 6-002',
        'mac_address': '4653XYZAA',
        'ip_address': '10.10.10.8',
        'asset_tag': 'HWR0003',
        'assigned_to': 'a8f98bb0eb32010045e1a5115206fe3a',
        'cpu_count': '16',
        'cpu_manufacturer': '820351a1c0a8018b67c73d51c074097c',
        'manufacturer': '820351a1c0a8018b67c73d51c074097c',
        'os': 'Linux Red Hat',
        'os_version': '2.6.9-22.0.1.ELsmp',
        'ram': '2014'
      }
    }
  ],
  'relations': [
    {
      'type': 'Runs on::Runs',
      'parent': 0,
      'child': 1
    }
  ]
}
```

|Element|Value|Description|
|-------|-----|-----------|
|className|cmdb\_ci\_db\_ora\_instance|Name of the related Oracle instance table.|
|className|samp\_oracle\_options|Name of the Oracle database option table.|
|option|Armstrong|Name of the Oracle database option.|
|currently\_used|true|Indicates the Armstrong option is currently enabled.|
|className|samp\_oracle\_options|Name of the Oracle database option table.|
|option|Aldrin|Name of the Oracle database option|
|currently\_used|true|Indicates the Aldrin option is currently enabled.|
|name|Dev Development 69|Name of the Oracle database server|
|edition|standard|edition of the Oracle database server|
|sid|1-2-569|Oracle system ID|
|version|11.2|Version of the Oracle database server|
|className|cmdb\_ci\_linux\_server|Name of the related Linux Server table.|
|mac address|4653XYZAA|MAC address of the interface in the Linux server.|

**Parent Topic:**[Software Asset Management references](references.md)

