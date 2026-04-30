---
title: Components installed with Process Mining
description: Several types of components are installed with activation of the com.sn\_po plugin, including tables, user roles, and scheduled jobs.Process Mining adds these roles.Access all projects and manage all project settings and configurations and schedule background and jobs.Perform the following actions when assigned to this role.Perform the following actions when assigned to this role.System properties control system behavior. The properties in this section are specific to the Process Mining application.
locale: en-US
release: zurich
product: Process Mining
classification: process-mining
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Process Mining reference, Process Mining, Platform Analytics]
---

# Components installed with Process Mining

Several types of components are installed with activation of the com.sn\_po plugin, including tables, user roles, and scheduled jobs.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Scheduled jobs installed

|Scheduled job|Description|
|-------------|-----------|
|ProminVersionCleanup|Deletes older backup versions.|

## Tables installed

<table><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Process Mining Definition \[ml\_capability\_definition\_promin\]

</td><td>

A discriminator to identify process mining solutions.

</td></tr><tr><td>

Process Mining Interactive Definition \[ml\_capability\_definition\_interactive\]

</td><td>

A discriminator to identify process mining on the fly solutions.

</td></tr><tr><td>

Process Mining Record Definition \[ml\_capability\_definition\_record\]

</td><td>

A discriminator to identify process mining view records solutions.

</td></tr><tr><td>

Activity Definition\[promin\_activity\_def\]

</td><td>

Stores the activities depicting the audit log changes to a field on the process graph.

</td></tr><tr><td>

Process Connection\[promin\_arc\]

</td><td>

Stores connections statistics for a project.

</td></tr><tr><td>

Breakdown Definition\[promin\_breakdown\_field\]

</td><td>

Stores the breakdowns by which the process map gets categorized.

</td></tr><tr><td>

Breakdown Stats\[promin\_breakdown\_stats\]

</td><td>

Stores breakdown statistics for a project.

</td></tr><tr><td>

Filter set\[promin\_filter\_set\]

</td><td>

Stores multiple sets of filters applied on a project definition.

</td></tr><tr><td>

Extract Data Log\[promin\_log\]

</td><td>

Stores the extracted audit log data entries generated when mining a project version.

</td></tr><tr><td>

Scheduled Process Mining Jobs \[promin\_job\]

</td><td>

Stores Process Mining scheduled jobs.

</td></tr><tr><td>

Process Model\[promin\_model\]

</td><td>

Stores multiple model statistics for a project version.

</td></tr><tr><td>

Version \[promin\_model\_def\_version\]

</td><td>

The version of a mined project.

</td></tr><tr><td>

Process Node\[promin\_node\]

</td><td>

Stores activities for a project definition.

</td></tr><tr><td>

Process Node Statistics\[promin\_node\_stats\]

</td><td>

Stores statistics for an activity.

</td></tr><tr><td>

Note \[promin\_note\]

</td><td>

Stores the note records.

</td></tr><tr><td>

Permission \[promin\_permission\]

</td><td>

Stores the users/groups for whom the project definition is shared.

</td></tr><tr><td>

Process Route \[promin\_route\]

</td><td>

Stores route statistics for a specific project.

</td></tr><tr><td>

Case Record \[promin\_case\_record\]

</td><td>

Stores record details from an activity, connection, or route.

</td></tr><tr><td>

Process Mining Tracker \[promin\_ua\_mining\_tracker\]

</td><td>

Stores information regarding the previous mines.

</td></tr><tr><td>

Filter Set Condition\[promin\_conditions\]

</td><td>

Stores the filter conditions corresponding to a project.

</td></tr><tr><td>

Process Scheduled Task\[promin\_scheduled\_task\]

</td><td>

Stores requested cluster analysis, data mining, and Process Mining tasks.

</td></tr><tr><td>

Process Configuration\[promin\_process\_def\]

</td><td>

Stores process configuration defaults.

</td></tr><tr><td>

Finding Definition\[promin\_finding\_def\]

</td><td>

Stores finding definition records.

</td></tr><tr><td>

Finding\[promin\_finding\]

</td><td>

Stores findings discovered for projects​.

</td></tr><tr><td>

Finding Rule\[promin\_finding\_def\_rule\]

</td><td>

Stores finding rule records.

</td></tr><tr><td>

Finding Condition\[promin\_finding\_def\_condition\]

</td><td>

Stores finding conditions.

</td></tr><tr><td>

Finding Constraint \[promin\_finding\_def\_constraint\]

</td><td>

Stores finding constraints that act on 2 conditions.

</td></tr><tr><td>

Automated Finding Definition \[promin\_automated\_finding\]

</td><td>

Stores definition for the Automated findings.

</td></tr><tr><td>

Automated Finding Configuration \[promin\_automated\_finding\_configuration\]

</td><td>

Stores configurations for Automated findings.

</td></tr><tr><td>

Process Route Statistics \[promin\_route\_stats\]

</td><td>

Stores statistics for the Routes.

</td></tr><tr><td>

Promin case data \[promin\_case\_data\]

</td><td>

Stores the log collected during full mine.

</td></tr><tr><td>

Job Process Mining Project\[promin\_job\_m2m\_project\]

