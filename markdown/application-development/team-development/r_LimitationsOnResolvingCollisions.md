---
title: Limitations on updating records
description: There are some types of records that you cannot merge while resolving differences on the Compare to Current and Resolve Collision pages.
locale: en-US
release: xanadu
product: Team Development
classification: team-development
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Team Development overview, Team Development, Planning your application, Building applications]
---

# Limitations on updating records

There are some types of records that you cannot merge while resolving differences on the Compare to Current and Resolve Collision pages.

## Record types that allow a choice only between reverting or accepting the pulled or current record

The following record types do not allow you to merge individual values. Instead, differences involving the following record types display a read-only comparison and allow a choice between updating and reverting:

-   sys\_choice \[Choice\]
-   sys\_choice\_set \[Choice Set\]
-   sys\_ui\_form \[Form\]
-   sys\_ui\_list \[List\]
-   sys\_ui\_related\_list \[Related List\]
-   sys\_ui\_section \[Form Section\]
-   wf\_workflow \[Workflow\]
-   wf\_workflow\_version \[Workflow Version\]

Team Development, Resolve Collision page: **Use Pulled Version** and **Use Local Version** options.

Upgrade History, Compare to Current page: Comparing non-current update versions to current update version. Allows only **Revert to Base System** option.

## Field types that do not support merging

The following field types do not support individual merging between versions or updates:

-   auto\_increment \[Auto Increment\]
-   auto\_number \[Auto Number\]
-   breakdown\_element \[Breakdown Element\]
-   catalog\_preview \[Catalog Preview\]
-   collection \[Collection\]
-   color\_display \[Color Display\]
-   composite\_field \[Composite Field\]
-   compressed \[Compressed\]
-   counter \[Counter\]
-   currency \[Counter\]
-   data\_array \[Data Array\]
-   data\_object \[Data Object\]
-   data\_structure \[Data Structure\]
-   date \[Other Date\]
-   datetime \[Basic Date/Time\]
-   days\_of\_week \[Days of Week\]
-   document\_id \[Document ID\]
-   due\_date \[Due Date\]
-   Email \[Email\]
-   external\_names \[External Names\]
-   field\_list \[Field List\]
-   float \[Floating Point Number\]
-   glide\_action\_list \[UI Action List\]
-   glide\_precise\_time \[Precise Time\]
-   glide\_var \[Glide Var\]
-   image \[Basic Image\]
-   index\_name \[Index Name\]
-   int \[Integer String\]
-   integer\_time \[Integer Time\]
-   ip\_address \[IP Address\]
-   journal \[Journal\]
-   journal\_input \[Journal Input\]
-   journal\_list \[Journal List\]
-   long \[Long Integer String\]
-   mask\_code \[Mask Code\]
-   metric\_absolute \[Metric Absolute\]
-   metric\_counter \[Metric Counter\]
-   metric\_derive \[Metric Derive\]
-   metric\_gauge \[Metric Gauge\]
-   mid\_config \[MID Server Configuration\]
-   month\_of\_year \[Month of Year\]
-   multi\_small \[Multiple Line Small Text Area\]
-   name\_values \[Name/Values\]
-   nl\_task\_int1 \[NL Task Integer 1\]
-   order\_index \[Order Index\]
-   password \[Password \(1 Way Encrypted\)\]
-   percent\_complete \[Percent Complete\]
-   ph\_number \[Phone Number\]
-   phone\_number \[Phone Number \(Unused\)\]
-   phone\_number\_e164 \[Phone Number \(E164\)\]
-   price \[Price\]
-   reference\_name \[Reference Name\]
-   related\_tags \[Related Tags\]
-   reminder\_field\_name \[Reminder Field Name\]
-   repeat\_count \[Repeat Count\]
-   repeat\_type \[Repeat Type\]
-   replication\_payload \[Replication Payload\]
-   schedule\_date\_time \[Schedule Date/Time\]
-   short\_field\_name \[Short Field Name\]
-   short\_table\_name \[Short Table Name\]
-   Slushbucket \[slushbucket\]
-   source\_id \[Source ID\]
-   source\_name \[Source Name\]
-   source\_table \[Source Table\]
-   string\_boolean \[&lt;none&gt;\]
-   sys\_class\_name \[System Class Name\]
-   sysrule\_field\_name \[System Rule Field Name\]
-   table \[\]
-   text \[\]
-   time \[\]
-   timer \[Timer\]
-   translated \[Translated\]
-   tree\_code \[Tree Code\]
-   tree\_path \[Tree Path\]
-   user\_image \[Image\]
-   user\_input \[User Input\]
-   variables \[Variables\]
-   version \[Version\]
-   video \[Video\]
-   week\_of\_month \[Week of Month\]
-   wide\_text \[Wide Text\]
-   wms\_job \[WMS Job\]
-   workflow \[Workflow\]

**Parent Topic:**[Team Development overview](../concept/c_UsingTeamDevelopment.md)

**Related topics**  


[Resolve a collision in Team Development](../task/t_ResolveACollision.md)

