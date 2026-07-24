---
title: Create the principal class recommendation criteria property
description: Create the sn\_cmdb\_advisor.principal\_class\_recommendation\_criteria system property to filter which CI classes CMDB success advisor considers when generating principal class recommendations for the Data Foundations advisor.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-rec-criteria.html
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-05-24"
reading_time_minutes: 1
breadcrumb: [CI class recommendations, Use Data Foundations advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create the principal class recommendation criteria property

Create the **sn\_cmdb\_advisor.principal\_class\_recommendation\_criteria** system property to filter which CI classes CMDB success advisor considers when generating principal class recommendations for the Data Foundations advisor.

## Before you begin

Role required: admin

## About this task

This property does not exist by default. Without it, CMDB success advisor generates recommendations based on CI class activity in task records. Create this property on instances with no prior task activity, where task-based recommendations produce no results. Setting the value to `PREDEFINED` tells CMDB success advisor to recommend a standard set of commonly managed CI classes instead.

## Procedure

1.  Set the application scope to CMDB success advisor using the application picker.

2.  In the navigation filter, enter `sys_properties.list` and press **Enter**.

3.  Select **New**.

4.  Fill in the following fields.

<table id="table_set_rec_criteria"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

**sn\_cmdb\_advisor.principal\_class\_recommendation\_criteria**

</td></tr><tr><td>

Type

</td><td>

**string**

</td></tr><tr><td>

Value

</td><td>

`PREDEFINED`

 Tells CMDB success advisor to recommend a standard set of commonly managed CI classes: Computer \[cmdb\_ci\_computer\], Server \[cmdb\_ci\_server\], Database \[cmdb\_ci\_database\], Cloud Database \[cmdb\_ci\_cloud\_database\], Virtual Machine Instance \[cmdb\_ci\_vm\_instance\], and IP Router \[cmdb\_ci\_ip\_router\].

</td></tr></tbody>
</table>5.  Select **Submit**.


## Result

CMDB success advisor uses the predefined set of CI classes as recommendations on instances where task history produces no results.

**Related topics**  


[Principal classes in CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-principal-class.md)

