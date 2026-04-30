---
title: Condition and script parameters for menu actions
description: You can use the following condition and script parameters for menu actions.
locale: en-US
release: zurich
product: Dependency Views
classification: dependency-views
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Administer, Dependency Views, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Condition and script parameters for menu actions

You can use the following condition and script parameters for menu actions.

## Condition parameters

**Note:** The usual regular expression conventions are valid in the condition field, such as ! for NOT, &amp;&amp; for AND, and \|\| for OR.

The **Condition** field contains a boolean expression that evaluates to true or false. If the condition is true or if there is no condition, the specified option appears in the menu when you right-click a CI or a relationship link. When you select the option from the menu, ServiceNow executes the associated script.

|Text|Description|
|----|-----------|
|item|Node or reference link's data on which you performed the right-click action.|
|item.label|Label of the node.|
|item.ci\_type|CI's type \(table\), such as `cmdb_ci_service`.|
|item.name|Name of CIs. CI's type name or the table label.|
|item.location|Location of the CI, such as New York.|
|item.manufacturer\_name|Name of the CI’s manufacturer, such as Dell Inc.|
|item.id|The sys\_id of the CI.|
|item.is\_selected|The item that is selected in the map.|
|item.level|The current default level.|
|item.locationId|The sys\_id of the CI node's location.|
|item.locationName|The full address of the location.|
|item.manufaturerId|The sys\_id of the CI's manufacturer.|

|Condition|Description|
|---------|-----------|
|item.is\_collapsed|The node is a collapsed node.|
|item.is\_cluster|The node is a cluster node.|

## Script parameters

Menu action scripts are executed on the client when a user clicks the menu option. You can use the same building blocks in scripts as in conditions. Menu action scripts do not function on separators. These are some additional, useful expressions for scripts:

|Condition|Description|
|---------|-----------|
|item.id|The sys\_id of the CI node or relationship link.|
|item.source|The sys\_id of the relationship's parent or child.|
|item.target|The sys\_id of the relationship's parent or child.|
|item.label|The name of the CI node, such as IronMail-SD-02.|
|item.location|The sys\_id of the CI node's location.|
|item.location\_name|The full address of the location, such as 4616 Clairemont Drive, North Clairemont, San Diego CA.|
|item.manufacturer\_id|The sys\_id of the CI's manufacturer.|

**Parent Topic:**[Administer Dependency Views](../topic/p_AdministerNGBSM.md)

**Related topics**  


[Create or modify map indicators](../task/t_CreateModifyNGBSMMapIndicators.md)

[Create or modify map icons](../task/t_CreateModifyNGBSMMapIcons.md)

[Create a predefined filter](../task/create-predefined-filter.md)

[Set a predefined filter as default](../task/set-predefined-filter-default.md)

[Create or modify Map Related Items](../task/t_CreateModifyNGBSMMapRelatedItems.md)

[Create or modify Dependency Views menu actions](../task/t_CreateModifyNGBSMMenuActions.md)

[Create or edit a dependency type](../task/t_CreateMapScript.md)

