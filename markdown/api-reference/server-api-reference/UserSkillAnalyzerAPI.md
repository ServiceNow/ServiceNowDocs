---
title: UserSkillAnalyzer - Global
description: The UserSkillAnalyzer API provides methods to analyze user skills against skills required to complete work items.Instantiates a new UserSkillAnalyzer object.Analyzes user skills against the required skills and sets the number of matching skills, skill level gap, and qualification that can be collected from an instance.Analyzes user skills against the required skills and sets the number of matching skills, skill-level gap, and qualification that can be collected from an instance.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# UserSkillAnalyzer- Global

The UserSkillAnalyzer API provides methods to analyze user skills against skills required to complete work items.

This API requires the Skills Management plugin \(com.snc.skills\_management\), which you can activate if you have the admin role.

See [Qualify and rank users based on skills and skill levels](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/skills-management/assign-work-based-on-skills.md).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## UserSkillAnalyzer - UserSkillAnalyzer\(\)

Instantiates a new UserSkillAnalyzer object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```

var userSkillAnalyzer = new SNC.UserSkillAnalyzer();
```

## UserSkillAnalyzer - analyzeUserByID\(String requiredSkillsJson, String userID, Boolean isSkillLevelEnforced\)

Analyzes user skills against the required skills and sets the number of matching skills, skill level gap, and qualification that can be collected from an instance.

Analyzes whether an agent is qualified to work on a task by verifying if the agent has the skills and skill levels required to complete the task. If an agent is qualified to work on a task, the API analyzes the level gap between required skills and user's skill level which can be further used by the application to choose the best agent based on level gap. It also analyzes the total number of skills with and without skill levels the agent has to execute that task.

<table id="table_qps_bzr_lhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

requiredSkillsJson

</td><td>

String

</td><td>

List of required skills to compare with user.Each skill is listed as a JSON entry in the following format:

-   sys\_id: String. Sys ID of skill from the Skills \[cmn\_skill\] table.
-   is\_mandatory: Boolean. Flag that indicates whether the skill is mandatory.
-   level: String. Sys ID from the Skill Levels \[cmn\_skill\_level\] table.

</td></tr><tr><td>

userID

</td><td>

String

</td><td>

Sys ID from the User \[sys\_user\] table.

</td></tr><tr><td>

isSkillLevelEnforced

</td><td>

Boolean

</td><td>

True if user must have a minimum skill level for all required mandatory skills, false otherwise. Default: false.

</td></tr></tbody>
</table><table id="table_kct_qrw_33b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

JSON that contains all the required information about the user based on the analyzer skills map as follows:-   sys\_id: String. Sys ID from the User \[sys\_user\] table.
-   is\_qualified: Boolean. Flag that indicates whether the user is qualified for the required skills.
    -   True if user has all the mandatory skills and skill level is enforced.
    -   False if user does not have all mandatory skills or does not meet level requirements.
-   num\_skills: Number. Skills matched against the required skills.
-   num\_skills\_matching\_level: Number. User skills matching the required skill level.
-   total\_skill\_level\_gap: Number. Skill level gap helps ranking algorithm find optimal user meeting minimum skill level requirements. Calculated based on overall gap between task skill level and user skill level. User must have required skill level for mandatory skills.
-   optional\_skill\_level\_gap: Number. Provides skill level gap for optional skills only. Assists the end points in distinguishing between total skill level and optional skill level gap.

 Error if inaccurate parameters or malformed JSON provided.

</td></tr></tbody>
</table>```
var skills = [{"sys_id":"48c9f873c0a8018b65c3814608b201e6", "is_mandatory": true, "level":"4e0ac4d6b3332300290ea943c6a8dc4e"},
			  {"sys_id":"48c9fdddc0a8018b04bd8d7914c82c9d", "is_mandatory": false, "level":"4e0ac4d6b3332300290ea943c6a8dc4e"}];
var userSysID = "a8f98bb0eb32010045e1a5115206fe3a";
var userSkillAnalyzer = new SNC.UserSkillAnalyzer();
var result = userSkillAnalyzer.analyzeUserById(JSON.stringify(skills), userSysID, true);
gs.info('Results: ' + result);
```

