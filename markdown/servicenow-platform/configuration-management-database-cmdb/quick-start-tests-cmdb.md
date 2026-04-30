---
title: Quick start tests for Configuration Management Database \(CMDB\)
description: Validate that Configuration Management Database \(CMDB\) still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Reference, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Quick start tests for Configuration Management Database \(CMDB\)

Validate that Configuration Management Database \(CMDB\) still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.

Configuration Management Database \(CMDB\) quick start tests require activating the Configuration Management \(CMDB\) plugin \(com.snc.cmdb\) and the CMDB - ATF Tests plugin \(com.snc.cmdb.atf\).

|Test|Description|Release version|
|----|-----------|---------------|
|CMDB BSM: Dependency Views|Test functionality of Dependency Views APIs. These APIs retrieve Dependency Views map and associated map items such as context menu items, for a given CI sys\_id and using itil user role.|New York|

<table id="table_ipl_qdw_nhb"><thead><tr><th>

Test

</th><th>

Description

</th><th class="filter">

Release version

</th></tr></thead><tbody><tr><td>

CMDB HEALTH: Health Job Status

</td><td>

Checks whether any CMDB Health dashboard jobs, which were started 30 or more days ago, are still in progress.

</td><td>

New York

</td></tr><tr><td>

CMDB HEALTH: CMDB Health Completeness/ Recommended

</td><td>

Checks whether the recommended metric \(included in the CMDB Health completeness KPI\) is fully functional.This test validates:

-   Creation of a health inclusion rule for the recommend metric.
-   Creation of a recommended field that satisfies the health inclusion rule.
-   Validate that the health inclusion rule is correctly applied to a test record with missing data in the recommended field.

</td><td>

New York

</td></tr></tbody>
</table><table id="table_zxd_11g_klb"><thead><tr><th>

Test

</th><th>

Description

</th><th class="filter">

Release version

</th></tr></thead><tbody><tr><td>

CMDB IRE: IRE Validation

</td><td>

Validate CI identifiers and reconciliation definitions and check indexes for CI identifiers.

</td><td>

Madrid

</td></tr><tr><td>

CMDB IRE: Reconciliation Rule

</td><td>

Check operations on a reconciliation rule, in CI Class Manager, using itil and itil\_admin roles. Operations include create, edit, and delete a reconciliation rule.

 Also, check for active and not active setting, and derived rules.

</td><td>

Paris

</td></tr><tr><td>

CMDB IRE: Identification Rule

</td><td>

Check operations on an identification rule, in CI Class Manager, using itil and itil\_admin roles. Operations include create, edit, and delete an identification rule.

 Also, check for active and not active setting, and derived rules.

</td><td>

Paris

</td></tr></tbody>
</table>|Test|Description|Release version|
|----|-----------|---------------|
|CMDB QB: Query Builder - cmdb\_query\_builder Role|Verify that cmdb\_query\_builder user role can save queries, and access and run all saved queries, in CMDB Query Builder.|New York|
|CMDB QB: Query Builder - cmdb\_query\_builder\_read Role|Verify that cmdb\_query\_builder\_read user role can access and run all saved queries, and cannot save any query, in CMDB Query Builder.|New York|

|Test|Description|Release version|
|----|-----------|---------------|
|CMDB REL EDITOR:Relationship Editor|Check addition of relations to a CI and deletion of relations from a CI using itil user role.|New York|
|CMDB REL FORMATTER:Relationship Formatter|Check accuracy of CI information, relationship types, relationships, associated records such as change tickets, and settings such as CMDB views \(relationship filters\), displayed for a specific CI in relationship formatter using itil user role.|New York|

|Test|Description|Release version|
|----|-----------|---------------|
|CMDB SDK: Query CMDB Metadata|Test querying CMDB metadata.|New York|
|CMDB SDK: Create a relation for a CI using REST APIs|Test creation of a relationship for a CI in the CMDB using the CMDB REST APIs.|New York|
|CMDB SDK: Delete a relation for a CI using REST APIs|Test deletion of a relationship for a CI using CMDB REST APIs.|New York|
|CMDB SDK: Create a CI using REST API|Test creation of a CI using CMDB REST APIs.|New York|
|CMDB SDK: Query CMDB using REST APIs|Test querying the CMDB using CMDB REST APIs.|New York|
|CMDB SDK: Update a CI using REST APIs|Test updating of a CI using CMDB REST APIs.|New York|
|CMDB SDK: Query for a CI using REST APIs|Test querying a CI using CMDB REST APIs.|New York|

**Related topics**  


[Quick start tests](https://www.servicenow.com/docs/access?context=quick-start-tests&version=zurich&pubname=zurich-application-development&ft:locale=en-US)

