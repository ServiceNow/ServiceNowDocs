---
title: MITRE D3FEND tables
description: MITRE D3FEND integration uses various tables to capture data.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [MITRE D3FEND framework, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# MITRE D3FEND tables

MITRE D3FEND integration uses various tables to capture data.

## Defend Tactics

|Field|Description|
|-----|-----------|
|Tactic ID|ID of the defend tactic.|
|Tactic Name|Name of the defend tactic|
|Definition|Description of the defend tactic.|

## Defend Techniques

|Field|Description|
|-----|-----------|
|Name|Name of the defend technique.|
|Defend Tactic|Tactic to which the defend technique belongs.|
|Technique ID|ID of the technique.|
|Definition|Description of the defend technique.|
|KB Article|Link to a knowledge base article or other additional information about this technique.|
|Parent Defend Technique|Parent technique of the defend technique.|
|Synonyms|Synonym of the defend technique.|

## Defend Artifacts

|Field|Description|
|-----|-----------|
|Artifact ID|ID of the defend artifact.|
|Artifact Name|Name of the defend artifact.|
|Definition|Description or the use of the defend technique.|
|Revoked|Revoked status of the defend artifact.|
|Domain|Domain of the defend artifact.|

## Defend Techniques Artifacts

|Field|Description|
|-----|-----------|
|Defend Artifact|Name of the defend artifact.|
|Defend Technique|Defend technique to which the artifact belongs to.|
|Relationship Label|Action that the defend technique takes on the defend artifact.|
|Revoked|Revoked status of the defend artifact.|
|Domain|Domain of the defend artifact.|

## Related Defend Techniques

|Field|Description|
|-----|-----------|
|Automatically added|Indicates whether the defend technique was automatically added to the table.|
|Defend Technique|Name of the defend technique.|
|Inheritance count|Number of times this technique is inherited.|
|Domain|Domain of the defend technique.|
|Task|Related security incident.|

## Defend ATT&amp;CK Techniques

|Field|Description|
|-----|-----------|
|ATTACK Technique|ATT&amp;CK technique name.|
|Defend Technique|Defend techniques that correspond to the ATT&amp;CK technique.|

