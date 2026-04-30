---
title: Sample payload for VMware software install records
description: A sample payload for VMware publisher pack that populates the VMware Discovered License key consumption \[samp\_vmware\_license\_key\_usage\] table with software install records from third-party discovery sources.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [References, Software Asset Management, IT Asset Management]
---

# Sample payload for VMware software install records

A sample payload for VMware publisher pack that populates the VMware Discovered License key consumption \[samp\_vmware\_license\_key\_usage\] table with software install records from third-party discovery sources.

After you discover software installs via your discovery source, send a payload via the IRE REST API endpoint to the ServiceNow instance to populate the VMware Discovered License key consumption \[samp\_vmware\_license\_key\_usage\] table with software install records.

**Note:** In the Properties page, make sure to select the Enable scheduled jobs when using third party Datasource Integration Framework \[com.snc.samp.ire.datasource.integration\] property.

1.  Send a payload to create a license key in the VMware Discovered License key \[samp\_vmware\_license\_key\] table.
2.  From the response body of the payload, copy the sys ID of the new license key and paste it in a text editor for later use.
3.  Use the Enhanced IRE API to query the sys IDs of the CIs that use the new license key.
4.  From the response body, copy the sys IDs of the CIs and paste them in a text editor for later use.
5.  Send a payload with the sys ID of the license key and the sys ID of the CIs.
6.  Run the schedule job, SAM- Update Software Usage to populate the VMware Discovered License key consumption \[samp\_vmware\_license\_key\_usage\] table with the software install records.