</td><td>

Stores information about the project attached to a job.

</td></tr></tbody>
</table>**Parent Topic:**[Process Mining reference](../concept/process-mining-reference.md)

## Process Mining roles

Process Mining adds these roles.

Roles control access to features and capabilities in applications and modules.

After access has been granted to a role, all the groups or users assigned to the role are granted the access. Roles can contain other roles, and any access granted to a role is granted to any role that contains it.

### Process mining administrator \[sn\_process\_optimization\_admin\]

Access all projects and manage all project settings and configurations and schedule background and jobs.

#### Contains Roles

The Process mining administrator \[sn\_process\_optimization\_admin\] role contains the sn\_process\_optimization\_power\_user role.

#### Groups

List of groups this role is assigned to by default.

None.

#### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

### Process Mining power user \[sn\_process\_optimization\_power\_user\]

Perform the following actions when assigned to this role.

-   Can access all projects and manage all project settings and configurations.
-   Can create and share projects.
-   Can view projects created by other users and shared with them.
-   Can schedule Process Mining jobs.

#### Contains Roles

The Process optimization power user \[sn\_process\_optimization\_power\_user\] role contains the sn\_process\_optimization\_analyst role.

#### Groups

List of groups this role is assigned to by default.

None.

#### Special considerations

None.

### Process Mining Analyst \[sn\_process\_optimization\_analyst\]

Perform the following actions when assigned to this role.

-   Create and share projects.
-   View projects created by other users and shared with them.

#### Contains Roles

None.

#### Groups

List of groups this role is assigned to by default.

None.

#### Special considerations

Users with this role cannot access all projects.

## Process Mining properties

System properties control system behavior. The properties in this section are specific to the Process Mining application.

These properties are available for Process Mining.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_tlv_5cf_xvb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

promin.limit.node\_def

</td><td>

Defines the maximum number of activities for parent nodes in the Process Mining process map.-   Type: Integer
-   Default value: 10

**Note:** Avoid performance issues and a cluttered UI by setting this value no higher than 10.

</td></tr><tr><td>

promin.limit.child\_node\_def

</td><td>

Defines the maximum number of activities for child nodes in the Process Mining process map.-   Type: Integer
-   Default value: 5

**Note:** Avoid performance issues by setting this value no higher than 5.

</td></tr><tr><td>

promin.limit.breakdown\_def

</td><td>

Defines the maximum number of breakdowns for parent nodes in the Process Mining process map.-   Type: Integer
-   Default value: 10

**Note:** Avoid performance issues by setting this value no higher than 10.

</td></tr><tr><td>

promin.limit.child\_breakdown\_def

</td><td>

Defines the maximum number of breakdowns for child nodes in the Process Mining process map.-   Type: Integer
-   Default value: 5

**Note:** Avoid performance issues by setting this value no higher than 5.

</td></tr><tr><td>

promin.primary\_metric

</td><td>

Primary metric used in Analyst workbench.-   Type: Choice List
-   Default value: caseFreq
-   Available values
    -   Avg duration=avgDuration
    -   Max duration=maxDuration
    -   Median duration=medianDuration
    -   Min duration=minDuration
    -   Standard deviation=stdDeviation
    -   Total duration=totalDuration
    -   Total occurrences=absoluteFreq
    -   Unique occurrences=caseFreq

</td></tr><tr><td>

promin.rca.min\_condition\_and\_effect

</td><td>

Minimum percentage of records needed to show in the leading influencers list.-   Type: Integer
-   Default value: 10

</td></tr><tr><td>

promin.rca.min\_odds\_ratio

</td><td>

Minimum required odds ratio.-   Type: String
-   Default value: 1

</td></tr><tr><td>

promin.rca.result\_count

</td><td>

Number of top leading influencers to display.-   Type: Integer
-   Default value: 20

</td></tr><tr><td>

promin.secondary\_metric

</td><td>

Secondary metric used in Analyst workbench.-   Type: Choice List
-   Default value: avgDuration
-   Available values
    -   Avg duration=avgDuration
    -   Max duration=maxDuration
    -   Median duration=medianDuration
    -   Min duration=minDuration
    -   Standard deviation=stdDeviation
    -   Total duration=totalDuration
    -   Total occurrences=absoluteFreq
    -   Unique occurrences=caseFreq

</td></tr><tr><td>

promin.perf.result\_page\_size

</td><td>

Configures the mining result pageThe default value is 700.

</td></tr><tr><td>

promin.pa\_integration\_required\_roles

</td><td>

Define the roles that can launch Process Mining from Platform Analytics Dashboard/Indicator.Type: String

Default: The default roles added to the property are:

-   itil
-   sn\_sd.success\_dashboard\_read
-   sn\_sd.success\_dashboard\_details\_read
-   business\_stakeholder
-   sn\_process\_optimization\_analyst
-   sn\_customerservice\_manager
-   sn\_customerservice\_agent
-   pa\_threshold\_admin
-   sn\_hr\_pa.admin
-   sn\_hr\_core.report\_creator
-   sn\_hr\_core.manager
-   sn\_hr\_core.admin
-   sn\_hr\_onboarding.admin

</td></tr></tbody>
</table>