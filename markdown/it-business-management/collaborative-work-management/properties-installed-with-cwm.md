---
title: Properties installed with Collaborative Work Management
description: System properties that you can configure to include other ServiceNow AI Platform records in CWM Docs and modify the way non-CWM users request access to the workspace.
locale: en-US
release: xanadu
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Collaborative Work Management, Strategic Portfolio Management]
---

# Properties installed with Collaborative Work Management

System properties that you can configure to include other ServiceNow AI Platform records in CWM Docs and modify the way non-CWM users request access to the workspace.

These properties are available for Collaborative Work Management.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_tc2_1xr_b1c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_cwm.request\_role\_access

</td><td>

Property to show or hide the **Request Access** button for non-CWM users in the workspace.By default, the button is hidden. When this property is set to true, an event **sn\_cwm.REQUEST\_ROLE\_ACCESS** is raised. Admins can configure this event to trigger one of the following workflows, allowing the non-CWM user to request access to the workspace.

-   Raising a Service Catalog request.
-   Sending an email.

-   Type: true \| false
-   Default value: false
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_cwm.record\_mention\_config

</td><td>

Property to configure mentioning any ServiceNow AI Platform record within Docs pages of CWM workspace.

 -   Type: string
-   Default value: `[{"sourceTable":"sn_cwm_task","label":"CWM Task","fields":["short_description","number"]}]`

By default, this property is configured to include CWM task records.

-   Location: System Property \[sys\_properties\] table

 To include any other ServiceNow AI Platform record, update the property.

 For example, to reference the Incident records in the Docs pages, update the **Value** field of this property to include the Incident table.

 The updated **Value** field would include the configuration for CWM task records and Incident records:

```
[{"sourceTable":"sn_cwm_task","label":"CWM Task","fields":["short_description","number"]},
{"sourceTable":"incident","label":"Incident","fields":["short_description","number"]}]
```

</td></tr><tr><td>

sn\_cwm.connect\_work\_import\_limit

</td><td>

Property to configure the maximum number of items that can be imported to a CWM Board for the first time when using the Connected work feature.

 -   Type: integer
-   Default value: 100
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_cwm.agile\_enabled

</td><td>

Property to control Agile-related features for CWM. If set to true, then agile items like Story and Epic can be created in a CWM Board and Sprint planning feature will be enabled.

 -   Type: true \| false
-   Default value: true
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>**Parent Topic:**[Collaborative Work Management reference](../concept/reference-cwm.md)

