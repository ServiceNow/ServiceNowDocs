---
title: Components installed with Content Governance
description: Several types of components install with the activation of the Content Governance \[sn\_cg\] plugin, including tables, user roles, and scheduled jobs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/ec-installed-content-governance.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Employee Center Pro reference, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Components installed with Content Governance

Several types of components install with the activation of the Content Governance \[sn\_cg\] plugin, including tables, user roles, and scheduled jobs.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

Demo data is available for this feature.

**Note:** The Content Governance \[sn\_cg\] plugin activates the sn\_cda.min\_admin\_count system property \[sys\_properties.list\]. This property prevents you from deleting your only Governance admin user by requiring a minimum number \(default is two\) of active users with this role.

## Roles installed

|Role title \[name\]|Description|Contains roles|
|-------------------|-----------|--------------|
|Governance admin \[sn\_cg.governance\_admin\]| |sn\_cg.governance\_manager|
|Governance manager \[sn\_cg.governance\_manager\]| |None|
|Content request user \[sn\_cg.content\_request\_user\]|Gives read and write access to content request records. This role is automatically assigned to the Content Publishing Content admin \(sn\_cd.content\_admin\) and Content manager \(sn\_cd.content\_manager\) roles.|None|
|Content items request user \[sn\_cg.content\_request\_item\_user\]|Gives read and write access to content items records. This role is automatically assigned to the Content Publishing Content admin \(sn\_cd.content\_admin\) and Content manager \(sn\_cd.content\_manager\) roles.|None|

## Tables installed

|Table|Description|
|-----|-----------|
|Content Request Item \[sn\_cg\_content\_request\_item\]|Content created from the Content Governance interface|
|Content Request \[sn\_cg\_content\_request\]|Request for content created by an employee or manager|

**Parent Topic:**[Employee Center Pro reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/emp-center-pro-reference.md)

**Related topics**  


[Block content form]()

[Campaign overview and Campaign analytics dashboards]()

[Components installed with Employee Center Pro]()

[Components installed with Content engagement]()

[Components installed with Content Experiences]()

[Components installed with Content Publishing]()

[Components installed with Content Analytics]()

[Content Analytics dashboards]()

[Content engagement dashboard]()

[Content Library Overview dashboard]()

[Employee Center Pro widgets]()

[Feedback configuration form]()

[Feedback definition form]()

[Link content form]()

[Notification content form]()

[Properties installed with Content Experiences]()

[Properties installed with Content Governance]()

[Properties installed with Content Publishing]()

[Standard banner and icon sizes]()

[To-do content form]()

