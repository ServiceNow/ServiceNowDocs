---
title: Create a CI finder mapping
description: Use the CI finder mapping to link the resources fetched by the ServiceNow Cloud Configuration Governance scan runs with the appropriate Configuration Management Database \(CMDB\) Configuration Items \(CIs\), if available. After you create the mapping, you can associate the reported configuration violations with the CIs to which they belong.
locale: en-US
release: zurich
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Cloud Configuration Governance policies, Using Cloud Configuration Governance, Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create a CI finder mapping

Use the CI finder mapping to link the resources fetched by the ServiceNow Cloud Configuration Governance scan runs with the appropriate Configuration Management Database \(CMDB\) Configuration Items \(CIs\), if available. After you create the mapping, you can associate the reported configuration violations with the CIs to which they belong.

## Before you begin

Role required: sn\_itom\_ccg.scheduling\_admin or sn\_itom\_ccg.governor

## About this task

After creating a resource type in Cloud Configuration Governance, you can optionally create a CI finder mapping for the new resource type. Cloud Configuration governance calls the CI finder mapping script for all the resources fetched by the scan runs.

## Procedure

1.  Navigate to **All** &gt; **Cloud Configuration Governance** &gt; **CI Finder Mappings**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_t5w_gtl_jtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Provider Type

</td><td>

Cloud service provider that hosts the resource.

</td></tr><tr><td>

Resource Type

</td><td>

Resource type of the cloud resource.

</td></tr><tr><td>

Script

</td><td>

Script to link the resources fetched by the Cloud Configuration Governance application with the existing CI.Use an existing CI finder mapping script as an example to create a script for the new resource type.

 Cloud Configuration Governance offers several objects and variables for use in the script. For more information, see [Cloud Configuration Governance scripting reference](../reference/ccg-scripting-reference.md).

</td></tr></tbody>
</table>
