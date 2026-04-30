---
title: MITRE DEFEND tables
description: The section describes all the tables used in the MITRE Defend integration.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2026-01-13"
reading_time_minutes: 1
breadcrumb: [MITRE DEFEND Framework, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# MITRE DEFEND tables

The section describes all the tables used in the MITRE Defend integration.

## Defend Tactics

|Field|Description|
|-----|-----------|
|Tactic ID|The ID of the defend tactic.|
|Tactic Name|The name of the defend tactic|
|Definition|The description or the use of the defend tactic.|

## Defend Techniques

|Field|Description|
|-----|-----------|
|Name|The name of the defend technique.|
|Defend Tactic|The tactic to which the defend technique belong to.|
|Technique ID|The ID of the technique.|
|Definition|The description or the use of the defend technique.|
|KB Article|A link to the KB article or more information about this technique.|
|Parent Defend Technique|The parent technique of this defend technique.|
|Synonyms|The synonym of the defend technique.|

## Defend Artifacts

|Field|Description|
|-----|-----------|
|Artifact ID|The ID of the defend artifact.|
|Artifact Name|The name of the defend artifact.|
|Definition|The description or the use of the defend technique.|
|Revoked|The revoked status of this defend artifact.|
|Domain|The domain of the defend artifact.|

## Defend Techniques Artifacts

|Field|Description|
|-----|-----------|
|Defend Artifact|The name of the defend artifact.|
|Defend Technique|The defend technique to which the artifact belongs to.|
|Relationship Label|The action that the defend technique take on the defend artifact.|
|Revoked|The revoked status of this defend artifact.|
|Domain|The domain of the defend artifact.|

## Related Defend Techniques

|Field|Description|
|-----|-----------|
|Automatically added|The defend technique is automatically added or not.|
|Defend Technique|The name of the defend technique.|
|Inheritance count|How many times this technique is inherited.|
|Domain|The domain of the defend technique.|
|Task|The related security incident.|

## Defend ATTACK Techniques

|Field|Description|
|-----|-----------|
|ATTACK Technique|The attack technique.|
|Defend Technique|The defend techniques correspond to the attack technique.|

