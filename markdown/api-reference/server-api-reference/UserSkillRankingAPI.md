---
title: UserSkillRanking - Global
description: The UserSkillRanking API provides methods to configure options for choosing the right user and getting a sorted list of qualified users based on number of matching skills and skill-level gap.Instantiates a UserSkillRanking object.Provides a list of qualified users based on matching mandatory skills and levels if the isSkillLevelEnforced parameter is true\).
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# UserSkillRanking- Global

The UserSkillRanking API provides methods to configure options for choosing the right user and getting a sorted list of qualified users based on number of matching skills and skill-level gap.

This API requires the Skills Management plugin \(com.snc.skills\_management\), which you can activate if you have the admin role.

See [Qualify and rank users based on skills and skill levels](https://www.servicenow.com/docs/access?context=assign-work-based-on-skills&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## UserSkillRanking - UserSkillRanking\(\)

Instantiates a UserSkillRanking object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

## UserSkillRanking - getQualifiedRankedUsers\(String requiredSkillsJson, String usersJson, String rankType, Boolean isSkillLevelEnforced\)

Provides a list of qualified users based on matching mandatory skills and levels if the `isSkillLevelEnforced` parameter is true\).

<table id="table_lcv_g1s_lhb" class="parameters"><thead><tr><th>

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

List of required skills to qualify users.Each skill is listed as a JSON entry in the following format:

-   sys\_id: String. Sys ID of skill from the Skills \[cmn\_skill\] table.
-   is\_mandatory: Boolean. Flag that indicates whether the skill is mandatory.
-   level: String. Sys ID from the Skill Levels \[cmn\_skill\_level\] table.

</td></tr><tr><td>

usersJson

</td><td>

String

</td><td>

List of user Sys IDs from sys\_user table \(in JSON format\) representing users to be qualified against required skills.

</td></tr><tr><td>

rankType

</td><td>

String

</td><td>

Enables sorting qualified users based on ranking type. Possible values are comparators to provide sorted list of qualified users based on number of matching skills and skill level gap:

 -   NO\_RANKING \(default\) – Used if empty value provided.
-   NUM\_SKILLS – Number of skills matched against required skills.
-   NUM\_SKILL\_ MATCHING\_LEVEL – Number of user skills matching the required skill level.
-   LEAST\_SKILL\_ LEVEL\_GAP – Finds user skill that most closely meets minimum skill level requirements.
-   MOST\_SKILL\_ LEVEL\_GAP – Finds user that least meets minimum skill level requirements.
-   BEST\_OPTIMUM\_ USER – Finds optimum user for all skill levels.

</td></tr><tr><td>

isSkillLevelEnforced

</td><td>

Boolean

</td><td>

True if user must have minimum skill level for all required mandatory skills, false otherwise. Default: false.

</td></tr></tbody>
</table><table id="table_mcv_g1s_lhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

List of qualified users as JSON.Error if inaccurate parameters or malformed JSON provided.

</td></tr></tbody>
</table>```
var skills = [{"sys_id":"48c9f873c0a8018b65c3814608b201e6", "is_mandatory": true, "level":"4e0ac4d6b3332300290ea943c6a8dc4e"},
				{"sys_id":"48c9fdddc0a8018b04bd8d7914c82c9d", "is_mandatory": false, "level":"4e0ac4d6b3332300290ea943c6a8dc4eS"}];
var users = ["a8f98bb0eb32010045e1a5115206fe3a", "62826bf03710200044e0bfc8bcbe5df1"];
var userSkillRanking = new SNC.UserSkillRanking();
var qualifiedUsers = userSkillRanking.getQualifiedRankedUsers(JSON.stringify(skills), JSON.stringify(users), "BEST_OPTIMUM_USER", true);
```

