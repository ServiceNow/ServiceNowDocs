---
title: Limitations on updating records
description: There are some types of records that you can’t merge while resolving differences on the Compare to Current and Resolve Collision pages.
locale: en-US
release: zurich
product: Team Development
classification: team-development
topic_type: reference
last_updated: "2025-10-02"
reading_time_minutes: 1
breadcrumb: [Team Development Reference, Team Development, Planning your application, Building applications]
---

# Limitations on updating records

There are some types of records that you can’t merge while resolving differences on the Compare to Current and Resolve Collision pages.

## Record types

You can't merge the individual values of the following record types. Instead, differences involving the following record types display a read-only comparison and enable a choice between updating and reverting:

|Record type|Value|
|-----------|-----|
|Choice|sys\_choice|
|Choice Set|sys\_choice\_set|
|Form|sys\_ui\_form|
|List|sys\_ui\_list|
|Related List|sys\_ui\_related\_list|
|Form Section|sys\_ui\_section|
|Workflow|wf\_workflow|
|Workflow Version|wf\_workflow\_version|

## Field types

The following field types don’t support individual merging between versions or updates:

|Field type|Value|
|----------|-----|
|Auto Increment|auto\_increment|
|Auto Number|auto\_number|
|Breakdown Element|breakdown\_element|
|Catalog Preview|catalog\_preview|
|Collection|collection|
|Color Display|color\_display|
|Composite Field|composite\_field|
|Compressed|compressed|
|Counter|counter|
|Currency|currency|
|Data Array|data\_array|
|Data Object|data\_object|
|Data Structure|data\_structure|
|Other Date|date|
|Basic Date/Time|datetime|
|Days of Week|days\_of\_week|
|Document ID|document\_id|
|Due Date|due\_date|
|Email|email|
|External Names|external\_names|
|Field List|field\_list|
|Floating Point Number|float|
|UI Action List|glide\_action\_list|
|Precise Time|glide\_precise\_time|
|Glide Var|glide\_var|
|Basic Image|image|
|Index Name|index\_name|
|Integer String|int|
|Integer Time|integer\_time|
|IP Address|ip\_address|
|Journal|journal|
|Journal Input|journal\_input|
|Journal List|journal\_list|
|Long Integer String|long|
|Mask Code|mask\_code|
|Metric Absolute|metric\_absolute|
|Metric Counter|metric\_counter|
|Metric Derive|metric\_derive|
|Metric Gauge|metric\_gauge|
|MID Server Configuration|mid\_config|
|Month of Year|month\_of\_year|
|Multiple Line Small Text Area|multi\_small|
|Name/Values|name\_values|
|NL Task Integer 1|nl\_task\_int1|
|Order Index|order\_index|
|Password \(One Way Encrypted\)|password|
|Percent Complete|percent\_complete|
|Phone Number|ph\_number|
|Phone Number \(Unused\)|phone\_number|
|Phone Number \(E164\)|phone\_number\_e164|
|Price|price|
|Reference Name|reference\_name|
|Related Tags|related\_tags|
|Reminder Field Name|reminder\_field\_name|
|Repeat Count|repeat\_count|
|Repeat Type|repeat\_type|
|Replication Payload|replication\_payload|
|Schedule Date/Time|schedule\_date\_time|
|Short Field Name|short\_field\_name|
|Short Table Name|short\_table\_name|
|Slushbucket|slushbucket|
|Source ID|source\_id|
|Source Name|source\_name|
|Source Table|source\_table|
|&lt;none&gt;|string\_boolean|
|System Class Name|sys\_class\_name|
|System Rule Field Name|sysrule\_field\_name|
|Table|table|
|Text|text|
|Time|time|
|Timer|timer|
|Translated|translated|
|Tree Code|tree\_code|
|Tree Path|tree\_path|
|Image|user\_image|
|User Input|user\_input|
|Variables|variables|
|Version|version|
|Video|video|
|Week of Month|week\_of\_month|
|Wide Text|wide\_text|
|WMS Job|wms\_job|
|Workflow|workflow|

**Parent Topic:**[Team Development Reference](team-development-reference.md)