```
Request Body
{ 'items': [
                {'className':'cmdb_ci_vcenter',
              'related': [
                          {
                          className:'samp_vmware_license_key',
                            values:{
                             'cost_unit':'cpuPackage',
                                      'edition':'esxEnterprisePlus.vram',
                                      'features':'autodeploy,das,dpvmotion',
                                      'license_key':'SYDOJ-28J5Q-78X48-0NC24-REKAR',
                                      'product_name':'VMware vSphere 5 Enterprise Plus',
                                      'product_version':'5.0',
                                      'rights_owned':'8',
                                      'rights_used':'6'
                              }
                          }
                        
                        ],
              'values': {
                 'name':'VCenter Ref 1A'
                  }
              },
              {
                'className':'cmdb_ci_win_server',
                 'values': {'name':'VirtualMachine-WS2'
                           }
                      }
              ],
              'relations':[{
                   'type':'Runs on::Runs',
                   'parent':0,
                   'child':1
                 }]
            }

Response Body
{
  "result": {
    "items": [
      {
        "className": "cmdb_ci_vcenter",
        "operation": "INSERT",
        "sysId": "8fb47793e7cc10107aea07d8d2f6a93a",
        "relatedSysIds": [
          "cbb47793e7cc10107aea07d8d2f6a93f"
        ],
        "relatedItems": [
          {
            "className": "samp_vmware_license_key",
            "sysId": "cbb47793e7cc10107aea07d8d2f6a93f",
            "markers": [],
            "inputIndices": [
              {
                "mainIndex": 0,
                "subIndex": 0
              }
            ]
          }
        ],
        "additionalRelatedItems": [],
        "identifierEntrySysId": "Unknown",
        "identificationAttempts": [
          {
            "attributes": [
              "name"
            ],
            "identifierName": "VMWare VCenter Ref CI",
            "attemptResult": "NO_MATCH",
            "searchOnTable": "cmdb_ci_vcenter",
            "hybridEntryCiAttributes": []
          }
        ],
        "errorCount": 0,
        "markers": [],
        "inputIndices": [
          0
        ]
      },
      {
        "className": "cmdb_ci_win_server",
        "operation": "UPDATE",
        "sysId": "30ccb31ddbe7720087b9fd441d961992",
        "identifierEntrySysId": "556eb250c3400200d8d4bea192d3ae92",
        "identificationAttempts": [
          {
            "attributes": [
              "serial_number",
              "serial_number_type"
            ],
            "identifierName": "Hardware Rule",
            "attemptResult": "SKIPPED",
            "searchOnTable": "cmdb_serial_number",
            "hybridEntryCiAttributes": []
          },
          {
            "attributes": [
              "serial_number"
            ],
            "identifierName": "Hardware Rule",
            "attemptResult": "SKIPPED",
            "searchOnTable": "cmdb_ci_hardware",
            "hybridEntryCiAttributes": []
          },
          {
            "attributes": [
              "name"
            ],
            "identifierName": "Hardware Rule",
            "attemptResult": "MATCHED",
            "searchOnTable": "cmdb_ci_hardware",
            "hybridEntryCiAttributes": []
          }
        ],
        "errorCount": 0,
        "markers": [],
        "inputIndices": [
          1
        ]
      }
    ],
    "additionalCommittedItems": [],
    "relations": [
      {
        "className": "cmdb_rel_ci",
        "operation": "INSERT",
        "sysId": "43b47793e7cc10107aea07d8d2f6a940",
        "identifierEntrySysId": "Unknown",
        "errorCount": 0,
        "markers": [],
        "inputIndices": [
          0
        ]
      }
    ],
    "additionalCommittedRelations": []
  }
}

From this we get the samp_vmware_license_key sys id
"relatedSysIds": [
          "cbb47793e7cc10107aea07d8d2f6a93f"
        ]

-- Obtaining the CI sys id (POST)
role: sam_admin


https://k8s0057813-node1.thunder.lab3.service-now.com/api/now/identifyreconcile/queryEnhanced?sysparm_data_source=ServiceNow

Request Body
{ 'items': [ {'className':'cmdb_ci_win_server', 'values': {'name':'Server-WS11'} }]}

Response Body
{
  "result": {
    "items": [
      {
        "className": "cmdb_ci_win_server",
        "operation": "UPDATE",
        "sysId": "99ccb31ddbe7720087b9fd441d9619da",
        "identifierEntrySysId": "556eb250c3400200d8d4bea192d3ae92",
        "identificationAttempts": [
          {
            "identifierName": "Hardware Rule",
            "attemptResult": "SKIPPED",
            "attributes": [
              "serial_number",
              "serial_number_type"
            ],
            "searchOnTable": "cmdb_serial_number",
            "hybridEntryCiAttributes": []
          },
          {
            "identifierName": "Hardware Rule",
            "attemptResult": "SKIPPED",
            "attributes": [
              "serial_number"
            ],
            "searchOnTable": "cmdb_ci_hardware",
            "hybridEntryCiAttributes": []
          },
          {
            "identifierName": "Hardware Rule",
            "attemptResult": "MATCHED",
            "attributes": [
              "name"
            ],
            "searchOnTable": "cmdb_ci_hardware",
            "hybridEntryCiAttributes": []
          }
        ],
        "markers": [],
        "inputIndices": [
          0
        ],
        "mergedPayloadIds": [],
        "errorCount": 0
      }
    ],
    "additionalCommittedItems": [],
    "relations": [],
    "additionalCommittedRelations": []
  }
}

where  "sysId": "99ccb31ddbe7720087b9fd441d9619da" is the sys id of the ci/used_by


// create usage table
POST 
https://k8s0057813-node1.thunder.lab3.service-now.com/api/now/table/samp_vmware_license_key_usage?sysparm_fields=sys_id

{"license_key":"cbb47793e7cc10107aea07d8d2f6a93f","rights_used":"1","used_by":"99ccb31ddbe7720087b9fd441d9619da"}
```

|Element|Value|Description|
|-------|-----|-----------|
|className|cmdb\_ci\_vcenter|Name of the table related \[samp\_vmware\_license\_key\] table|
|className|samp\_vmware\_license\_key|Name of the table where the license key is created.|
|className|cmdb\_ci\_win\_server|The name of the Windows server table|
|name|VirtualMachine-WS2|Name of the Windows server virtual machine.|

**Parent Topic:**[Software Asset Management references](references.md)

