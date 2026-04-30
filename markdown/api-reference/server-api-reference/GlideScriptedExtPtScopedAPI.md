---
title: GlideScriptedExtensionPoint - Scoped
description: The GlideScriptedExtensionPoint API provides a method that returns the extension instances associated with a specified extension point.Returns the extension instances associated with a specified extension point.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideScriptedExtensionPoint- Scoped

The GlideScriptedExtensionPoint API provides a method that returns the extension instances associated with a specified extension point.

From these extension instances, you can extend the functionality of an application without altering the original application code. You can use pre-existing extension points available in selected ServiceNow AI Platform applications, or you can add extension points when you develop custom applications in your own instance.

This API is available in the base ServiceNow instance.

For more information on extension points, see [Using extension points to extend application functionality](../../../../../build/applications/concept/extension-points.md).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideScriptedExtensionPoint - getExtensions\(String name\)

Returns the extension instances associated with a specified extension point.

These extension instances are persisted in the Extension Instance \[sys\_extension\_instance\] table. For more information on extension points, see [Using extension points to extend application functionality](../../../../../build/applications/concept/extension-points.md).

**Note:** The script include instances returned by the getExtensions\(\) method are uninitialized. If your interface includes an initialize method, call that method before calling other methods on the returned instance. For example:

```
var eps = new GlideScriptedExtensionPoint().getExtensions("RelatedListItemCandidateFilter");
 for (var i = 0; i < eps.length; i++) {    
   eps[i].initialize(tableName, parentFieldName, parentRecordSysId, referencedFieldName);
   eps[i].getFilterQuery();
 }
```

<table id="table_tkf_cgt_x5b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

String

</td><td>

Name of the extension point for which to return the extension instances.Table: Extension Instance \[sys\_extension\_instance\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Array of Objects|Extension instances associated with the specified endpoint.|

The following code example returns the extension instances for the RelatedListItemCandidateFilter extension point. The "class" listed for each instance represents a script include.

```
var eps = new GlideScriptedExtensionPoint().getExtensions("RelatedListItemCandidateFilter");
```

Response:

```
global.RelatedListItemCandidateFilter RelatedListItemCandidateFilter
global.RelatedListItemCandidateFilter ProblemRelatedListChangeRequestItemFilter
global.RelatedListItemCandidateFilter RelatedListConfigItemFilter
global.RelatedListItemCandidateFilter RelatedListItemCandidateFilterForAgileDevelopment
global.RelatedListItemCandidateFilter ProblemRelatedListIncidentItemFilter
global.RelatedListItemCandidateFilter RelatedListIncidentItemCandidateFilter
global.RelatedListItemCandidateFilter RelatedListCIItemCandidateFilter
```