Output:

```
Calling user analyzer
*** Script: Results: {"sys_id":"a8f98bb0eb32010045e1a5115206fe3a","is_qualified":false,"num_skills":0,"num_skills_matching_level":0,"total_skill_level_gap":0,"optional_skill_level_gap":0}
```

## UserSkillAnalyzer - analyzeUserBySkills\(String requiredSkillsJson, String userSkillsJson, Boolean isSkillLevelEnforced\)

Analyzes user skills against the required skills and sets the number of matching skills, skill-level gap, and qualification that can be collected from an instance.

<table id="table_crq_fzr_lhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

requiredSkillsJson

</td><td>

String

</td><td>

List of required skills to qualify the users against.Each skill is listed as a JSON entry in the following format:

-   sys\_id: String. Sys ID of skill from the Skills \[cmn\_skill\] table.
-   is\_mandatory: Boolean. Flag that indicates whether the skill is mandatory.
-   level: String. Sys ID from the Skill Levels \[cmn\_skill\_level\] table.

</td></tr><tr><td>

userSkillsJson

</td><td>

String

</td><td>

List of user skills to determine qualification for required skills.Each skill is listed as a JSON entry in the following format:

-   sys\_id: String. Sys ID of skill from the Skills \[cmn\_skill\] table.
-   is\_mandatory: Boolean. Flag that indicates whether the skill is mandatory.
-   level: String. Sys ID from the Skill Levels \[cmn\_skill\_level\] table.

</td></tr><tr><td>

isSkillLevelEnforced

</td><td>

Boolean

</td><td>

True if user must have minimum skill level for all required mandatory skills, false otherwise. Default: false.

</td></tr></tbody>
</table><table id="table_vdx_prw_33b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

JSON that contains all the required information about the user based on the analyzer skills map as follows:-   sys\_id: String. Sys ID from the User \[sys\_user\] table.
-   is\_qualified: Boolean. Flag that indicates whether the user is qualified for the required skills.
    -   True if user has all the mandatory skills and skill level is enforced.
    -   False if user does not have all mandatory skills or does not meet level requirements.
-   num\_skills: Number. Skills matched against the required skills.
-   num\_skills\_matching\_level: Number. User skills matching the required skill level.
-   total\_skill\_level\_gap: Number. Skill level gap helps ranking algorithm find optimal user meeting minimum skill level requirements. Calculated based on overall gap between task skill level and user skill level. User must have required skill level for mandatory skills.
-   optional\_skill\_level\_gap: Number. Provides skill level gap for optional skills only. Assists the end points in distinguishing between total skill level and optional skill level gap.

 Error if inaccurate parameters or malformed JSON provided.

</td></tr></tbody>
</table>```
var skills = [{"sys_id":"48c9f873c0a8018b65c3814608b201e6", "is_mandatory": true, "level":"4e0ac4d6b3332300290ea943c6a8dc4e"},
				{"sys_id":"48c9fdddc0a8018b04bd8d7914c82c9d", "is_mandatory": false, "level":"4e0ac4d6b3332300290ea943c6a8dc4e"}];
var userSkills = [{"sys_id":"48c9f873c0a8018b65c3814608b201e6", "is_mandatory": true, "level":"4e0ac4d6b3332300290ea943c6a8dc4e"},
		    {"sys_id":"k, th", "is_mandatory": false, "level":"4e0ac4d6b3332300290ea943c6a8dc4e"}];
var userSkillAnalyzer = new SNC.UserSkillAnalyzer();
var result = userSkillAnalyzer.analyzeUserBySkills(JSON.stringify(skills), JSON.stringify(userSkills));
gs.info('Results: ' + result);
```

