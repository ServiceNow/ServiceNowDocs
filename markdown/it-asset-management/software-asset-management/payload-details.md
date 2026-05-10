---
title: Sample payload for generic software install records
description: A sample payload that populates the Software Installation \[cmdb\_sam\_sw\_install\] table in the ServiceNow instance with discovery data collected by third-party discovery sources.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management]
---

# Sample payload for generic software install records

A sample payload that populates the Software Installation \[cmdb\_sam\_sw\_install\] table in the ServiceNow instance with discovery data collected by third-party discovery sources.

The following is a sample payload for creating software install records for publishers such as Microsoft, IBM. For Oracle, VMware, and Citrix, specialized payloads are used.

In this sample payload, you are passing the information of the installed software, Microsoft Word 2016, and the related CI to inform where it is installed \(on a computer CI "SAMILMT8"\). You can look up column names in the cmdb\_sam\_sw\_install table and send information by passing the columns, value pairs in the payload. For example, in this payload you are sending the publisher, version and display\_name columns. You can also send additional information such as the edition column.

**Note:** For more information on CI Identifier rules, see [Identifier Rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/c_IdentificationRules.md).

```
{ 'items': [{'className':'cmdb_ci_computer',
                'related': [{
                              className:'cmdb_sam_sw_install',
                              values: {
                                'publisher':'Microsoft',
                                'version':'2016',
                                'display_name':'Word'
                                }
                            }
                        ],
                   'values': {'name':'SAMILMT8'}
                             }]
              }
```

|Element|Value|Description|
|-------|-----|-----------|
|className|cmdb\_ci\_computer|The class name of the CI.|
|className|cmdb\_sam\_sw\_install|The name of the related table in the CMDB application where the CI is to be created.|
|publisher|Microsoft|The name of the publisher for whom this entry is being created in the table.|
|version|2016|The version of the software for which this entry is created in the table.|
|display name|Word|The display name for this entry in the table.|
|name|SAMILMT8|Unique identifier of the CI.|

**Parent Topic:**[Software Asset Management references](references.md)

