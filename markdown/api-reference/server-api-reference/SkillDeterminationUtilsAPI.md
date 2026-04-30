---
title: SkillDeterminationUtils - Scoped
description: The SkillDeterminationUtils script include provides utility methods to get or set work item skill data.Constructor to create an instance of SkillDeterminationUtils.Assigns an array of active skill objects to a work item.Gets skills for a specified work item, indicates if the skills are mandatory, and lists any skill levels.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SkillDeterminationUtils- Scoped

The SkillDeterminationUtils script include provides utility methods to get or set work item skill data.

This script include requires the Skill Determination \(com.snc.skill\_determination\) plugin and is provided within the `sn_skill_rule` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## SkillDeterminationUtils - SkillDeterminationUtils\(\)

Constructor to create an instance of SkillDeterminationUtils.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
var util = new sn_skill_rule.SkillDeterminationUtils();
```

## SkillDeterminationUtils - assignSkillsToWorkItem\(Array skills, GlideRecord now\_GR\)

Assigns an array of active skill objects to a work item.

|Name|Type|Description|
|----|----|-----------|
|skills|Array|Array of active skill objects to be assigned.|
|skill.skillName|String|Name of the skill.|
|skill.skillSysId|String|Sys ID of the skill.|
|skill.mandatory|Boolean|True if the skill is mandatory, false otherwise.|
|skill.skillLevelName|String|Optional skill level name.|
|skill.skillLevelSysId|String|Optional skill level Sys ID.|
|now\_GR|GlideRecord|GlideRecord of the work item on which to assign skills.|

|Type|Description|
|----|-----------|
|None| |

The examples below create an Interaction record using the table name \(interaction\) and show how to assign skills to the interaction work item, creating a record in the Interaction Skills \[interaction\_m2m\_skill\] table.

Use case 1: Use returned results from determineWorkItemSkills\(\) to assign skills to a work item from the Interaction table.

```
// Create an interaction record
var now_GR = new GlideRecord('interaction');
now_GR.insert();

var util = new sn_skill_rule.SkillDeterminationUtils();

// Get interaction skills interaction 
// and specify if any are mandatory
var result = util.determineWorkItemSkills(now_GR);

// Assign skills determined by result and 
// assign them to the interaction work item
util.assignSkillsToWorkItem(result, now_GR);
```

Use case 2: Manually insert skills array. In this case, assign IT skills to the Interaction work item.

```
var now_GR = new GlideRecord('interaction');
now_GR.insert();

var util = new sn_skill_rule.SkillDeterminationUtils();

var skills = [{"skillSysId":"2eb1c2029f100200a3bc1471367fcfe4", "skillName":"IT", "mandatory":true, "skillLevelName":"", "skillLevelSysId":null}];

util.assignSkillsToWorkItem(skills, now_GR);
```

## SkillDeterminationUtils - determineWorkItemSkills\(GlideRecord now\_GR\)

Gets skills for a specified work item, indicates if the skills are mandatory, and lists any skill levels.

|Name|Type|Description|
|----|----|-----------|
|now\_GR|GlideRecord|GlideRecord of a work item from any interaction or task table extension.|

<table id="table_ict_yl5_fhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array

</td><td>

One or more skill objects.-   skillSysId: String. Sys ID of the skill from the Skills \[cmn\_skill\] table.
-   skillName: String. Name of the skill.
-   mandatory: Boolean. True if mandatory, false otherwise.
-   skillLevelName: If skill exists, name of the skill level.
-   skillLevelSysId: If skill exists, Sys ID of the skill level from the Skill Levels \[cmn\_skill\_level\] table.

</td></tr></tbody>
</table>The following script creates an interaction record, gets skills for the interaction work item, and indicates if the skills are mandatory.

```
// Create an interaction record
var now_GR = new GlideRecord('interaction');
now_GR.insert();

var util = new sn_skill_rule.SkillDeterminationUtils();

var result = util.determineWorkItemSkills(now_GR);
gs.info(JSON.stringify(result));
```

Output:

```
[{"skillSysId":"6c0f025c7f672300a8b1bdc8adfa917f",
"skillName":"Premier Support Certified",
"mandatory":false,"skillLevelName":"",
"skillLevelSysId":null}]
```

