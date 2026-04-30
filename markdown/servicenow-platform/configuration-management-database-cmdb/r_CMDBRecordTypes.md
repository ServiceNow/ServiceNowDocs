---
title: CMDB record types
description: The CMDB contains the following major record types.
locale: en-US
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [CMDB classifications and class dependency, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB record types

The CMDB contains the following major record types.

<table id="table_qtk_dyw_wq"><thead><tr><th>

Record types

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration Item \(CI\)

</td><td>

Any computer, device, or service in the CMDB. A CI's record includes all of the relevant data, such as manufacturer, vendor, location, etc. Configuration items can be created or maintained either using tables, lists, and forms within the platform, or using the Discovery application.

</td></tr><tr><td>

Relation Type

</td><td>

A defined relationship between a CI and either another CI, a user, or a group. Relation types are defined twice, once from the perspective of the child CI and once from the parent CI's perspective. For example, a parent CI that powers a child CI uses relation type **Powers::Is Powered By**. Example relation types include **In Rack::Rack contains**, **Log Reviewed by::Reviews logs** for, or **Backup done by::Does backups** for.

 CMDB relationships can be established using Discovery or using the tables, lists, and forms within the platform. The CMDB form has a specific Related Items toolbar optimized for modifying relationships.

</td></tr></tbody>
</table>**Parent Topic:**[CMDB classifications and class dependency](../concept/c_CMDBClassifications.md)

**Related topics**  


[Dependent CIs management](../concept/manage-dependent-ci.md)

[Related Lists of CI components](r_RelatedListsOfCIComponents.md)

[Create a CI class](../task/t_CreateCIType.md)

[Reclassify a CI](../task/t_ManuallyReclassifyCI.md)

[Delete CIs](../task/delete-class-records-ci-class-mgr.md)

[View and edit class definitions and metadata](../task/t_ViewTableDefinitions.md)

[Update the list of classes in the Principal Class filter](../task/update-principal-class-filter.md)

