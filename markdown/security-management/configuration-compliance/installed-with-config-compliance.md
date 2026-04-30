---
title: Components installed with Configuration Compliance
description: Several types of components are installed with activation of the Configuration Compliance plugin, including tables and user roles.
locale: en-US
release: yokohama
product: Configuration Compliance
classification: configuration-compliance
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Reference, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Components installed with Configuration Compliance

Several types of components are installed with activation of the Configuration Compliance plugin, including tables and user roles.

Starting with v15.1.5 of Configuration Compliance, the most frequently used system properties are now accessible within the Configuration Compliance application. To view these system properties, navigate to **All**Configuration Compliance**Properties**.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

## View filtered lists for components installed with an application

Filter the Applications Files table so that only the roles, scheduled jobs, and tables that are installed with an application are displayed. The application you want to view these components for should be installed so that its files are loaded onto the instance and into the metadata table. Follow these steps to view filtered lists from the Applications Files table.

1.  In the filter navigator, enter **sys\_metadata.list** to navigate to the metadata table.
2.  Select the condition builder \(filter icon\), and select, **Application** &gt; **is** followed by the name of your application. For example, **Application** &gt; **is** &gt; **Vulnerability Response**.
3.  In the condition builder, to add a second filter, select **AND**, then select, **Class** &gt; **is a** and choose one of the following classes from the list: **Role**, **Scheduled job**, or **Table**.
4.  Select **Run**.

The results for the class you selected are displayed in a filtered list.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Configuration Compliance administrator\[sn\_vulc.admin\]

</td><td>

Able to modify application property, configuration, update rules, integrations of Configuration Compliance application. Starting with v15.0, an admin user cannot delete source records such as Expliots, CVEs, etc.

</td><td>

sn\_vulc.write**Note:** Inherits the roles that are required for the administration of the records of the Configuration Compliance application.

</td></tr><tr><td>

read\[sn\_vulc.read\]

</td><td>

Read lists and records in Configuration Compliance.**Important:** Starting with v24.0 of Vulnerability Response, the sn\_vulc.read role has the privilege to access the Vulnerability Manager Workspace.

</td><td>

-   sn\_sec\_cmn.calc\_read
-   sn\_vul.view\_manager\_workspace

</td></tr><tr><td>

write\[sn\_vulc.write\]

</td><td>

Write lists and records in Configuration Compliance.

</td><td>

-   sn\_vulc.read
-   sn\_vulc.remediation\_owner

</td></tr><tr><td>

