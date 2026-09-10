---
title: Revoked MITRE tactic-technique review fields
description: Fields on the review record that MITRE ingestion creates for a revoked tactic and technique pair, and the values that each field can hold.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/security-management/threat-intelligence-security-center/tisc-mitre-revoked-review-fields.html
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
keywords: [MITRE Tactic Technique Review, Revoked Collection Version, Action Taken]
breadcrumb: [Review revoked pairs, MITRE-ATT&amp;CK repository, TISC Library Repository, Threat Intel Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Revoked MITRE tactic-technique review fields

Fields on the review record that MITRE ingestion creates for a revoked tactic and technique pair, and the values that each field can hold.

## Field descriptions

The fields on the MITRE Tactic Technique Review \[sn\_sec\_tisc\_mitre\_tactic\_technique\_review\] table are described in the following table.

<table id="table_review_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Display name of the review record, in the format &lt;tactic ID&gt; - &lt;technique ID&gt;.**Note:**

Review records that were created before this field was introduced have an empty name, because the name is set only when the record is created.

</td></tr><tr><td>

Tactic

</td><td>

MITRE ATT&amp;CK tactic that is no longer linked to the technique.

</td></tr><tr><td>

Technique

</td><td>

MITRE ATT&amp;CK technique that is no longer linked to the tactic.

</td></tr><tr><td>

Review Reason

</td><td>

Reason that the pair was raised for review. See the following table for the two values.

</td></tr><tr><td>

Revoked Collection Version

</td><td>

MITRE ATT&amp;CK collection version in which the pair was revoked.

</td></tr><tr><td>

Status

</td><td>

Progress of the review. See the status values described later in this topic.

</td></tr><tr><td>

Action Taken

</td><td>

Action that was run on the pair. **Delete** removes the associations, and **Update mapping** moves them to another pair.

</td></tr><tr><td>

New Tactic

</td><td>

Tactic that the associations were remapped to. This field is populated only when Action Taken is Update mapping.

</td></tr><tr><td>

New Technique

</td><td>

Technique that the associations were remapped to. This field is populated only when Action Taken is Update mapping.

</td></tr><tr><td>

Work Notes

</td><td>

Journal of the review activity, including the action that was requested and the pair that the associations were moved to.

</td></tr></tbody>
</table>## Review reason values

|Value|Meaning|
|-----|-------|
|Technique has been revoked in the MITRE Collection|MITRE revoked the technique itself, so every tactic that the technique belonged to loses the link.|
|Technique no longer mapped to the Tactic in the MITRE Collection|The technique is still current, but MITRE no longer maps it to this tactic.|

## Status values

|Value|Meaning|
|-----|-------|
|Review|The pair is waiting for you to delete or remap its associations. This value is set when ingestion creates the record.|
|In Progress|An action was requested and is running in the background.|
|Complete|The requested action finished.|
|Error|The background work didn't finish. You can run the action again from the record.|

**Parent Topic:**[Review revoked MITRE tactic and technique associations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/tisc-review-revoked-mitre-associations.md)

**Related topics**  


[Review revoked MITRE tactic and technique associations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/tisc-review-revoked-mitre-associations.md)

