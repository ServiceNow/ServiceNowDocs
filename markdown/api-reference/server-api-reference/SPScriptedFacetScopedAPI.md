---
title: SPScriptedFacet - Scoped
description: Defines facet items, filters, or mapped queries for a facets object.Adds facet items or mapped queries to a facets object.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SPScriptedFacet- Scoped

Defines facet items, filters, or mapped queries for a facets object.

You can only use the SPScriptedFacet API in a facet generation script in a Service Portal search source. The facet generation script is only visible when **Is scripted source** is selected.

There is no constructor for this class. Instead, use the [createFacet\(\)](../../SPScriptedFacetService/concept/SPScriptedFacetServiceScopedAPI.md#) or [createMultiChoiceFacet\(\)](../../SPScriptedFacetService/concept/SPScriptedFacetServiceScopedAPI.md#) methods of the [SPScriptedFacetService](../../SPScriptedFacetService/concept/SPScriptedFacetServiceScopedAPI.md#) class to generate a facets object.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## SPScriptedFacet - addFacetItem\(String label, Object valueObj\)

Adds facet items or mapped queries to a facets object.

Before adding facet items to a facets object, create the facets object using the createFacet\(\) or createMultiChoiceFacet\(\) methods of the SPScriptedFacetService class.

|Name|Type|Description|
|----|----|-----------|
|label|String|The display label for the facet item or mapped query.|
|valueObj|Object|The facet item or mapped query for the facet. Can only contain types String, Number, Boolean, and Double.|

|Type|Description|
|----|-----------|
|void| |

```
function createMultiChoiceFacetFromKB(label, variable, values, orderBy){
  if(!values || values.length == 0)
    return;

  var kbFacet = facetService.createMultiChoiceFacet(label, variable);
  var kbMap = {};
  for(var i in values) {
    var key = values[i].label;
    var value = values[i].id;
    var parent = new KBParentData().getParentCategory(value, key);
    key = parent.join(' > ');
    kbMap[key] = value;
  }

  var labels = Object.keys(kbMap).sort();
  for (i = 0; i < labels.length; i++) {
    var currentLabel = labels[i];
    kbFacet.addFacetItem(currentLabel, kbMap[currentLabel]);
    //adds facet search options for each kbMap entry
  }
}
```

