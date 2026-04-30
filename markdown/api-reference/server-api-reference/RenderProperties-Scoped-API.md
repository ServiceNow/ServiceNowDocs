---
title: RenderProperties - Scoped
description: The RenderProperties API provides methods to obtain information about the current page and is available in Jelly scripts and in UI-action conditions and scripts.Returns the encoded query from the URL sent to the page.Returns the list control object for the page.Returns the value of the specified URL parameter.Returns the URL where the request originated.Returns the name of the view in use.Returns the window's properties.Returns true if the page is part of Studio.Returns true if this is an interactive session. An interactive session is when a user has logged in as opposed to a REST request.Returns true when the sysparm\_collection\_related\_file URL parameter is set.Returns true when the sys\_is\_related\_list URL-parameter is true. Returns false if the parameter is not present.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# RenderProperties- Scoped

The RenderProperties API provides methods to obtain information about the current page and is available in Jelly scripts and in UI-action conditions and scripts.

Access RenderProperties methods using the static variable `RP`.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Scoped RenderProperties - getEncodedQuery\(\)

Returns the encoded query from the URL sent to the page.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Encoded query from the URL sent to the form.|

The following example is used in a condition for UI action named listed in the UI Actions \[sys\_ui\_action\] table. See also [UI actions](https://www.servicenow.com/docs/access?context=c_UIActions&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

```
RP.getEncodedQuery() != null && (RP.getEncodedQuery().indexOf('table=global') < 0 && RP.getEncodedQuery().indexOf('table=') >= 0)
```

## Scoped RenderProperties - getListControl\(\)

Returns the list control object for the page.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|ScopedSysListControl object|Lst control object for the page.|

The following example is used in a condition named New for CAB Agenda Items. This UI action is listed in the UI Actions \[sys\_ui\_action\] table. See also [UI actions](https://www.servicenow.com/docs/access?context=c_UIActions&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

```
current.canCreate() && !RP.getListControl().isOmitNewButton() && RP.isRelatedList() && !RP.isManyToMany() && !RP.isInDevStudio() && (new sn_change_cab.CABMeeting(parent)).canAddAgendaItem()
```

## Scoped RenderProperties - getParameterValue\(String parameterName\)

Returns the value of the specified URL parameter.

|Name|Type|Description|
|----|----|-----------|
|parameterName|String|Name of the parameter passed on the URL.|

|Type|Description|
|----|-----------|
|String|The parameter's value.|

The following example is used in a condition for the Insert and Stay UI action for configuration items listed in the UI Actions \[sys\_ui\_action\] table. See also [UI actions](https://www.servicenow.com/docs/access?context=c_UIActions&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

```
current.canCreate() && (!current.instanceOf('task') || gs.getProperty('glide.ui.task.insert') == 'true') && (!current.instanceOf('sys_db_object')) && JSUtil.nil(RP.getParameterValue("sysparm_changeset"))
```

## Scoped RenderProperties - getReferringURL\(\)

Returns the URL where the request originated.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|URL of the page where the request originated.|

The following example is used in a condition for the Import Sets UI action for import set row listed in the UI Actions \[sys\_ui\_action\] table. See also [UI actions](https://www.servicenow.com/docs/access?context=c_UIActions&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

```
RP.getReferringURL().indexOf("sys_import_set.do") == -1 && new global.ImportSetRowHelper().canReadImportSets();
```

## Scoped RenderProperties - getViewName\(\)

Returns the name of the view in use.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the view being used.|

The following example is used in a condition named New for action assignment. This UI action is listed in the UI Actions \[sys\_ui\_action\] table. See also [UI actions](https://www.servicenow.com/docs/access?context=c_UIActions&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

```
RP.getViewName() != '' && RP.getViewName() != null && RP.getViewName() != undefined
```

## Scoped RenderProperties - getWindowProperties\(\)

Returns the window's properties.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Window's properties.|

## Scoped RenderProperties - isInDevStudio\(\)

Returns true if the page is part of Studio.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_pcv_yxz_yx" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the page is part of Studio.Possible values:

-   true: Page is part of Studio.
-   false: Page isn't part of Studio.

</td></tr></tbody>
</table>The following example is used in a condition named New for CAB Agenda Items. This UI action is listed in the UI Actions \[sys\_ui\_action\] table. See also [UI actions](https://www.servicenow.com/docs/access?context=c_UIActions&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

```
current.canCreate() && !RP.getListControl().isOmitNewButton() && RP.isRelatedList() && !RP.isManyToMany() && !RP.isInDevStudio() && (new sn_change_cab.CABMeeting(parent)).canAddAgendaItem()
```

## Scoped RenderProperties - isInteractive\(\)

Returns true if this is an interactive session. An interactive session is when a user has logged in as opposed to a REST request.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_hwd_2tz_yx" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether this is an interactive session.Possible values:

-   true: Interactive session.
-   false: Not an interactive session.

</td></tr></tbody>
</table>## Scoped RenderProperties - isManyToMany\(\)

Returns true when the `sysparm_collection_related_file` URL parameter is set.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_u2z_g4z_yx" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the `sysparm_collection_related_file` URL parameter is set.Possible values:

-   true: Parameter is set.
-   false: Parameter isn't set.

</td></tr></tbody>
</table>The following example is used in a condition named New for CAB Agenda Items. This UI action is listed in the UI Actions \[sys\_ui\_action\] table. See also [UI actions](https://www.servicenow.com/docs/access?context=c_UIActions&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

```
current.canCreate() && !RP.getListControl().isOmitNewButton() && RP.isRelatedList() && !RP.isManyToMany() && !RP.isInDevStudio() && (new sn_change_cab.CABMeeting(parent)).canAddAgendaItem()
```

## Scoped RenderProperties - isRelatedList\(\)

Returns true when the `sys_is_related_list` URL-parameter is true. Returns false if the parameter is not present.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_xwh_xlz_yx" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the URL parameter `sys_is_related_list` is set to `true`.Possible values:

-   true: `sys_is_related_list` is set to `true`.
-   false: `sys_is_related_list` is set to `false`.

</td></tr></tbody>
</table>The following example is used in a condition for a UI action listed in the UI Actions \[sys\_ui\_action\] table. See also [UI actions](https://www.servicenow.com/docs/access?context=c_UIActions&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

```
current.canCreate() && RP.isRelatedList()
```

