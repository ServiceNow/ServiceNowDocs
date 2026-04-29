---
title: Define an EVAM view template
description: You can configure multiple view templates per data source based on conditions to customize how data displays for users. The view template maps fields from the view configuration to component.
locale: en-US
release: australia
product: Entity View Action Mapper \(EVAM\)
classification: entity-view-action-mapper-evam
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring entity view action mapper, Entity view action mapper, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Define an EVAM view template

You can configure multiple view templates per data source based on conditions to customize how data displays for users. The view template maps fields from the view configuration to component.

## Before you begin

Role required: admin or evam\_admin

## About this task

The view template is referenced from the Entity View Action Mapper \(EVAM\) view configuration record. For more information, see [Define an EVAM configuration bundle](define-view-configuration-bundle.md).

## Procedure

1.  Navigate to **All** &gt; **Entity View Action Mapper \(EVAM\)** &gt; **View Definition** &gt; **View Templates**, and then select **New**.

2.  On the form, fill in the fields.

<table id="table_ayv_pry_2nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the EVAM view template.

</td></tr><tr><td>

Application

</td><td>

Application scope of the EVAM view template.

</td></tr><tr><td>

Active

</td><td>

Option to activate the EVAM view template.

</td></tr><tr><td>

Template

</td><td>

A JSON template that defines the view for a mapped data source.For example, the default search template contains the following:

```json
{
    "component": "sn-search-result-evam-card", 
    "staticValues":  {  
      },
    "mappings": {
        "title": "ai_search_teaser_title",
        "summary": "ai_search_teaser_text"
    },
    "actionMappings": {
        "clickAction": "navigation"
    }
}
```

 Use `sn-search-result-evam-card` as the component for search result pages.

</td></tr></tbody>
</table>3.  Select **Submit**.


