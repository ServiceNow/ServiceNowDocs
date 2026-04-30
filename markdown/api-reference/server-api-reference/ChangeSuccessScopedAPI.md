---
title: ChangeSuccess - Scoped
description: The ChangeSuccess script include provides methods that return the Performance Analytics \(PA\) success scores for change requests \(original change success score based on group\), change models, and change types.Returns the value specified in the system property com.snc.change\_management.success\_score.entry\_level\_score.Returns the value specified in the system property com.snc.change\_management.success\_score.maximum\_score.Returns the value specified in the system property com.snc.change\_management.success\_score.minimum\_score.Returns the latest model success score based on the specified change request GlideRecord.Returns the latest model success score for the specified model sys\_id.Returns the latest change team success score \(original change success score based on group\), model success score, and type success score based on the specified change request GlideRecord.Returns the latest change team success score \(original change success score based on group\) based on the specified change request GlideRecord.Returns the latest change team success score \(original change success score based on group\) for the specified group.Returns the latest type success score based on the specified change request GlideRecord.Returns the latest type success score for the specified change type.Controls whether the associated method returns the details of the Performance Analytics \(PA\) indicators used to generate each of the different types of scores \(team, model and type\). By default, this information is not returned.Only valid when called with the getScoresForChange\(\) method. Controls whether the getScoresForChange\(\) method returns the model score. By default the model score is returned.Controls whether the method validates the user calling the associated method, ensuring that they have the rights to read the requested content.Only valid when called with the getScoresForChange\(\) method. Controls whether the getScoresForChange\(\) method returns the team score. By default the team score is returned.Controls whether the associated method returns the details for all change success score rating records. By default, this information is not returned.Only valid when called with the getScoresForChange\(\) method. Controls whether the getScoresForChange\(\) method returns the type score. By default the type score is returned.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 102
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ChangeSuccess- Scoped

The ChangeSuccess script include provides methods that return the Performance Analytics \(PA\) success scores for change requests \(original change success score based on group\), change models, and change types.

This script include also provides helper methods that enable you to modify the return results of the getScoresForChange\(\) method, which by default returns all three success scores. Using these helper methods, you can determine whether or not to return any of the success scores. You can also use these helper methods to provide return results with success score ratings or the PA indicators used to generate different types of scores for any method that returns a success score. In addition, you can request that the associated method bypass the access rights security check that is by default performed for each method.

You associate helper methods to a primary method using dot nomenclature such as the following:

`new sn_chg_score.ChangeSuccess().withTeamScore(false).withTypeScore(false).withSecurity(false).getScoresForChange(chgGr);`

`new sn_chg_score.ChangeSuccess().withRatings().withIndicatorScores().getTeamScoreForGroupId("287ebd7da9fe198100f92cc8d1d2154e");`

