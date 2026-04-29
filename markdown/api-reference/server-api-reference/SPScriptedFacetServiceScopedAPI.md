---
title: SPScriptedFacetService - Scoped
description: Generates a multi-choice or single-choice facets object for an advanced search source.Creates a single choice facets object.Creates a multi choice facets object.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SPScriptedFacetService- Scoped

Generates a multi-choice or single-choice facets object for an advanced search source.

The SPScriptedFacetService API can only be used in a facet generation script in a Service Portal search source. The facet generation script is only visible when **Is scripted source** is selected.

There is no constructor for this class. Instead, use the createFacet\(\) or createMultiChoiceFacet\(\) methods to generate a facets object.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## SPScriptedFacetService - createFacet\(String label, String id\)

Creates a single choice facets object.

After creating the facets object, add facet items or mapped queries to the facet using the addFacetItem\(\) method of the SPScriptedFacet class.

|Name|Type|Description|
|----|----|-----------|
|label|String|Label for the facet.|
|id|String|ID for the facet.|

<table id="table_bpb_rfv_5cb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Single choice facets object. Returns an error when:-   A duplicate label or ID is found.
-   A label or ID is not defined.

</td></tr></tbody>
</table>Can only be used in a facet generation script in a Service Portal advanced search source.

```
var stateFacet = facetService.createFacet("State", "state");
```

## SPScriptedFacetService - createMultiChoiceFacet\(String label, String id\)

Creates a multi choice facets object.

After creating the facets object, add facet items or mapped queries to the facet using the addFacetItem\(\) method of the SPScriptedFacet class.

|Name|Type|Description|
|----|----|-----------|
|label|String|Label for the facet.|
|id|String|ID for the facet.|

<table id="table_bpb_rfv_5cb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Multi choice facets object. Returns an error when:

 -   A duplicate label or ID is found.
-   A label or ID is not defined.

</td></tr></tbody>
</table>```
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

