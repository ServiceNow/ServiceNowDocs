---
title: CMDB Coverage properties
description: CMDB Coverage properties control the behavior of the application.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-03-02"
reading_time_minutes: 1
breadcrumb: [Reference, CMDB Coverage, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB Coverage properties

CMDB Coverage properties control the behavior of the application.

## Default system properties

These default system properties are available for the CMDB Coverage application.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_y5f_vmw_l3c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

db\_listener\_enabled​

</td><td>

The DB Listener functionality is enabled when this property is set to `true`.​ The DB Listener creates records in the IP Address Staging \[sn\_cmdb\_ip\_cov\_ip\_staging\] table that correspond to the new and updated records in the tables that are configured in the IP Coverage CI Table Configuration \[sn\_cmdb\_ip\_cov\_ci\_config\] table.**Note:** Do not modify this property. The DB Listener functionality is deactivated when this property is set to `false`.

-   Type: true \| false
-   Default value: `true`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

table\_extension\_enabled

</td><td>

Records from the child tables \(table extensions\) of the parent tables that are defined in the IP Coverage CI Table Configuration \[sn\_cmdb\_ip\_cov\_ci\_config\] table are included in the analysis when this property is set to `true`.**Note:** Do not modify this property. Only records from explicitly configured tables are included in the analysis when this property is set to `false`.

-   Type: true \| false
-   Default value: `true`
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>## Custom system property

You can create the sn\_cmdb\_ip\_cov.log\_associated\_missing\_ip custom system property for the CMDB Coverage application. This property must be created in the CMDB Coverage application scope. The custom property that you create is listed in the System Properties \[sys\_properties\] table. For more information about creating custom system properties, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

To populate data in the Discovery schedule gaps to allocated IP \[sn\_cmdb\_ip\_cov\_m2m\_discovery\_schedule\_gap\]​ table, create the sn\_cmdb\_ip\_cov.log\_associated\_missing\_ip custom system property, and set the value to `true`.

-   Type: true \| false
-   Default value: `false`

**Parent Topic:**[CMDB Coverage reference](../concept/cmdb-coverage-reference.md)

