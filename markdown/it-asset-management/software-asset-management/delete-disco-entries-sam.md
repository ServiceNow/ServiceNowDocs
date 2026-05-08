---
title: Delete uninstalled software from the Software Installation table
description: Delete installations from the Software Installation \[cmdb\_sam\_sw\_install\] table if those software installations are also uninstalled from a CI.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Software Asset Management administration, Software Asset Management, IT Asset Management]
---

# Delete uninstalled software from the Software Installation table

Delete installations from the Software Installation \[cmdb\_sam\_sw\_install\] table if those software installations are also uninstalled from a CI.

## Before you begin

After the discovery process runs and you identify software installations that are uninstalled from a CI, delete those installations from the Software Installation \[cmdb\_sam\_sw\_install\] table in the CMDB application.

Create a script to delete multiple software installation records from the Software Installation \[cmdb\_sam\_sw\_install\] table. You can use the Table API to query the Software Installation table to get the installation list for the CI.

Role required: sam\_developer

## About this task

You can also delete software installation records for specific publishers like Oracle, VMware, and Citrix.

## Procedure

1.  Use the REST Table API api/now/table/cmdb\_sam\_sw\_install?sysparm\_query=installed\_on%3D28c9c3b8c0a8000b009b2d941d7e3ee9 to query and identify the list of software installs on a specific CI.

    For more information on the REST endpoint API, see Table API-GET.

    1.  Specify the table name, Software Installation \[cmdb\_sam\_sw\_install\] table, and query parameters.

        For the query parameters, specify either the sys\_id of the CI or a list of fields that are separated by commas such as publisher, version, and product on which you want to perform the delete operation.

    2.  After entering the query parameters, send the request.

        You get a response in a JSON format listing of all the software installations for that specific CI. You can view the sys\_id for all the software installations in the response.

2.  Based on the response, identify the sys\_ids of the software installations that are deleted on a CI.

    Only the sys\_ids of those software installations must be passed through the Delete API.

3.  Use the Delete API request.setEndpoint\('http://xyz/api/now/table/cmdb\_sam\_sw\_install/728e87dafd841010fa9bea491bfdc1ff'\); request.setHttpMethod\('DELETE'\); to delete the software installs from the Software Installation \[cmdb\_sam\_sw\_install\] table.

    xyz in the URL refers to your ServiceNow instance.

    1.  Specify the table name, Software Installation \[cmdb\_sam\_sw\_install\] table, and the sys\_ids of the software installations that are deleted on the CIs.

    2.  Send the request.

        The software installations are deleted from the Software Installation \[cmdb\_sam\_sw\_install\] table.


**Parent Topic:**[Software Asset Management administration](../concept/c_SAMAdministration.md)

