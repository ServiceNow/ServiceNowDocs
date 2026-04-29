---
title: Process Mining properties
description: The Process Mining properties page provides configuration options for Process Mining.Set properties that determine how long Process Mining projects are maintained before being deleted by the scheduled cleanup job.Schedule a job to delete older backup versions and clean up cluster analysis records by executing the scheduled script ProminVersionCleanup.Set properties that determine the thresholds for root cause analysis.Set properties that determine the kind of data you want to view in Analyst workbench.Set the property to enable or disable activity field recommendation when creating a project.Set properties that determine when the work notes analysis will be available.Select the tables that you do not want to be used for projects in Process Mining.Set properties that determine how you can export a project to playbook.Set properties that set the number of highlights generated per page for improvement opportunities.Set properties that determine who can access Process Mining from Platform Analytics Dashboard.Set properties that specify the functioning of intent and activity analysis.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Configure, Process Mining, Platform Analytics]
---

# Process Mining properties

The Process Mining properties page provides configuration options for Process Mining.

**Parent Topic:**[Configuring Process Mining](setting-up-process-mining.md)

## Data cleanup properties

Set properties that determine how long Process Mining projects are maintained before being deleted by the scheduled cleanup job.

<table id="table_u43_ldx_gnb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Define the number of days to persist PA Projects \(Project Definition\) from the last updated date **promin.persist.pa\_model**

</td><td>

Set the number of days that Process Mining projects will be kept after the last date it was updated.-   Type: integer
-   Default value: 30 days
-   Location: Process Mining &gt; **System** &gt; **Properties**

</td></tr><tr><td>

Define the number of days to retire projects due to inactivity **promin.auto\_retire\_days**

</td><td>

Set the number of days of inactivity after which the projects will be retired.-   Type: integer
-   Default value: 90 days
-   Location: Process Mining &gt; **System** &gt; **Properties**

</td></tr><tr><td>

Define the number of days to clean up retired projects **promin.auto\_clean\_days**

</td><td>

Set the number of days post retirement after which the projects will be cleaned up. However, the project configuration will be retained.-   Type: integer
-   Default value: 90 days
-   Location: Process Mining **System** **Properties**

</td></tr></tbody>
</table>**Related topics**  