write assignment\[sn\_vulc.write\_assignment

</td><td>

Write to Test Result assignment fields.

</td><td>

Contained in the sn\_vulc.remediation\_owner role.

</td></tr><tr><td>

remediation ownersn\_vulc.remediation\_owner

</td><td>

View and update permission for test results assigned to you or your group.

</td><td>

Contained in the itil role.

 Contains:

-   sn\_sec\_cmn.read
-   sn\_vulc.write\_assignment
-   sn\_vul.view\_rem\_workspace

</td></tr><tr><td>

CC.Systemsn\_vulc.import\_admin

</td><td>

Runs all scheduled jobs in configuration compliance application.**Note:** This user is the default run-as user for every scheduled job in configuration compliance.

</td><td>

-   sn\_vulc.write
-   import\_admin
-   sn\_vul\_tenable.read\_integration

</td></tr><tr><td>

VRCommon.Systemsn\_vul\_cmn.admin

</td><td>

Default run-as user for all scheduled jobs in Vulnerability Response common application.

</td><td>

-   sn\_vul\_cmn.write
-   sn\_sec\_cmn.admin
-   report\_admin

</td></tr><tr><td>

SecCommon.Systemsn\_sec\_cmn.admin

</td><td>

Default run-as user for all scheduled jobs which are used for the background jobs capability in Security support common application

</td><td>

-   sn\_sec\_cmn.int\_write
-   sn\_sec\_cmn.write
-   workflow\_admin
-   sn\_sec\_cmn.calc\_write
-   sn\_sec\_core.read\_dictionary
-   sn\_sec\_cmn.manage\_approval\_rules
-   sn\_sec\_int.admin
-   sn\_sec\_cmn.cap\_email\_write
-   sn\_sec\_cmn.manage\_classification\_rules
-   sn\_sec\_cmn.manage\_background\_job

</td></tr><tr><td>

V14.7: sn\_vulc.edit\_watch\_topic

</td><td>

Edit watch topics for Configuration Compliance.

</td><td>

sn\_vulc.read\_watch\_topic

</td></tr><tr><td>

V14.7: sn\_vulc.read\_watch\_topic

</td><td>

Read watch topics for Configuration Compliance.

</td><td>

cmdb\_read

</td></tr><tr><td>

V14.7: sn\_vulc.create\_watch\_topic

</td><td>

Create watch topics for Configuration Compliance.

</td><td>

sn\_vulc.read\_watch\_topic

</td></tr><tr><td>

sn\_vulc.auditor

</td><td>

Allow read for all configuration compliance modules

</td><td>

sn\_vulc.read

 sn\_vulc.advanced\_read

</td></tr><tr><td>

sn\_vulc.advanced\_read

</td><td>

Allow read for all the configuration compliance administration modules

</td><td>

sn\_vulc.read\_auto\_close\_rules

 sn\_vulc.read\_exception\_configuration

 sn\_vulc.read\_assignment\_rules

 sn\_vulc.read\_task\_rules

 sn\_vulc.read\_auto\_exception\_rule

 sn\_vulc.read\_notifications

 sn\_vulc.read\_risk\_score\_configuration

 sn\_vulc.read\_test\_criticality\_mapping

 sn\_sec\_cmn.read\_approval\_rules

 sn\_vulc.read\_auto\_delete

 sn\_vulc.read\_remediation\_target\_rules

</td></tr><tr><td>

sn\_vulc.read\_test\_criticality\_mapping

</td><td>

Allow read for test criticality mapping

</td><td>

 

</td></tr><tr><td>

sn\_vulc.read\_task\_rules

</td><td>

Allow read for remediation task rules

</td><td>

 

</td></tr><tr><td>

sn\_vulc.read\_assignment\_rules

</td><td>

Allow read for assignment rules

</td><td>

 

</td></tr><tr><td>

sn\_vulc.read\_risk\_score\_configuration

</td><td>

Allow read for risk score configuration

</td><td>

 

</td></tr><tr><td>

sn\_vulc.read\_auto\_close\_rules

</td><td>

Allow read for auto close configuration

</td><td>

 

</td></tr><tr><td>

sn\_vulc.false\_positive\_approver

</td><td>

Allows approving /rejecting closing remediation tasks as false positive

</td><td>

sn\_vul.view\_manager\_workspace

</td></tr><tr><td>

sn\_vulc.exception\_approver

</td><td>

Approved or rejects exception requests.

</td><td>

sn\_vul.view\_manager\_workspace

</td></tr><tr><td>

sn\_vulc.delete

</td><td>

Deletes source records.

</td><td>

 

</td></tr></tbody>
</table>## Scheduled jobs installed

<table id="table_dx3_gb1_wdr"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

V15.0: Update test group on configuration tests

</td><td>

Updates test group on tests for Tenable and Microsoft Defender source. This is a one-time job.

</td></tr><tr><td>

V15.0: Populate existing test result fields

</td><td>

Updates values into newly added columns \(such as Age, Age closed, Active, etc\) in the test results table, saved filters and modules. This is a one-time job.

</td></tr><tr><td>

V15.0: Populate Vulnerable CIs table - Delete and Re-populate for Test Results

</td><td>

Populates total records in the Vulnerable CIs table. This is a one-time job.

</td></tr><tr><td>

Version 12.0 Calculate remediation metrics for all the test results groups

</td><td>

Calculates and updates values for status metrics on remediation task records.

</td></tr><tr><td>

Version 12.0: Calculate remediation metrics for all the test results

</td><td>

Calculates and updates values for status metrics on test results records.

</td></tr><tr><td>

Version 12.0: Change Request State Synchronization

</td><td>

On-demand job that synchronizes the states of all existing remediation tasks \(RTs\) with change requests \(CHGs\). As a change request moves through its life cycle, it also moves the states of any related remediation tasks automatically. Enables state synchronization going forward.

</td></tr><tr><td>

Version 11.1: Check Test Result Groups Deferment

 Expiration

</td><td>

Sends notifications if remediation tasks have expired \(and if they expire in one week\).

</td></tr><tr><td>

Configuration Compliance CI count

</td><td>

Populates distinct configuration item \(CI\) count and the 90 day rolling average in the Configuration Item Count \[sn\_vulc\_cc\_configuration\_item\_count\] table.

</td></tr><tr><td>

Version 11.1: Evaluate and notify remediation targets

</td><td>

Sets or updates remediation target dates on all test results. Determines the status of remediation target dates against rules. Sends notifications

</td></tr><tr><td>

V14.7: Insert Test Result Groups Into Unified Remediation Task

</td><td>

One-time scheduled job to insert all the remediation tasks created in the classic UI into the Unified remediation task \(sn\_vul\_remediation\_task\).

</td></tr><tr><td>

Version 12.0: Populate CR-TRG m2m for CR and CR-Parent

</td><td>

Populates change requests on remediation tasks.

</td></tr><tr><td>

Removed in v11.1: Re-open deferred test result groups**Note:** Deprecated for versions prior to 11.1. Do not use.

</td><td>

Reopens deferred groups when the due-date has passed.

</td></tr><tr><td>

Reapply all assignment rules

</td><td>

Reapplies all assignment rules.

</td></tr><tr><td>

Version 14.3: Reassignment count for assignment rules

</td><td>

Runs daily and posts the total number of test results and remediation tasks that are unassigned by this feature for a particular assignment rule.

</td></tr><tr><td>

Reassess the state of the test result groups

</td><td>

Reassesses the state of remediation tasks for entries where **assess\_state** is false. Runs every 15 minutes.

</td></tr><tr><td>

Rollup test result risk score to test result group and configuration test

</td><td>

Runs hourly and calculates the rollup scores for the changed configuration tests and remediation tasks.-   Calculates rollup risk score for all tests in sn\_vulc\_test\_manifest and deletes the manifest record upon completion.
-   Calculates the rollup risk score for all the tests in sn\_vulc\_result\_group\_manifest and deletes the manifest upon completion.

</td></tr><tr><td>

Version 12.0:Update policy remediation metrics

</td><td>

Starting with v15.0 of Configuration Compliance, this scheduled job has been renamed to Update remediation metrics.-   Calculates and updates values for status metrics on policy records.
-   Calculates test result compliance % of a CI on Discovered Item.

</td></tr><tr><td>

Version 14.3: Set deferral counts

</td><td>

Collects the number of times a test result or a remediation task is deferred.

</td></tr><tr><td>

Update Risk Rating for Test Results

</td><td>

Updates Risk Rating for Test Results.

</td></tr><tr><td>

Update Rollup risk score for all non closed Result groups and Configuration tests.

</td><td>

Updates the rollup risk score for all non-closed Result groups and Configuration Compliance tests.

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assignment Rule

 \[sn\_vulc\_assignment\_rule\]

</td><td>

Contains the set of rules evaluated to set the assignment group on test results.

</td></tr><tr><td>

Authoritative Source

 \[sn\_vulc\_auth\_src\]

</td><td>

Store imported authoritative sources.

</td></tr><tr><td>

Calculator

 \[sn\_vulc\_calculator\_risk\_score\]

</td><td>

Contains the calculator that sets certain test result fields when certain conditions are met.

</td></tr><tr><td>

CC Configuration Item Count\[sn\_vulc\_cc\_configuration\_item\_count\]

</td><td>

Contains the total number of configuration items.

</td></tr><tr><td>

Version 12.0: Change request association\[sn\_vulc\_action\_associate\_cr\]

</td><td>

Staging table used for associating change requests to remediation tasks.

</td></tr><tr><td>

Version 12.0: Change request creation\[sn\_vulc\_action\_create\_cr\]

</td><td>

Staging table used for creating change request forms.

</td></tr><tr><td>

Version 12.0: Change request form \[sn\_vulc\_cr\_form\]

</td><td>

Base table for change request management.

</td></tr><tr><td>

Citation

 \[sn\_vulc\_citation\]

</td><td>

Contains imported citations

</td></tr><tr><td>

Configuration Test

 \[sn\_vulc\_test\]

</td><td>

Contains imported configuration test data.

</td></tr><tr><td>

Configuration test manifest

 \[sn\_vulc\_test\_manifest\]

</td><td>

Contains the configurations tests for which the rollup risk score needs to be calculated.

</td></tr><tr><td>

Version 12.2 Missing asset table \[sn\_vul\_missing\_asset\]

</td><td>

Contains temporary asset records for imported configuration compliance assessment data with unmatched assets.

</td></tr><tr><td>

Configuration Test Technology

 \[sn\_vulc\_test\_technology\]

</td><td>

Contains imported configuration test technologies.

</td></tr><tr><td>

Remediation Task Rule\[sn\_vulc\_grouping\_rule\]

</td><td>

Contains the rules that define the criteria with which groups are automatically created for a set of test results.

</td></tr><tr><td>

Test Groups

 \[sn\_vulc\_policy\]

</td><td>

Contains imported policies.

</td></tr><tr><td>

Policy Configuration Test

 \[sn\_vulc\_policy\_test\]

</td><td>

Contains imported policy configuration test data.

</td></tr><tr><td>

Remediation Target Rule

 \[sn\_vulc\_ttr\_rule\]

</td><td>

Defines the expected time frame for remediating a test result.

</td></tr><tr><td>

Risk Calculators

 \[sn\_vulc\_calculator\_group\]

</td><td>

Contains the grouping of Configuration Compliance calculators. The order of the calculator group determines which group is evaluated first, and in each group, one calculator at most is used.

</td></tr><tr><td>

Risk Score Rollup Calculator

 \[sn\_vulc\_risk\_score\_rollup\]

</td><td>

Contains rollup calculator configurations.

</td></tr><tr><td>

Split remediation tasks

 \[sn\_vulc\_action\_split\_trg\]

</td><td>

Staging table used for splitting remediation tasks.

</td></tr><tr><td>

State Change Approval

 \[sn\_vulc\_state\_change\_approval\]

</td><td>

Contains approval state process data.

</td></tr><tr><td>

Technology

 \[sn\_vulc\_technology\]

</td><td>

Contains imported technologies.

</td></tr><tr><td>

Test Criticality Map

 \[sn\_vulc\_test\_criticality\_map\]

</td><td>

Contains criticality map data.

</td></tr><tr><td>

Test Result

 \[sn\_vulc\_result\]

</td><td>

Contains imported test results.

</td></tr><tr><td>

Remediation Tasks

 \[sn\_vulc\_result\_group\]

</td><td>

Contains imported remediation tasks.

</td></tr><tr><td>

Version 12.0:Remediation Task Change Requests

</td><td>

Contains change requests for remediation tasks.

</td></tr><tr><td>

Remediation task manifest

 \[sn\_vulc\_result\_group\_manifest\]

</td><td>

Contains the remediation tasks for which the rollup risk score needs to be calculated.

</td></tr><tr><td>

Remediation Tasks

 \[sn\_vulc\_m2m\_result\_result\_group\]

</td><td>

Contains remediation task data.

</td></tr><tr><td>

Test Result History

 \[sn\_vulc\_result\_history\]

</td><td>

Contains imported test result history.

</td></tr><tr><td>

Test Result Remediation Status

</td><td>

Status of the test result against the closest applied remediation target rule.

</td></tr><tr><td>

V14.7: Watch Topic Test Counts\[sn\_vulc\_wt\_test\_counts\]

</td><td>

Cache table for the Distinct Configuration Tests tab in the Vulnerability Manager workspace.

</td></tr></tbody>
</table>