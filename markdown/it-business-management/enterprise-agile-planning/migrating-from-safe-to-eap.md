---
title: Migrating from SAFe to EAP
description: Learn about the process required For a successful migration of data from Scaled Agile Framework applications to Enterprise Agile Planning.
locale: en-US
release: australia
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Migrating from SAFe to EAP

Learn about the process required For a successful migration of data from Scaled Agile Framework applications to Enterprise Agile Planning.

Step by step guidance on migrating SAFe data to EAP. 

## Guided Setup to migrate data from SAFe to EAP

Guided Setup provides a sequence of tasks to help you complete the required tasks on your ServiceNow instances. Navigate to **All** &gt; **Strategic Planning** &gt; **Enterprise Agile Planning** &gt; **SAFe Migration Guided Setup**.

The following tasks are included in the guided setup.

## SAFe to EAP migration tasks

1.  [Verify EAP configuration for migration from SAFe](../task/verify-eap-configuration-for-migration-from-safe.md).

    Based on your existing SAFe configuration, verify that the right EAP configuration is activated in your instance and ensure that the right work types \(Epic, Feature, and Story\) are allowed for this configuration.

    For example, if you are a user of ServiceNow Essential SAFe application, you must activate the Essential Configuration in EAP and ensure that EAP Epic and Feature are allowed as work types.

2.  [Verify table, field, and choice mapping between SAFe and EAP](../task/verify-table-field-and-choice-mapping-between-safe-and-eap.md).

    Verify that the tables, columns, choice fields, and custom tables of your SAFe application are correctly mapped to those in EAP.

    **Note:** By default, all columns of SAFe Story \[sn\_safe\_story\] and SAFe Scrum Task \[sn\_safe\_scrum\_task\] tables are migrated to the Story \[rm\_story\] and Scrum Task \[rm\_scrum\_task\] tables. To include or exclude any columns, see [Modify columns to migrate from SAFe story and SAFe Scrum task tables to EAP](../task/modify-columns-to-migrate-safe-story-task-tables-to-eap.md).

3.  [Start migration of SAFe data to EAP](../task/migrate-safe-data-to-eap.md).
4.  Add **Agile Team** as the type for existing SAFe groups. See [Add Agile Team type to SAFe groups for EAP migration](../task/change-safe-groups-type-to-agile-team.md).
5.  Assign the EAP roles sn\_apw\_advanced.eap\_read\_only, sn\_apw\_advanced.eap\_user, and sn\_apw\_advanced.eap\_admin to your SAFe groups or to individual users in your teams.

    See [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=australia&pubname=australia-platform-administration&ft:locale=en-US) or [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=australia&pubname=australia-platform-administration&ft:locale=en-US).