[Example of an indicator using Process Mining](integrate-pa.md#)

## Schedule job for version cleanup

Schedule a job to delete older backup versions and clean up cluster analysis records by executing the scheduled script **ProminVersionCleanup**.

### Before you begin

Role required: Administrator

### About this task

When regenerating projects, the **ProminVersionCleanup** job deletes obsolete, cached statistics. The older statistics move into a previous version, while the new version is created for the updated project.

When regenerating or deleting projects, this job cleans records created during cluster analyses.

### Procedure

1.  Navigate to **All** &gt; **Process Mining** &gt; **Background Jobs**.

2.  Select the scheduled job **ProminVersionCleanup**.

3.  Check or set the following.

4.  1.  Enable the **Active** check box.
2.  Check if the **Run** field is **Daily**.
3.  Set the time in hours.
5.  Select **Execute Now**.


### Result

Backup version and cluster record cleanup execute daily.

## Root cause analysis properties

Set properties that determine the thresholds for root cause analysis.

<table id="table_u43_ldx_gnb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number of top leading influencers to be displayed **promin.rca.result-count**

</td><td>

Set the number of influencers that are required for a project to have the root cause analysis enabled for a project.-   Type: integer
-   Default value: 20
-   Location: Process Mining &gt; **System** &gt; **Properties**

</td></tr><tr><td>

Minimum % of records \(1 to 100\) needed to show in the leading influencers list **promin.rca.min\_condition\_and\_effect**

</td><td>

Set the minimum percentage of records to be displayed in the leading influencers list. For example, if the value specified is 10% and there are 100 total records, then 10 records will be displayed.-   Type: integer
-   Default value: 10
-   Location: Process Mining &gt; **System** &gt; **Properties**

</td></tr><tr><td>

Minimum required odds ratio **promin.rca.min\_odds\_ratio**

</td><td>

Set the minimum value that decides the odd ratio when doing the root cause analysis.

 -   Type: integer
-   Default value: 1
-   Location: Process Mining **System** **Properties**

</td></tr></tbody>
</table>## Analyst workbench properties

Set properties that determine the kind of data you want to view in Analyst workbench.

<table id="table_u43_ldx_gnb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Primary Metric in Analyst workbench **promin.primary\_metric**

</td><td>

Specify the primary metric that is used in displaying the result in Analyst workbench.-   Type: string
-   Default value: Unique Occurrences
-   Location: Process Mining &gt; **System** &gt; **Properties**

</td></tr><tr><td>

Secondary Metric in Analyst workbench **promin.secondary\_metric**

</td><td>

Specify the secondary metric that is used in displaying the result in Analyst workbench.-   Type: string
-   Default value: Avg Duration
-   Location: Process Mining &gt; **System** &gt; **Properties**

</td></tr></tbody>
</table>## Activity recommendations properties

Set the property to enable or disable activity field recommendation when creating a project.

<table id="table_u43_ldx_gnb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property to enable/disable Activity field recommendations in Process mining **promin.activity.recommendation.enabled**

</td><td>

Select this filed to enable the recommendations to be displayed when setting activity definitions for a project.-   Type: Boolean
-   Default value: True
-   Location: Process Mining &gt; **System** &gt; **Properties**

</td></tr></tbody>
</table>## Work notes analysis properties

Set properties that determine when the work notes analysis will be available.

<table id="table_u43_ldx_gnb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Minimum records required per transition to initiate work notes analysis for users eligible for Now Assist work notes analysis **promin.work\_notes.min\_records\_with\_llm**

</td><td>

Set the minimum records required per transition to initiate work notes analysis for users eligible for Now Assist work notes analysis.-   Type: integer
-   Default value: 5
-   Location: Process Mining &gt; **System** &gt; **Properties**

</td></tr><tr><td>

Set the minimum transition records to trigger work notes analysis **promin.worknotes.min\_records**

</td><td>

Set the minimum transition records to trigger work notes analysis. If the transition records are below the provided value, work notes analysis will not be available.-   Type: integer
-   Default value: 50
-   Location: Process Mining &gt; **System** &gt; **Properties**

</td></tr><tr><td>

Minimum number of eligible work notes to run single LLM call **promin.work\_notes.min\_eligible\_notes\_for\_single\_llm\_call**

</td><td>

Set the minimum number of eligible work notes to run a single LLM call.-   Type: integer
-   Default value: 5
-   Location: Process Mining &gt; **System** &gt; **Properties**

</td></tr><tr><td>

Minimum percentage transition threshold \(X%\) for eligible work notes **promin.work\_notes.min\_percentage\_transition\_threshold**

</td><td>

Set the minimum percentage as a threshold for eligible work notes. For example, if the value specified is 10% and there are 100 total records, then 10 records will be displayed.-   Type: integer
-   Default value: 20
-   Location: Process Mining &gt; **System** &gt; **Properties**

</td></tr><tr><td>

Minimum number of eligible work notes **promin.work\_notes.min\_eligible\_records**

</td><td>

Set the limit for minimum eligible work notes. Work notes are eligible when they meet the criteria that is set when creating process configuration \(such as, time range for work notes, length range of work notes analysis, and so on\). For more information, see [Configure investigative features](../task/investigative-features.md).

 -   Type: integer
-   Default value: 25
-   Location: Process Mining **System** **Properties**

</td></tr></tbody>
</table>## Blocked table

Select the tables that you do not want to be used for projects in Process Mining.

<table id="table_u43_ldx_gnb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Define the tables that must be blocked from mining, activity definition, and breakdown **promin.blocked.tables**

</td><td>

Provide the tables that must be blocked from being used in Process Mining.-   Type: String
-   Default value: None
-   Location: Process Mining &gt; **System** &gt; **Properties**

</td></tr></tbody>
</table>## Playbook generation properties

Set properties that determine how you can export a project to playbook.

<table id="table_tnq_pv5_zfc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Set the maximum number of variants to generate playbook **promin.playbook.max\_variants**

</td><td>

Set the maximum number of variants to generate playbook.-   Type: Integer
-   Default value: 10
-   Location: Process Mining &gt; **System** &gt; **Properties**

</td></tr></tbody>
</table>## Improvement opportunities highlights properties

Set properties that set the number of highlights generated per page for improvement opportunities.

<table id="table_u43_ldx_gnb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**promin.highlights.analysis.findings.pageSize**

</td><td>

Enables you to set the number of highlights generated per page for improvement opportunities.-   Type: Integer
-   Default value: 5
-   Location: Process Mining &gt; **System** &gt; **Properties**

</td></tr></tbody>
</table>## Access control properties

Set properties that determine who can access Process Mining from Platform Analytics Dashboard.

<table id="table_hsk_mw5_zfc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Define the roles that can launch Process Mining from Platform Analytics Dashboard/Indicator **promin.pa\_integration\_required\_roles**

</td><td>

Define the roles that can launch Process Mining from Platform Analytics Dashboard/Indicator.-   Type: String
-   Default: The default roles added to the property are:
    -   itil
    -   sn\_sd.success\_dashboard\_read
    -   sn\_sd.success\_dashboard\_details\_read
    -   business\_stakeholder
    -   sn\_process\_mining\_analyst
    -   sn\_customerservice\_manager
    -   sn\_customerservice\_agent
    -   pa\_threshold\_admin
    -   sn\_hr\_pa.admin
    -   sn\_hr\_core.report\_creator
    -   sn\_hr\_core.manager
    -   sn\_hr\_core.admin
    -   sn\_hr\_onboarding.admin
-   Location: Process Mining &gt; **System** &gt; **Properties**

</td></tr></tbody>
</table>## Intent and agent activity analysis properties

Set properties that specify the functioning of intent and activity analysis.

<table id="table_u43_ldx_gnb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Specify the minimum percentage of records with eligible work notes/comments required to start clustering, excluding those that are too long, too short, or machine-generated **promin.agent\_activity\_analysis.min\_worknote\_percentage\_threshold**

</td><td>

Sets the minimum percentage of records with eligible work notes/comments required to start clustering, excluding those that are too long, too short, or machine-generated.-   Type: integer
-   Default value: 20
-   Location: Process Mining &gt; **System** &gt; **Properties**

</td></tr><tr><td>

Specify the minimum length of worknote to filter out short worknotes **promin.agent\_activity\_analysis.min\_length\_work\_note**

</td><td>

Set the minimum length of worknote to filter out short work notes.-   Type: integer
-   Default value: 5
-   Location: Process Mining &gt; **System** &gt; **Properties**

</td></tr><tr><td>

Specify the maximum number of records per cluster sent to the LLM for analyzing agent activity **promin.agent\_activity\_analysis.max\_records\_per\_cluster**

</td><td>

Set the maximum number of records per cluster sent to the LLM for analyzing agent activity.-   Type: integer
-   Default value: 200
-   Location: Process Mining &gt; **System** &gt; **Properties**

</td></tr><tr><td>

Specify the maximum length of worknote to filter out long worknotes **promin.agent\_activity\_analysis.max\_length\_work\_note**

</td><td>

Set the maximum length of worknote to filter out long work notes.-   Type: integer
-   Default value: 1000
-   Location: Process Mining &gt; **System** &gt; **Properties**

</td></tr><tr><td>

Specify the minimum number of records with eligible work notes/comments, excluding those that are too long, too short, or machine-generated **promin.agent\_activity\_analysis.min\_eligible\_worknotes**

</td><td>

Set the minimum number of records with eligible work notes/comments, excluding those that are too long, too short, or machine-generated.

 -   Type: integer
-   Default value: 25
-   Location: Process Mining **System** **Properties**

</td></tr></tbody>
</table>