There are also methods that enable you to obtain the current values of specific Change Management system properties, such as com.snc.change\_management.success\_score.minimum\_score, com.snc.change\_management.success\_score.maximum\_score, and com.snc.change\_management.success\_score.entry\_level\_score. For a description of their functionality, see [Change Management properties](https://www.servicenow.com/docs/access?context=r_ChangeManagementProperties&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

This API runs in the `sn_chg_score` namespace and the Change Management - Change Success Score \(com.snc.change\_management.change\_success\_score\) plugin must be activated.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ChangeSuccess - getEntryLevelTeamScore\(\)

Returns the value specified in the system property com.snc.change\_management.success\_score.entry\_level\_score.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Current value of com.snc.change\_management.success\_score.entry\_level\_score. If this system property does not exist, the method uses a default value of 500 in the success score calculations.|

The following code example shows how to call this method.

```
gs.info(new sn_chg_score.ChangeSuccess().getEntryLevelTeamScore());
```

Return results:

```
500
```

## ChangeSuccess - getMaximumPermittedTeamScore\(\)

Returns the value specified in the system property com.snc.change\_management.success\_score.maximum\_score.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Current value of com.snc.change\_management.success\_score.maximum\_score. If the system property does not exist, the method uses a default value of 850 in the success score calculations.|

This code example shows how to obtain the maximum permitted team score \(com.snc.change\_management.success\_score.maximum\_score\) value.

```
gs.info(new sn_chg_score.ChangeSuccess().getMaximumPermittedTeamScore());
```

Return results:

```
850
```

## ChangeSuccess - getMinimumPermittedTeamScore\(\)

Returns the value specified in the system property com.snc.change\_management.success\_score.minimum\_score.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Current value of com.snc.change\_management.success\_score.minimum\_score. If this system property does not exist, the method uses a default value of 0 in the success score calculations.|

The following code example shows how to call this method.

```
gs.info(new sn_chg_score.ChangeSuccess().getMinimumPermittedTeamScore());
```

Return results:

```
0
```

## ChangeSuccess - getModelScoreForChange\(Object chgGr\)

Returns the latest model success score based on the specified change request GlideRecord.

|Name|Type|Description|
|----|----|-----------|
|chgGr|Object|Change request GlideRecord for which to return the model success score.|

<table><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr id="can_read-chg_model-row"><td>

can\_read

</td><td id="can_read-chg_model-entry">

Flag that indicates whether a model success score could be retrieved for the specified change request.Valid values:

-   true: Model success score was retrieved.
-   false: Model success score was not retrieved.

 Data type: Boolean

</td></tr><tr id="chg_model-chg_model-row"><td>

chg\_model

</td><td id="chg_model-chg_model-entry">

Individual objects for each field in the Change Model \[chg\_model\] record referenced by the specified change request. Each object has a key that is the field name and contains value and display\_value properties. If the field type is date/time, then the method also returns a display\_value\_internal property which is in the user's timezone but in the system format YYYY-MM-DD HH24:MM:SS.```
"chg_model": {
  "active": {Object},
  "advanced_security": {Object},
  "available_in_ui": {Object},
  "color": {Object},
  "default_change_model": {Object},
  "description": {Object},
  "implementation_states": {Object},
  "name": {Object},
  "read_roles": {Object},
  "record_preset": {Object},
  "state_field": {Object},
  "sys_class_name": {Object},
  "sys_created_by": {Object},
  "sys_created_on": {Object},
  "sys_domain": {Object},
  "sys_domain_path": {Object},
  "sys_id": {Object},
  "sys_mod_count": {Object},
  "sys_name": {Object},
  "sys_tags": {Object},
  "sys_updated_by": {Object},
  "sys_updated_name": {Object},
  "sys_updated_on": {Object},
  "table_name": {Object},
  "write_roles": {Object}
}
```

 Data type: Object

</td></tr><tr id="active-chg_model-row"><td>

chg\_model.active

</td><td id="active-chg_model-entry">

Flag that indicates whether the associated change model record is active and available within the instance.Valid values:

-   true: Change model is active.
-   false: Change model is not active.

 Data type: Object

 ```
"active": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr id="active_display_value-chg_model-row"><td>

chg\_model.active.display\_value

</td><td id="active_display_value-chg_model-entry">

Display value for the active flag.Data type: String

</td></tr><tr id="active_value-chg_model-row"><td>

chg\_model.active.value

</td><td id="active_value-chg_model-entry">

Internal value for the active flag.Data type: Boolean

</td></tr><tr id="advanced_security-chg_model-row"><td>

chg\_model.advanced\_security

</td><td id="advanced_security-chg_model-entry">

Flag that indicates whether user criteria based security is being used in addition to role based security for this change model.Valid values:

-   true: Advanced security is used.
-   false: Advanced security in not used.

 Data type: Object

 ```
"advanced_security": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr id="advanced_security_display_value-chg_model-row"><td>

chg\_model.advanced\_security.display\_value

</td><td id="advanced_security_display_value-chg_model-entry">

Display value for the advanced\_security flag.Data type: String

</td></tr><tr id="advanced_security_value-chg_model-row"><td>

chg\_model.advanced\_security.value

</td><td id="advanced_security_value-chg_model-entry">

Internal value for the advanced\_security flag.Data type: Boolean

</td></tr><tr id="available_in_ui-chg_model-row"><td>

chg\_model.available\_in\_ui

</td><td id="available_in_ui-chg_model-entry">

Flag that indicates whether the associated change model record is available within the user interface.Valid values:

-   true: Change model is available in the user interface.
-   false: Change model is not available in the user interface.

 Data type: Object

 ```
"available_in_ui": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr id="available_in_ui_display_value-chg_model-row"><td>

chg\_model.available\_in\_ui.display\_value

</td><td id="available_in_ui_display_value-chg_model-entry">

Display value for the available\_in\_ui flag.Data type: String

</td></tr><tr id="available_in_ui_value-chg_model-row"><td>

chg\_model.available\_in\_ui.value

</td><td id="available_in_ui_value-chg_model-entry">

Value for the available\_in\_ui flag.Data type: Boolean

</td></tr><tr id="color-chg_model-row"><td>

chg\_model.color

</td><td id="color-chg_model-entry">

Color of the associated change model on the change request landing page.Data type: Object

 ```
"color": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="color_display_value-chg_model-row"><td>

chg\_model.color.display\_value

</td><td id="color_display_value-chg_model-entry">

Display value for color.Data type: String

</td></tr><tr id="color_value-chg_model-row"><td>

chg\_model.color.value

</td><td id="color_value-chg_model-entry">

Internal value for color.Data type: String

</td></tr><tr id="default_change_model-chg_model-row"><td>

chg\_model.default\_change\_model

</td><td id="default_change_model-chg_model-entry">

Flag that indicates whether the associated change model record is the default change model.Possible values:

-   true: Default
-   false: Not the default

 Data type: Object

 ```
"default_change_model": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr id="default_change_model_display_value-chg_model-row"><td>

chg\_model.default\_change\_model.display\_value

</td><td id="default_change_model_display_value-chg_model-entry">

Display value for the default change model flag.Data type: String

</td></tr><tr id="default_change_model_value-chg_model-row"><td>

chg\_model.default\_change\_model.value

</td><td id="default_change_model_value-chg_model-entry">

Internal value for the default change model flag.Data type: Boolean

</td></tr><tr id="description-chg_model-row"><td>

chg\_model.description

</td><td id="description-chg_model-entry">

Short description of the purpose of the change model.Data type: Object

 ```
"description": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="description_display_value-chg_model-row"><td>

chg\_model.description.display\_value

</td><td id="description_display_value-chg_model-entry">

Display value for description.Data type: String

</td></tr><tr id="description_value-chg_model-row"><td>

chg\_model.description.value

</td><td id="description_value-chg_model-entry">

Internal value for description.Data type: String

</td></tr><tr id="implementation_states-chg_model-row"><td>

chg\_model.implementation\_states

</td><td id="implementation_states-chg_model-entry">

List of sys\_ids of states for which change requests using this model can be implemented.Data type: Object

 ```
"implementation_states": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="implementation_states_display_value-chg_model-row"><td>

chg\_model.implementation\_states.display\_value

</td><td id="implementation_states_display_value-chg_model-entry">

Display value for read\_roles.Data type: String

</td></tr><tr id="implementation_states_value-chg_model-row"><td>

chg\_model.implementation\_states.value

</td><td id="implementation_states_value-chg_model-entry">

Internal value for read\_roles.Data type: String

</td></tr><tr id="name-chg_model-row"><td>

chg\_model.name

</td><td id="name-chg_model-entry">

Name of the change model.Data type: Object

 ```
"name": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="name-chg_model_display_value-row"><td>

chg\_model.name.display\_value

</td><td id="name-chg_model_display_value-entry">

Display value for name.Data type: String

</td></tr><tr id="name_value-chg_model-row"><td>

chg\_model.name.value

</td><td id="name_value-chg_model-entry">

Internal value for name.Data type: String

</td></tr><tr id="read_roles-chg_model-row"><td>

chg\_model.read\_roles

</td><td id="read_roles-chg_model-entry">

Security roles needed to read the change model record.Data type: Object

 ```
"read_roles": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="read_roles_display_value-chg_model-row"><td>

chg\_model.read\_roles.display\_value

</td><td id="read_roles_display_value-chg_model-entry">

Display value for read\_roles.Data type: String

</td></tr><tr id="read_roles_value-chg_model-row"><td>

chg\_model.read\_roles.value

</td><td id="read_roles_value-chg_model-entry">

Internal value for read\_roles.Data type: String

</td></tr><tr id="record_preset-chg_model-row"><td>

chg\_model.record\_preset

</td><td id="record_preset-chg_model-entry">

Name-value pairs of the fields that should automatically be populated, with their associated values, when a new change request record is created. Values are separated by caret symbols.For example:

 `"type=normal^assignment_group=a715cd759f2002002920bde8132e7018^short_description=Automated : Change^EQ"`

 Data type: Object

 ```
"record_preset": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="record_preset_display_value-chg_model-row"><td>

chg\_model.record\_preset.display\_value

</td><td id="record_preset_display_value-chg_model-entry">

Display value for record\_preset.Data type: String

</td></tr><tr id="record_preset_value-chg_model-row"><td>

chg\_model.record\_preset.value

</td><td id="record_preset_value-chg_model-entry">

Internal value for record\_preset.Data type: String

</td></tr><tr id="state_field-chg_model-row"><td>

chg\_model.state\_field

</td><td id="state_field-chg_model-entry">

Choice list field from which to collect choices, based on the value provided in **table\_name**. For change models, this is always set to "state".Data type: Object

 ```
"state_field": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="state_field_display_value-chg_model-row"><td>

chg\_model.state\_field.display\_value

</td><td id="state_field_display_value-chg_model-entry">

Display value for state\_field.Data type: String

</td></tr><tr id="state_field_value-chg_model-row"><td>

chg\_model.state\_field.value

</td><td id="state_field_value-chg_model-entry">

Internal value for state\_field.Data type: String

</td></tr><tr id="sys_class_name-chg_model-row"><td>

chg\_model.sys\_class\_name

</td><td id="sys_class_name-chg_model-entry">

Change module table name. Always Change Model/chg\_model.Data type: Object

 ```
"sys_class_name": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_class_name_display_value-chg_model-row"><td>

chg\_model.sys\_class\_name.display\_value

</td><td id="sys_class_name_display_value-chg_model-entry">

Display value for sys\_class\_name.Data type: String

</td></tr><tr id="sys_class_name_value-chg_model-row"><td>

chg\_model.sys\_class\_name.display\_value

</td><td id="sys_class_name_value-chg_model-entry">

Internal value for sys\_class\_name.Data type: String

</td></tr><tr id="sys_created_by-chg_model-row"><td>

chg\_model.sys\_created\_by

</td><td id="sys_created_by-chg_model-entry">

Name of the user that initially created the associated change module record. Data type: Object

 ```
"sys_created_by": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_created_by_display_value-chg_model-row"><td>

chg\_model.sys\_created\_by.display\_value

</td><td id="sys_created_by_display_value-chg_model-entry">

Display value for sys\_created\_by.Data type: String

</td></tr><tr id="sys_created_by_value-chg_model-row"><td>

chg\_model.sys\_created\_by.value

</td><td id="sys_created_by_value-chg_model-entry">

Internal value for sys\_created\_by.Data type: String

</td></tr><tr id="sys_created_on-chg_model-row"><td>

chg\_model.sys\_created\_on

</td><td id="sys_created_on-chg_model-entry">

Date and time that the change module record was originally created.Data type: Object

 ```
"sys_created_on": {
  "display_value": "String",
  "display_value_internal": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_created_on_display_value-chg_model-row"><td>

chg\_model.sys\_created\_on.display\_value

</td><td id="sys_created_on_display_value-chg_model-entry">

Display value for sys\_created\_on.Data type: String

</td></tr><tr id="sys_created_on_display_value_internal-chg_model-row"><td>

chg\_model.sys\_created\_on.display\_value\_internal

</td><td id="sys_created_on_display_value_internal-chg_model-entry">

Internal display value for sys\_created\_on.Data type: String

</td></tr><tr id="sys_created_on_value-chg_model-row"><td>

chg\_model.sys\_created\_on.value

</td><td id="sys_created_on_value-chg_model-entry">

Internal value for sys\_created\_on.Data type: String

</td></tr><tr id="sys_domain-chg_model-row"><td>

chg\_model.sys\_domain

</td><td id="sys_domain-chg_model-entry">

If using domains in the instance, the name of the domain to which the change module record is associated.Data type: Object

 ```
"sys_domain": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_domain_display_value-chg_model-row"><td>

chg\_model.sys\_domain.display\_value

</td><td id="sys_domain_display_value-chg_model-entry">

Display value for sys\_domain.Data type: String

</td></tr><tr id="sys_domain_value-chg_model-row"><td>

chg\_model.sys\_domain.value

</td><td id="sys_domain_value-chg_model-entry">

Internal value for sys\_domain.Data type: String

</td></tr><tr id="sys_domain_path-chg_model-row"><td>

chg\_model.sys\_domain\_path

</td><td id="sys_domain_path-chg_model-entry">

If using domains in the instance, the domain path in which the associated change module record resides.Data type: Object

 ```
"sys_domain_path": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_domain_path_display_value-chg_model-row"><td>

chg\_model.sys\_domain\_path.display\_value

</td><td id="sys_domain_path_display_value-chg_model-entry">

Display value for sys\_domain\_path.Data type: String

</td></tr><tr id="sys_domain_path_value-chg_model-row"><td>

chg\_model.sys\_domain\_path.value

</td><td id="sys_domain_path_value-chg_model-entry">

Internal value for sys\_domain\_path.Data type: String

</td></tr><tr id="sys_id-chg_model-row"><td>

chg\_model.sys\_id

</td><td id="sys_id-chg_model-entry">

Unique identifier of the associated change model record.Data type: Object

 ```
"sys_id": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_id_display_value-chg_model-row"><td>

chg\_model.sys\_id.display\_value

</td><td id="sys_id_display_value-chg_model-entry">

Display value for sys\_id.Data type: String

</td></tr><tr id="sys_id_value-chg_model-row"><td>

chg\_model.sys\_id.value

</td><td id="sys_id_value-chg_model-entry">

Internal value for sys\_id.Data type: String

</td></tr><tr id="sys_mod_count-chg_model-row"><td>

chg\_model.sys\_mod\_count

</td><td id="sys_mod_count-chg_model-entry">

Number of times that the associated change model record has been modified.Data type: Object

 ```
"sys_mod_count": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr id="sys_mod_count_display_value-chg_model-row"><td>

chg\_model.sys\_mod\_count.display\_value

</td><td id="sys_mod_count_display_value-chg_model-entry">

Display value for sys\_mod\_count.Data type: String

</td></tr><tr id="sys_mod_count_value-chg_model-row"><td>

chg\_model.sys\_mod\_count.value

</td><td id="sys_mod_count_value-chg_model-entry">

Internal value for sys\_mod\_count.Data type: Number

</td></tr><tr id="sys_name-chg_model-row"><td>

chg\_model.sys\_name

</td><td id="sys_name-chg_model-entry">

Name of the change model. Always the same as the **name** parameter.Data type: Object

 ```
"sys_name": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_name_display_value-chg_model-row"><td>

chg\_model.sys\_name.display\_value

</td><td id="sys_name_display_value-chg_model-entry">

Display value for sys\_name.Data type: String

</td></tr><tr id="sys_name_value-chg_model-row"><td>

chg\_model.sys\_name.value

</td><td id="sys_name_value-chg_model-entry">

Internal value for sys\_name.Data type: String

</td></tr><tr id="sys_tags-chg_model-row"><td>

chg\_model.sys\_tags

</td><td id="sys_tags-chg_model-entry">

System tags associated with the change model record.Data type: Object

 ```
"sys_tags": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_tags_display_value-chg_model-row"><td>

chg\_model.sys\_tags.display\_value

</td><td id="sys_tags_display_value-chg_model-entry">

Display value for sys\_tags.Data type: String

</td></tr><tr id="sys_tags_value-chg_model-row"><td>

chg\_model.sys\_tags.value

</td><td id="sys_tags_value-chg_model-entry">

Internal value for sys\_tags.Data type: String

</td></tr><tr id="sys_updated_by-chg_model-row"><td>

chg\_model.sys\_updated\_by

</td><td id="sys_updated_by-chg_model-entry">

Name of the user that last updated the associated change model record.Data type: Object

 ```
"sys_updated_by": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_updated_by_display_value-chg_model-row"><td>

chg\_model.sys\_updated\_by.display\_value

</td><td id="sys_updated_by_display_value-chg_model-entry">

Display value for sys\_updated\_by.Data type: String

</td></tr><tr id="sys_updated_by_value-chg_model-row"><td>

chg\_model.sys\_updated\_by.value

</td><td id="sys_updated_by_value-chg_model-entry">

Internal value for sys\_updated\_by.Data type: String

</td></tr><tr id="sys_updated_on-chg_model-row"><td>

chg\_model.sys\_updated\_on

</td><td id="sys_updated_on-chg_model-entry">

Date and time the associated change model record was last updated.Data type: Object

 ```
"sys_updated_on": {
  "display_value": "String",
  "display_value_internal": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_updated_on_display_value-chg_model-row"><td>

chg\_model.sys\_updated\_on.display\_value

</td><td id="sys_updated_on_display_value-chg_model-entry">

Display value for sys\_updated\_on.Data type: String

</td></tr><tr id="sys_updated_on_display_value_internal-chg_model-row"><td>

chg\_model.sys\_updated\_on.display\_value\_internal

</td><td id="sys_updated_on_display_value_internal-chg_model-entry">

Internal display value for sys\_updated\_on.Data type: String

</td></tr><tr id="sys_updated_on_value-chg_model-row"><td>

chg\_model.sys\_updated\_on.value

</td><td id="sys_updated_on_value-chg_model-entry">

Internal value for sys\_updated\_on.Data type: String

</td></tr><tr id="table_name-chg_model-row"><td>

chg\_model.table\_name

</td><td id="table_name-chg_model-entry">

Table that defines the Choice list field from which to collect choices. For change models this is always set to "change\_request".Data type: Object

 ```
"table_name": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="table_name_display_value-chg_model-row"><td>

chg\_model.table\_name.display\_value

</td><td id="table_name_display_value-chg_model-entry">

Display value for table\_name.Data type: String

</td></tr><tr id="table_name_value-chg_model-row"><td>

chg\_model.table\_name.value

</td><td id="table_name_value-chg_model-entry">

Internal value for table\_name.Data type: String

</td></tr><tr id="write_roles-chg_model-row"><td>

chg\_model.write\_roles

</td><td id="write_roles-chg_model-entry">

Security roles needed to write to the change model record.Data type: Object

 ```
"write_roles": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="write_roles_display_value-chg_model-row"><td>

chg\_model.write\_roles.display\_value

</td><td id="write_roles_display_value-chg_model-entry">

Display value for write\_roles.Data type: String

</td></tr><tr id="write_roles_value-chg_model-row"><td>

chg\_model.write\_roles.value

</td><td id="write_roles_value-chg_model-entry">

Internal value for write\_roles.Data type: String

</td></tr><tr id="score-chg_suc-row"><td>

score

</td><td id="score-chg_suc-entry">

Details about the returned score indicator.Data type: Object

 ```
"score": {
  "delta": {Object},
  "display_value": "String",
  "has_score": Boolean,
  "indicator": {Object},
  "value": Number
}
```

</td></tr><tr id="score_delta-chg_suc-row"><td>

score.delta

</td><td id="score_delta-chg_suc-entry">

Change in the score from the previous score.Data type: Object

 ```
"delta": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="score_delta_display_value-chg_suc-row"><td>

score.delta.display\_value

</td><td id="score_delta_display_value-chg_suc-entry">

Display value for delta.Data type: String

</td></tr><tr id="score_delta_value-chg_suc-row"><td>

score.delta.value

</td><td id="score_delta_value-chg_suc-entry">

Internal value for delta.Data type: String

</td></tr><tr id="score_display_value-chg_suc-row"><td>

score.display\_value

</td><td id="score_display_value-chg_suc-entry">

Display value returned by Performance Analytics \(PA\).Data type: String

</td></tr><tr id="score_has_score-chg_suc-row"><td>

score.has\_score

</td><td id="score_has_score-chg_suc-entry">

Flag that indicates whether a score was returned for the specified change request.

 Valid values:

-   true: Score was returned.
-   false: No score was returned.

 Data type: Boolean

</td></tr><tr id="score_indicator-chg_suc-row"><td>

score.indicator

</td><td id="score_indicator-chg_suc-entry">

Additional details on the PA indicator used to obtain the score.Data type: Object

 ```
"indicator": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="score_indicator_name-chg_suc-row"><td>

score.indicator.name

</td><td id="score_indicator_name-chg_suc-entry">

Name of the PA indicator used to obtain the score.Data type: String

</td></tr><tr id="score_indicator_sys_id-chg_suc-row"><td>

score.indicator.sys\_id

</td><td id="score_indicator_sys_id-chg_suc-entry">

Sys\_id of the PA indicator used to obtain the score.Data type: String

</td></tr><tr id="score_value-chg_suc-row"><td>

score.value

</td><td id="score_value-chg_suc-entry">

Value returned by PA for the success score.Data type: String

</td></tr></tbody>
</table>This code example shows how to retrieve the latest model success score for the current change models GlideRecord, check if the user has read access to that change model, and if so, make an entry in the work notes if the success score value that is less than 50%.

```
var changeModelSuccess = new sn_chg_score.ChangeSuccess().getModelScoreForChange(current);
 
gs.info(JSON.stringify(changeModelSuccess,null,2));
 
if (changeModelSuccess.can_read && changeModelSuccess.score.has_score && changeModelSuccess.score.value < 50) {
   chgGr.work_notes.setJournalEntry("The selected Change Model of \"" + changeModelSuccess.chg_model.name.display_value + "\" has a success rate of less than 50% (current success rate is: " + changeModelSuccess.score.display_value + "%).\nConsider using a different Model or adding additional approvers or discuss with your Change Manager.");
   chgGr.update();
}
```

Example of the return results when calling this method:

```
{
  "can_read": true,
  "chg_model": {
    "color": {
      "display_value": "",
      "value": ""
    },
    "default_change_model": {
      "display_value": "false",
      "value": false
    },
    "description": {
      "display_value": "This model can be used to capture unauthorized change events that were detected.",
      "value": "This model can be used to capture unauthorized change events that were detected."
    },
    "sys_updated_on": {
      "display_value": "2020-10-21 11:10:57",
      "value": "2020-10-21 10:10:57",
      "display_value_internal": "2020-10-21 11:10:57"
    },
    "table_name": {
      "display_value": "change_request",
      "value": "change_request"
    },
    "sys_class_name": {
      "display_value": "Change Model",
      "value": "chg_model"
    },
    "sys_id": {
      "display_value": "aedc6a625323101034d1ddeeff7b1296",
      "value": "aedc6a625323101034d1ddeeff7b1296"
    },
    "sys_updated_by": {
      "display_value": "admin",
      "value": "admin"
    },
    "write_roles": {
      "display_value": "",
      "value": ""
    },
    "sys_created_on": {
      "display_value": "2020-10-02 14:50:20",
      "value": "2020-10-02 13:50:20",
      "display_value_internal": "2020-10-02 14:50:20"
    },
    "read_roles": {
      "display_value": "itil,sn_change_read",
      "value": "itil,sn_change_read"
    },
    "sys_name": {
      "display_value": "Unauthorized Change",
      "value": "Unauthorized Change"
    },
    "advanced_security": {
      "display_value": "false",
      "value": false
    },
    "sys_created_by": {
      "display_value": "admin",
      "value": "admin"
    },
    "record_preset": {
      "display_value": "type=emergency^short_description=An unauthorized change has been detected^assignment_group=a715cd759f2002002920bde8132e7018^work_start=javascript:gs.nowDateTime()^unauthorized=true^EQ",
      "value": "type=emergency^short_description=An unauthorized change has been detected^assignment_group=a715cd759f2002002920bde8132e7018^work_start=javascript:gs.nowDateTime()^unauthorized=true^EQ"
    },
    "sys_mod_count": {
      "display_value": "9",
      "value": 9
    },
    "active": {
      "display_value": "true",
      "value": true
    },
    "sys_tags": {
      "display_value": "",
      "value": ""
    },
    "available_in_ui": {
      "display_value": "false",
      "value": false
    },
    "state_field": {
      "display_value": "state",
      "value": "state"
    },
    "name": {
      "display_value": "Unauthorized Change",
      "value": "Unauthorized Change"
    },
    "implementation_states": {
      "display_value": "",
      "value": ""
    }
  },
  "score": {
    "indicator": {
      "name": "Change Model: % Successful and Successful With Issues",
      "sys_id": "604f98dfc302011005aea539e540dd75"
    },
    "value": 76.92307692307693,
    "display_value": "76.92",
    "delta": {
      "value": "0",
      "display_value": ""
    },
    "has_score": true
  }
}
```

## ChangeSuccess - getModelScoreForModelId\(String sys\_id, String domain\_id\)

Returns the latest model success score for the specified model sys\_id.

|Name|Type|Description|
|----|----|-----------|
|sys\_id|String|Sys\_id of the group for which to return the model success score. Located in the User Group \[sys\_user\_grou\] table.|
|domain\_id|String|Optional. Sys\_id of a domain to use when querying Performance Analytics for the model success score.|

<table id="id_plb_kfk_ptb"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr id="can_read-chg_model-row"><td>

can\_read

</td><td id="can_read-chg_model-entry">

Flag that indicates whether a model success score could be retrieved for the specified change request.Valid values:

-   true: Model success score was retrieved.
-   false: Model success score was not retrieved.

 Data type: Boolean

</td></tr><tr id="chg_model-chg_model-row"><td>

chg\_model

</td><td id="chg_model-chg_model-entry">

Individual objects for each field in the Change Model \[chg\_model\] record referenced by the specified change request. Each object has a key that is the field name and contains value and display\_value properties. If the field type is date/time, then the method also returns a display\_value\_internal property which is in the user's timezone but in the system format YYYY-MM-DD HH24:MM:SS.```
"chg_model": {
  "active": {Object},
  "advanced_security": {Object},
  "available_in_ui": {Object},
  "color": {Object},
  "default_change_model": {Object},
  "description": {Object},
  "implementation_states": {Object},
  "name": {Object},
  "read_roles": {Object},
  "record_preset": {Object},
  "state_field": {Object},
  "sys_class_name": {Object},
  "sys_created_by": {Object},
  "sys_created_on": {Object},
  "sys_domain": {Object},
  "sys_domain_path": {Object},
  "sys_id": {Object},
  "sys_mod_count": {Object},
  "sys_name": {Object},
  "sys_tags": {Object},
  "sys_updated_by": {Object},
  "sys_updated_name": {Object},
  "sys_updated_on": {Object},
  "table_name": {Object},
  "write_roles": {Object}
}
```

 Data type: Object

</td></tr><tr id="active-chg_model-row"><td>

chg\_model.active

</td><td id="active-chg_model-entry">

Flag that indicates whether the associated change model record is active and available within the instance.Valid values:

-   true: Change model is active.
-   false: Change model is not active.

 Data type: Object

 ```
"active": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr id="active_display_value-chg_model-row"><td>

chg\_model.active.display\_value

</td><td id="active_display_value-chg_model-entry">

Display value for the active flag.Data type: String

</td></tr><tr id="active_value-chg_model-row"><td>

chg\_model.active.value

</td><td id="active_value-chg_model-entry">

Internal value for the active flag.Data type: Boolean

</td></tr><tr id="advanced_security-chg_model-row"><td>

chg\_model.advanced\_security

</td><td id="advanced_security-chg_model-entry">

Flag that indicates whether user criteria based security is being used in addition to role based security for this change model.Valid values:

-   true: Advanced security is used.
-   false: Advanced security in not used.

 Data type: Object

 ```
"advanced_security": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr id="advanced_security_display_value-chg_model-row"><td>

chg\_model.advanced\_security.display\_value

</td><td id="advanced_security_display_value-chg_model-entry">

Display value for the advanced\_security flag.Data type: String

</td></tr><tr id="advanced_security_value-chg_model-row"><td>

chg\_model.advanced\_security.value

</td><td id="advanced_security_value-chg_model-entry">

Internal value for the advanced\_security flag.Data type: Boolean

</td></tr><tr id="available_in_ui-chg_model-row"><td>

chg\_model.available\_in\_ui

</td><td id="available_in_ui-chg_model-entry">

Flag that indicates whether the associated change model record is available within the user interface.Valid values:

-   true: Change model is available in the user interface.
-   false: Change model is not available in the user interface.

 Data type: Object

 ```
"available_in_ui": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr id="available_in_ui_display_value-chg_model-row"><td>

chg\_model.available\_in\_ui.display\_value

</td><td id="available_in_ui_display_value-chg_model-entry">

Display value for the available\_in\_ui flag.Data type: String

</td></tr><tr id="available_in_ui_value-chg_model-row"><td>

chg\_model.available\_in\_ui.value

</td><td id="available_in_ui_value-chg_model-entry">

Value for the available\_in\_ui flag.Data type: Boolean

</td></tr><tr id="color-chg_model-row"><td>

chg\_model.color

</td><td id="color-chg_model-entry">

Color of the associated change model on the change request landing page.Data type: Object

 ```
"color": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="color_display_value-chg_model-row"><td>

chg\_model.color.display\_value

</td><td id="color_display_value-chg_model-entry">

Display value for color.Data type: String

</td></tr><tr id="color_value-chg_model-row"><td>

chg\_model.color.value

</td><td id="color_value-chg_model-entry">

Internal value for color.Data type: String

</td></tr><tr id="default_change_model-chg_model-row"><td>

chg\_model.default\_change\_model

</td><td id="default_change_model-chg_model-entry">

Flag that indicates whether the associated change model record is the default change model.Possible values:

-   true: Default
-   false: Not the default

 Data type: Object

 ```
"default_change_model": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr id="default_change_model_display_value-chg_model-row"><td>

chg\_model.default\_change\_model.display\_value

</td><td id="default_change_model_display_value-chg_model-entry">

Display value for the default change model flag.Data type: String

</td></tr><tr id="default_change_model_value-chg_model-row"><td>

chg\_model.default\_change\_model.value

</td><td id="default_change_model_value-chg_model-entry">

Internal value for the default change model flag.Data type: Boolean

</td></tr><tr id="description-chg_model-row"><td>

chg\_model.description

</td><td id="description-chg_model-entry">

Short description of the purpose of the change model.Data type: Object

 ```
"description": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="description_display_value-chg_model-row"><td>

chg\_model.description.display\_value

</td><td id="description_display_value-chg_model-entry">

Display value for description.Data type: String

</td></tr><tr id="description_value-chg_model-row"><td>

chg\_model.description.value

</td><td id="description_value-chg_model-entry">

Internal value for description.Data type: String

</td></tr><tr id="implementation_states-chg_model-row"><td>

chg\_model.implementation\_states

</td><td id="implementation_states-chg_model-entry">

List of sys\_ids of states for which change requests using this model can be implemented.Data type: Object

 ```
"implementation_states": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="implementation_states_display_value-chg_model-row"><td>

chg\_model.implementation\_states.display\_value

</td><td id="implementation_states_display_value-chg_model-entry">

Display value for read\_roles.Data type: String

</td></tr><tr id="implementation_states_value-chg_model-row"><td>

chg\_model.implementation\_states.value

</td><td id="implementation_states_value-chg_model-entry">

Internal value for read\_roles.Data type: String

</td></tr><tr id="name-chg_model-row"><td>

chg\_model.name

</td><td id="name-chg_model-entry">

Name of the change model.Data type: Object

 ```
"name": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="name-chg_model_display_value-row"><td>

chg\_model.name.display\_value

</td><td id="name-chg_model_display_value-entry">

Display value for name.Data type: String

</td></tr><tr id="name_value-chg_model-row"><td>

chg\_model.name.value

</td><td id="name_value-chg_model-entry">

Internal value for name.Data type: String

</td></tr><tr id="read_roles-chg_model-row"><td>

chg\_model.read\_roles

</td><td id="read_roles-chg_model-entry">

Security roles needed to read the change model record.Data type: Object

 ```
"read_roles": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="read_roles_display_value-chg_model-row"><td>

chg\_model.read\_roles.display\_value

</td><td id="read_roles_display_value-chg_model-entry">

Display value for read\_roles.Data type: String

</td></tr><tr id="read_roles_value-chg_model-row"><td>

chg\_model.read\_roles.value

</td><td id="read_roles_value-chg_model-entry">

Internal value for read\_roles.Data type: String

</td></tr><tr id="record_preset-chg_model-row"><td>

chg\_model.record\_preset

</td><td id="record_preset-chg_model-entry">

Name-value pairs of the fields that should automatically be populated, with their associated values, when a new change request record is created. Values are separated by caret symbols.For example:

 `"type=normal^assignment_group=a715cd759f2002002920bde8132e7018^short_description=Automated : Change^EQ"`

 Data type: Object

 ```
"record_preset": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="record_preset_display_value-chg_model-row"><td>

chg\_model.record\_preset.display\_value

</td><td id="record_preset_display_value-chg_model-entry">

Display value for record\_preset.Data type: String

</td></tr><tr id="record_preset_value-chg_model-row"><td>

chg\_model.record\_preset.value

</td><td id="record_preset_value-chg_model-entry">

Internal value for record\_preset.Data type: String

</td></tr><tr id="state_field-chg_model-row"><td>

chg\_model.state\_field

</td><td id="state_field-chg_model-entry">

Choice list field from which to collect choices, based on the value provided in **table\_name**. For change models, this is always set to "state".Data type: Object

 ```
"state_field": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="state_field_display_value-chg_model-row"><td>

chg\_model.state\_field.display\_value

</td><td id="state_field_display_value-chg_model-entry">

Display value for state\_field.Data type: String

</td></tr><tr id="state_field_value-chg_model-row"><td>

chg\_model.state\_field.value

</td><td id="state_field_value-chg_model-entry">

Internal value for state\_field.Data type: String

</td></tr><tr id="sys_class_name-chg_model-row"><td>

chg\_model.sys\_class\_name

</td><td id="sys_class_name-chg_model-entry">

Change module table name. Always Change Model/chg\_model.Data type: Object

 ```
"sys_class_name": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_class_name_display_value-chg_model-row"><td>

chg\_model.sys\_class\_name.display\_value

</td><td id="sys_class_name_display_value-chg_model-entry">

Display value for sys\_class\_name.Data type: String

</td></tr><tr id="sys_class_name_value-chg_model-row"><td>

chg\_model.sys\_class\_name.display\_value

</td><td id="sys_class_name_value-chg_model-entry">

Internal value for sys\_class\_name.Data type: String

</td></tr><tr id="sys_created_by-chg_model-row"><td>

chg\_model.sys\_created\_by

</td><td id="sys_created_by-chg_model-entry">

Name of the user that initially created the associated change module record. Data type: Object

 ```
"sys_created_by": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_created_by_display_value-chg_model-row"><td>

chg\_model.sys\_created\_by.display\_value

</td><td id="sys_created_by_display_value-chg_model-entry">

Display value for sys\_created\_by.Data type: String

</td></tr><tr id="sys_created_by_value-chg_model-row"><td>

chg\_model.sys\_created\_by.value

</td><td id="sys_created_by_value-chg_model-entry">

Internal value for sys\_created\_by.Data type: String

</td></tr><tr id="sys_created_on-chg_model-row"><td>

chg\_model.sys\_created\_on

</td><td id="sys_created_on-chg_model-entry">

Date and time that the change module record was originally created.Data type: Object

 ```
"sys_created_on": {
  "display_value": "String",
  "display_value_internal": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_created_on_display_value-chg_model-row"><td>

chg\_model.sys\_created\_on.display\_value

</td><td id="sys_created_on_display_value-chg_model-entry">

Display value for sys\_created\_on.Data type: String

</td></tr><tr id="sys_created_on_display_value_internal-chg_model-row"><td>

chg\_model.sys\_created\_on.display\_value\_internal

</td><td id="sys_created_on_display_value_internal-chg_model-entry">

Internal display value for sys\_created\_on.Data type: String

</td></tr><tr id="sys_created_on_value-chg_model-row"><td>

chg\_model.sys\_created\_on.value

</td><td id="sys_created_on_value-chg_model-entry">

Internal value for sys\_created\_on.Data type: String

</td></tr><tr id="sys_domain-chg_model-row"><td>

chg\_model.sys\_domain

</td><td id="sys_domain-chg_model-entry">

If using domains in the instance, the name of the domain to which the change module record is associated.Data type: Object

 ```
"sys_domain": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_domain_display_value-chg_model-row"><td>

chg\_model.sys\_domain.display\_value

</td><td id="sys_domain_display_value-chg_model-entry">

Display value for sys\_domain.Data type: String

</td></tr><tr id="sys_domain_value-chg_model-row"><td>

chg\_model.sys\_domain.value

</td><td id="sys_domain_value-chg_model-entry">

Internal value for sys\_domain.Data type: String

</td></tr><tr id="sys_domain_path-chg_model-row"><td>

chg\_model.sys\_domain\_path

</td><td id="sys_domain_path-chg_model-entry">

If using domains in the instance, the domain path in which the associated change module record resides.Data type: Object

 ```
"sys_domain_path": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_domain_path_display_value-chg_model-row"><td>

chg\_model.sys\_domain\_path.display\_value

</td><td id="sys_domain_path_display_value-chg_model-entry">

Display value for sys\_domain\_path.Data type: String

</td></tr><tr id="sys_domain_path_value-chg_model-row"><td>

chg\_model.sys\_domain\_path.value

</td><td id="sys_domain_path_value-chg_model-entry">

Internal value for sys\_domain\_path.Data type: String

</td></tr><tr id="sys_id-chg_model-row"><td>

chg\_model.sys\_id

</td><td id="sys_id-chg_model-entry">

Unique identifier of the associated change model record.Data type: Object

 ```
"sys_id": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_id_display_value-chg_model-row"><td>

chg\_model.sys\_id.display\_value

</td><td id="sys_id_display_value-chg_model-entry">

Display value for sys\_id.Data type: String

</td></tr><tr id="sys_id_value-chg_model-row"><td>

chg\_model.sys\_id.value

</td><td id="sys_id_value-chg_model-entry">

Internal value for sys\_id.Data type: String

</td></tr><tr id="sys_mod_count-chg_model-row"><td>

chg\_model.sys\_mod\_count

</td><td id="sys_mod_count-chg_model-entry">

Number of times that the associated change model record has been modified.Data type: Object

 ```
"sys_mod_count": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr id="sys_mod_count_display_value-chg_model-row"><td>

chg\_model.sys\_mod\_count.display\_value

</td><td id="sys_mod_count_display_value-chg_model-entry">

Display value for sys\_mod\_count.Data type: String

</td></tr><tr id="sys_mod_count_value-chg_model-row"><td>

chg\_model.sys\_mod\_count.value

</td><td id="sys_mod_count_value-chg_model-entry">

Internal value for sys\_mod\_count.Data type: Number

</td></tr><tr id="sys_name-chg_model-row"><td>

chg\_model.sys\_name

</td><td id="sys_name-chg_model-entry">

Name of the change model. Always the same as the **name** parameter.Data type: Object

 ```
"sys_name": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_name_display_value-chg_model-row"><td>

chg\_model.sys\_name.display\_value

</td><td id="sys_name_display_value-chg_model-entry">

Display value for sys\_name.Data type: String

</td></tr><tr id="sys_name_value-chg_model-row"><td>

chg\_model.sys\_name.value

</td><td id="sys_name_value-chg_model-entry">

Internal value for sys\_name.Data type: String

</td></tr><tr id="sys_tags-chg_model-row"><td>

chg\_model.sys\_tags

</td><td id="sys_tags-chg_model-entry">

System tags associated with the change model record.Data type: Object

 ```
"sys_tags": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_tags_display_value-chg_model-row"><td>

chg\_model.sys\_tags.display\_value

</td><td id="sys_tags_display_value-chg_model-entry">

Display value for sys\_tags.Data type: String

</td></tr><tr id="sys_tags_value-chg_model-row"><td>

chg\_model.sys\_tags.value

</td><td id="sys_tags_value-chg_model-entry">

Internal value for sys\_tags.Data type: String

</td></tr><tr id="sys_updated_by-chg_model-row"><td>

chg\_model.sys\_updated\_by

</td><td id="sys_updated_by-chg_model-entry">

Name of the user that last updated the associated change model record.Data type: Object

 ```
"sys_updated_by": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_updated_by_display_value-chg_model-row"><td>

chg\_model.sys\_updated\_by.display\_value

</td><td id="sys_updated_by_display_value-chg_model-entry">

Display value for sys\_updated\_by.Data type: String

</td></tr><tr id="sys_updated_by_value-chg_model-row"><td>

chg\_model.sys\_updated\_by.value

</td><td id="sys_updated_by_value-chg_model-entry">

Internal value for sys\_updated\_by.Data type: String

</td></tr><tr id="sys_updated_on-chg_model-row"><td>

chg\_model.sys\_updated\_on

</td><td id="sys_updated_on-chg_model-entry">

Date and time the associated change model record was last updated.Data type: Object

 ```
"sys_updated_on": {
  "display_value": "String",
  "display_value_internal": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_updated_on_display_value-chg_model-row"><td>

chg\_model.sys\_updated\_on.display\_value

</td><td id="sys_updated_on_display_value-chg_model-entry">

Display value for sys\_updated\_on.Data type: String

</td></tr><tr id="sys_updated_on_display_value_internal-chg_model-row"><td>

chg\_model.sys\_updated\_on.display\_value\_internal

</td><td id="sys_updated_on_display_value_internal-chg_model-entry">

Internal display value for sys\_updated\_on.Data type: String

</td></tr><tr id="sys_updated_on_value-chg_model-row"><td>

chg\_model.sys\_updated\_on.value

</td><td id="sys_updated_on_value-chg_model-entry">

Internal value for sys\_updated\_on.Data type: String

</td></tr><tr id="table_name-chg_model-row"><td>

chg\_model.table\_name

</td><td id="table_name-chg_model-entry">

Table that defines the Choice list field from which to collect choices. For change models this is always set to "change\_request".Data type: Object

 ```
"table_name": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="table_name_display_value-chg_model-row"><td>

chg\_model.table\_name.display\_value

</td><td id="table_name_display_value-chg_model-entry">

Display value for table\_name.Data type: String

</td></tr><tr id="table_name_value-chg_model-row"><td>

chg\_model.table\_name.value

</td><td id="table_name_value-chg_model-entry">

Internal value for table\_name.Data type: String

</td></tr><tr id="write_roles-chg_model-row"><td>

chg\_model.write\_roles

</td><td id="write_roles-chg_model-entry">

Security roles needed to write to the change model record.Data type: Object

 ```
"write_roles": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="write_roles_display_value-chg_model-row"><td>

chg\_model.write\_roles.display\_value

</td><td id="write_roles_display_value-chg_model-entry">

Display value for write\_roles.Data type: String

</td></tr><tr id="write_roles_value-chg_model-row"><td>

chg\_model.write\_roles.value

</td><td id="write_roles_value-chg_model-entry">

Internal value for write\_roles.Data type: String

</td></tr><tr id="score-chg_suc-row"><td>

score

</td><td id="score-chg_suc-entry">

Details about the returned score indicator.Data type: Object

 ```
"score": {
  "delta": {Object},
  "display_value": "String",
  "has_score": Boolean,
  "indicator": {Object},
  "value": Number
}
```

</td></tr><tr id="score_delta-chg_suc-row"><td>

score.delta

</td><td id="score_delta-chg_suc-entry">

Change in the score from the previous score.Data type: Object

 ```
"delta": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="score_delta_display_value-chg_suc-row"><td>

score.delta.display\_value

</td><td id="score_delta_display_value-chg_suc-entry">

Display value for delta.Data type: String

</td></tr><tr id="score_delta_value-chg_suc-row"><td>

score.delta.value

</td><td id="score_delta_value-chg_suc-entry">

Internal value for delta.Data type: String

</td></tr><tr id="score_display_value-chg_suc-row"><td>

score.display\_value

</td><td id="score_display_value-chg_suc-entry">

Display value returned by Performance Analytics \(PA\).Data type: String

</td></tr><tr id="score_has_score-chg_suc-row"><td>

score.has\_score

</td><td id="score_has_score-chg_suc-entry">

Flag that indicates whether a score was returned for the specified change request.

 Valid values:

-   true: Score was returned.
-   false: No score was returned.

 Data type: Boolean

</td></tr><tr id="score_indicator-chg_suc-row"><td>

score.indicator

</td><td id="score_indicator-chg_suc-entry">

Additional details on the PA indicator used to obtain the score.Data type: Object

 ```
"indicator": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="score_indicator_name-chg_suc-row"><td>

score.indicator.name

</td><td id="score_indicator_name-chg_suc-entry">

Name of the PA indicator used to obtain the score.Data type: String

</td></tr><tr id="score_indicator_sys_id-chg_suc-row"><td>

score.indicator.sys\_id

</td><td id="score_indicator_sys_id-chg_suc-entry">

Sys\_id of the PA indicator used to obtain the score.Data type: String

</td></tr><tr id="score_value-chg_suc-row"><td>

score.value

</td><td id="score_value-chg_suc-entry">

Value returned by PA for the success score.Data type: String

</td></tr></tbody>
</table>The following code example shows how to use the getTeamScoreForModelId\(\) method to retrieve the model scores for all active records for the associated change model, filter through the requested records, and then places all model scores that are less than 65% and their associated deltas in the event queue `change_success.model.warning` of the associated change model record.

```
var chgModelGr = new GlideRecord("chg_model");
chgModelGr.addActiveQuery();
chgModelGr.query();
 
while (chgModelGr.next()) {
    var changeModelSuccess = new sn_chg_score.ChangeSuccess().getModelScoreForModelId(chgModelGr.getUniqueValue());
    if (changeModelSuccess.can_read && changeModelSuccess.score.has_score && changeModelSuccess.score.value < 65)
        gs.eventQueue("change_success.model.warning", chgModelGr, changeModelSuccess.score.value, changeModelSuccess.score.delta.value);
}
```

Output:

```
{
  "can_read": true,
  "chg_model": {
    "color": {
      "display_value": "",
      "value": ""
    },
    "default_change_model": {
      "display_value": "false",
      "value": false
    },
    "description": {
      "display_value": "This model can be used to capture unauthorized change events that were detected.",
      "value": "This model can be used to capture unauthorized change events that were detected."
    },
    "sys_updated_on": {
      "display_value": "2020-10-21 11:10:57",
      "value": "2020-10-21 10:10:57",
      "display_value_internal": "2020-10-21 11:10:57"
    },
    "table_name": {
      "display_value": "change_request",
      "value": "change_request"
    },
    "sys_class_name": {
      "display_value": "Change Model",
      "value": "chg_model"
    },
    "sys_id": {
      "display_value": "aedc6a625323101034d1ddeeff7b1296",
      "value": "aedc6a625323101034d1ddeeff7b1296"
    },
    "sys_updated_by": {
      "display_value": "admin",
      "value": "admin"
    },
    "write_roles": {
      "display_value": "",
      "value": ""
    },
    "sys_created_on": {
      "display_value": "2020-10-02 14:50:20",
      "value": "2020-10-02 13:50:20",
      "display_value_internal": "2020-10-02 14:50:20"
    },
    "read_roles": {
      "display_value": "itil,sn_change_read",
      "value": "itil,sn_change_read"
    },
    "sys_name": {
      "display_value": "Unauthorized Change",
      "value": "Unauthorized Change"
    },
    "advanced_security": {
      "display_value": "false",
      "value": false
    },
    "sys_created_by": {
      "display_value": "admin",
      "value": "admin"
    },
    "record_preset": {
      "display_value": "type=emergency^short_description=An unauthorized change has been detected^assignment_group=a715cd759f2002002920bde8132e7018^work_start=javascript:gs.nowDateTime()^unauthorized=true^EQ",
      "value": "type=emergency^short_description=An unauthorized change has been detected^assignment_group=a715cd759f2002002920bde8132e7018^work_start=javascript:gs.nowDateTime()^unauthorized=true^EQ"
    },
    "sys_mod_count": {
      "display_value": "9",
      "value": 9
    },
    "active": {
      "display_value": "true",
      "value": true
    },
    "sys_tags": {
      "display_value": "",
      "value": ""
    },
    "available_in_ui": {
      "display_value": "false",
      "value": false
    },
    "state_field": {
      "display_value": "state",
      "value": "state"
    },
    "name": {
      "display_value": "Unauthorized Change",
      "value": "Unauthorized Change"
    },
    "implementation_states": {
      "display_value": "",
      "value": ""
    }
  },
  "score": {
    "indicator": {
      "name": "Change Model: % Successful and Successful With Issues",
      "sys_id": "604f98dfc302011005aea539e540dd75"
    },
    "value": 76.92307692307693,
    "display_value": "76.92",
    "delta": {
      "value": "0",
      "display_value": ""
    },
    "has_score": true
  }
}
```

## ChangeSuccess - getScoresForChange\(Object chgGr\)

Returns the latest change team success score \(original change success score based on group\), model success score, and type success score based on the specified change request GlideRecord.

|Name|Type|Description|
|----|----|-----------|
|chgGr|Object|Change request GlideRecord.|

<table id="table_hnw_hn2_ltb" class="returns"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

model\_success\_score

</td><td>

Details on the model success score.Data type: Object

 ```
"model_success_score" {
  "can_read": Boolean,
  "chg_model": {Object},
  "score": {Object}
}
```

</td></tr><tr><td>

model\_success\_score.can\_read

</td><td>

Flag that indicates whether a model success score could be retrieved for the specified change request.Valid values:

-   true: Model success score was retrieved.
-   false: Model success score was not retrieved.

 Data type: Boolean

</td></tr><tr><td>

model\_success\_score.chg\_model

</td><td>

Individual objects for each field in the Change Model \[chg\_model\] record referenced by the specified change request. Each object has a key that is the field name and contains value and display\_value properties. If the field type is date/time, then the method also returns a display\_value\_internal property which is in the user's timezone but in the system format YYYY-MM-DD HH24:MM:SS.```
"chg_model": {
  "active": {Object},
  "advanced_security": {Object},
  "available_in_ui": {Object},
  "color": {Object},
  "default_change_model": {Object},
  "description": {Object},
  "implementation_states": {Object},
  "name": {Object},
  "read_roles": {Object},
  "record_preset": {Object},
  "state_field": {Object},
  "sys_class_name": {Object},
  "sys_created_by": {Object},
  "sys_created_on": {Object},
  "sys_domain": {Object},
  "sys_domain_path": {Object},
  "sys_id": {Object},
  "sys_mod_count": {Object},
  "sys_name": {Object},
  "sys_tags": {Object},
  "sys_updated_by": {Object},
  "sys_updated_name": {Object},
  "sys_updated_on": {Object},
  "table_name": {Object},
  "write_roles": {Object}
}
```

 Data type: Object

</td></tr><tr><td>

model\_success\_score.chg\_model.active

</td><td>

Flag that indicates whether the associated change model record is active and available within the instance.Valid values:

-   true: Change model is active.
-   false: Change model is not active.

 Data type: Object

 ```
"active": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.active.display\_value

</td><td>

Display value for the active flag.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.active.value

</td><td>

Internal value for the active flag.Data type: Boolean

</td></tr><tr><td>

model\_success\_score.chg\_model.advanced\_security

</td><td>

Flag that indicates whether user criteria based security is being used in addition to role based security for this change model.Valid values:

-   true: Advanced security is used.
-   false: Advanced security in not used.

 Data type: Object

 ```
"advanced_security": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.advanced\_security.display\_value

</td><td>

Display value for the advanced\_security flag.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.advanced\_security.value

</td><td>

Internal value for the advanced\_security flag.Data type: Boolean

</td></tr><tr><td>

model\_success\_score.chg\_model.available\_in\_ui

</td><td>

Flag that indicates whether the associated change model record is available within the user interface.Valid values:

-   true: Change model is available in the user interface.
-   false: Change model is not available in the user interface.

 Data type: Object

 ```
"available_in_ui": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.available\_in\_ui.display\_value

</td><td>

Display value for the available\_in\_ui flag.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.available\_in\_ui.value

</td><td>

Value for the available\_in\_ui flag.Data type: Boolean

</td></tr><tr><td>

model\_success\_score.chg\_model.color

</td><td>

Color of the associated change model on the change request landing page.Data type: Object

 ```
"color": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.color.display\_value

</td><td>

Display value for color.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.color.value

</td><td>

Internal value for color.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.default\_change\_model

</td><td>

Flag that indicates whether the associated change model record is the default change model.Valid values:

-   true: Default
-   false: Not the default

 Data type: Boolean

 Default: false

</td></tr><tr><td>

model\_success\_score.chg\_model.default\_change\_model.display\_value

</td><td>

Display value for the default change model flag.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.default\_change\_model.value

</td><td>

Internal value for the default change model flag.Data type: Boolean

</td></tr><tr><td>

model\_success\_score.chg\_model.description

</td><td>

Short description of the purpose of the change model.Data type: Object

 ```
"description": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.description.display\_value

</td><td>

Display value for description.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.description.value

</td><td>

Internal value for description.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.implementation\_states

</td><td>

List of sys\_ids of states for which change requests using this model can be implemented.Data type: Object

 ```
"implementation_states": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.implementation\_states.display\_value

</td><td>

Display value for read\_roles.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.implementation\_states.value

</td><td>

Internal value for read\_roles.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.name

</td><td>

Name of the change model.Data type: Object

 ```
"name": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.name.display\_value

</td><td>

Display value for name.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.name.value

</td><td>

Internal value for name.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.read\_roles

</td><td>

Security roles needed to read the change model record.Data type: Object

 ```
"read_roles": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.read\_roles.display\_value

</td><td>

Display value for read\_roles.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.read\_roles.value

</td><td>

Internal value for read\_roles.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.record\_preset

</td><td>

Name-value pairs of the fields that should automatically be populated, with their associated values, when a new change request record is created. Values are separated by caret symbols.For example:

 `"type=normal^assignment_group=a715cd759f2002002920bde8132e7018^short_description=Automated : Change^EQ"`

 Data type: Object

 ```
"record_preset": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.record\_preset.display\_value

</td><td>

Display value for record\_preset.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.record\_preset.value

</td><td>

Internal value for record\_preset.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.state\_field

</td><td>

Choice list field from which to collect choices, based on the value provided in **table\_name**. For change models, this is always set to "state".Data type: Object

 ```
"state_field": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.state\_field.display\_value

</td><td>

Display value for state\_field.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.state\_field.value

</td><td>

Internal value for state\_field.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_class\_name

</td><td>

Change module table name. Always Change Model/chg\_model.Data type: Object

 ```
"sys_class_name": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_class\_name.display\_value

</td><td>

Display value for sys\_class\_name.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_class\_name.value

</td><td>

Internal value for sys\_class\_name.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_created\_by

</td><td>

Name of the user that initially created the associated change module record. Data type: Object

 ```
"sys_created_by": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_created\_by.display\_value

</td><td>

Display value for sys\_created\_by.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_created\_by.value

</td><td>

Internal value for sys\_created\_by.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_created\_on

</td><td>

Date and time that the change module record was originally created.Data type: Object

 ```
"sys_created_on": {
  "display_value": "String",
  "display_value_internal": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_created\_on.display\_value

</td><td>

Display value for sys\_created\_on.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_created\_on.display\_value.internal

</td><td>

Internal display value for sys\_created\_on.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_created\_on.value

</td><td>

Internal value for sys\_created\_on.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_domain

</td><td>

If using domains in the instance, the name of the domain to which the change module record is associated.Data type: Object

 ```
"sys_domain": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_domain.display\_value

</td><td>

Display value for sys\_domain.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_domain.value

</td><td>

Internal value for sys\_domain.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_domain\_path

</td><td>

If using domains in the instance, the domain path in which the associated change module record resides.Data type: Object

 ```
"sys_domain_path": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_domain\_path.display\_value

</td><td>

Display value for sys\_domain\_path.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_domain\_path.value

</td><td>

Internal value for sys\_domain\_path.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_id

</td><td>

Unique identifier of the associated change model record.Data type: Object

 ```
"sys_id": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_id.display\_value

</td><td>

Display value for sys\_id.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_id.value

</td><td>

Internal value for sys\_id.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_mod\_count

</td><td>

Number of times that the associated change model record has been modified.Data type: Object

 ```
"sys_mod_count": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_mod\_count.display\_value

</td><td>

Display value for sys\_mod\_count.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_mod\_count.value

</td><td>

Internal value for sys\_mod\_count.Data type: Number

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_name

</td><td>

Name of the change model. Always the same as the **name** parameter.Data type: Object

 ```
"sys_name": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_name

</td><td>

Display value for sys\_name.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_name

</td><td>

Internal value for sys\_name.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_tags

</td><td>

System tags associated with the change model record.Data type: Object

 ```
"sys_tags": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_tags.display\_value

</td><td>

Display value for sys\_tags.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_tags.value

</td><td>

Internal value for sys\_tags.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_updated\_by

</td><td>

Name of the user that last updated the associated change model record.Data type: Object

 ```
"sys_updated_by": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_updated\_by.display\_value

</td><td>

Display value for sys\_updated\_by.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_updated\_by.value

</td><td>

Internal value for sys\_updated\_by.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_updated\_on

</td><td>

Date and time the associated change model record was last updated.Data type: Object

 ```
"sys_updated_on": {
  "display_value": "String",
  "display_value_internal": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_updated\_on.display\_value

</td><td>

Display value for sys\_updated\_on.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_updated\_on.display\_internal\_value

</td><td>

Internal display value for sys\_updated\_on.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_updated\_on.value

</td><td>

Internal value for sys\_updated\_on.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.table\_name

</td><td>

Table that defines the Choice list field from which to collect choices. For change models this is always set to "change\_request".Data type: Object

 ```
"table_name": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.table\_name.display\_value

</td><td>

Display value for table\_name.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.table\_name.value

</td><td>

Internal value for table\_name.Data type: String

</td></tr><tr><td>

model\_success\_score.score

</td><td>

Details about the returned score indicator.Data type: Object

 ```
"score": {
  "delta": {Object},
  "display_value": "String",
  "has_score": Boolean,
  "indicator": {Object},
  "value": Number
}
```

</td></tr><tr><td>

model\_success\_score.score.delta

</td><td>

Change in the score from the previous score.Data type: Object

 ```
"delta": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.score.delta.display\_value

</td><td>

Display value for delta.Data type: String

</td></tr><tr><td>

model\_success\_score.score.delta.value

</td><td>

Internal value for delta.Data type: String

</td></tr><tr><td>

model\_success\_score.score.display\_value

</td><td>

Display value returned by Performance Analytics \(PA\).Data type: String

</td></tr><tr><td>

model\_success\_score.score.score.has\_score

</td><td>

Flag that indicates whether a score was returned for the specified change request.

 Valid values:

-   true: Score was returned.
-   false: No score was returned.

 Data type: Boolean

</td></tr><tr><td>

model\_success\_score.score.indicator

</td><td>

Additional details on the PA indicator used to obtain the score.Data type: Object

 ```
"indicator": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

model\_success\_score.score.indicator.name

</td><td>

Name of the PA indicator used to obtain the score.Data type: String

</td></tr><tr><td>

model\_success\_score.score.indicator.sys\_id

</td><td>

Sys\_id of the PA indicator used to obtain the score.Data type: String

</td></tr><tr><td>

model\_success\_score.score.value

</td><td>

Value returned by PA for the success score.Data type: String

</td></tr><tr><td>

team\_success\_score

</td><td>

Details on the team success score.Data type: Object

 ```
"team_success_score" {
  "can_read": Boolean,
  "chg_success_score_rating": {Object},
  "score": {Object},
  "sys_user_group":{Object}
}
```

</td></tr><tr id="can_read-team_suc-row"><td>

team\_success\_score.can\_read

</td><td>

Flag that indicates whether a change team success score could be retrieved for the specified change request.Valid values:

-   true: Team success score was retrieved.
-   false: Team success score was not retrieved.

 Data type: Boolean

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating

</td><td>

Individual objects for each field from the Change Success Score Rating \[chg\_success\_score\_rating\] record that matches the returned score. Each field object has a key that is the field name and contains **value** and **display\_value** properties. If the field type is date/time, then the method also returns a **display\_value\_internal** property which is in the user's timezone but in the system format YYYY-MM-DD HH24:MM:SS.Data type: Object

 ```
"chg_success_score_rating": {
  "active": {Object},
  "color": {Object},
  "rating": {Object},
  "score_end": {Object},
  "score_start": {Object},
  "sys_class_name": {Object},
  "sys_created_by": {Object},
  "sys_created_on": {Object},
  "sys_domain": {Object},
  "sys_id": {Object},
  "sys_mod_count": {Object},
  "sys_name": {Object},
  "sys_overrides": {Object},
  "sys_tags": {Object},
  "sys_updated_by": {Object},
  "sys_updated_on": {Object}
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.active

</td><td>

Flag that indicates whether the associated change success score record is active and available within the instance.Valid values:

-   true: Change success score record is active.
-   false: Change success score record is not active.

 Data type: Object

 ```
"active": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.active.display\_value

</td><td>

Display value for the active flag.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.active.value

</td><td>

Internal value for the active flag.Data type: Boolean

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.color

</td><td>

Color of the associated change success score as shown in the Change Success Score Card for a change request.Data type: Object

 ```
"color": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.color.display\_value

</td><td>

Display value for color.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.color.value

</td><td>

Internal value for color.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.rating

</td><td>

Change success score rating, such as Low or High.Data type: Object

 ```
"rating": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.rating.display\_value

</td><td>

Display value for rating.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.rating.value

</td><td>

Internal value for rating.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.score\_end

</td><td>

Highest value in the change success score.Data type: Object

 ```
"score_end": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.score\_end.display\_value

</td><td>

Display value for score\_end.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.score\_end.value

</td><td>

Internal value for score\_end.Data type: Number

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.score\_start

</td><td>

Lowest value in the change success score.Data type: Object

 ```
"score_start": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.score\_start.display\_value

</td><td>

Display value for score\_start.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.score\_start.value

</td><td>

Internal value for score\_start.Data type: Number

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_class\_name

</td><td>

Change Success Score Rating table name. Always Change Success Score Rating/chg\_success\_score\_rating.Data type: Object

 ```
"sys_class_name": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_class\_name.display\_value

</td><td>

Display value for sys\_class\_name.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_class\_name.value

</td><td>

Internal value for sys\_class\_name.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_created\_by

</td><td>

Name of the user that initially created the associated change success score rating record. Data type: Object

 ```
"sys_created_by": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_created\_by.display\_value

</td><td>

Display value for sys\_created\_by.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_created\_by.value

</td><td>

Internal value for sys\_created\_by.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_created\_on

</td><td>

Date and time that the change success score rating record was originally created.Data type: Object

 ```
"sys_created_on": {
  "display_value": "String",
  "display_value_internal": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_created\_on.display\_value

</td><td>

Display value for sys\_created\_on.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_created\_on.display\_internal.value

</td><td>

Internal display value for sys\_created\_on.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_created\_on.value

</td><td>

Internal value for sys\_created\_on.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_domain

</td><td>

If using domains in the instance, the name of the domain to which the change success score record is associated.Data type: Object

 ```
"sys_domain": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_domain.display\_value

</td><td>

Display value for sys\_domain.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_domain.value

</td><td>

Internal value for sys\_domain.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_id

</td><td>

Unique identifier of the associated change success score record.Data type: Object

 ```
"sys_id": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_id.display\_value

</td><td>

Display value for sys\_id.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_id.value

</td><td>

Internal value for sys\_id.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_mod\_count

</td><td>

Number of times that the associated change success score record has been modified.Data type: Object

 ```
"sys_mod_count": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_mod\_count.display\_value

</td><td>

Display value for sys\_mod\_count.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_mod\_count.value

</td><td>

Internal value for sys\_mod\_count.Data type: Number

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_name

</td><td>

Name of the change success score rating.Possible values:

 -   Excellent
-   High
-   Low
-   Medium

 Data type: Object

 ```
"sys_name": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_name.display\_value

</td><td>

Display value for sys\_name.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_name.value

</td><td>

Internal value for sys\_name.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_overrides

</td><td>

Sys\_id of a record in the same table but in a domain above that of the current record. This allows a record in a lower domain to override a record in a domain above it.For example, if you have a rating record defined in the "global" domain but for domain "TOP/ACME" you override the record in "global".

 Data type: Object

 ```
"sys_overrides": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_overrides.display\_value

</td><td>

Display value for sys\_overrides.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_overrides.value

</td><td>

Internal value for sys\_overrides.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_tags

</td><td>

List of system tags associated with the change success score record.Data type: Object

 ```
"sys_tags": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_tags.display\_value

</td><td>

Display value for sys\_tags.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_tags.value

</td><td>

Internal value for sys\_tags.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_updated\_by

</td><td>

Name of the user that last updated the associated change success score record.Data type: Object

 ```
"sys_updated_by": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_updated\_by.display\_value

</td><td>

Display value for sys\_updated\_by.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_updated\_by.value

</td><td>

Internal value for sys\_updated\_by.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_updated\_on

</td><td>

Date and time the associated change success score record was last updated.Data type: Object

 ```
"sys_created_on": {
  "display_value": "String",
  "display_value_internal": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_updated\_on.display\_value

</td><td>

Display value for sys\_updated\_on.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_updated\_on.display\_internal\_value

</td><td>

Internal display value for sys\_updated\_on.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_updated\_on.value

</td><td>

Internal value for sys\_updated\_on.Data type: String

</td></tr><tr id="chg_suc-score-row"><td>

team\_success\_score.score

</td><td>

Details about the returned score indicator.Data type: Object

 ```
"score": {
  "delta": {Object},
  "display_value": "String",
  "has_score": Boolean,
  "indicator": {Object},
  "value": Number
}
```

</td></tr><tr id="chg_suc-score_delta-row"><td>

team\_success\_score.score.delta

</td><td>

Change in the score from the previous score.Data type: Object

 ```
"delta": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.score.delta.display\_value

</td><td>

Display value for delta.Data type: String

</td></tr><tr><td>

team\_success\_score.score.delta.value

</td><td>

Internal value for delta.Data type: String

</td></tr><tr id="chg_suc-score_display_value-row"><td>

team\_success\_score.score.display\_value

</td><td>

Display value returned by Performance Analytics \(PA\).Data type: String

</td></tr><tr id="chg_suc-score_has_score-row"><td>

team\_success\_score.score.score.has\_score

</td><td>

Flag that indicates whether a score was returned for the specified change request.

 Valid values:

-   true: Score was returned.
-   false: No score was returned.

 Data type: Boolean

</td></tr><tr id="chg_suc-score_indicator-row"><td>

team\_success\_score.score.indicator

</td><td>

Additional details on the PA indicator used to obtain the score.Data type: Object

 ```
"indicator": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="chg_suc-score_indicator_name-row"><td>

team\_success\_score.score.indicator.name

</td><td>

Name of the PA indicator used to obtain the score.Data type: String

</td></tr><tr id="chg_suc-score_indicator_sys_id-row"><td>

team\_success\_score.score.indicator.sys\_id

</td><td>

Sys\_id of the PA indicator used to obtain the score.Data type: String

</td></tr><tr id="chg_suc-score_value-row"><td>

team\_success\_score.score.value

</td><td>

Value returned by PA for the success score.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group

</td><td>

Individual objects for each field from the Group \[sys\_user\_group\] record referenced by the specified change request. Each field object has a key that is the field name and contains **value** and **display\_value** properties. If the field type is date/time, then the method also returns a **display\_value\_internal** property which is in the user's timezone but in the system format YYYY-MM-DD HH24:MM:SS.Data type: Object

```
"sys_user_group": {
  "active": {Object},
  "cost_center": {Object},
  "default_assignee": {Object},
  "description": {Object},
  "email": {Object},
  "exclude_manager": {Object},
  "include_members": {Object},
  "manager": {Object},
  "name": {Object},
  "parent": {Object},
  "roles": {Object},
  "source": {Object},
  "sys_created_by": {Object},
  "sys_created_on": {Object},
  "sys_id": {Object},
  "sys_mod_count": {Object},
  "sys_tags": {Object},
  "sys_updated_by": {Object},
  "sys_updated_on": {Object},
  "type": {Object}
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.active

</td><td>

Flag that indicates whether the group is active.Possible values:

 -   true: Group is active
-   false: Group is de-activated

 Data type: Object

 ```
"active": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.active.display\_value

</td><td>

Display value for the active flag.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.active.value

</td><td>

Internal value for the active flag.Data type: Boolean

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.cost\_center

</td><td>

Sys\_id of the cost center associated with the group.Data type: Object

 ```
"cost_center": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.cost\_center.display\_value

</td><td>

Display value for cost\_center.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.cost\_center.value

</td><td>

Internal value for cost\_center.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.default\_assignee

</td><td>

Sys\_id of the user that is the default assignee of the group.Data type: Object

 ```
"default_assignee": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.default\_assignee.display\_value

</td><td>

Display value for default\_assignee.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.default\_assignee.value

</td><td>

Internal value for default\_assignee.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.description

</td><td>

Description of the groupData type: Object

 ```
"description": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.description.display\_value

</td><td>

Display value for description.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.description.value

</td><td>

Internal value for description.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.email

</td><td>

Email address for the group.Data type: Object

 ```
"description": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.email.display\_value

</td><td>

Display value for email.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.email.value

</td><td>

Internal value for email.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.exclude\_manager

</td><td>

Flag that indicates whether the manager of the group receives group emails.Valid values:

 -   true: Manager does not receive group emails.
-   false: Manager receives group emails.

 Data type: Object

 ```
"exclude_manager": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.exclude\_manager.display\_value

</td><td>

Display value for exclude\_manager.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.exclude\_manager.value

</td><td>

Internal value for exclude\_manager.Data type: Boolean

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.include\_members

</td><td>

Flag that indicates whether the group members receive individual emails when someone sends an email to the group email address. The only exception to this functionality is for approval notifications, whereby all members of a group receive an approval notification, regardless of this selection.Valid values:

 -   true: Send emails to the entire group.
-   false: Only send emails to the default\_assignee.

 Data type: Object

 ```
"include_members": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.include\_members.display\_value

</td><td>

Display value for include\_members.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.include\_members.value

</td><td>

Internal value for include\_members.Data type: Boolean

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.manager

</td><td>

Sys\_id of the manager of the group.Data type: Object

 ```
"manager": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.manager.display\_value

</td><td>

Display value for manager.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.manager.value

</td><td>

Internal value for manager.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.name

</td><td>

Name of the group.Data type: Object

 ```
"name": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.name.display\_value

</td><td>

Display value for name.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.name.value

</td><td>

Internal value for name.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.parent

</td><td>

Sys\_id of the parent of this group. If a group has a parent, the child group inherits the roles of the parent group. The members of the child group are not members of the parent group. For example, if an incident is assigned to the parent group and you click the Assigned to lookup icon, only the members in the parent group are available. The members of the child group are not available.Data type: Object

 ```
"parent": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.parent.display\_value

</td><td>

Display value for parent.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.parent.value

</td><td>

Internal value for parent.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.roles

</td><td>

User roles assigned to the group.Data type: Object

 ```
"roles": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.roles.display\_value

</td><td>

Display value for roles.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.roles.value

</td><td>

Internal value for roles.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.source

</td><td>

Source of the group.Data type: Object

 ```
"source": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.source.display\_value

</td><td>

Display value for source.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.source.value

</td><td>

Internal value for source.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_created\_by

</td><td>

User that created the group record.Data type: Object

 ```
"sys_created_by": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_created\_by.display\_value

</td><td>

Display value for sys\_created\_by.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_created\_by.value

</td><td>

Internal value for sys\_created\_by.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_created\_on

</td><td>

Date and time that the group record was originally created.Data type: Object

 ```
"sys_created_on": {
  "display_value": "String",
  "display_value_internal": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_created\_on.display\_value

</td><td>

Display value for sys\_created\_on.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_created\_on.display\_internal\_value

</td><td>

Internal display value for sys\_created\_on.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_created\_on.value

</td><td>

Internal value for sys\_created\_on.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_id

</td><td>

Sys\_id for the group.Data type: Object

 ```
"sys_id": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_id.display\_value

</td><td>

Display value for sys\_id.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_id.value

</td><td>

Internal value for sys\_id.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_mod\_count

</td><td>

Number of times that the associated group information has been modified.Data type: Object

 ```
"sys_mod_count": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_mod\_count.display\_value

</td><td>

Display value for sys\_mod\_count.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_mod\_count.value

</td><td>

Internal value for sys\_mod\_count.Data type: Number

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_updated\_by

</td><td>

User that last updated the group information.Data type: Object

 ```
"sys_updated_by": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_updated\_by.display\_value

</td><td>

Display value for sys\_updated\_by.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_updated\_by.value

</td><td>

Internal value for sys\_updated\_by.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_updated\_on

</td><td>

Date and time when the group information was last updated.Data type: Object

 ```
"sys_updated_on": {
  "display_value": "String",
  "display_value_internal": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_updated\_on.display\_value

</td><td>

Display value for sys\_updated\_on.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_updated\_on.display\_internal\_value

</td><td>

Internal display value for sys\_updated\_on.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_updated\_on.value

</td><td>

Internal value for sys\_updated\_on.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.type

</td><td>

Type of group. Data type: Object

 ```
"type": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.type.display\_value

</td><td>

Display value for type.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.type.value

</td><td>

Internal value for type.Data type: String

</td></tr><tr><td>

type\_success\_score

</td><td>

Details about the type success score.Data type: Object

 ```
"type_success_score": {
  "can_read": Boolean,
  "score": {Object},
  "type": {Object}
}
```

</td></tr><tr><td>

type\_success\_score.can\_read

</td><td>

Flag that indicates whether a type success score could be retrieved for the specified change request.Valid values:

-   true: Type success score was retrieved.
-   false: Type success score was not retrieved.

 Data type: Boolean

</td></tr><tr><td>

type\_success\_score.score

</td><td>

Details about the returned score indicator.Data type: Object

 ```
"score": {
  "delta": {Object},
  "display_value": "String",
  "has_score": Boolean,
  "indicator": {Object},
  "value": Number
}
```

</td></tr><tr><td>

type\_success\_score.score.delta

</td><td>

Change in the score from the previous score.Data type: Object

 ```
"delta": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

type\_success\_score.score.delta.display\_value

</td><td>

Display value for delta.Data type: String

</td></tr><tr><td>

type\_success\_score.score.delta.value

</td><td>

Internal value for delta.Data type: String

</td></tr><tr><td>

type\_success\_score.score.display\_value

</td><td>

Display value returned by Performance Analytics \(PA\).Data type: String

</td></tr><tr><td>

type\_success\_score.score.has\_score

</td><td>

Flag that indicates whether a score was returned for the specified change request.

 Valid values:

-   true: Score was returned.
-   false: No score was returned.

 Data type: Boolean

</td></tr><tr><td>

type\_success\_score.score.indicator

</td><td>

Additional details on the PA indicator used to obtain the score.Data type: Object

 ```
"indicator": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

type\_success\_score.score.indicator.name

</td><td>

Name of the PA indicator used to obtain the score.Data type: String

</td></tr><tr><td>

type\_success\_score.score.indicator.sys\_id

</td><td>

Sys\_id of the PA indicator used to obtain the score.Data type: String

</td></tr><tr><td>

type\_success\_score.score.value

</td><td>

Value returned by PA for the success score.Data type: String

</td></tr><tr><td>

type\_success\_score.type

</td><td>

Details about the type success score.Data type: Object

 ```
"type": {
  "display_value": "String",
  "sys_id": "String",
  "value": "String"
}
```

</td></tr><tr><td>

type\_success\_score.type.display\_value

</td><td>

Label of the choice.Data type: String

</td></tr><tr><td>

type\_success\_score.type.sys\_id

</td><td>

Sys\_id of the Choice \[sys\_choice\] record for the specified change type.Data type: String

</td></tr><tr><td>

type\_success\_score.type.value

</td><td>

Value of the choice.Data type: String

</td></tr></tbody>
</table>This code example shows how to retrieve the latest change team success score \(original change success score based on group\), model success score, and type success score based on the current GlideRecord using the getScoresForChange\(\) method and then uses various attributes to filter the results and save a constructed success score summary in the work notes.

```
var changeSuccessScores = new sn_chg_score.ChangeSuccess().getScoresForChange(current);
 
gs.info(JSON.stringify(changeSuccessScores, null, 2));
 
var changeSuccessScoresSummary = "";
if (changeSuccessScores.team_success_score.can_read && changeSuccessScores.team_success_score.score.has_score)
   changeSuccessScoresSummary += "Assignment group \"" + chgGr.assignment_group.getDisplayValue() + "\" has a success rating of \"" + changeSuccessScores.team_success_score.chg_success_score_rating.rating.display_value + "\" (Current team success score: " +  changeSuccessScores.team_success_score.score.display_value + ")\n";
if (changeSuccessScores.model_success_score.can_read && changeSuccessScores.model_success_score.score.has_score)
   changeSuccessScoresSummary += "Model \"" + changeSuccessScores.model_success_score.chg_model.name.display_value + "\" has a success rate of " + changeSuccessScores.model_success_score.score.display_value + "%\n";
if (changeSuccessScores.type_success_score.can_read && changeSuccessScores.type_success_score.score.has_score)
   changeSuccessScoresSummary += "Type \"" + changeSuccessScores.type_success_score.type.display_value + "\" has a success rate of " + changeSuccessScores.type_success_score.score.display_value + "%\n";
 
if (changeSuccessScoresSummary !== "") {
   changeSuccessScoresSummary = "Change success scores summary:\n\n" + changeSuccessScoresSummary;
   chgGr.work_notes.setJournalEntry(changeSuccessScoresSummary);
   chgGr.update();
}
```

Example return results:

```
{
  "team_success_score": {
    "can_read": true,
    "sys_user_group": {
      "parent": {
        "display_value": "",
        "value": ""
      },
      "manager": {
        "display_value": "",
        "value": ""
      },
      "roles": {
        "display_value": "",
        "value": ""
      },
      "sys_mod_count": {
        "display_value": "0",
        "value": 0
      },
      "description": {
        "display_value": "",
        "value": ""
      },
      "active": {
        "display_value": "true",
        "value": true
      },
      "source": {
        "display_value": "",
        "value": ""
      },
      "sys_updated_on": {
        "display_value": "2018-03-07 21:00:41",
        "value": "2018-03-07 21:00:41",
        "display_value_internal": "2018-03-07 21:00:41"
      },
      "type": {
        "display_value": "",
        "value": ""
      },
      "sys_tags": {
        "display_value": "",
        "value": ""
      },
      "sys_id": {
        "display_value": "5f6441efc0a8010e0177fcb589156352",
        "value": "5f6441efc0a8010e0177fcb589156352"
      },
      "sys_updated_by": {
        "display_value": "glide.maint",
        "value": "glide.maint"
      },
      "cost_center": {
        "display_value": "",
        "value": ""
      },
      "default_assignee": {
        "display_value": "",
        "value": ""
      },
      "sys_created_on": {
        "display_value": "2018-03-07 21:00:41",
        "value": "2018-03-07 21:00:41",
        "display_value_internal": "2018-03-07 21:00:41"
      },
      "name": {
        "display_value": "IT Securities",
        "value": "IT Securities"
      },
      "exclude_manager": {
        "display_value": "false",
        "value": false
      },
      "email": {
        "display_value": "",
        "value": ""
      },
      "include_members": {
        "display_value": "false",
        "value": false
      },
      "sys_created_by": {
        "display_value": "glide.maint",
        "value": "glide.maint"
      }
    },
    "score": {
      "indicator": {
        "name": "Change success scores",
        "sys_id": "0ff316e173081010491d235f04f6a758"
      },
      "value": 465,
      "display_value": "465",
      "delta": {
        "value": 0,
        "display_value": "0"
      },
      "has_score": true
    },
    "chg_success_score_rating": {
      "score_start": {
        "display_value": "0",
        "value": 0
      },
      "score_end": {
        "display_value": "499",
        "value": 499
      },
      "color": {
        "display_value": "#FCCAC9",
        "value": "#FCCAC9"
      },
      "rating": {
        "display_value": "Low",
        "value": "Low"
      },
      "sys_mod_count": {
        "display_value": "0",
        "value": 0
      },
      "active": {
        "display_value": "true",
        "value": true
      },
      "sys_overrides": {
        "display_value": "",
        "value": ""
      },
      "sys_updated_on": {
        "display_value": "2020-03-27 07:43:29",
        "value": "2020-03-27 07:43:29",
        "display_value_internal": "2020-03-27 07:43:29"
      },
      "sys_tags": {
        "display_value": "",
        "value": ""
      },
      "sys_class_name": {
        "display_value": "Change Success Score Rating",
        "value": "chg_success_score_rating"
      },
      "sys_id": {
        "display_value": "7ad380b573330010491d235f04f6a717",
        "value": "7ad380b573330010491d235f04f6a717"
      },
      "sys_updated_by": {
        "display_value": "admin",
        "value": "admin"
      },
      "sys_created_on": {
        "display_value": "2020-03-27 07:43:29",
        "value": "2020-03-27 07:43:29",
        "display_value_internal": "2020-03-27 07:43:29"
      },
      "sys_domain": {
        "display_value": "global",
        "value": "global"
      },
      "sys_name": {
        "display_value": "Low",
        "value": "Low"
      },
      "sys_created_by": {
        "display_value": "admin",
        "value": "admin"
      }
    }
  },
  "model_success_score": {
    "can_read": true,
    "chg_model": {
      "color": {
        "display_value": "",
        "value": ""
      },
      "default_change_model": {
        "display_value": "false",
        "value": false
      },
      "description": {
        "display_value": "This model can be used to capture unauthorized change events that were detected.",
        "value": "This model can be used to capture unauthorized change events that were detected."
      },
      "sys_updated_on": {
        "display_value": "2020-10-21 11:10:57",
        "value": "2020-10-21 10:10:57",
        "display_value_internal": "2020-10-21 11:10:57"
      },
      "table_name": {
        "display_value": "change_request",
        "value": "change_request"
      },
      "sys_class_name": {
        "display_value": "Change Model",
        "value": "chg_model"
      },
      "sys_id": {
        "display_value": "aedc6a625323101034d1ddeeff7b1296",
        "value": "aedc6a625323101034d1ddeeff7b1296"
      },
      "sys_updated_by": {
        "display_value": "admin",
        "value": "admin"
      },
      "write_roles": {
        "display_value": "",
        "value": ""
      },
      "sys_created_on": {
        "display_value": "2020-10-02 14:50:20",
        "value": "2020-10-02 13:50:20",
        "display_value_internal": "2020-10-02 14:50:20"
      },
      "read_roles": {
        "display_value": "itil,sn_change_read",
        "value": "itil,sn_change_read"
      },
      "sys_name": {
        "display_value": "Unauthorized Change",
        "value": "Unauthorized Change"
      },
      "advanced_security": {
        "display_value": "false",
        "value": false
      },
      "sys_created_by": {
        "display_value": "admin",
        "value": "admin"
      },
      "record_preset": {
        "display_value": "type=emergency^short_description=An unauthorized change has been detected^assignment_group=a715cd759f2002002920bde8132e7018^work_start=javascript:gs.nowDateTime()^unauthorized=true^EQ",
        "value": "type=emergency^short_description=An unauthorized change has been detected^assignment_group=a715cd759f2002002920bde8132e7018^work_start=javascript:gs.nowDateTime()^unauthorized=true^EQ"
      },
      "sys_mod_count": {
        "display_value": "9",
        "value": 9
      },
      "active": {
        "display_value": "true",
        "value": true
      },
      "sys_tags": {
        "display_value": "",
        "value": ""
      },
      "available_in_ui": {
        "display_value": "false",
        "value": false
      },
      "state_field": {
        "display_value": "state",
        "value": "state"
      },
      "name": {
        "display_value": "Unauthorized Change",
        "value": "Unauthorized Change"
      },
      "implementation_states": {
        "display_value": "",
        "value": ""
      }
    },
    "score": {
      "indicator": {
        "name": "Change Model: % Successful and Successful With Issues",
        "sys_id": "604f98dfc302011005aea539e540dd75"
      },
      "value": 76.92307692307693,
      "display_value": "76.92",
      "delta": {
        "value": 0,
        "display_value": "0.00"
      },
      "has_score": true
    }
  },
  "type_success_score": {
    "can_read": true,
    "type": {
      "sys_id": "e7a27d53cb100200d71cb9c0c24c9c2f",
      "value": "normal",
      "display_value": "Normal"
    },
    "score": {
      "indicator": {
        "name": "Change Type: % Successful and Successful With Issues",
        "sys_id": "f9d25995c3ce011005aea539e540ddee"
      },
      "value": 74.29906542056075,
      "display_value": "74.30",
      "delta": {
        "value": 0,
        "display_value": "0.00"
      },
      "has_score": true
    }
  }
}
```

## ChangeSuccess - getTeamScoreForChange\(Object chgGr\)

Returns the latest change team success score \(original change success score based on group\) based on the specified change request GlideRecord.

|Name|Type|Description|
|----|----|-----------|
|chgGr|Object|Change request GlideRecord for which to return the change team success score.|

<table id="id_nm2_1z5_15b" class="returns"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr id="can_read-team_suc-row"><td>

can\_read

</td><td id="can_read-team_suc-entry">

Flag that indicates whether a change team success score could be retrieved for the specified change request.Valid values:

-   true: Team success score was retrieved.
-   false: Team success score was not retrieved.

 Data type: Boolean

</td></tr><tr id="chg_success_score_rating-team_suc-row"><td>

chg\_success\_score\_rating

</td><td id="chg_success_score_rating-team_suc-entry">

Individual objects for each field from the Change Success Score Rating \[chg\_success\_score\_rating\] record that matches the returned score. Each field object has a key that is the field name and contains **value** and **display\_value** properties. If the field type is date/time, then the method also returns a **display\_value\_internal** property which is in the user's timezone but in the system format YYYY-MM-DD HH24:MM:SS.Data type: Object

 ```
"chg_success_score_rating": {
  "active": {Object},
  "color": {Object},
  "rating": {Object},
  "score_end": {Object},
  "score_start": {Object},
  "sys_class_name": {Object},
  "sys_created_by": {Object},
  "sys_created_on": {Object},
  "sys_domain": {Object},
  "sys_id": {Object},
  "sys_mod_count": {Object},
  "sys_name": {Object},
  "sys_overrides": {Object},
  "sys_tags": {Object},
  "sys_updated_by": {Object},
  "sys_updated_on": {Object}
}
```

</td></tr><tr id="active-team_suc-row"><td>

chg\_success\_score\_rating.active

</td><td id="active-team_suc-entry">

Flag that indicates whether the associated change success score record is active and available within the instance.Valid values:

-   true: Change success score record is active.
-   false: Change success score record is not active.

 Data type: Object

 ```
"active": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr id="active_display_value-team_suc-row"><td>

chg\_success\_score\_rating.active.display\_value

</td><td id="active_display_value-team_suc-entry">

Display value for the active flag.Data type: String

</td></tr><tr id="active_value-team_suc-row"><td>

chg\_success\_score\_rating.active.value

</td><td id="active_value-team_suc-entry">

Internal value for the active flag.Data type: Boolean

</td></tr><tr id="color-team_suc-row"><td>

chg\_success\_score\_rating.color

</td><td id="color-team_suc-entry">

Color of the associated change success score as shown in the Change Success Score Card for a change request.Data type: Object

 ```
"color": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="color_display_value-team_suc-row"><td>

chg\_success\_score\_rating.color.display\_value

</td><td id="color_display_value-team_suc-entry">

Display value for color.Data type: String

</td></tr><tr id="color_value-team_suc-row"><td>

chg\_success\_score\_rating.color.value

</td><td id="color_value-team_suc-entry">

Internal value for color.Data type: String

</td></tr><tr id="rating-team_suc-row"><td>

chg\_success\_score\_rating.rating

</td><td id="rating-team_suc-entry">

Change success score rating, such as Low or High.Data type: Object

 ```
"rating": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="rating_display_value-team_suc-row"><td>

chg\_success\_score\_rating.rating.display\_value

</td><td id="rating_display_value-team_suc-entry">

Display value for rating.Data type: String

</td></tr><tr id="rating_value-team_suc-row"><td>

chg\_success\_score\_rating.rating.value

</td><td id="rating_value-team_suc-entry">

Internal value for rating.Data type: String

</td></tr><tr id="score_end-team_suc-row"><td>

chg\_success\_score\_rating.score\_end

</td><td id="score_end-team_suc-entry">

Highest value in the change success score.Data type: Object

 ```
"score_end": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr id="score_end_display_value-team_suc-row"><td>

chg\_success\_score\_rating.score\_end.display\_value

</td><td id="score_end_display_value-team_suc-entry">

Display value for score\_end.Data type: String

</td></tr><tr id="score_end_value-team_suc-row"><td>

chg\_success\_score\_rating.score\_end.value

</td><td id="score_end_value-team_suc-entry">

Internal value for score\_end.Data type: Number

</td></tr><tr id="score_start-team_suc-row"><td>

chg\_success\_score\_rating.score\_start

</td><td id="score_start-team_suc-entry">

Lowest value in the change success score.Data type: Object

 ```
"score_start": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr id="score_start_display_value-team_suc-row"><td>

chg\_success\_score\_rating.score\_start.display\_value

</td><td id="score_start_display_value-team_suc-entry">

Display value for score\_start.Data type: String

</td></tr><tr id="score_start_value-team_suc-row"><td>

chg\_success\_score\_rating.score\_start.value

</td><td id="score_start_value-team_suc-emtry">

Internal value for score\_start.Data type: Number

</td></tr><tr id="sys_class_name-team_suc-row"><td>

chg\_success\_score\_rating.sys\_class\_name

</td><td id="sys_class_name-team_suc-entry">

Change Success Score Rating table name. Always Change Success Score Rating/chg\_success\_score\_rating.Data type: Object

 ```
"sys_class_name": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_class_name_display_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_class\_name.display\_value

</td><td id="sys_class_name_display_value-team_suc-entry">

Display value for sys\_class\_name.Data type: String

</td></tr><tr id="sys_class_name_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_class\_name.value

</td><td id="sys_class_name_value-team_suc-entry">

Internal value for sys\_class\_name.Data type: String

</td></tr><tr id="sys_created_by-team_suc-row"><td>

chg\_success\_score\_rating.sys\_created\_by

</td><td id="sys_created_by-team_suc-entry">

Name of the user that initially created the associated change success score rating record. Data type: Object

 ```
"sys_created_by": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_created_by_display_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_created\_by.display\_value

</td><td id="sys_created_by_display_value-team_suc-entry">

Display value for sys\_created\_by.Data type: String

</td></tr><tr id="sys_created_by_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_created\_by.value

</td><td id="sys_created_by_value-team_suc-entry">

Internal value for sys\_created\_by.Data type: String

</td></tr><tr id="sys_created_on-team_suc-row"><td>

chg\_success\_score\_rating.sys\_created\_on

</td><td id="sys_created_on-team_suc-entry">

Date and time that the change success score rating record was originally created.Data type: Object

 ```
"sys_created_on": {
  "display_value": "String",
  "display_value_internal": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_created_on_display_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_created\_on.display\_value

</td><td id="sys_created_on_display_value-team_suc-entry">

Display value for sys\_created\_on.Data type: String

</td></tr><tr id="sys_created_on_display_value_internal-team_suc-row"><td>

chg\_success\_score\_rating.sys\_created\_on.display\_value\_internal

</td><td id="sys_created_on_display_value_internal-team_suc-entry">

Internal display value for sys\_created\_on.Data type: String

</td></tr><tr id="sys_created_on_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_created\_on.value

</td><td id="sys_created_on_value-team_suc-entry">

Internal value for sys\_created\_on.Data type: String

</td></tr><tr id="sys_domain-team_suc-row"><td>

chg\_success\_score\_rating.sys\_domain

</td><td id="sys_domain-team_suc-entry">

If using domains in the instance, the name of the domain to which the change success score record is associated.Data type: Object

 ```
"sys_domain": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_domain_display_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_domain.display\_value

</td><td id="sys_domain_display_value-team_suc-entry">

Display value for sys\_domain.Data type: String

</td></tr><tr id="sys_domain_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_domain.value

</td><td id="sys_domain_value-team_suc-entry">

Internal value for sys\_domain.Data type: String

</td></tr><tr id="sys_id-team_suc-row"><td>

chg\_success\_score\_rating.sys\_id

</td><td id="sys_id-team_suc-entry">

Unique identifier of the associated change success score record.Data type: Object

 ```
"sys_id": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_id_display_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_id.display\_value

</td><td id="sys_id_display_value-team_suc-entry">

Display value for sys\_id.Data type: String

</td></tr><tr id="sys_id_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_id.value

</td><td id="sys_id_value-team_suc-entry">

Internal value for sys\_id.Data type: String

</td></tr><tr id="sys_mod_count-team_suc-row"><td>

chg\_success\_score\_rating.sys\_mod\_count

</td><td id="sys_mod_count-team_suc-entry">

Number of times that the associated change success score record has been modified.Data type: Object

 ```
"sys_mod_count": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr id="sys_mod_count_display_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_mod\_count.display\_value

</td><td id="sys_mod_count_display_value-team_suc-entry">

Display value for sys\_mod\_count.Data type: String

</td></tr><tr id="sys_mod_count_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_mod\_count.value

</td><td id="sys_mod_count_value-team_suc-entry">

Internal value for sys\_mod\_count.Data type: Number

</td></tr><tr id="sys_name-team_suc-row"><td>

chg\_success\_score\_rating.sys\_name

</td><td id="sys_name-team_suc-entry">

Name of the change success score rating.Possible values:

 -   Excellent
-   High
-   Low
-   Medium

 Data type: Object

 ```
"sys_name": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr id="sys_name_display_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_name.display\_value

</td><td id="sys_name_display_value-team_suc-entry">

Display value for sys\_name.Data type: String

</td></tr><tr id="sys_name_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_name.value

</td><td id="sys_name_value-team_suc-entry">

Internal value for sys\_name.Data type: String

</td></tr><tr id="sys_overrides-team_suc-row"><td>

chg\_success\_score\_rating.sys\_overrides

</td><td id="sys_overrides-team_suc-entry">

Sys\_id of a record in the same table but in a domain above that of the current record. This allows a record in a lower domain to override a record in a domain above it.For example, if you have a rating record defined in the "global" domain but for domain "TOP/ACME" you override the record in "global".

 Data type: Object

 ```
"sys_overrides": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_overrides_display_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_overrides.display\_value

</td><td id="sys_overrides_display_value-team_suc-entry">

Display value for sys\_overrides.Data type: String

</td></tr><tr id="sys_overrides_value-team_suc-row"><td>

tchg\_success\_score\_rating.sys\_overrides.value

</td><td id="sys_overrides_value-team_suc-entry">

Internal value for sys\_overrides.Data type: String

</td></tr><tr id="sys_tags-team_suc-row"><td>

chg\_success\_score\_rating.sys\_tags

</td><td id="sys_tags-team_suc-entry">

List of system tags associated with the change success score record.Data type: Object

 ```
"sys_tags": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_tags_display_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_tags.display\_value

</td><td id="sys_tags_display_value-team_suc-entry">

Display value for sys\_tags.Data type: String

</td></tr><tr id="sys_tags_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_tags.value

</td><td id="sys_tags_value-team_suc-entry">

Internal value for sys\_tags.Data type: String

</td></tr><tr id="sys_updated_by-team_suc-row"><td>

chg\_success\_score\_rating.sys\_updated\_by

</td><td id="sys_updated_by-team_suc-entry">

Name of the user that last updated the associated change success score record.Data type: Object

 ```
"sys_updated_by": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_updated_by_display_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_updated\_by.display\_value

</td><td id="sys_updated_by_display_value-team_suc-entry">

Display value for sys\_updated\_by.Data type: String

</td></tr><tr id="sys_updated_by_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_updated\_by.value

</td><td id="sys_updated_by_value-team_suc-entry">

Internal value for sys\_updated\_by.Data type: String

</td></tr><tr id="sys_updated_on-team_suc-row"><td>

chg\_success\_score\_rating.sys\_updated\_on

</td><td id="sys_updated_on-team_suc-entry">

Date and time the associated change success score record was last updated.Data type: Object

 ```
"sys_created_on": {
  "display_value": "String",
  "display_value_internal": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_updated_on_display_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_updated\_on.display\_value

</td><td id="sys_updated_on_display_value-team_suc-entry">

Display value for sys\_updated\_on.Data type: String

</td></tr><tr id="sys_updated_on_display_value_internal-team_suc-row"><td>

chg\_success\_score\_rating.sys\_updated\_on.display\_value\_internal

</td><td id="sys_updated_on_display_value_internal-team_suc-entry">

Internal display value for sys\_updated\_on.Data type: String

</td></tr><tr id="sys_updated_on_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_updated\_on.value

</td><td id="sys_updated_on_value-team_suc-entry">

Internal value for sys\_updated\_on.Data type: String

</td></tr><tr><td>

score

</td><td id="score-chg_suc-entry">

Details about the returned score indicator.Data type: Object

 ```
"score": {
  "delta": {Object},
  "display_value": "String",
  "has_score": Boolean,
  "indicator": {Object},
  "value": Number
}
```

</td></tr><tr><td>

score.delta

</td><td id="score_delta-chg_suc-entry">

Change in the score from the previous score.Data type: Object

 ```
"delta": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

score.delta.display\_value

</td><td id="score_delta_display_value-chg_suc-entry">

Display value for delta.Data type: String

</td></tr><tr><td>

score.delta.value

</td><td id="score_delta_value-chg_suc-entry">

Internal value for delta.Data type: String

</td></tr><tr><td>

score.display\_value

</td><td id="score_display_value-chg_suc-entry">

Display value returned by Performance Analytics \(PA\).Data type: String

</td></tr><tr><td>

score.has\_score

</td><td id="score_has_score-chg_suc-entry">

Flag that indicates whether a score was returned for the specified change request.

 Valid values:

-   true: Score was returned.
-   false: No score was returned.

 Data type: Boolean

</td></tr><tr><td>

score.indicator

</td><td id="score_indicator-chg_suc-entry">

Additional details on the PA indicator used to obtain the score.Data type: Object

 ```
"indicator": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

score.indicator.name

</td><td id="score_indicator_name-chg_suc-entry">

Name of the PA indicator used to obtain the score.Data type: String

</td></tr><tr><td>

score.indicator.sys\_id

</td><td id="score_indicator_sys_id-chg_suc-entry">

Sys\_id of the PA indicator used to obtain the score.Data type: String

</td></tr><tr><td>

score.value

</td><td id="score_value-chg_suc-entry">

Value returned by PA for the success score.Data type: String

</td></tr><tr id="sys_user_group-team_suc-row"><td>

sys\_user\_group

</td><td id="sys_user_group-team_suc-entry">

Individual objects for each field from the Group \[sys\_user\_group\] record referenced by the specified change request. Each field object has a key that is the field name and contains **value** and **display\_value** properties. If the field type is date/time, then the method also returns a **display\_value\_internal** property which is in the user's timezone but in the system format YYYY-MM-DD HH24:MM:SS.Data type: Object

```
"sys_user_group": {
  "active": {Object},
  "cost_center": {Object},
  "default_assignee": {Object},
  "description": {Object},
  "email": {Object},
  "exclude_manager": {Object},
  "include_members": {Object},
  "manager": {Object},
  "name": {Object},
  "parent": {Object},
  "roles": {Object},
  "source": {Object},
  "sys_created_by": {Object},
  "sys_created_on": {Object},
  "sys_id": {Object},
  "sys_mod_count": {Object},
  "sys_tags": {Object},
  "sys_updated_by": {Object},
  "sys_updated_on": {Object},
  "type": {Object}
}
```

</td></tr><tr id="sys_user_group_active-team_suc-row"><td>

sys\_user\_group.active

</td><td id="sys_user_group_active-team_suc-entry">

Flag that indicates whether the group is active.Possible values:

 -   true: Group is active
-   false: Group is de-activated

 Data type: Object

 ```
"active": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr id="sys_user_group_active_display_value-team_suc-row"><td>

sys\_user\_group.active.display\_value

</td><td id="sys_user_group_active_display_value-team_suc-entry">

Display value for the active flag.Data type: String

</td></tr><tr id="sys_user_group_active_value-team_suc-row"><td>

sys\_user\_group.active.value

</td><td id="sys_user_group_active_value-team_suc-entry">

Internal value for the active flag.Data type: Boolean

</td></tr><tr id="sys_user_group_cost_center-team_suc-row"><td>

sys\_user\_group.cost\_center

</td><td id="sys_user_group_cost_center-team_suc-entry">

Sys\_id of the cost center associated with the group.Data type: Object

 ```
"cost_center": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_cost_center_display_value-team_suc-row"><td>

sys\_user\_group.cost\_center.display\_value

</td><td id="sys_user_group_cost_center_display_value-team_suc-entry">

Display value for cost\_center.Data type: String

</td></tr><tr id="sys_user_group_cost_center_value-team_suc-row"><td>

sys\_user\_group.cost\_center.value

</td><td id="sys_user_group_cost_center_value-team_suc-entry">

Internal value for cost\_center.Data type: String

</td></tr><tr id="sys_user_group_default_assignee-team_suc-row"><td>

sys\_user\_group.default\_assignee

</td><td id="sys_user_group_default_assignee-team_suc-entry">

Sys\_id of the user that is the default assignee of the group.Data type: Object

 ```
"default_assignee": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_default_assignee_display_value-team_suc-row"><td>

sys\_user\_group.default\_assignee.display\_value

</td><td id="sys_user_group_default_assignee_display_value-team_suc-entry">

Display value for default\_assignee.Data type: String

</td></tr><tr id="sys_user_group_default_assignee_value-team_suc-row"><td>

sys\_user\_group.default\_assignee.value

</td><td id="sys_user_group_default_assignee_value-team_suc-entry">

Internal value for default\_assignee.Data type: String

</td></tr><tr id="sys_user_group_description-team_suc-row"><td>

sys\_user\_group.description

</td><td id="sys_user_group_description-team_suc-entry">

Description of the groupData type: Object

 ```
"description": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_description_display_value-team_suc-row"><td>

sys\_user\_group.description.display\_value

</td><td id="sys_user_group_description_display_value-team_suc-entry">

Display value for description.Data type: String

</td></tr><tr id="sys_user_group_description_value-team_suc-row"><td>

sys\_user\_group.description.value

</td><td id="sys_user_group_description_value-team_suc-entry">

Internal value for description.Data type: String

</td></tr><tr id="sys_user_group_email-team_suc-row"><td>

sys\_user\_group.email

</td><td id="sys_user_group_email-team_suc-entry">

Email address for the group.Data type: Object

 ```
"description": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_email_display_value-team_suc-row"><td>

sys\_user\_group.email.display\_value

</td><td id="sys_user_group_email_display_value-team_suc-entry">

Display value for email.Data type: String

</td></tr><tr id="sys_user_group_email_value-team_suc-row"><td>

sys\_user\_group.email.value

</td><td id="sys_user_group_email_value-team_suc-entry">

Internal value for email.Data type: String

</td></tr><tr id="sys_user_group_exclude_manager-team_suc-row"><td>

sys\_user\_group.exclude\_manager

</td><td id="sys_user_group_exclude_manager-team_suc-entry">

Flag that indicates whether the manager of the group receives group emails.Valid values:

 -   true: Manager does not receive group emails.
-   false: Manager receives group emails.

 Data type: Object

 ```
"exclude_manager": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr id="sys_user_group_exclude_manager_display_value-team_suc-row"><td>

sys\_user\_group.exclude\_manager.display\_value

</td><td id="sys_user_group_exclude_manager_display_value-team_suc-entry">

Display value for exclude\_manager.Data type: String

</td></tr><tr id="sys_user_group_exclude_manager_value-team_suc-row"><td>

sys\_user\_group.exclude\_manager.value

</td><td id="sys_user_group_exclude_manager_value-team_suc-entry">

Internal value for exclude\_manager.Data type: Boolean

</td></tr><tr id="sys_user_group_include_members-team_suc-row"><td>

sys\_user\_group.include\_members

</td><td id="sys_user_group_include_members-team_suc-entry">

Flag that indicates whether the group members receive individual emails when someone sends an email to the group email address. The only exception to this functionality is for approval notifications, whereby all members of a group receive an approval notification, regardless of this selection.Valid values:

 -   true: Send emails to the entire group.
-   false: Only send emails to the default\_assignee.

 Data type: Object

 ```
"include_members": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr id="sys_user_group_include_members_display_value-team_suc-row"><td>

sys\_user\_group.include\_members.display\_value

</td><td id="sys_user_group_include_members_display_value-team_suc-entry">

Display value for include\_members.Data type: String

</td></tr><tr id="sys_user_group_include_members_value-team_suc-row"><td>

sys\_user\_group.include\_members.value

</td><td id="sys_user_group_include_members_value-team_suc-entry">

Internal value for include\_members.Data type: Boolean

</td></tr><tr id="sys_user_group_manager-team_suc-row"><td>

sys\_user\_group.manager

</td><td id="sys_user_group_manager-team_suc-entry">

Sys\_id of the manager of the group.Data type: Object

 ```
"manager": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_manager_display_value-team_suc-row"><td>

sys\_user\_group.manager.display\_value

</td><td id="sys_user_group_manager_display_value-team_suc-entry">

Display value for manager.Data type: String

</td></tr><tr id="sys_user_group_manager_value-team_suc-row"><td>

sys\_user\_group.manager.value

</td><td id="sys_user_group_manager_value-team_suc-entry">

Internal value for manager.Data type: String

</td></tr><tr id="sys_user_group_name-team_suc-row"><td>

sys\_user\_group.name

</td><td id="sys_user_group_name-team_suc-entry">

Name of the group.Data type: Object

 ```
"name": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_name_display_value-team_suc-row"><td>

sys\_user\_group.name.display\_value

</td><td id="sys_user_group_name_display_value-team_suc-entry">

Display value for name.Data type: String

</td></tr><tr id="sys_user_group_name_value-team_suc-row"><td>

sys\_user\_group.name.value

</td><td id="sys_user_group_name_value-team_suc-entry">

Internal value for name.Data type: String

</td></tr><tr id="sys_user_group_parent-team_suc-row"><td>

sys\_user\_group.parent

</td><td id="sys_user_group_parent-team_suc-entry">

Sys\_id of the parent of this group. If a group has a parent, the child group inherits the roles of the parent group. The members of the child group are not members of the parent group. For example, if an incident is assigned to the parent group and you click the Assigned to lookup icon, only the members in the parent group are available. The members of the child group are not available.Data type: Object

 ```
"parent": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_parent_display_value-team_suc-row"><td>

sys\_user\_group.parent.display\_value

</td><td id="sys_user_group_parent_display_value-team_suc-entry">

Display value for parent.Data type: String

</td></tr><tr id="sys_user_group_parent_value-team_suc-row"><td>

sys\_user\_group.parent.value

</td><td id="sys_user_group_parent_value-team_suc-entry">

Internal value for parent.Data type: String

</td></tr><tr id="sys_user_group_roles-team_suc-row"><td>

sys\_user\_group.roles

</td><td id="sys_user_group_roles-team_suc-entry">

User roles assigned to the group.Data type: Object

 ```
"roles": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_roles_display_value-team_suc-row"><td>

sys\_user\_group.roles.display\_value

</td><td id="sys_user_group_roles_display_value-team_suc-entry">

Display value for roles.Data type: String

</td></tr><tr id="sys_user_group_roles_value-team_suc-row"><td>

sys\_user\_group.roles.value

</td><td id="sys_user_group_roles_value-team_suc-entry">

Internal value for roles.Data type: String

</td></tr><tr id="sys_user_group_source-team_suc-row"><td>

sys\_user\_group.source

</td><td id="sys_user_group_source-team_suc-entry">

Source of the group.Data type: Object

 ```
"source": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_source_display_value-team_suc-row"><td>

sys\_user\_group.source.display\_value

</td><td id="sys_user_group_source_display_value-team_suc-entry">

Display value for source.Data type: String

</td></tr><tr id="sys_user_group_source_value-team_suc-row"><td>

sys\_user\_group.source.value

</td><td id="sys_user_group_source_value-team_suc-entry">

Internal value for source.Data type: String

</td></tr><tr id="sys_user_group_sys_created_by-team_suc-row"><td>

sys\_user\_group.sys\_created\_by

</td><td id="sys_user_group_sys_created_by-team_suc-entry">

User that created the group record.Data type: Object

 ```
"sys_created_by": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_sys_created_by_display_value-team_suc-row"><td>

sys\_user\_group.sys\_created\_by.display\_value

</td><td id="sys_user_group_sys_created_by_display_value-team_suc-entry">

Display value for sys\_created\_by.Data type: String

</td></tr><tr id="sys_user_group_sys_created_by_value-team_suc-row"><td>

sys\_user\_group.sys\_created\_by.value

</td><td id="sys_user_group_sys_created_by_value-team_suc-entry">

Internal value for sys\_created\_by.Data type: String

</td></tr><tr id="sys_user_group_sys_created_on-team_suc-row"><td>

sys\_user\_group.sys\_created\_on

</td><td id="sys_user_group_sys_created_on-team_suc-entry">

Date and time that the group record was originally created.Data type: Object

 ```
"sys_created_on": {
  "display_value": "String",
  "display_value_internal": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_sys_created_on_display_value-team_suc-row"><td>

sys\_user\_group.sys\_created\_on.display\_value

</td><td id="sys_user_group_sys_created_on_display_value-team_suc-entry">

Display value for sys\_created\_on.Data type: String

</td></tr><tr id="sys_user_group_sys_created_on_display_value_internal-team_suc-row"><td>

sys\_user\_group.sys\_created\_on.display\_value\_internal

</td><td id="sys_user_group_sys_created_on_display_value_internal-team_suc-entry">

Internal display value for sys\_created\_on.Data type: String

</td></tr><tr id="sys_user_group_sys_created_on_value-team_suc-row"><td>

sys\_user\_group.sys\_created\_on.value

</td><td id="sys_user_group_sys_created_on_value-team_suc-entry">

Internal value for sys\_created\_on.Data type: String

</td></tr><tr id="sys_user_group_sys_id-team_suc-row"><td>

sys\_user\_group.sys\_id

</td><td id="sys_user_group_sys_id-team_suc-entry">

Sys\_id for the group.Data type: Object

 ```
"sys_id": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_sys_id_display_value-team_suc-row"><td>

sys\_user\_group.sys\_id.display\_value

</td><td id="sys_user_group_sys_id_display_value-team_suc-entry">

Display value for sys\_id.Data type: String

</td></tr><tr id="sys_user_group_sys_id_value-team_suc-row"><td>

sys\_user\_group.sys\_id.value

</td><td id="sys_user_group_sys_id_value-team_suc-entry">

Internal value for sys\_id.Data type: String

</td></tr><tr id="sys_user_group_sys_mod_count-team_suc-row"><td>

sys\_user\_group.sys\_mod\_count

</td><td id="sys_user_group_sys_mod_count-team_suc-entry">

Number of times that the associated group information has been modified.Data type: Object

 ```
"sys_mod_count": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr id="sys_user_group_sys_mod_count_display_value-team_suc-row"><td>

sys\_user\_group.sys\_mod\_count.display\_value

</td><td id="sys_user_group_sys_mod_count_display_value-team_suc-entry">

Display value for sys\_mod\_count.Data type: String

</td></tr><tr id="sys_user_group_sys_mod_count_value-team_suc-row"><td>

sys\_user\_group.sys\_mod\_count.value

</td><td id="sys_user_group_sys_mod_count_value-team_suc-entry">

Internal value for sys\_mod\_count.Data type: Number

</td></tr><tr id="sys_user_group_sys_updated_by-team_suc-row"><td>

sys\_user\_group.sys\_updated\_by

</td><td id="sys_user_group_sys_updated_by-team_suc-entry">

User that last updated the group information.Data type: Object

 ```
"sys_updated_by": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_sys_updated_by_display_value-team_suc-row"><td>

sys\_user\_group.sys\_updated\_by.display\_value

</td><td id="sys_user_group_sys_updated_by_display_value-team_suc-entry">

Display value for sys\_updated\_by.Data type: String

</td></tr><tr id="sys_user_group_sys_updated_by_value-team_suc-row"><td>

sys\_user\_group.sys\_updated\_by.value

</td><td id="sys_user_group_sys_updated_by_value-team_suc-entry">

Internal value for sys\_updated\_by.Data type: String

</td></tr><tr id="sys_user_group_sys_updated_on-team_suc-row"><td>

sys\_user\_group.sys\_updated\_on

</td><td id="sys_user_group_sys_updated_on-team_suc-entry">

Date and time when the group information was last updated.Data type: Object

 ```
"sys_updated_on": {
  "display_value": "String",
  "display_value_internal": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_sys_updated_on_display_value-team_suc-row"><td>

sys\_user\_group.sys\_updated\_on.display\_value

</td><td id="sys_user_group_sys_updated_on_display_value-team_suc-entry">

Display value for sys\_updated\_on.Data type: String

</td></tr><tr id="sys_user_group_sys_updated_on_display_value_internal-team_suc-row"><td>

sys\_user\_group.sys\_updated\_on.display\_value\_internal

</td><td id="sys_user_group_sys_updated_on_display_value_internal-team_suc-entry">

Internal display value for sys\_updated\_on.Data type: String

</td></tr><tr id="sys_user_group_sys_updated_on_value-team_suc-row"><td>

sys\_user\_group.sys\_updated\_on.value

</td><td id="sys_user_group_sys_updated_on_value-team_suc-entry">

Internal value for sys\_updated\_on.Data type: String

</td></tr><tr id="sys_user_group_sys_type-team_suc-row"><td>

sys\_user\_group.type

</td><td id="sys_user_group_sys_type-team_suc-entry">

Type of group. Data type: Object

 ```
"type": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_sys_type_display_value-team_suc-row"><td>

sys\_user\_group.type.display\_value

</td><td id="sys_user_group_sys_type_display_value-team_suc-entry">

Display value for type.Data type: String

</td></tr><tr id="sys_user_group_sys_type_value-team_suc-row"><td>

sys\_user\_group.type.value

</td><td id="sys_user_group_sys_type_value-team_suc-entry">

Internal value for type.Data type: String

</td></tr></tbody>
</table>This example shows how to use the getTeamScoreForChange\(\) method for the current change request GlideRecord to retrieve the team score for the change request and then use its various attributes to construct a score summary and write it in the work notes.

```
var changeTeamSuccess = new sn_chg_score.ChangeSuccess().getTeamScoreForChange(current);
 
gs.info(JSON.stringify(changeTeamSuccess, null, 2));
 
if (changeTeamSuccess.can_read && changeTeamSuccess.score.has_score && changeTeamSuccess.chg_success_score_rating.rating.value === "Low") {
    chgGr.work_notes.setJournalEntry("The selected assignment group \"" + chgGr.assignment_group.getDisplayValue() + "\" has a " + changeTeamSuccess.chg_success_score_rating.rating.display_value + " success rating (current success score is: " + changeTeamSuccess.score.display_value + ").\nConsider adding additional approvers or discuss with your Change Manager.");
    chgGr.update();
}
```

Sample return results:

```
{
  "can_read": true,
  "sys_user_group": {
    "parent": {
      "display_value": "",
      "value": ""
    },
    "manager": {
      "display_value": "",
      "value": ""
    },
    "roles": {
      "display_value": "",
      "value": ""
    },
    "sys_mod_count": {
      "display_value": "0",
      "value": 0
    },
    "description": {
      "display_value": "",
      "value": ""
    },
    "active": {
      "display_value": "true",
      "value": true
    },
    "source": {
      "display_value": "",
      "value": ""
    },
    "sys_updated_on": {
      "display_value": "2018-03-07 21:00:41",
      "value": "2018-03-07 21:00:41",
      "display_value_internal": "2018-03-07 21:00:41"
    },
    "type": {
      "display_value": "",
      "value": ""
    },
    "sys_tags": {
      "display_value": "",
      "value": ""
    },
    "sys_id": {
      "display_value": "5f6441efc0a8010e0177fcb589156352",
      "value": "5f6441efc0a8010e0177fcb589156352"
    },
    "sys_updated_by": {
      "display_value": "glide.maint",
      "value": "glide.maint"
    },
    "cost_center": {
      "display_value": "",
      "value": ""
    },
    "default_assignee": {
      "display_value": "",
      "value": ""
    },
    "sys_created_on": {
      "display_value": "2018-03-07 21:00:41",
      "value": "2018-03-07 21:00:41",
      "display_value_internal": "2018-03-07 21:00:41"
    },
    "name": {
      "display_value": "IT Securities",
      "value": "IT Securities"
    },
    "exclude_manager": {
      "display_value": "false",
      "value": false
    },
    "email": {
      "display_value": "",
      "value": ""
    },
    "include_members": {
      "display_value": "false",
      "value": false
    },
    "sys_created_by": {
      "display_value": "glide.maint",
      "value": "glide.maint"
    }
  },
  "score": {
    "indicator": {
      "name": "Change success scores",
      "sys_id": "0ff316e173081010491d235f04f6a758"
    },
    "value": 465,
    "display_value": "465",
    "delta": {
      "value": 0,
      "display_value": "0"
    },
    "has_score": true
  },
  "chg_success_score_rating": {
    "score_start": {
      "display_value": "0",
      "value": 0
    },
    "score_end": {
      "display_value": "499",
      "value": 499
    },
    "color": {
      "display_value": "#FCCAC9",
      "value": "#FCCAC9"
    },
    "rating": {
      "display_value": "Low",
      "value": "Low"
    },
    "sys_mod_count": {
      "display_value": "0",
      "value": 0
    },
    "active": {
      "display_value": "true",
      "value": true
    },
    "sys_overrides": {
      "display_value": "",
      "value": ""
    },
    "sys_updated_on": {
      "display_value": "2020-03-27 07:43:29",
      "value": "2020-03-27 07:43:29",
      "display_value_internal": "2020-03-27 07:43:29"
    },
    "sys_tags": {
      "display_value": "",
      "value": ""
    },
    "sys_class_name": {
      "display_value": "Change Success Score Rating",
      "value": "chg_success_score_rating"
    },
    "sys_id": {
      "display_value": "7ad380b573330010491d235f04f6a717",
      "value": "7ad380b573330010491d235f04f6a717"
    },
    "sys_updated_by": {
      "display_value": "admin",
      "value": "admin"
    },
    "sys_created_on": {
      "display_value": "2020-03-27 07:43:29",
      "value": "2020-03-27 07:43:29",
      "display_value_internal": "2020-03-27 07:43:29"
    },
    "sys_domain": {
      "display_value": "global",
      "value": "global"
    },
    "sys_name": {
      "display_value": "Low",
      "value": "Low"
    },
    "sys_created_by": {
      "display_value": "admin",
      "value": "admin"
    }
  }
}
```

## ChangeSuccess - getTeamScoreForGroupId\(String sys\_id, String domain\_id\)

Returns the latest change team success score \(original change success score based on group\) for the specified group.

|Name|Type|Description|
|----|----|-----------|
|sys\_id|String|Sys\_id of the group for which to return the change team success score. Located in the User Group \[sys\_user\_group\] table.|
|domain\_id|String|Optional. Sys\_id of a domain to use when querying Performance Analytics for the team success score.|

<table id="id_yqw_l1v_15b" class="returns"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr id="can_read-team_suc-row"><td>

can\_read

</td><td id="can_read-team_suc-entry">

Flag that indicates whether a change team success score could be retrieved for the specified change request.Valid values:

-   true: Team success score was retrieved.
-   false: Team success score was not retrieved.

 Data type: Boolean

</td></tr><tr id="chg_success_score_rating-team_suc-row"><td>

chg\_success\_score\_rating

</td><td id="chg_success_score_rating-team_suc-entry">

Individual objects for each field from the Change Success Score Rating \[chg\_success\_score\_rating\] record that matches the returned score. Each field object has a key that is the field name and contains **value** and **display\_value** properties. If the field type is date/time, then the method also returns a **display\_value\_internal** property which is in the user's timezone but in the system format YYYY-MM-DD HH24:MM:SS.Data type: Object

 ```
"chg_success_score_rating": {
  "active": {Object},
  "color": {Object},
  "rating": {Object},
  "score_end": {Object},
  "score_start": {Object},
  "sys_class_name": {Object},
  "sys_created_by": {Object},
  "sys_created_on": {Object},
  "sys_domain": {Object},
  "sys_id": {Object},
  "sys_mod_count": {Object},
  "sys_name": {Object},
  "sys_overrides": {Object},
  "sys_tags": {Object},
  "sys_updated_by": {Object},
  "sys_updated_on": {Object}
}
```

</td></tr><tr id="active-team_suc-row"><td>

chg\_success\_score\_rating.active

</td><td id="active-team_suc-entry">

Flag that indicates whether the associated change success score record is active and available within the instance.Valid values:

-   true: Change success score record is active.
-   false: Change success score record is not active.

 Data type: Object

 ```
"active": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr id="active_display_value-team_suc-row"><td>

chg\_success\_score\_rating.active.display\_value

</td><td id="active_display_value-team_suc-entry">

Display value for the active flag.Data type: String

</td></tr><tr id="active_value-team_suc-row"><td>

chg\_success\_score\_rating.active.value

</td><td id="active_value-team_suc-entry">

Internal value for the active flag.Data type: Boolean

</td></tr><tr id="color-team_suc-row"><td>

chg\_success\_score\_rating.color

</td><td id="color-team_suc-entry">

Color of the associated change success score as shown in the Change Success Score Card for a change request.Data type: Object

 ```
"color": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="color_display_value-team_suc-row"><td>

chg\_success\_score\_rating.color.display\_value

</td><td id="color_display_value-team_suc-entry">

Display value for color.Data type: String

</td></tr><tr id="color_value-team_suc-row"><td>

chg\_success\_score\_rating.color.value

</td><td id="color_value-team_suc-entry">

Internal value for color.Data type: String

</td></tr><tr id="rating-team_suc-row"><td>

chg\_success\_score\_rating.rating

</td><td id="rating-team_suc-entry">

Change success score rating, such as Low or High.Data type: Object

 ```
"rating": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="rating_display_value-team_suc-row"><td>

chg\_success\_score\_rating.rating.display\_value

</td><td id="rating_display_value-team_suc-entry">

Display value for rating.Data type: String

</td></tr><tr id="rating_value-team_suc-row"><td>

chg\_success\_score\_rating.rating.value

</td><td id="rating_value-team_suc-entry">

Internal value for rating.Data type: String

</td></tr><tr id="score_end-team_suc-row"><td>

chg\_success\_score\_rating.score\_end

</td><td id="score_end-team_suc-entry">

Highest value in the change success score.Data type: Object

 ```
"score_end": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr id="score_end_display_value-team_suc-row"><td>

chg\_success\_score\_rating.score\_end.display\_value

</td><td id="score_end_display_value-team_suc-entry">

Display value for score\_end.Data type: String

</td></tr><tr id="score_end_value-team_suc-row"><td>

chg\_success\_score\_rating.score\_end.value

</td><td id="score_end_value-team_suc-entry">

Internal value for score\_end.Data type: Number

</td></tr><tr id="score_start-team_suc-row"><td>

chg\_success\_score\_rating.score\_start

</td><td id="score_start-team_suc-entry">

Lowest value in the change success score.Data type: Object

 ```
"score_start": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr id="score_start_display_value-team_suc-row"><td>

chg\_success\_score\_rating.score\_start.display\_value

</td><td id="score_start_display_value-team_suc-entry">

Display value for score\_start.Data type: String

</td></tr><tr id="score_start_value-team_suc-row"><td>

chg\_success\_score\_rating.score\_start.value

</td><td id="score_start_value-team_suc-emtry">

Internal value for score\_start.Data type: Number

</td></tr><tr id="sys_class_name-team_suc-row"><td>

chg\_success\_score\_rating.sys\_class\_name

</td><td id="sys_class_name-team_suc-entry">

Change Success Score Rating table name. Always Change Success Score Rating/chg\_success\_score\_rating.Data type: Object

 ```
"sys_class_name": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_class_name_display_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_class\_name.display\_value

</td><td id="sys_class_name_display_value-team_suc-entry">

Display value for sys\_class\_name.Data type: String

</td></tr><tr id="sys_class_name_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_class\_name.value

</td><td id="sys_class_name_value-team_suc-entry">

Internal value for sys\_class\_name.Data type: String

</td></tr><tr id="sys_created_by-team_suc-row"><td>

chg\_success\_score\_rating.sys\_created\_by

</td><td id="sys_created_by-team_suc-entry">

Name of the user that initially created the associated change success score rating record. Data type: Object

 ```
"sys_created_by": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_created_by_display_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_created\_by.display\_value

</td><td id="sys_created_by_display_value-team_suc-entry">

Display value for sys\_created\_by.Data type: String

</td></tr><tr id="sys_created_by_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_created\_by.value

</td><td id="sys_created_by_value-team_suc-entry">

Internal value for sys\_created\_by.Data type: String

</td></tr><tr id="sys_created_on-team_suc-row"><td>

chg\_success\_score\_rating.sys\_created\_on

</td><td id="sys_created_on-team_suc-entry">

Date and time that the change success score rating record was originally created.Data type: Object

 ```
"sys_created_on": {
  "display_value": "String",
  "display_value_internal": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_created_on_display_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_created\_on.display\_value

</td><td id="sys_created_on_display_value-team_suc-entry">

Display value for sys\_created\_on.Data type: String

</td></tr><tr id="sys_created_on_display_value_internal-team_suc-row"><td>

chg\_success\_score\_rating.sys\_created\_on.display\_value\_internal

</td><td id="sys_created_on_display_value_internal-team_suc-entry">

Internal display value for sys\_created\_on.Data type: String

</td></tr><tr id="sys_created_on_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_created\_on.value

</td><td id="sys_created_on_value-team_suc-entry">

Internal value for sys\_created\_on.Data type: String

</td></tr><tr id="sys_domain-team_suc-row"><td>

chg\_success\_score\_rating.sys\_domain

</td><td id="sys_domain-team_suc-entry">

If using domains in the instance, the name of the domain to which the change success score record is associated.Data type: Object

 ```
"sys_domain": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_domain_display_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_domain.display\_value

</td><td id="sys_domain_display_value-team_suc-entry">

Display value for sys\_domain.Data type: String

</td></tr><tr id="sys_domain_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_domain.value

</td><td id="sys_domain_value-team_suc-entry">

Internal value for sys\_domain.Data type: String

</td></tr><tr id="sys_id-team_suc-row"><td>

chg\_success\_score\_rating.sys\_id

</td><td id="sys_id-team_suc-entry">

Unique identifier of the associated change success score record.Data type: Object

 ```
"sys_id": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_id_display_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_id.display\_value

</td><td id="sys_id_display_value-team_suc-entry">

Display value for sys\_id.Data type: String

</td></tr><tr id="sys_id_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_id.value

</td><td id="sys_id_value-team_suc-entry">

Internal value for sys\_id.Data type: String

</td></tr><tr id="sys_mod_count-team_suc-row"><td>

chg\_success\_score\_rating.sys\_mod\_count

</td><td id="sys_mod_count-team_suc-entry">

Number of times that the associated change success score record has been modified.Data type: Object

 ```
"sys_mod_count": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr id="sys_mod_count_display_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_mod\_count.display\_value

</td><td id="sys_mod_count_display_value-team_suc-entry">

Display value for sys\_mod\_count.Data type: String

</td></tr><tr id="sys_mod_count_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_mod\_count.value

</td><td id="sys_mod_count_value-team_suc-entry">

Internal value for sys\_mod\_count.Data type: Number

</td></tr><tr id="sys_name-team_suc-row"><td>

chg\_success\_score\_rating.sys\_name

</td><td id="sys_name-team_suc-entry">

Name of the change success score rating.Possible values:

 -   Excellent
-   High
-   Low
-   Medium

 Data type: Object

 ```
"sys_name": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr id="sys_name_display_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_name.display\_value

</td><td id="sys_name_display_value-team_suc-entry">

Display value for sys\_name.Data type: String

</td></tr><tr id="sys_name_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_name.value

</td><td id="sys_name_value-team_suc-entry">

Internal value for sys\_name.Data type: String

</td></tr><tr id="sys_overrides-team_suc-row"><td>

chg\_success\_score\_rating.sys\_overrides

</td><td id="sys_overrides-team_suc-entry">

Sys\_id of a record in the same table but in a domain above that of the current record. This allows a record in a lower domain to override a record in a domain above it.For example, if you have a rating record defined in the "global" domain but for domain "TOP/ACME" you override the record in "global".

 Data type: Object

 ```
"sys_overrides": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_overrides_display_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_overrides.display\_value

</td><td id="sys_overrides_display_value-team_suc-entry">

Display value for sys\_overrides.Data type: String

</td></tr><tr id="sys_overrides_value-team_suc-row"><td>

tchg\_success\_score\_rating.sys\_overrides.value

</td><td id="sys_overrides_value-team_suc-entry">

Internal value for sys\_overrides.Data type: String

</td></tr><tr id="sys_tags-team_suc-row"><td>

chg\_success\_score\_rating.sys\_tags

</td><td id="sys_tags-team_suc-entry">

List of system tags associated with the change success score record.Data type: Object

 ```
"sys_tags": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_tags_display_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_tags.display\_value

</td><td id="sys_tags_display_value-team_suc-entry">

Display value for sys\_tags.Data type: String

</td></tr><tr id="sys_tags_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_tags.value

</td><td id="sys_tags_value-team_suc-entry">

Internal value for sys\_tags.Data type: String

</td></tr><tr id="sys_updated_by-team_suc-row"><td>

chg\_success\_score\_rating.sys\_updated\_by

</td><td id="sys_updated_by-team_suc-entry">

Name of the user that last updated the associated change success score record.Data type: Object

 ```
"sys_updated_by": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_updated_by_display_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_updated\_by.display\_value

</td><td id="sys_updated_by_display_value-team_suc-entry">

Display value for sys\_updated\_by.Data type: String

</td></tr><tr id="sys_updated_by_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_updated\_by.value

</td><td id="sys_updated_by_value-team_suc-entry">

Internal value for sys\_updated\_by.Data type: String

</td></tr><tr id="sys_updated_on-team_suc-row"><td>

chg\_success\_score\_rating.sys\_updated\_on

</td><td id="sys_updated_on-team_suc-entry">

Date and time the associated change success score record was last updated.Data type: Object

 ```
"sys_created_on": {
  "display_value": "String",
  "display_value_internal": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_updated_on_display_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_updated\_on.display\_value

</td><td id="sys_updated_on_display_value-team_suc-entry">

Display value for sys\_updated\_on.Data type: String

</td></tr><tr id="sys_updated_on_display_value_internal-team_suc-row"><td>

chg\_success\_score\_rating.sys\_updated\_on.display\_value\_internal

</td><td id="sys_updated_on_display_value_internal-team_suc-entry">

Internal display value for sys\_updated\_on.Data type: String

</td></tr><tr id="sys_updated_on_value-team_suc-row"><td>

chg\_success\_score\_rating.sys\_updated\_on.value

</td><td id="sys_updated_on_value-team_suc-entry">

Internal value for sys\_updated\_on.Data type: String

</td></tr><tr><td>

score

</td><td id="score-chg_suc-entry">

Details about the returned score indicator.Data type: Object

 ```
"score": {
  "delta": {Object},
  "display_value": "String",
  "has_score": Boolean,
  "indicator": {Object},
  "value": Number
}
```

</td></tr><tr><td>

score.delta

</td><td id="score_delta-chg_suc-entry">

Change in the score from the previous score.Data type: Object

 ```
"delta": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

score.delta.display\_value

</td><td id="score_delta_display_value-chg_suc-entry">

Display value for delta.Data type: String

</td></tr><tr><td>

score.delta.value

</td><td id="score_delta_value-chg_suc-entry">

Internal value for delta.Data type: String

</td></tr><tr><td>

score.display\_value

</td><td id="score_display_value-chg_suc-entry">

Display value returned by Performance Analytics \(PA\).Data type: String

</td></tr><tr><td>

score.has\_score

</td><td id="score_has_score-chg_suc-entry">

Flag that indicates whether a score was returned for the specified change request.

 Valid values:

-   true: Score was returned.
-   false: No score was returned.

 Data type: Boolean

</td></tr><tr><td>

score.indicator

</td><td id="score_indicator-chg_suc-entry">

Additional details on the PA indicator used to obtain the score.Data type: Object

 ```
"indicator": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

score.indicator.name

</td><td id="score_indicator_name-chg_suc-entry">

Name of the PA indicator used to obtain the score.Data type: String

</td></tr><tr><td>

score.indicator.sys\_id

</td><td id="score_indicator_sys_id-chg_suc-entry">

Sys\_id of the PA indicator used to obtain the score.Data type: String

</td></tr><tr><td>

score.value

</td><td id="score_value-chg_suc-entry">

Value returned by PA for the success score.Data type: String

</td></tr><tr id="sys_user_group-team_suc-row"><td>

sys\_user\_group

</td><td id="sys_user_group-team_suc-entry">

Individual objects for each field from the Group \[sys\_user\_group\] record referenced by the specified change request. Each field object has a key that is the field name and contains **value** and **display\_value** properties. If the field type is date/time, then the method also returns a **display\_value\_internal** property which is in the user's timezone but in the system format YYYY-MM-DD HH24:MM:SS.Data type: Object

```
"sys_user_group": {
  "active": {Object},
  "cost_center": {Object},
  "default_assignee": {Object},
  "description": {Object},
  "email": {Object},
  "exclude_manager": {Object},
  "include_members": {Object},
  "manager": {Object},
  "name": {Object},
  "parent": {Object},
  "roles": {Object},
  "source": {Object},
  "sys_created_by": {Object},
  "sys_created_on": {Object},
  "sys_id": {Object},
  "sys_mod_count": {Object},
  "sys_tags": {Object},
  "sys_updated_by": {Object},
  "sys_updated_on": {Object},
  "type": {Object}
}
```

</td></tr><tr id="sys_user_group_active-team_suc-row"><td>

sys\_user\_group.active

</td><td id="sys_user_group_active-team_suc-entry">

Flag that indicates whether the group is active.Possible values:

 -   true: Group is active
-   false: Group is de-activated

 Data type: Object

 ```
"active": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr id="sys_user_group_active_display_value-team_suc-row"><td>

sys\_user\_group.active.display\_value

</td><td id="sys_user_group_active_display_value-team_suc-entry">

Display value for the active flag.Data type: String

</td></tr><tr id="sys_user_group_active_value-team_suc-row"><td>

sys\_user\_group.active.value

</td><td id="sys_user_group_active_value-team_suc-entry">

Internal value for the active flag.Data type: Boolean

</td></tr><tr id="sys_user_group_cost_center-team_suc-row"><td>

sys\_user\_group.cost\_center

</td><td id="sys_user_group_cost_center-team_suc-entry">

Sys\_id of the cost center associated with the group.Data type: Object

 ```
"cost_center": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_cost_center_display_value-team_suc-row"><td>

sys\_user\_group.cost\_center.display\_value

</td><td id="sys_user_group_cost_center_display_value-team_suc-entry">

Display value for cost\_center.Data type: String

</td></tr><tr id="sys_user_group_cost_center_value-team_suc-row"><td>

sys\_user\_group.cost\_center.value

</td><td id="sys_user_group_cost_center_value-team_suc-entry">

Internal value for cost\_center.Data type: String

</td></tr><tr id="sys_user_group_default_assignee-team_suc-row"><td>

sys\_user\_group.default\_assignee

</td><td id="sys_user_group_default_assignee-team_suc-entry">

Sys\_id of the user that is the default assignee of the group.Data type: Object

 ```
"default_assignee": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_default_assignee_display_value-team_suc-row"><td>

sys\_user\_group.default\_assignee.display\_value

</td><td id="sys_user_group_default_assignee_display_value-team_suc-entry">

Display value for default\_assignee.Data type: String

</td></tr><tr id="sys_user_group_default_assignee_value-team_suc-row"><td>

sys\_user\_group.default\_assignee.value

</td><td id="sys_user_group_default_assignee_value-team_suc-entry">

Internal value for default\_assignee.Data type: String

</td></tr><tr id="sys_user_group_description-team_suc-row"><td>

sys\_user\_group.description

</td><td id="sys_user_group_description-team_suc-entry">

Description of the groupData type: Object

 ```
"description": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_description_display_value-team_suc-row"><td>

sys\_user\_group.description.display\_value

</td><td id="sys_user_group_description_display_value-team_suc-entry">

Display value for description.Data type: String

</td></tr><tr id="sys_user_group_description_value-team_suc-row"><td>

sys\_user\_group.description.value

</td><td id="sys_user_group_description_value-team_suc-entry">

Internal value for description.Data type: String

</td></tr><tr id="sys_user_group_email-team_suc-row"><td>

sys\_user\_group.email

</td><td id="sys_user_group_email-team_suc-entry">

Email address for the group.Data type: Object

 ```
"description": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_email_display_value-team_suc-row"><td>

sys\_user\_group.email.display\_value

</td><td id="sys_user_group_email_display_value-team_suc-entry">

Display value for email.Data type: String

</td></tr><tr id="sys_user_group_email_value-team_suc-row"><td>

sys\_user\_group.email.value

</td><td id="sys_user_group_email_value-team_suc-entry">

Internal value for email.Data type: String

</td></tr><tr id="sys_user_group_exclude_manager-team_suc-row"><td>

sys\_user\_group.exclude\_manager

</td><td id="sys_user_group_exclude_manager-team_suc-entry">

Flag that indicates whether the manager of the group receives group emails.Valid values:

 -   true: Manager does not receive group emails.
-   false: Manager receives group emails.

 Data type: Object

 ```
"exclude_manager": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr id="sys_user_group_exclude_manager_display_value-team_suc-row"><td>

sys\_user\_group.exclude\_manager.display\_value

</td><td id="sys_user_group_exclude_manager_display_value-team_suc-entry">

Display value for exclude\_manager.Data type: String

</td></tr><tr id="sys_user_group_exclude_manager_value-team_suc-row"><td>

sys\_user\_group.exclude\_manager.value

</td><td id="sys_user_group_exclude_manager_value-team_suc-entry">

Internal value for exclude\_manager.Data type: Boolean

</td></tr><tr id="sys_user_group_include_members-team_suc-row"><td>

sys\_user\_group.include\_members

</td><td id="sys_user_group_include_members-team_suc-entry">

Flag that indicates whether the group members receive individual emails when someone sends an email to the group email address. The only exception to this functionality is for approval notifications, whereby all members of a group receive an approval notification, regardless of this selection.Valid values:

 -   true: Send emails to the entire group.
-   false: Only send emails to the default\_assignee.

 Data type: Object

 ```
"include_members": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr id="sys_user_group_include_members_display_value-team_suc-row"><td>

sys\_user\_group.include\_members.display\_value

</td><td id="sys_user_group_include_members_display_value-team_suc-entry">

Display value for include\_members.Data type: String

</td></tr><tr id="sys_user_group_include_members_value-team_suc-row"><td>

sys\_user\_group.include\_members.value

</td><td id="sys_user_group_include_members_value-team_suc-entry">

Internal value for include\_members.Data type: Boolean

</td></tr><tr id="sys_user_group_manager-team_suc-row"><td>

sys\_user\_group.manager

</td><td id="sys_user_group_manager-team_suc-entry">

Sys\_id of the manager of the group.Data type: Object

 ```
"manager": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_manager_display_value-team_suc-row"><td>

sys\_user\_group.manager.display\_value

</td><td id="sys_user_group_manager_display_value-team_suc-entry">

Display value for manager.Data type: String

</td></tr><tr id="sys_user_group_manager_value-team_suc-row"><td>

sys\_user\_group.manager.value

</td><td id="sys_user_group_manager_value-team_suc-entry">

Internal value for manager.Data type: String

</td></tr><tr id="sys_user_group_name-team_suc-row"><td>

sys\_user\_group.name

</td><td id="sys_user_group_name-team_suc-entry">

Name of the group.Data type: Object

 ```
"name": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_name_display_value-team_suc-row"><td>

sys\_user\_group.name.display\_value

</td><td id="sys_user_group_name_display_value-team_suc-entry">

Display value for name.Data type: String

</td></tr><tr id="sys_user_group_name_value-team_suc-row"><td>

sys\_user\_group.name.value

</td><td id="sys_user_group_name_value-team_suc-entry">

Internal value for name.Data type: String

</td></tr><tr id="sys_user_group_parent-team_suc-row"><td>

sys\_user\_group.parent

</td><td id="sys_user_group_parent-team_suc-entry">

Sys\_id of the parent of this group. If a group has a parent, the child group inherits the roles of the parent group. The members of the child group are not members of the parent group. For example, if an incident is assigned to the parent group and you click the Assigned to lookup icon, only the members in the parent group are available. The members of the child group are not available.Data type: Object

 ```
"parent": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_parent_display_value-team_suc-row"><td>

sys\_user\_group.parent.display\_value

</td><td id="sys_user_group_parent_display_value-team_suc-entry">

Display value for parent.Data type: String

</td></tr><tr id="sys_user_group_parent_value-team_suc-row"><td>

sys\_user\_group.parent.value

</td><td id="sys_user_group_parent_value-team_suc-entry">

Internal value for parent.Data type: String

</td></tr><tr id="sys_user_group_roles-team_suc-row"><td>

sys\_user\_group.roles

</td><td id="sys_user_group_roles-team_suc-entry">

User roles assigned to the group.Data type: Object

 ```
"roles": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_roles_display_value-team_suc-row"><td>

sys\_user\_group.roles.display\_value

</td><td id="sys_user_group_roles_display_value-team_suc-entry">

Display value for roles.Data type: String

</td></tr><tr id="sys_user_group_roles_value-team_suc-row"><td>

sys\_user\_group.roles.value

</td><td id="sys_user_group_roles_value-team_suc-entry">

Internal value for roles.Data type: String

</td></tr><tr id="sys_user_group_source-team_suc-row"><td>

sys\_user\_group.source

</td><td id="sys_user_group_source-team_suc-entry">

Source of the group.Data type: Object

 ```
"source": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_source_display_value-team_suc-row"><td>

sys\_user\_group.source.display\_value

</td><td id="sys_user_group_source_display_value-team_suc-entry">

Display value for source.Data type: String

</td></tr><tr id="sys_user_group_source_value-team_suc-row"><td>

sys\_user\_group.source.value

</td><td id="sys_user_group_source_value-team_suc-entry">

Internal value for source.Data type: String

</td></tr><tr id="sys_user_group_sys_created_by-team_suc-row"><td>

sys\_user\_group.sys\_created\_by

</td><td id="sys_user_group_sys_created_by-team_suc-entry">

User that created the group record.Data type: Object

 ```
"sys_created_by": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_sys_created_by_display_value-team_suc-row"><td>

sys\_user\_group.sys\_created\_by.display\_value

</td><td id="sys_user_group_sys_created_by_display_value-team_suc-entry">

Display value for sys\_created\_by.Data type: String

</td></tr><tr id="sys_user_group_sys_created_by_value-team_suc-row"><td>

sys\_user\_group.sys\_created\_by.value

</td><td id="sys_user_group_sys_created_by_value-team_suc-entry">

Internal value for sys\_created\_by.Data type: String

</td></tr><tr id="sys_user_group_sys_created_on-team_suc-row"><td>

sys\_user\_group.sys\_created\_on

</td><td id="sys_user_group_sys_created_on-team_suc-entry">

Date and time that the group record was originally created.Data type: Object

 ```
"sys_created_on": {
  "display_value": "String",
  "display_value_internal": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_sys_created_on_display_value-team_suc-row"><td>

sys\_user\_group.sys\_created\_on.display\_value

</td><td id="sys_user_group_sys_created_on_display_value-team_suc-entry">

Display value for sys\_created\_on.Data type: String

</td></tr><tr id="sys_user_group_sys_created_on_display_value_internal-team_suc-row"><td>

sys\_user\_group.sys\_created\_on.display\_value\_internal

</td><td id="sys_user_group_sys_created_on_display_value_internal-team_suc-entry">

Internal display value for sys\_created\_on.Data type: String

</td></tr><tr id="sys_user_group_sys_created_on_value-team_suc-row"><td>

sys\_user\_group.sys\_created\_on.value

</td><td id="sys_user_group_sys_created_on_value-team_suc-entry">

Internal value for sys\_created\_on.Data type: String

</td></tr><tr id="sys_user_group_sys_id-team_suc-row"><td>

sys\_user\_group.sys\_id

</td><td id="sys_user_group_sys_id-team_suc-entry">

Sys\_id for the group.Data type: Object

 ```
"sys_id": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_sys_id_display_value-team_suc-row"><td>

sys\_user\_group.sys\_id.display\_value

</td><td id="sys_user_group_sys_id_display_value-team_suc-entry">

Display value for sys\_id.Data type: String

</td></tr><tr id="sys_user_group_sys_id_value-team_suc-row"><td>

sys\_user\_group.sys\_id.value

</td><td id="sys_user_group_sys_id_value-team_suc-entry">

Internal value for sys\_id.Data type: String

</td></tr><tr id="sys_user_group_sys_mod_count-team_suc-row"><td>

sys\_user\_group.sys\_mod\_count

</td><td id="sys_user_group_sys_mod_count-team_suc-entry">

Number of times that the associated group information has been modified.Data type: Object

 ```
"sys_mod_count": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr id="sys_user_group_sys_mod_count_display_value-team_suc-row"><td>

sys\_user\_group.sys\_mod\_count.display\_value

</td><td id="sys_user_group_sys_mod_count_display_value-team_suc-entry">

Display value for sys\_mod\_count.Data type: String

</td></tr><tr id="sys_user_group_sys_mod_count_value-team_suc-row"><td>

sys\_user\_group.sys\_mod\_count.value

</td><td id="sys_user_group_sys_mod_count_value-team_suc-entry">

Internal value for sys\_mod\_count.Data type: Number

</td></tr><tr id="sys_user_group_sys_updated_by-team_suc-row"><td>

sys\_user\_group.sys\_updated\_by

</td><td id="sys_user_group_sys_updated_by-team_suc-entry">

User that last updated the group information.Data type: Object

 ```
"sys_updated_by": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_sys_updated_by_display_value-team_suc-row"><td>

sys\_user\_group.sys\_updated\_by.display\_value

</td><td id="sys_user_group_sys_updated_by_display_value-team_suc-entry">

Display value for sys\_updated\_by.Data type: String

</td></tr><tr id="sys_user_group_sys_updated_by_value-team_suc-row"><td>

sys\_user\_group.sys\_updated\_by.value

</td><td id="sys_user_group_sys_updated_by_value-team_suc-entry">

Internal value for sys\_updated\_by.Data type: String

</td></tr><tr id="sys_user_group_sys_updated_on-team_suc-row"><td>

sys\_user\_group.sys\_updated\_on

</td><td id="sys_user_group_sys_updated_on-team_suc-entry">

Date and time when the group information was last updated.Data type: Object

 ```
"sys_updated_on": {
  "display_value": "String",
  "display_value_internal": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_sys_updated_on_display_value-team_suc-row"><td>

sys\_user\_group.sys\_updated\_on.display\_value

</td><td id="sys_user_group_sys_updated_on_display_value-team_suc-entry">

Display value for sys\_updated\_on.Data type: String

</td></tr><tr id="sys_user_group_sys_updated_on_display_value_internal-team_suc-row"><td>

sys\_user\_group.sys\_updated\_on.display\_value\_internal

</td><td id="sys_user_group_sys_updated_on_display_value_internal-team_suc-entry">

Internal display value for sys\_updated\_on.Data type: String

</td></tr><tr id="sys_user_group_sys_updated_on_value-team_suc-row"><td>

sys\_user\_group.sys\_updated\_on.value

</td><td id="sys_user_group_sys_updated_on_value-team_suc-entry">

Internal value for sys\_updated\_on.Data type: String

</td></tr><tr id="sys_user_group_sys_type-team_suc-row"><td>

sys\_user\_group.type

</td><td id="sys_user_group_sys_type-team_suc-entry">

Type of group. Data type: Object

 ```
"type": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="sys_user_group_sys_type_display_value-team_suc-row"><td>

sys\_user\_group.type.display\_value

</td><td id="sys_user_group_sys_type_display_value-team_suc-entry">

Display value for type.Data type: String

</td></tr><tr id="sys_user_group_sys_type_value-team_suc-row"><td>

sys\_user\_group.type.value

</td><td id="sys_user_group_sys_type_value-team_suc-entry">

Internal value for type.Data type: String

</td></tr></tbody>
</table>The following code example shows how to use the getTeamScoreForGroupId\(\) method to retrieve the team score for a group, filter through the requested records, and then places all low group scores and deltas in the event queue `change_success.team.warning` of the associated group record.

```
var chgGroupGr = new GlideAggregate("change_request");
chgGroupGr.addInactiveQuery();
chgGroupGr.addNotNullQuery("close_code");
chgGroupGr.groupBy("assignment_group");
chgGroupGr.query();
 
while (chgGroupGr.next()) {
    var groupId = chgGroupGr.getValue("assignment_group");
    var changeTeamSuccess = new sn_chg_score.ChangeSuccess().getTeamScoreForGroupId(groupId);
    if (changeTeamSuccess.can_read && changeTeamSuccess.score.has_score && changeTeamSuccess.chg_success_score_rating.rating.value === "Low") {
        var grpGr = new GlideRecord("sys_user_group");
        grpGr.get(groupId);
        gs.eventQueue("change_success.team.warning", grpGr, changeTeamSuccess.score.value, changeTeamSuccess.score.delta.value);
    }
}
```

Example of the return results when calling this method:

```
{
  "can_read": true,
  "sys_user_group": {
    "parent": {
      "display_value": "",
      "value": ""
    },
    "manager": {
      "display_value": "",
      "value": ""
    },
    "roles": {
      "display_value": "",
      "value": ""
    },
    "sys_mod_count": {
      "display_value": "1",
      "value": 1
    },
    "description": {
      "display_value": "LDAP admins group",
      "value": "LDAP admins group"
    },
    "active": {
      "display_value": "true",
      "value": true
    },
    "source": {
      "display_value": "",
      "value": ""
    },
    "sys_updated_on": {
      "display_value": "2013-07-26 22:48:47",
      "value": "2013-07-26 21:48:47",
      "display_value_internal": "2013-07-26 22:48:47"
    },
    "type": {
      "display_value": "",
      "value": ""
    },
    "sys_tags": {
      "display_value": "",
      "value": ""
    },
    "sys_id": {
      "display_value": "dc0db135c332010016194ffe5bba8f23",
      "value": "dc0db135c332010016194ffe5bba8f23"
    },
    "sys_updated_by": {
      "display_value": "admin",
      "value": "admin"
    },
    "cost_center": {
      "display_value": "",
      "value": ""
    },
    "default_assignee": {
      "display_value": "",
      "value": ""
    },
    "sys_created_on": {
      "display_value": "2013-07-26 22:12:56",
      "value": "2013-07-26 21:12:56",
      "display_value_internal": "2013-07-26 22:12:56"
    },
    "name": {
      "display_value": "LDAP Admins",
      "value": "LDAP Admins"
    },
    "exclude_manager": {
      "display_value": "false",
      "value": false
    },
    "email": {
      "display_value": "",
      "value": ""
    },
    "include_members": {
      "display_value": "false",
      "value": false
    },
    "sys_created_by": {
      "display_value": "admin",
      "value": "admin"
    }
  },
  "score": {
    "indicator": {
      "name": "Change success scores",
      "sys_id": "0ff316e173081010491d235f04f6a758"
    },
    "value": 510,
    "display_value": "510",
    "delta": {
      "value": 0,
      "display_value": "0"
    },
    "has_score": true
  },
  "chg_success_score_rating": {
    "score_start": {
      "display_value": "500",
      "value": 500
    },
    "score_end": {
      "display_value": "599",
      "value": 599
    },
    "color": {
      "display_value": "#FDEEC5",
      "value": "#FDEEC5"
    },
    "rating": {
      "display_value": "Medium",
      "value": "Medium"
    },
    "sys_mod_count": {
      "display_value": "0",
      "value": 0
    },
    "active": {
      "display_value": "true",
      "value": true
    },
    "sys_overrides": {
      "display_value": "",
      "value": ""
    },
    "sys_updated_on": {
      "display_value": "2020-03-27 07:44:07",
      "value": "2020-03-27 07:44:07",
      "display_value_internal": "2020-03-27 07:44:07"
    },
    "sys_tags": {
      "display_value": "",
      "value": ""
    },
    "sys_class_name": {
      "display_value": "Change Success Score Rating",
      "value": "chg_success_score_rating"
    },
    "sys_id": {
      "display_value": "5dc448fd73330010491d235f04f6a7de",
      "value": "5dc448fd73330010491d235f04f6a7de"
    },
    "sys_updated_by": {
      "display_value": "admin",
      "value": "admin"
    },
    "sys_created_on": {
      "display_value": "2020-03-27 07:44:07",
      "value": "2020-03-27 07:44:07",
      "display_value_internal": "2020-03-27 07:44:07"
    },
    "sys_domain": {
      "display_value": "global",
      "value": "global"
    },
    "sys_name": {
      "display_value": "Medium",
      "value": "Medium"
    },
    "sys_created_by": {
      "display_value": "admin",
      "value": "admin"
    }
  }
}
```

## ChangeSuccess - getTypeScoreForChange\(Object chgGr\)

Returns the latest type success score based on the specified change request GlideRecord.

|Name|Type|Description|
|----|----|-----------|
|chgGr|Object|Change request GlideRecord for which to return the type success score.|

<table id="table_n3y_xr2_ltb" class="returns"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

can\_read

</td><td id="can_read-type_suc-entry">

Flag that indicates whether a type success score could be retrieved for the specified change request.Valid values:

-   true: Type success score was retrieved.
-   false: Type success score was not retrieved.

 Data type: Boolean

</td></tr><tr><td>

score

</td><td id="score-chg_suc-entry">

Details about the returned score indicator.Data type: Object

 ```
"score": {
  "delta": {Object},
  "display_value": "String",
  "has_score": Boolean,
  "indicator": {Object},
  "value": Number
}
```

</td></tr><tr><td>

score.delta

</td><td id="score_delta-chg_suc-entry">

Change in the score from the previous score.Data type: Object

 ```
"delta": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

score.delta.display\_value

</td><td id="score_delta_display_value-chg_suc-entry">

Display value for delta.Data type: String

</td></tr><tr><td>

score.delta.value

</td><td id="score_delta_value-chg_suc-entry">

Internal value for delta.Data type: String

</td></tr><tr><td>

score.display\_value

</td><td id="score_display_value-chg_suc-entry">

Display value returned by Performance Analytics \(PA\).Data type: String

</td></tr><tr><td>

score.has\_score

</td><td id="score_has_score-chg_suc-entry">

Flag that indicates whether a score was returned for the specified change request.

 Valid values:

-   true: Score was returned.
-   false: No score was returned.

 Data type: Boolean

</td></tr><tr><td>

score.indicator

</td><td id="score_indicator-chg_suc-entry">

Additional details on the PA indicator used to obtain the score.Data type: Object

 ```
"indicator": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

score.indicator.name

</td><td id="score_indicator_name-chg_suc-entry">

Name of the PA indicator used to obtain the score.Data type: String

</td></tr><tr><td>

score.indicator.sys\_id

</td><td id="score_indicator_sys_id-chg_suc-entry">

Sys\_id of the PA indicator used to obtain the score.Data type: String

</td></tr><tr><td>

score.value

</td><td id="score_value-chg_suc-entry">

Value returned by PA for the success score.Data type: String

</td></tr><tr><td>

type

</td><td id="type-type_suc-entry">

Details about the type success score.Data type: Object

 ```
"type": {
  "display_value": "String",
  "sys_id": "String",
  "value": "String"
}
```

</td></tr><tr><td>

type.display\_value

</td><td id="type__display_value-type_suc-entry">

Label of the choice.Data type: String

</td></tr><tr><td>

type.sys\_id

</td><td id="type_sys_id-type_suc-entry">

Sys\_id of the Choice \[sys\_choice\] record for the specified change type.Data type: String

</td></tr><tr><td>

type.value

</td><td id="type_value-type_suc-entry">

Value of the choice.Data type: String

</td></tr></tbody>
</table>This code example shows how to retrieve the latest type success score based on the current GlideRecord for change models that the user has read access for and have a success score value that is less than 50%. It then stores them in the work notes.

```
var changeTypeSuccess = new sn_chg_score.ChangeSuccess().getTypeScoreForChange(current);
 
gs.info(JSON.stringify(changeTypeSuccess, null, 2));
 
if (changeTypeSuccess.can_read && changeTypeSuccess.score.has_score && changeTypeSuccess.score.value < 50) {
   current.work_notes.setJournalEntry("The selected Change Type of \"" + changeTypeSuccess.type.display_value + "\" has a success rate of less than 50% (current success rate is: " + changeTypeSuccess.score.display_value + "%).\nConsider using a different Type or adding additional approvers or discuss with your Change Manager.");
   current.update();
}
```

Example of the return results when calling this method:

```
{
  "can_read": true,
  "type": {
    "sys_id": "e7a27d53cb100200d71cb9c0c24c9c2f",
    "value": "normal",
    "display_value": "Normal"
  },
  "score": {
    "indicator": {
      "name": "Change Type: % Successful and Successful With Issues",
      "sys_id": "f9d25995c3ce011005aea539e540ddee"
    },
    "value": 74.29906542056075,
    "display_value": "74.30",
    "delta": {
      "value": 0,
      "display_value": "0.00"
    },
    "has_score": true
  }
}
```

## ChangeSuccess - getTypeScoreForType\(String type, String domain\_id\)

Returns the latest type success score for the specified change type.

|Name|Type|Description|
|----|----|-----------|
|type|String|Type of change request for which to return the type success score, such as "emergency".|
|domain\_id|String|Optional. Sys\_id of a domain to use when querying Performance Analytics for the type success score.|

<table id="table_fcg_mt2_ltb" class="returns"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

can\_read

</td><td id="can_read-type_suc-entry">

Flag that indicates whether a type success score could be retrieved for the specified change request.Valid values:

-   true: Type success score was retrieved.
-   false: Type success score was not retrieved.

 Data type: Boolean

</td></tr><tr><td>

score

</td><td id="score-chg_suc-entry">

Details about the returned score indicator.Data type: Object

 ```
"score": {
  "delta": {Object},
  "display_value": "String",
  "has_score": Boolean,
  "indicator": {Object},
  "value": Number
}
```

</td></tr><tr><td>

score.delta

</td><td id="score_delta-chg_suc-entry">

Change in the score from the previous score.Data type: Object

 ```
"delta": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

score.delta.display\_value

</td><td id="score_delta_display_value-chg_suc-entry">

Display value for delta.Data type: String

</td></tr><tr><td>

score.delta.value

</td><td id="score_delta_value-chg_suc-entry">

Internal value for delta.Data type: String

</td></tr><tr><td>

score.display\_value

</td><td id="score_display_value-chg_suc-entry">

Display value returned by Performance Analytics \(PA\).Data type: String

</td></tr><tr><td>

score.has\_score

</td><td id="score_has_score-chg_suc-entry">

Flag that indicates whether a score was returned for the specified change request.

 Valid values:

-   true: Score was returned.
-   false: No score was returned.

 Data type: Boolean

</td></tr><tr><td>

score.indicator

</td><td id="score_indicator-chg_suc-entry">

Additional details on the PA indicator used to obtain the score.Data type: Object

 ```
"indicator": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

score.indicator.name

</td><td id="score_indicator_name-chg_suc-entry">

Name of the PA indicator used to obtain the score.Data type: String

</td></tr><tr><td>

score.indicator.sys\_id

</td><td id="score_indicator_sys_id-chg_suc-entry">

Sys\_id of the PA indicator used to obtain the score.Data type: String

</td></tr><tr><td>

score.value

</td><td id="score_value-chg_suc-entry">

Value returned by PA for the success score.Data type: String

</td></tr><tr><td>

type

</td><td id="type-type_suc-entry">

Details about the type success score.Data type: Object

 ```
"type": {
  "display_value": "String",
  "sys_id": "String",
  "value": "String"
}
```

</td></tr><tr><td>

type.sys\_id

</td><td id="type_sys_id-type_suc-entry">

Sys\_id of the Choice \[sys\_choice\] record for the specified change type.Data type: String

</td></tr><tr><td>

type.value

</td><td id="type_value-type_suc-entry">

Value of the choice.Data type: String

</td></tr><tr><td>

type.display\_value

</td><td id="type__display_value-type_suc-entry">

Label of the choice.Data type: String

</td></tr></tbody>
</table>The following code example shows how to use the getTypeScoreForType\(\) method to retrieve the type score for specified types \(name, element, and language\) and filter through the requested records. It then places all type scores that are less than 65% in the event queue `change_success.type.warning` of the associated sys\_choice record.

```
var chgTypeGr = new GlideRecord("sys_choice");
chgTypeGr.addQuery("name", "change_request");
chgTypeGr.addQuery("element", "type");
chgTypeGr.addQuery("language", "en");
chgTypeGr.query();
 
while (chgTypeGr.next()) {
    var changeTypeSuccess = new sn_chg_score.ChangeSuccess().getTypeScoreForType(chgTypeGr.getValue("value"));
    if (changeTypeSuccess.can_read && changeTypeSuccess.score.has_score && changeTypeSuccess.score.value < 65)
        gs.eventQueue("change_success.type.warning", chgTypeGr, changeTypeSuccess.score.value, changeTypeSuccess.score.delta.value);
}
```

Example of the return results when calling this method:

```
{
  "can_read": true,
  "type": {
    "sys_id": "2ba27d53cb100200d71cb9c0c24c9c2f",
    "value": "emergency",
    "display_value": "Emergency"
  },
  "score": {
    "indicator": {
      "name": "Change Type: % Successful and Successful With Issues",
      "sys_id": "f9d25995c3ce011005aea539e540ddee"
    },
    "value": 82.97872340425532,
    "display_value": "82.98",
    "delta": {
      "value": 0,
      "display_value": "0.00"
    },
    "has_score": true
  }
}
```

## ChangeSuccess - withIndicatorScores\(Boolean toggle\)

Controls whether the associated method returns the details of the Performance Analytics \(PA\) indicators used to generate each of the different types of scores \(team, model and type\). By default, this information is not returned.

Use this method to toggle the return of this data on or off for the current ChangeSuccess object. This method is a helper method and must be used in conjunction with one of the other methods that return a success score such as:

-   [ChangeSuccess - getScoresForChange\(Object chgGr\)](ChangeSuccessScopedAPI.md#)
-   [ChangeSuccess - getTeamScoreForChange\(Object chgGr\)](ChangeSuccessScopedAPI.md#)
-   [ChangeSuccess - getModelScoreForModelId\(String sys\_id, String domain\_id\)](ChangeSuccessScopedAPI.md#)

<table id="table_zhv_yhk_ltb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

toggle

</td><td>

Boolean

</td><td>

Flag that indicates whether to include the details of the PA indicators.Valid values:

-   true: Return the details of the PA indicators.
-   false: Do not return the details of the PA indicators.

 Default: false

</td></tr></tbody>
</table><table id="table_a3v_yhk_ltb" class="returns"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

indicator\_scores

</td><td>

Details about the returned score indicator.Data type: Object

 ```
"score": {
  "delta": {Object},
  "display_value": "String",
  "has_score": Boolean,
  "indicator": {Object},
  "value": Number
}
```

</td></tr><tr><td>

indicator\_scores.delta

</td><td>

Change in the score from the previous score.Data type: Object

 ```
"delta": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

indicator\_scores.delta.display\_value

</td><td>

Display value for delta.Data type: String

</td></tr><tr><td>

indicator\_scores.delta.value

</td><td>

Internal value for delta.Data type: String

</td></tr><tr><td>

indicator\_scores.display\_value

</td><td>

Display value returned by Performance Analytics \(PA\).Data type: String

</td></tr><tr><td>

indicator\_scores.has\_score

</td><td>

Flag that indicates whether a score was returned for the specified change request.

 Valid values:

-   true: Score was returned.
-   false: No score was returned.

 Data type: Boolean

</td></tr><tr><td>

indicator\_scores.indicator

</td><td>

Additional details on the PA indicator used to obtain the score.Data type: Object

 ```
"indicator": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

indicator\_scores.indicator.name

</td><td>

Name of the PA indicator used to obtain the score.Data type: String

</td></tr><tr><td>

indicator\_scores.indicator.sys\_id

</td><td>

Sys\_id of the PA indicator used to obtain the score.Data type: String

</td></tr><tr><td>

indicator\_scores.value

</td><td>

Value returned by PA for the success score.Data type: String

</td></tr></tbody>
</table>The following example shows how to request that the indicator scores not be returned in a getScoresForChange\(\) call.

```
var chgGr = new GlideRecord("change_request");
chgGr.get("number", "CHG0030305");

gs.info(JSON.stringify(new sn_chg_score.ChangeSuccess().withIndicatorScores(false).getScoresForChange(chgGr), null, 2));
```

The following output only shows the indicator score values that are returned if this helper is set to true. Other values may also be returned based on the method that this helper is attached to.

```
"indicator_scores": [
  {
    "indicator": {
      "name": "Total changes",
      "sys_id": "966e899173401010491d235f04f6a7ef"
    },
    "value": 11,
    "display_value": "11",
    "delta": {
      "value": 0,
      "display_value": "0"
    },
    "has_score": true
  }
]
```

## ChangeSuccess - withModelScore\(Boolean toggle\)

Only valid when called with the getScoresForChange\(\) method. Controls whether the getScoresForChange\(\) method returns the model score. By default the model score is returned.

Use this method to toggle the return of this data on or off for the current ChangeSuccess object.

<table id="table_ppv_vx2_ltb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

toggle

</td><td>

Boolean

</td><td>

Flag that indicates whether to include the model success score.

 Valid values:

-   true: Return the model success score.
-   false: Do not return the model success score.

 Default: true

</td></tr></tbody>
</table><table id="table_qpv_vx2_ltb" class="returns"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

model\_success\_score

</td><td>

Details on the model success score.Data type: Object

 ```
"model_success_score" {
  "can_read": Boolean,
  "chg_model": {Object},
  "score": {Object}
}
```

</td></tr><tr><td>

model\_success\_score.can\_read

</td><td>

Flag that indicates whether a model success score could be retrieved for the specified change request.Valid values:

-   true: Model success score was retrieved.
-   false: Model success score was not retrieved.

 Data type: Boolean

</td></tr><tr><td>

model\_success\_score.chg\_model

</td><td>

Individual objects for each field in the Change Model \[chg\_model\] record referenced by the specified change request. Each object has a key that is the field name and contains value and display\_value properties. If the field type is date/time, then the method also returns a display\_value\_internal property which is in the user's timezone but in the system format YYYY-MM-DD HH24:MM:SS.```
"chg_model": {
  "active": {Object},
  "advanced_security": {Object},
  "available_in_ui": {Object},
  "color": {Object},
  "default_change_model": {Object},
  "description": {Object},
  "implementation_states": {Object},
  "name": {Object},
  "read_roles": {Object},
  "record_preset": {Object},
  "state_field": {Object},
  "sys_class_name": {Object},
  "sys_created_by": {Object},
  "sys_created_on": {Object},
  "sys_domain": {Object},
  "sys_domain_path": {Object},
  "sys_id": {Object},
  "sys_mod_count": {Object},
  "sys_name": {Object},
  "sys_tags": {Object},
  "sys_updated_by": {Object},
  "sys_updated_name": {Object},
  "sys_updated_on": {Object},
  "table_name": {Object},
  "write_roles": {Object}
}
```

 Data type: Object

</td></tr><tr><td>

model\_success\_score.chg\_model.active

</td><td>

Flag that indicates whether the associated change model record is active and available within the instance.Valid values:

-   true: Change model is active.
-   false: Change model is not active.

 Data type: Object

 ```
"active": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.active.display\_value

</td><td>

Display value for the active flag.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.active.value

</td><td>

Internal value for the active flag.Data type: Boolean

</td></tr><tr><td>

model\_success\_score.chg\_model.advanced\_security

</td><td>

Flag that indicates whether user criteria based security is being used in addition to role based security for this change model.Valid values:

-   true: Advanced security is used.
-   false: Advanced security in not used.

 Data type: Object

 ```
"advanced_security": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.advanced\_security.display\_value

</td><td>

Display value for the advanced\_security flag.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.advanced\_security.value

</td><td>

Internal value for the advanced\_security flag.Data type: Boolean

</td></tr><tr><td>

model\_success\_score.chg\_model.available\_in\_ui

</td><td>

Flag that indicates whether the associated change model record is available within the user interface.Valid values:

-   true: Change model is available in the user interface.
-   false: Change model is not available in the user interface.

 Data type: Object

 ```
"available_in_ui": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.available\_in\_ui.display\_value

</td><td>

Display value for the available\_in\_ui flag.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.available\_in\_ui.value

</td><td>

Value for the available\_in\_ui flag.Data type: Boolean

</td></tr><tr><td>

model\_success\_score.chg\_model.color

</td><td>

Color of the associated change model on the change request landing page.Data type: Object

 ```
"color": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.color.display\_value

</td><td>

Display value for color.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.color.value

</td><td>

Internal value for color.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.default\_change\_model

</td><td>

Flag that indicates whether the associated change model record is the default change model.Possible values:

-   true: Default
-   false: Not the default

 Data type: Object

 ```
"default_change_model": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.default\_change\_model.display\_value

</td><td>

Display value for the default change model flag.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.default\_change\_model.value

</td><td>

Internal value for the default change model flag.Data type: Boolean

</td></tr><tr><td>

model\_success\_score.chg\_model.description

</td><td>

Short description of the purpose of the change model.Data type: Object

 ```
"description": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.description.display\_value

</td><td>

Display value for description.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.description.value

</td><td>

Internal value for description.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.name

</td><td>

Name of the change model.Data type: Object

 ```
"name": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.name.display\_value

</td><td>

Display value for name.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.name.value

</td><td>

Internal value for name.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.record\_preset

</td><td>

Name-value pairs of the fields that should automatically be populated, with their associated values, when a new change request record is created. Values are separated by caret symbols.For example:

 `"type=normal^assignment_group=a715cd759f2002002920bde8132e7018^short_description=Automated : Change^EQ"`

 Data type: Object

 ```
"record_preset": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.record\_preset.display\_value

</td><td>

Display value for record\_preset.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.record\_preset.value

</td><td>

Internal value for record\_preset.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.state\_field

</td><td>

Choice list field from which to collect choices, based on the value provided in **table\_name**. For change models, this is always set to "state".Data type: Object

 ```
"state_field": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.state\_field.display\_value

</td><td>

Display value for state\_field.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.state\_field.value

</td><td>

Internal value for state\_field.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_class\_name

</td><td>

Change module table name. Always Change Model/chg\_model.Data type: Object

 ```
"sys_class_name": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_class\_name.display\_value

</td><td>

Display value for sys\_class\_name.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_class\_name.value

</td><td>

Internal value for sys\_class\_name.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_created\_by

</td><td>

Name of the user that initially created the associated change module record. Data type: Object

 ```
"sys_created_by": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_created\_by.display\_value

</td><td>

Display value for sys\_created\_by.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_created\_by.value

</td><td>

Internal value for sys\_created\_by.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_created\_on

</td><td>

Date and time that the change module record was originally created.Data type: Object

 ```
"sys_created_on": {
  "display_value": "String",
  "display_value_internal": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_created\_on.display\_value

</td><td>

Display value for sys\_created\_on.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_created\_on.display\_value\_internal

</td><td>

Internal display value for sys\_created\_on.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_created\_on.value

</td><td>

Internal value for sys\_created\_on.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_domain

</td><td>

If using domains in the instance, the name of the domain to which the change module record is associated.Data type: Object

 ```
"sys_domain": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_domain.display\_value

</td><td>

Display value for sys\_domain.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_domain.value

</td><td>

Internal value for sys\_domain.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_domain\_path

</td><td>

If using domains in the instance, the domain path in which the associated change module record resides.Data type: Object

 ```
"sys_domain_path": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_domain\_path.display\_value

</td><td>

Display value for sys\_domain\_path.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_domain\_path.value

</td><td>

Internal value for sys\_domain\_path.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_id

</td><td>

Unique identifier of the associated change model record.Data type: Object

 ```
"sys_id": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_id.display\_value

</td><td>

Display value for sys\_id.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_id.value

</td><td>

Internal value for sys\_id.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_mod\_count

</td><td>

Number of times that the associated change model record has been modified.Data type: Object

 ```
"sys_mod_count": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_mod\_count.display\_value

</td><td>

Display value for sys\_mod\_count.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_mod\_count.value

</td><td>

Internal value for sys\_mod\_count.Data type: Number

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_name

</td><td>

Name of the change model. Always the same as the **name** parameter.Data type: Object

 ```
"sys_name": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_name.display\_value

</td><td>

Display value for sys\_name.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_name.value

</td><td>

Internal value for sys\_name.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_updated\_by

</td><td>

Name of the user that last updated the associated change model record.Data type: Object

 ```
"sys_updated_by": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_updated\_by.display\_value

</td><td>

Display value for sys\_updated\_by.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_updated\_by.value

</td><td>

Internal value for sys\_updated\_by.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_updated\_on

</td><td>

Date and time the associated change model record was last updated.Data type: Object

 ```
"sys_updated_on": {
  "display_value": "String",
  "display_value_internal": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_updated\_on.display\_value

</td><td>

Display value for sys\_updated\_on.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_updated\_on.display\_value\_internal

</td><td>

Internal display value for sys\_updated\_on.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.sys\_updated\_on.value

</td><td>

Internal value for sys\_updated\_on.Data type: String

</td></tr><tr><td>

model\_success\_score.chg\_model.table\_name

</td><td>

Table that defines the Choice list field from which to collect choices. For change models this is always set to "change\_request".Data type: String

 Maximum length: 80

</td></tr><tr><td>

model\_success\_score.score

</td><td>

Details about the returned score indicator.Data type: Object

 ```
"score": {
  "delta": {Object},
  "display_value": "String",
  "has_score": Boolean,
  "indicator": {Object},
  "value": Number
}
```

</td></tr><tr><td>

model\_success\_score.score.delta

</td><td>

Change in the score from the previous score.Data type: Object

 ```
"delta": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

model\_success\_score.score.delta.display\_value

</td><td>

Display value for delta.Data type: String

</td></tr><tr><td>

model\_success\_score.score.delta.value

</td><td>

Internal value for delta.Data type: String

</td></tr><tr><td>

model\_success\_score.score.display\_value

</td><td>

Display value returned by Performance Analytics \(PA\).Data type: String

</td></tr><tr><td>

model\_success\_score.score.score.has\_score

</td><td>

Flag that indicates whether a score was returned for the specified change request.

 Valid values:

-   true: Score was returned.
-   false: No score was returned.

 Data type: Boolean

</td></tr><tr><td>

model\_success\_score.score.indicator

</td><td>

Additional details on the PA indicator used to obtain the score.Data type: Object

 ```
"indicator": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

model\_success\_score.score.indicator.name

</td><td>

Name of the PA indicator used to obtain the score.Data type: String

</td></tr><tr><td>

model\_success\_score.score.indicator.sys\_id

</td><td>

Sys\_id of the PA indicator used to obtain the score.Data type: String

</td></tr><tr><td>

model\_success\_score.score.value

</td><td>

Value returned by PA for the success score.Data type: String

</td></tr></tbody>
</table>The following example shows how to request that the model score information not be returned in a getScoresForChange\(\) call.

```
var chgGr = new GlideRecord("change_request");
chgGr.get("number", "CHG0030305");

gs.info(JSON.stringify(new sn_chg_score.ChangeSuccess().withModelScore(false).getScoresForChange(chgGr), null, 2));

```

The following output only shows the model success score values that are returned if this helper is set to true. To see the other scores that may be returned, see [getScoresForChange\(\)](ChangeSuccessScopedAPI.md#).

```
"model_success_score": {
    "can_read": true,
    "chg_model": {
      "color": {
        "display_value": "",
        "value": ""
      },
      "default_change_model": {
        "display_value": "false",
        "value": false
      },
      "description": {
        "display_value": "This model can be used to capture unauthorized change events that were detected.",
        "value": "This model can be used to capture unauthorized change events that were detected."
      },
      "sys_updated_on": {
        "display_value": "2020-10-21 11:10:57",
        "value": "2020-10-21 10:10:57",
        "display_value_internal": "2020-10-21 11:10:57"
      },
      "table_name": {
        "display_value": "change_request",
        "value": "change_request"
      },
      "sys_class_name": {
        "display_value": "Change Model",
        "value": "chg_model"
      },
      "sys_id": {
        "display_value": "aedc6a625323101034d1ddeeff7b1296",
        "value": "aedc6a625323101034d1ddeeff7b1296"
      },
      "sys_updated_by": {
        "display_value": "admin",
        "value": "admin"
      },
      "write_roles": {
        "display_value": "",
        "value": ""
      },
      "sys_created_on": {
        "display_value": "2020-10-02 14:50:20",
        "value": "2020-10-02 13:50:20",
        "display_value_internal": "2020-10-02 14:50:20"
      },
      "read_roles": {
        "display_value": "itil,sn_change_read",
        "value": "itil,sn_change_read"
      },
      "sys_name": {
        "display_value": "Unauthorized Change",
        "value": "Unauthorized Change"
      },
      "advanced_security": {
        "display_value": "false",
        "value": false
      },
      "sys_created_by": {
        "display_value": "admin",
        "value": "admin"
      },
      "record_preset": {
        "display_value": "type=emergency^short_description=An unauthorized change has been detected^assignment_group=a715cd759f2002002920bde8132e7018^work_start=javascript:gs.nowDateTime()^unauthorized=true^EQ",
        "value": "type=emergency^short_description=An unauthorized change has been detected^assignment_group=a715cd759f2002002920bde8132e7018^work_start=javascript:gs.nowDateTime()^unauthorized=true^EQ"
      },
      "sys_mod_count": {
        "display_value": "9",
        "value": 9
      },
      "active": {
        "display_value": "true",
        "value": true
      },
      "sys_tags": {
        "display_value": "",
        "value": ""
      },
      "available_in_ui": {
        "display_value": "false",
        "value": false
      },
      "state_field": {
        "display_value": "state",
        "value": "state"
      },
      "name": {
        "display_value": "Unauthorized Change",
        "value": "Unauthorized Change"
      },
      "implementation_states": {
        "display_value": "",
        "value": ""
      }
    },
    "score": {
      "indicator": {
        "name": "Change Model: % Successful and Successful With Issues",
        "sys_id": "604f98dfc302011005aea539e540dd75"
      },
      "value": 76.92307692307693,
      "display_value": "76.92",
      "delta": {
        "value": 0,
        "display_value": "0.00"
      },
      "has_score": true
    }
  }
```

## ChangeSuccess - withSecurity\(Boolean toggle\)

Controls whether the method validates the user calling the associated method, ensuring that they have the rights to read the requested content.

For example:

-   For the team success score: Checks that the user has read rights to the associated group.
-   For model score: Checks that the user has read rights to the change model record.
-   For type score: Checks that the user has read rights to the choice record for that change type.

By default, all ChangeSuccess methods perform this validation. Use this method to toggle this validation on and off for the current ChangeSuccess object.

<table id="table_kbt_lz2_ltb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

toggle

</td><td>

Boolean

</td><td>

Flag that indicates whether to validate the user calling the associated method.Valid values:

-   true: Validate the user calling the associated method.
-   false: Do not validate the user calling the associated method.

 Default: true

</td></tr></tbody>
</table>|Parameter|Description|
|---------|-----------|
|None| |

The following example shows how to turn the user security check off when calling the getScoresForChange\(\) method.

```
var chgGr = new GlideRecord("change_request");
chgGr.get("number", "CHG0030305");
new sn_chg_score.ChangeSuccess().withSecurity(false).getScoresForChange(chgGr);
```

Output:

```
None
```

## ChangeSuccess - withTeamScore\(Boolean toggle\)

Only valid when called with the getScoresForChange\(\) method. Controls whether the getScoresForChange\(\) method returns the team score. By default the team score is returned.

Use this method to toggle the return of this data on or off for the current ChangeSuccess object.

<table id="table_vcc_252_ltb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

toggle

</td><td>

Boolean

</td><td>

Flag that indicates whether to include the team success score.Valid values:

-   true: Return the team success score.
-   false: Do not return the team success score.

 Default: true

</td></tr></tbody>
</table><table id="table_wcc_252_ltb" class="returns"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

team\_success\_score

</td><td>

Details on the team success score.Data type: Object

 ```
"team_success_score" {
  "can_read": Boolean,
  "chg_success_score_rating": {Object},
  "score": {Object},
  "sys_user_group":{Object}
}
```

</td></tr><tr id="can_read-team_suc-row"><td>

team\_success\_score.can\_read

</td><td>

Flag that indicates whether a change team success score could be retrieved for the specified change request.Valid values:

-   true: Team success score was retrieved.
-   false: Team success score was not retrieved.

 Data type: Boolean

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating

</td><td>

Individual objects for each field from the Change Success Score Rating \[chg\_success\_score\_rating\] record that matches the returned score. Each field object has a key that is the field name and contains **value** and **display\_value** properties. If the field type is date/time, then the method also returns a **display\_value\_internal** property which is in the user's timezone but in the system format YYYY-MM-DD HH24:MM:SS.Data type: Object

 ```
"chg_success_score_rating": {
  "active": {Object},
  "color": {Object},
  "rating": {Object},
  "score_end": {Object},
  "score_start": {Object},
  "sys_class_name": {Object},
  "sys_created_by": {Object},
  "sys_created_on": {Object},
  "sys_domain": {Object},
  "sys_id": {Object},
  "sys_mod_count": {Object},
  "sys_name": {Object},
  "sys_overrides": {Object},
  "sys_tags": {Object},
  "sys_updated_by": {Object},
  "sys_updated_on": {Object}
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.active

</td><td>

Flag that indicates whether the associated change success score record is active and available within the instance.Valid values:

-   true: Change success score record is active.
-   false: Change success score record is not active.

 Data type: Object

 ```
"active": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.active.display\_value

</td><td>

Display value for the active flag.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.active.value

</td><td>

Internal value for the active flag.Data type: Boolean

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.color

</td><td>

Color of the associated change success score as shown in the Change Success Score Card for a change request.Data type: Object

 ```
"color": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.color.display\_value

</td><td>

Display value for color.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.color.value

</td><td>

Internal value for color.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.rating

</td><td>

Change success score rating, such as Low or High.Data type: Object

 ```
"rating": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.rating.display\_value

</td><td>

Display value for rating.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.rating.value

</td><td>

Internal value for rating.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.score\_end

</td><td>

Highest value in the change success score.Data type: Object

 ```
"score_end": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.score\_end.display\_value

</td><td>

Display value for score\_end.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.score\_end.value

</td><td>

Internal value for score\_end.Data type: Number

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.score\_start

</td><td>

Lowest value in the change success score.Data type: Object

 ```
"score_start": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.score\_start.display\_value

</td><td>

Display value for score\_start.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.score\_start.value

</td><td>

Internal value for score\_start.Data type: Number

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_class\_name

</td><td>

Change Success Score Rating table name. Always Change Success Score Rating/chg\_success\_score\_rating.Data type: Object

 ```
"sys_class_name": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_class\_name.display\_value

</td><td>

Display value for sys\_class\_name.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_class\_name.value

</td><td>

Internal value for sys\_class\_name.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_created\_by

</td><td>

Name of the user that initially created the associated change success score rating record. Data type: Object

 ```
"sys_created_by": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_created\_by.display\_value

</td><td>

Display value for sys\_created\_by.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_created\_by.value

</td><td>

Internal value for sys\_created\_by.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_created\_on

</td><td>

Date and time that the change success score rating record was originally created.Data type: Object

 ```
"sys_created_on": {
  "display_value": "String",
  "display_value_internal": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_created\_on.display\_value

</td><td>

Display value for sys\_created\_on.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_created\_on.display\_value\_internal

</td><td>

Internal display value for sys\_created\_on.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_created\_on.value

</td><td>

Internal value for sys\_created\_on.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_domain

</td><td>

If using domains in the instance, the name of the domain to which the change success score record is associated.Data type: Object

 ```
"sys_domain": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_domain.display\_value

</td><td>

Display value for sys\_domain.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_domain.value

</td><td>

Internal value for sys\_domain.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_id

</td><td>

Unique identifier of the associated change success score record.Data type: Object

 ```
"sys_id": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_id.display\_value

</td><td>

Display value for sys\_id.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_id.value

</td><td>

Internal value for sys\_id.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_mod\_count

</td><td>

Number of times that the associated change success score record has been modified.Data type: Object

 ```
"sys_mod_count": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_mod\_count.display\_value

</td><td>

Display value for sys\_mod\_count.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_mod\_count.value

</td><td>

Internal value for sys\_mod\_count.Data type: Number

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_name

</td><td>

Name of the change success score rating.Possible values:

 -   Excellent
-   High
-   Low
-   Medium

 Data type: Object

 ```
"sys_name": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_name.display\_value

</td><td>

Display value for sys\_name.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_name.value

</td><td>

Internal value for sys\_name.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_overrides

</td><td>

Sys\_id of a record in the same table but in a domain above that of the current record. This allows a record in a lower domain to override a record in a domain above it.For example, if you have a rating record defined in the "global" domain but for domain "TOP/ACME" you override the record in "global".

 Data type: Object

 ```
"sys_overrides": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_overrides.display\_value

</td><td>

Display value for sys\_overrides.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_overrides.value

</td><td>

Internal value for sys\_overrides.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_tags

</td><td>

List of system tags associated with the change success score record.Data type: Object

 ```
"sys_tags": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_tags.display\_value

</td><td>

Display value for sys\_tags.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_tags.value

</td><td>

Internal value for sys\_tags.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_updated\_by

</td><td>

Name of the user that last updated the associated change success score record.Data type: Object

 ```
"sys_updated_by": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_updated\_by.display\_value

</td><td>

Display value for sys\_updated\_by.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_updated\_by.value

</td><td>

Internal value for sys\_updated\_by.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_updated\_on

</td><td>

Date and time the associated change success score record was last updated.Data type: Object

 ```
"sys_created_on": {
  "display_value": "String",
  "display_value_internal": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_updated\_on.display\_value

</td><td>

Display value for sys\_updated\_on.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_updated\_on.display\_value\_internal

</td><td>

Internal display value for sys\_updated\_on.Data type: String

</td></tr><tr><td>

team\_success\_score.chg\_success\_score\_rating.sys\_updated\_on.value

</td><td>

Internal value for sys\_updated\_on.Data type: String

</td></tr><tr id="chg_suc-score-row"><td>

team\_success\_score.score

</td><td>

Details about the returned score indicator.Data type: Object

 ```
"score": {
  "delta": {Object},
  "display_value": "String",
  "has_score": Boolean,
  "indicator": {Object},
  "value": Number
}
```

</td></tr><tr id="chg_suc-score_delta-row"><td>

team\_success\_score.score.delta

</td><td>

Change in the score from the previous score.Data type: Object

 ```
"delta": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.score.delta.display\_value

</td><td>

Display value for delta.Data type: String

</td></tr><tr><td>

team\_success\_score.score.delta.value

</td><td>

Internal value for delta.Data type: String

</td></tr><tr id="chg_suc-score_display_value-row"><td>

team\_success\_score.score.display\_value

</td><td>

Display value returned by Performance Analytics \(PA\).Data type: String

</td></tr><tr id="chg_suc-score_has_score-row"><td>

team\_success\_score.score.has\_score

</td><td>

Flag that indicates whether a score was returned for the specified change request.

 Valid values:

-   true: Score was returned.
-   false: No score was returned.

 Data type: Boolean

</td></tr><tr id="chg_suc-score_indicator-row"><td>

team\_success\_score.score.indicator

</td><td>

Additional details on the PA indicator used to obtain the score.Data type: Object

 ```
"indicator": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="chg_suc-score_indicator_name-row"><td>

team\_success\_score.score.indicator.name

</td><td>

Name of the PA indicator used to obtain the score.Data type: String

</td></tr><tr id="chg_suc-score_indicator_sys_id-row"><td>

team\_success\_score.score.indicator.sys\_id

</td><td>

Sys\_id of the PA indicator used to obtain the score.Data type: String

</td></tr><tr id="chg_suc-score_value-row"><td>

team\_success\_score.score.value

</td><td>

Value returned by PA for the success score.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group

</td><td>

Individual objects for each field from the Group \[sys\_user\_group\] record referenced by the specified change request. Each field object has a key that is the field name and contains **value** and **display\_value** properties. If the field type is date/time, then the method also returns a **display\_value\_internal** property which is in the user's timezone but in the system format YYYY-MM-DD HH24:MM:SS.Data type: Object

```
"sys_user_group": {
  "active": {Object},
  "cost_center": {Object},
  "default_assignee": {Object},
  "description": {Object},
  "email": {Object},
  "exclude_manager": {Object},
  "include_members": {Object},
  "manager": {Object},
  "name": {Object},
  "parent": {Object},
  "roles": {Object},
  "source": {Object},
  "sys_created_by": {Object},
  "sys_created_on": {Object},
  "sys_id": {Object},
  "sys_mod_count": {Object},
  "sys_tags": {Object},
  "sys_updated_by": {Object},
  "sys_updated_on": {Object},
  "type": {Object}
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.active

</td><td>

Flag that indicates whether the group is active.Possible values:

 -   true: Group is active
-   false: Group is de-activated

 Data type: Object

 ```
"active": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.active.display\_value

</td><td>

Display value for the active flag.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.active.value

</td><td>

Internal value for the active flag.Data type: Boolean

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.cost\_center

</td><td>

Sys\_id of the cost center associated with the group.Data type: Object

 ```
"cost_center": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.cost\_center.display\_value

</td><td>

Display value for cost\_center.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.cost\_center.value

</td><td>

Internal value for cost\_center.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.default\_assignee

</td><td>

Sys\_id of the user that is the default assignee of the group.Data type: Object

 ```
"default_assignee": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.default\_assignee.display\_value

</td><td>

Display value for default\_assignee.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.default\_assignee.value

</td><td>

Internal value for default\_assignee.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.description

</td><td>

Description of the groupData type: Object

 ```
"description": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.description.display\_value

</td><td>

Display value for description.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.description.value

</td><td>

Internal value for description.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.email

</td><td>

Email address for the group.Data type: Object

 ```
"description": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.email.display\_value

</td><td>

Display value for email.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.email.value

</td><td>

Internal value for email.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.exclude\_manager

</td><td>

Flag that indicates whether the manager of the group receives group emails.Valid values:

 -   true: Manager does not receive group emails.
-   false: Manager receives group emails.

 Data type: Object

 ```
"exclude_manager": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.exclude\_manager.display\_value

</td><td>

Display value for exclude\_manager.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.exclude\_manager.value

</td><td>

Internal value for exclude\_manager.Data type: Boolean

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.include\_members

</td><td>

Flag that indicates whether the group members receive individual emails when someone sends an email to the group email address. The only exception to this functionality is for approval notifications, whereby all members of a group receive an approval notification, regardless of this selection.Valid values:

 -   true: Send emails to the entire group.
-   false: Only send emails to the default\_assignee.

 Data type: Object

 ```
"include_members": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.include\_members.display\_value

</td><td>

Display value for include\_members.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.include\_members.value

</td><td>

Internal value for include\_members.Data type: Boolean

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.manager

</td><td>

Sys\_id of the manager of the group.Data type: Object

 ```
"manager": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.manager.display\_value

</td><td>

Display value for manager.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.manager.value

</td><td>

Internal value for manager.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.name

</td><td>

Name of the group.Data type: Object

 ```
"name": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.name.display\_value

</td><td>

Display value for name.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.name.value

</td><td>

Internal value for name.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.parent

</td><td>

Sys\_id of the parent of this group. If a group has a parent, the child group inherits the roles of the parent group. The members of the child group are not members of the parent group. For example, if an incident is assigned to the parent group and you click the Assigned to lookup icon, only the members in the parent group are available. The members of the child group are not available.Data type: Object

 ```
"parent": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.parent.display\_value

</td><td>

Display value for parent.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.parent.value

</td><td>

Internal value for parent.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.roles

</td><td>

User roles assigned to the group.Data type: Object

 ```
"roles": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.roles.display\_value

</td><td>

Display value for roles.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.roles.value

</td><td>

Internal value for roles.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.source

</td><td>

Source of the group.Data type: Object

 ```
"source": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.source.display\_value

</td><td>

Display value for source.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.source.value

</td><td>

Internal value for source.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_created\_by

</td><td>

User that created the group record.Data type: Object

 ```
"sys_created_by": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_created\_by.display\_value

</td><td>

Display value for sys\_created\_by.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_created\_by.value

</td><td>

Internal value for sys\_created\_by.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_created\_on

</td><td>

Date and time that the group record was originally created.Data type: Object

 ```
"sys_created_on": {
  "display_value": "String",
  "display_value_internal": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_created\_on.display\_value

</td><td>

Display value for sys\_created\_on.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_created\_on.display\_value\_internal

</td><td>

Internal display value for sys\_created\_on.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_created\_on.value

</td><td>

Internal value for sys\_created\_on.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_id

</td><td>

Sys\_id for the group.Data type: Object

 ```
"sys_id": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_id.display\_value

</td><td>

Display value for sys\_id.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_id.value

</td><td>

Internal value for sys\_id.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_mod\_count

</td><td>

Number of times that the associated group information has been modified.Data type: Object

 ```
"sys_mod_count": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_mod\_count.display\_value

</td><td>

Display value for sys\_mod\_count.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_mod\_count.value

</td><td>

Internal value for sys\_mod\_count.Data type: Number

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_updated\_by

</td><td>

User that last updated the group information.Data type: Object

 ```
"sys_updated_by": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_updated\_by.display\_value

</td><td>

Display value for sys\_updated\_by.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_updated\_by.value

</td><td>

Internal value for sys\_updated\_by.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_updated\_on

</td><td>

Date and time when the group information was last updated.Data type: Object

 ```
"sys_updated_on": {
  "display_value": "String",
  "display_value_internal": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_updated\_on.display\_value

</td><td>

Display value for sys\_updated\_on.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_updated\_on.display\_value\_internal

</td><td>

Internal display value for sys\_updated\_on.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.sys\_updated\_on.value

</td><td>

Internal value for sys\_updated\_on.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.type

</td><td>

Type of group. Data type: Object

 ```
"type": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.type.display\_value

</td><td>

Display value for type.Data type: String

</td></tr><tr><td>

team\_success\_score.sys\_user\_group.type.value

</td><td>

Internal value for type.Data type: String

</td></tr></tbody>
</table>The following code example shows how to use this method to set the team score return response to false.

```
var chgGr = new GlideRecord("change_request");
chgGr.get("number", "CHG0030305");

gs.info(JSON.stringify(new sn_chg_score.ChangeSuccess().withTeamScore(false).getScoresForChange(chgGr), null, 2));
```

The following output only shows the team score values that are returned if this helper is set to true. To see the other scores that may be returned, see [getScoresForChange\(\)](ChangeSuccessScopedAPI.md#).

```
{
  "team_success_score": {
    "can_read": true,
    "sys_user_group": {
      "parent": {
        "display_value": "",
        "value": ""
      },
      "manager": {
        "display_value": "",
        "value": ""
      },
      "roles": {
        "display_value": "",
        "value": ""
      },
      "sys_mod_count": {
        "display_value": "0",
        "value": 0
      },
      "description": {
        "display_value": "",
        "value": ""
      },
      "active": {
        "display_value": "true",
        "value": true
      },
      "source": {
        "display_value": "",
        "value": ""
      },
      "sys_updated_on": {
        "display_value": "2018-03-07 21:00:41",
        "value": "2018-03-07 21:00:41",
        "display_value_internal": "2018-03-07 21:00:41"
      },
      "type": {
        "display_value": "",
        "value": ""
      },
      "sys_tags": {
        "display_value": "",
        "value": ""
      },
      "sys_id": {
        "display_value": "5f6441efc0a8010e0177fcb589156352",
        "value": "5f6441efc0a8010e0177fcb589156352"
      },
      "sys_updated_by": {
        "display_value": "glide.maint",
        "value": "glide.maint"
      },
      "cost_center": {
        "display_value": "",
        "value": ""
      },
      "default_assignee": {
        "display_value": "",
        "value": ""
      },
      "sys_created_on": {
        "display_value": "2018-03-07 21:00:41",
        "value": "2018-03-07 21:00:41",
        "display_value_internal": "2018-03-07 21:00:41"
      },
      "name": {
        "display_value": "IT Securities",
        "value": "IT Securities"
      },
      "exclude_manager": {
        "display_value": "false",
        "value": false
      },
      "email": {
        "display_value": "",
        "value": ""
      },
      "include_members": {
        "display_value": "false",
        "value": false
      },
      "sys_created_by": {
        "display_value": "glide.maint",
        "value": "glide.maint"
      }
    },
    "score": {
      "indicator": {
        "name": "Change success scores",
        "sys_id": "0ff316e173081010491d235f04f6a758"
      },
      "value": 465,
      "display_value": "465",
      "delta": {
        "value": 0,
        "display_value": "0"
      },
      "has_score": true
    },
    "chg_success_score_rating": {
      "score_start": {
        "display_value": "0",
        "value": 0
      },
      "score_end": {
        "display_value": "499",
        "value": 499
      },
      "color": {
        "display_value": "#FCCAC9",
        "value": "#FCCAC9"
      },
      "rating": {
        "display_value": "Low",
        "value": "Low"
      },
      "sys_mod_count": {
        "display_value": "0",
        "value": 0
      },
      "active": {
        "display_value": "true",
        "value": true
      },
      "sys_overrides": {
        "display_value": "",
        "value": ""
      },
      "sys_updated_on": {
        "display_value": "2020-03-27 07:43:29",
        "value": "2020-03-27 07:43:29",
        "display_value_internal": "2020-03-27 07:43:29"
      },
      "sys_tags": {
        "display_value": "",
        "value": ""
      },
      "sys_class_name": {
        "display_value": "Change Success Score Rating",
        "value": "chg_success_score_rating"
      },
      "sys_id": {
        "display_value": "7ad380b573330010491d235f04f6a717",
        "value": "7ad380b573330010491d235f04f6a717"
      },
      "sys_updated_by": {
        "display_value": "admin",
        "value": "admin"
      },
      "sys_created_on": {
        "display_value": "2020-03-27 07:43:29",
        "value": "2020-03-27 07:43:29",
        "display_value_internal": "2020-03-27 07:43:29"
      },
      "sys_domain": {
        "display_value": "global",
        "value": "global"
      },
      "sys_name": {
        "display_value": "Low",
        "value": "Low"
      },
      "sys_created_by": {
        "display_value": "admin",
        "value": "admin"
      }
    }
  }
```

## ChangeSuccess - withTeamScoreRatings\(Boolean toggle\)

Controls whether the associated method returns the details for all change success score rating records. By default, this information is not returned.

Use this method to toggle the return of this data on or off for the current ChangeSuccess object. This method is a helper method and must be used in conjunction with one of the other methods that return a success score such as:

-   [ChangeSuccess - getScoresForChange\(Object chgGr\)](ChangeSuccessScopedAPI.md#)
-   [ChangeSuccess - getTeamScoreForChange\(Object chgGr\)](ChangeSuccessScopedAPI.md#)
-   [ChangeSuccess - getModelScoreForModelId\(String sys\_id, String domain\_id\)](ChangeSuccessScopedAPI.md#)

<table id="table_eqg_lhk_ltb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

toggle

</td><td>

Boolean

</td><td>

Flag that indicates whether to include the details for all team success score rating records.Valid values:

-   true: Return the details for all change success score rating records.
-   false: Do not return the details for all change success score rating records.

 Default: false

</td></tr></tbody>
</table><table id="table_fqg_lhk_ltb" class="returns"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ratings

</td><td>

 

</td></tr><tr><td>

ratings.active

</td><td>

Flag that indicates whether the associated change success score record is active and available within the instance.Valid values:

-   true: Change success score record is active.
-   false: Change success score record is not active.

 Data type: Object

 ```
"active": {
  "display_value": "String",
  "value": Boolean
}
```

</td></tr><tr><td>

ratings.active.display\_value

</td><td>

Display value for the active flag.Data type: String

</td></tr><tr><td>

ratings.active.value

</td><td>

Internal value for the active flag.Data type: Boolean

</td></tr><tr><td>

ratings.color

</td><td>

Color of the associated change success score as shown in the Change Success Score Card for a change request.Data type: Object

 ```
"color": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

ratings.color.display\_value

</td><td>

Display value for color.Data type: String

</td></tr><tr><td>

ratings.color.value

</td><td>

Internal value for color.Data type: String

</td></tr><tr><td>

ratings.rating

</td><td>

Change success score rating, such as Low or High.Data type: Object

 ```
"rating": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

ratings.rating.display\_value

</td><td>

Display value for rating.Data type: String

</td></tr><tr><td>

ratings.rating.value

</td><td>

Internal value for rating.Data type: String

</td></tr><tr><td>

ratings.score\_end

</td><td>

Highest value in the change success score.Data type: Object

 ```
"score_end": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr><td>

ratings.score\_end.display\_value

</td><td>

Display value for score\_end.Data type: String

</td></tr><tr><td>

ratings.score\_end.value

</td><td>

Internal value for score\_end.Data type: Number

</td></tr><tr><td>

ratings.score\_start

</td><td>

Lowest value in the change success score.Data type: Object

 ```
"score_start": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr><td>

ratings.score\_start.display\_value

</td><td>

Display value for score\_start.Data type: String

</td></tr><tr><td>

ratings.score\_start.value

</td><td>

Internal value for score\_start.Data type: Number

</td></tr><tr><td>

ratings.sys\_class\_name

</td><td>

Change Success Score Rating table name. Always Change Success Score Rating/chg\_success\_score\_rating.Data type: Object

 ```
"sys_class_name": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

ratings.sys\_class\_name.display\_value

</td><td>

Display value for sys\_class\_name.Data type: String

</td></tr><tr><td>

ratings.sys\_class\_name.value

</td><td>

Internal value for sys\_class\_name.Data type: String

</td></tr><tr><td>

ratings.sys\_created\_by

</td><td>

Name of the user that initially created the associated change success score rating record. Data type: Object

 ```
"sys_created_by": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

ratings.sys\_created\_by.display\_value

</td><td>

Display value for sys\_created\_by.Data type: String

</td></tr><tr><td>

ratings.sys\_created\_by.value

</td><td>

Internal value for sys\_created\_by.Data type: String

</td></tr><tr><td>

ratings.sys\_created\_on

</td><td>

Date and time that the change success score rating record was originally created.Data type: Object

 ```
"sys_created_on": {
  "display_value": "String",
  "display_value_internal": "String",
  "value": "String"
}
```

</td></tr><tr><td>

ratings.sys\_created\_on.display\_value

</td><td>

Display value for sys\_created\_on.Data type: String

</td></tr><tr><td>

ratings.sys\_created\_on.display\_value\_internal

</td><td>

Internal display value for sys\_created\_on.Data type: String

</td></tr><tr><td>

ratings.sys\_created\_on.value

</td><td>

Internal value for sys\_created\_on.Data type: String

</td></tr><tr><td>

ratings.sys\_domain

</td><td>

If using domains in the instance, the name of the domain to which the change success score record is associated.Data type: Object

 ```
"sys_domain": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

ratings.sys\_domain.display\_value

</td><td>

Display value for sys\_domain.Data type: String

</td></tr><tr><td>

ratings.sys\_domain.value

</td><td>

Internal value for sys\_domain.Data type: String

</td></tr><tr><td>

ratings.sys\_id

</td><td>

Unique identifier of the associated change success score record.Data type: Object

 ```
"sys_id": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

ratings.sys\_id.display\_value

</td><td>

Display value for sys\_id.Data type: String

</td></tr><tr><td>

ratings.sys\_id.value

</td><td>

Internal value for sys\_id.Data type: String

</td></tr><tr><td>

ratings.sys\_mod\_count

</td><td>

Number of times that the associated change success score record has been modified.Data type: Object

 ```
"sys_mod_count": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr><td>

ratings.sys\_mod\_count.display\_value

</td><td>

Display value for sys\_mod\_count.Data type: String

</td></tr><tr><td>

ratings.sys\_mod\_count.value

</td><td>

Internal value for sys\_mod\_count.Data type: Number

</td></tr><tr><td>

ratings.sys\_name

</td><td>

Name of the change success score rating.Possible values:

 -   Excellent
-   High
-   Low
-   Medium

 Data type: Object

 ```
"sys_name": {
  "display_value": "String",
  "value": Number
}
```

</td></tr><tr><td>

ratings.sys\_name.display\_value

</td><td>

Display value for sys\_name.Data type: String

</td></tr><tr><td>

ratings.sys\_name.value

</td><td>

Internal value for sys\_name.Data type: String

</td></tr><tr><td>

ratings.sys\_overrides

</td><td>

Sys\_id of a record in the same table but in a domain above that of the current record. This allows a record in a lower domain to override a record in a domain above it.For example, if you have a rating record defined in the "global" domain but for domain "TOP/ACME" you override the record in "global".

 Data type: Object

 ```
"sys_overrides": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

ratings.sys\_overrides.display\_value

</td><td>

Display value for sys\_overrides.Data type: String

</td></tr><tr><td>

ratings.sys\_overrides.value

</td><td>

Internal value for sys\_overrides.Data type: String

</td></tr><tr><td>

ratings.sys\_tags

</td><td>

List of system tags associated with the change success score record.Data type: Object

 ```
"sys_tags": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

ratings.sys\_tags.display\_value

</td><td>

Display value for sys\_tags.Data type: String

</td></tr><tr><td>

ratings.sys\_tags.value

</td><td>

Internal value for sys\_tags.Data type: String

</td></tr><tr><td>

ratings.sys\_updated\_by

</td><td>

Name of the user that last updated the associated change success score record.Data type: Object

 ```
"sys_updated_by": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

ratings.sys\_updated\_by.display\_value

</td><td>

Display value for sys\_updated\_by.Data type: String

</td></tr><tr><td>

ratings.sys\_updated\_by.value

</td><td>

Internal value for sys\_updated\_by.Data type: String

</td></tr><tr><td>

ratings.sys\_updated\_on

</td><td>

Date and time the associated change success score record was last updated.Data type: Object

 ```
"sys_created_on": {
  "display_value": "String",
  "display_value_internal": "String",
  "value": "String"
}
```

</td></tr><tr><td>

ratings.sys\_updated\_on.display\_value

</td><td>

Display value for sys\_updated\_on.Data type: String

</td></tr><tr><td>

ratings.sys\_updated\_on.display\_value\_internal

</td><td>

Internal display value for sys\_updated\_on.Data type: String

</td></tr><tr><td>

ratings.sys\_updated\_on.value

</td><td>

Internal value for sys\_updated\_on.Data type: String

</td></tr></tbody>
</table>The following code example shows how to use this method to set the team score rating return response to false.

```
var chgGr = new GlideRecord("change_request");
chgGr.get("number", "CHG0030305");

gs.info(JSON.stringify(new sn_chg_score.ChangeSuccess().withTeamScoreRatings(false).getTeamScoreForChange(chgGr), null, 2));
```

The following output only shows the team score values that are returned if this helper is set to true. To see the other scores that may be returned, refer to the method to which you are associating this helper.

```
"ratings": [
  {
    "score_start": {
      "display_value": "700",
      "value": 700
    },
    "score_end": {
      "display_value": "850",
      "value": 850
    },
    "color": {
      "display_value": "#A4EDA8",
      "value": "#A4EDA8"
    },
    "rating": {
      "display_value": "Excellent",
      "value": "Excellent"
    },
    "sys_mod_count": {
      "display_value": "1",
      "value": 1
    },
    "active": {
      "display_value": "true",
      "value": true
    },
    "sys_overrides": {
      "display_value": "",
      "value": ""
    },
    "sys_updated_on": {
      "display_value": "2020-03-27 07:45:36",
      "value": "2020-03-27 07:45:36",
      "display_value_internal": "2020-03-27 07:45:36"
    },
    "sys_tags": {
      "display_value": "",
      "value": ""
    },
    "sys_class_name": {
      "display_value": "Change Success Score Rating",
      "value": "chg_success_score_rating"
    },
    "sys_id": {
      "display_value": "76e440fd73330010491d235f04f6a7df",
      "value": "76e440fd73330010491d235f04f6a7df"
    },
    "sys_updated_by": {
      "display_value": "admin",
      "value": "admin"
    },
    "sys_created_on": {
      "display_value": "2020-03-27 07:44:46",
      "value": "2020-03-27 07:44:46",
      "display_value_internal": "2020-03-27 07:44:46"
    },
    "sys_domain": {
      "display_value": "global",
      "value": "global"
    },
    "sys_name": {
      "display_value": "Excellent",
      "value": "Excellent"
    },
    "sys_created_by": {
      "display_value": "admin",
      "value": "admin"
    }
  }
]
```

## ChangeSuccess - withTypeScore\(Boolean toggle\)

Only valid when called with the getScoresForChange\(\) method. Controls whether the getScoresForChange\(\) method returns the type score. By default the type score is returned.

Use this method to toggle the return of this data on or off for the current ChangeSuccess object.

<table id="table_fp5_3y2_ltb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

toggle

</td><td>

Boolean

</td><td>

Flag that indicates whether to include the type success score.Valid values:

-   true: Return the type success score.
-   false: Do not return the type success score.

 Default: true

</td></tr></tbody>
</table><table id="table_gp5_3y2_ltb" class="returns"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

type\_success\_score

</td><td>

Details about the type success score.Data type: Object

 ```
"type_success_score": {
  "can_read": Boolean,
  "score": {Object},
  "type": {Object}
}
```

</td></tr><tr><td>

type\_success\_score.can\_read

</td><td>

Flag that indicates whether a type success score could be retrieved for the specified change request.Valid values:

-   true: Type success score was retrieved.
-   false: Type success score was not retrieved.

 Data type: Boolean

</td></tr><tr><td>

type\_success\_score.score

</td><td>

Details about the returned score indicator.Data type: Object

 ```
"score": {
  "delta": {Object},
  "display_value": "String",
  "has_score": Boolean,
  "indicator": {Object},
  "value": Number
}
```

</td></tr><tr><td>

type\_success\_score.score.delta

</td><td>

Change in the score from the previous score.Data type: Object

 ```
"delta": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

type\_success\_score.score.delta.display\_value

</td><td>

Display value for delta.Data type: String

</td></tr><tr><td>

type\_success\_score.score.delta.value

</td><td>

Internal value for delta.Data type: String

</td></tr><tr><td>

type\_success\_score.score.display\_value

</td><td>

Display value returned by Performance Analytics \(PA\).Data type: String

</td></tr><tr><td>

type\_success\_score.score.has\_score

</td><td>

Flag that indicates whether a score was returned for the specified change request.

 Valid values:

-   true: Score was returned.
-   false: No score was returned.

 Data type: Boolean

</td></tr><tr><td>

type\_success\_score.score.indicator

</td><td>

Additional details on the PA indicator used to obtain the score.Data type: Object

 ```
"indicator": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

type\_success\_score.score.indicator.name

</td><td>

Name of the PA indicator used to obtain the score.Data type: String

</td></tr><tr><td>

type\_success\_score.score.indicator.sys\_id

</td><td>

Sys\_id of the PA indicator used to obtain the score.Data type: String

</td></tr><tr><td>

type\_success\_score.score.value

</td><td>

Value returned by PA for the success score.Data type: String

</td></tr><tr><td>

type\_success\_score.type

</td><td>

Details about the type success score.Data type: Object

 ```
"type": {
  "display_value": "String",
  "sys_id": "String",
  "value": "String"
}
```

</td></tr><tr><td>

type\_success\_score.type.display\_value

</td><td>

Label of the choice.Data type: String

</td></tr><tr><td>

type\_success\_score.type.sys\_id

</td><td>

Sys\_id of the Choice \[sys\_choice\] record for the specified change type.Data type: String

</td></tr><tr><td>

type\_success\_score.type.value

</td><td>

Value of the choice.Data type: String

</td></tr></tbody>
</table>The following code example shows how to use this method to set the desired type score return response.

```
var chgGr = new GlideRecord("change_request");
chgGr.get("number", "CHG0030305");

gs.info(JSON.stringify(new sn_chg_score.ChangeSuccess().withTypeScore(true).getScoresForChange(chgGr), null, 2));

```

The following output only shows the type success score values that are returned if this helper is set to true. To see the other scores that may be returned, see [getScoresForChange\(\)](ChangeSuccessScopedAPI.md#).

```
"type_success_score": {
  "can_read": true,
  "type": {
    "sys_id": "e7a27d53cb100200d71cb9c0c24c9c2f",
    "value": "normal",
    "display_value": "Normal"
  },
  "score": {
    "indicator": {
      "name": "Change Type: % Successful and Successful With Issues",
      "sys_id": "f9d25995c3ce011005aea539e540ddee"
    },
    "value": null,
    "display_value": "",
    "delta": {
      "value": "0",
      "display_value": ""
    },
    "has_score": false
  }
}
```

