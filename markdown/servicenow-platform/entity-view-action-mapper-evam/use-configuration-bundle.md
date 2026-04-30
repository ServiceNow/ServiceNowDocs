---
title: View configurations, view templates, and configuration bundles for EVAM
description: A view configuration combines conditions, database fields, and declarative actions with an associated view template. You can also group view configurations together to create configuration bundles.
locale: en-US
release: yokohama
product: Entity View Action Mapper \(EVAM\)
classification: entity-view-action-mapper-evam
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Exploring Entity View Action Mapper, EVAM, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# View configurations, view templates, and configuration bundles for EVAM

A view configuration combines conditions, database fields, and declarative actions with an associated view template. You can also group view configurations together to create configuration bundles.

EVAM has pre-defined view configurations, view templates, and configuration bundles to make it easier to use the feature. The base system configuration bundles include:

-   Service Portal Search Bundle
-   Service Portal bundle \(sp\_bundle\)

These bundles have view configurations attached that are anticipated to fit the business unit associated. You can also create or edit configuration bundles to meet your needs.

View configurations have an associated view template, tables and conditions, designated table field with data, and associated declarative actions. You can look at the demo\_evam\_dataset for examples of base system configuration views. These view configurations are ready to use and are meant to work with many use cases. You can also create or edit view configurations to meet specific needs.

The base system view templates match an associated view configuration. The templates contain the JSON used to give the necessary information for the card display and use. For example, the Attachment Search Template contains the following:

```
{
    "component": "sn-search-result-evam-card",
    "staticValues":  {
        "detailLabelType": {
            "translatable": false,
            "key": "inline"
        },
        "textHeaderLabelOne": {
            "translatable": true,
            "key": "Attachment"
        },
        "detailLabelOne": {
            "translatable": true,
            "key": "From:"
        }
    },
    "mappings": {
        "imageType": "doctype_image_type",
        "icon": "doctype_image",
        "imageURL":"doctype_image",
        "textHeaderLabelTwo": "doctype",
        "title": "ai_search_teaser_title",
        "summary": "ai_search_teaser_text",
        "detailValueOne":"parent_title"
    },
    "actionMappings": {
        "clickAction": "navigation",
        "footerLinkAction": "navigation_to_parent_record"
    }
}
```

The JSON structure has the following sections:

<table id="table_p1k_svl_xnb"><thead><tr><th>

Template

</th><th>

Description

</th></tr></thead><tbody><tr><td>

component

</td><td>

The card component name.

</td></tr><tr><td>

staticValues

</td><td>

The static text mapping to component properties. These values have the following properties: -   translatable – Determines whether the key text should be translated based on the user's language. Can be either True or False.
-   key – The value the property is set to.

</td></tr><tr><td>

mappings

</td><td>

The mapping of the data source field to the component properties.

</td></tr><tr><td>

actionMappings

</td><td>

The actions that you can associate with the card.

</td></tr></tbody>
</table>These view templates are ready to use and are meant to work with many use cases. You can also create or edit view templates to meet specific needs.

