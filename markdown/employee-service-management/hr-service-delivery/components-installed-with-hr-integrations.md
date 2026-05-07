---
title: Components installed with HR Integrations
description: Several types of components install with the activation of the HR Integrations plugin, including tables, user roles, and scheduled jobs.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Activate, HR Integrations, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Components installed with HR Integrations

Several types of components install with the activation of the HR Integrations plugin, including tables, user roles, and scheduled jobs.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

**Note:** The Human Resources Scoped App: Integrations \[com.sn\_hr\_integrations\] plugin activates the sn\_hr\_integrations.min\_admin\_count system property \[sys\_properties.list\]. This property prevents you from deleting your only HR Integrations admin user by requiring a minimum number \(default is two\) of active users with this role.

## Roles installed

<table id="table_fl3_fx1_ggc"><thead><tr><th>

Role Name

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

HR integrations administrator \[sn\_hr\_integrations.admin\]

</td><td>

Can access and configure the HR Integrations application.

</td><td>

sn\_hr\_integrations.user

</td></tr><tr><td>

HR integrations user \[sn\_hr\_integrations.user\]

</td><td>

Can access and read data in the HR Integrations application.

</td><td>

None

</td></tr></tbody>
</table>## Scheduled jobs installed

<table id="table_ixq_yx1_ggc"><thead><tr><th>

Scheduled Job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assign HR Client Roles for Integration Users Sync.

</td><td>

Assigns HR roles for integration users daily.

</td></tr><tr><td>

HR Integrations - External Interface Push Retry Job.

</td><td>

Retries data push to the third-party system on a periodic basis.

</td></tr><tr><td>

HR Integrations-Accurate Background Check Get Order Updates.

</td><td>

Gets background check order updates for the Accurate integration on a periodic basis.

</td></tr></tbody>
</table>## Tables installed

<table id="table_rqp_ny1_ggc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

HR Integrations Additional Inputs

 \[sn\_hr\_integrations\_additional\_inputs\]

</td><td>

Table for additional inputs.

</td></tr><tr><td>

Background Check Package

 \[sn\_hr\_integrations\_background\_check\_package\]

</td><td>

Table for background check packages.

</td></tr><tr><td>

HR Integrations Background Check Staging

 \[sn\_hr\_integrations\_background\_check\_staging\]

</td><td>

Staging table for background checks.

</td></tr><tr><td>

HR Integrations Department Staging

 \[sn\_hr\_integrations\_dept\_staging\]

</td><td>

Staging table for departments.

</td></tr><tr><td>

HR Integrations External Interface

 \[sn\_hr\_integrations\_external\_interface\]

</td><td>

Table for HR external interfaces.

</td></tr><tr><td>

HR Integrations Job Profile

 \[sn\_hr\_integrations\_job\_profile\]

</td><td>

Staging table for job profiles.

</td></tr><tr><td>

HR Integrations Job Tracker

 \[sn\_hr\_integrations\_job\_tracker\]

</td><td>

Table for job trackers.

</td></tr><tr><td>

Leave Types

 \[sn\_hr\_integrations\_leave\_type\]

</td><td>

Table for leave types.

</td></tr><tr><td>

HR Integrations Location Staging

 \[sn\_hr\_integrations\_loc\_staging\]

</td><td>

Staging table for locations.

</td></tr><tr><td>

HR Integrations Outbound Schema Mapping

 \[sn\_hr\_integrations\_outbound\_schema\_mapping\]

</td><td>

Table for HR outbound schema mappings.

</td></tr><tr><td>

HR Integrations Outbound Service

 \[sn\_hr\_integrations\_outbound\_service\]

</td><td>

Table for HR integration outbound services.

</td></tr><tr><td>

HR Integrations Outbound Service Trigger

 \[sn\_hr\_integrations\_outbound\_service\_trigger\]

</td><td>

Table for outbound service trigger.

</td></tr><tr><td>

HR Integrations Schema Mapping

 \[sn\_hr\_integrations\_schema\_mapping\]

</td><td>

Table for HR schema mappings.

</td></tr><tr><td>

HR Integrations Service

 \[sn\_hr\_integrations\_service\]

</td><td>

Table for HR integration services.

</td></tr><tr><td>

HR Integrations Service Job Tracker

 \[sn\_hr\_integrations\_service\_job\_tracker\]

</td><td>

Table for service job trackers.

</td></tr><tr><td>

HR Integrations Service Mapping

 \[sn\_hr\_integrations\_service\_mapping\]

</td><td>

Table for HR service mappings.

</td></tr><tr><td>

HR Integrations Source

 \[sn\_hr\_integrations\_source\]

</td><td>

Table for sources.

</td></tr><tr><td>

HR Integrations Source Properties

 \[sn\_hr\_integrations\_source\_properties\]

</td><td>

Table for source properties.

</td></tr><tr><td>

HR Integrations Source Version

 \[sn\_hr\_integrations\_source\_version\]

</td><td>

Table for source versions.

</td></tr><tr><td>

HR Integrations Staging

 \[sn\_hr\_integrations\_staging\]

</td><td>

Core HR integrations staging table.

 **Note:** All HR integrations staging tables should be an extension of this core table.

</td></tr><tr><td>

HR Integrations Worker Profile

 \[sn\_hr\_integrations\_worker\_profile\]

</td><td>

Staging table for worker profiles, effective worker profiles, and future worker profiles.

</td></tr></tbody>
</table>**Parent Topic:**[Activate HR Integrations](../task/activate-hr-integrations.md)

