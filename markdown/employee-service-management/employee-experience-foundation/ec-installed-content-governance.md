---
title: Components installed with Content Governance
description: Several types of components install with the activation of the Content Governance \[sn\_cg\] plugin, including tables, user roles, and scheduled jobs.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Reference, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Components installed with Content Governance

Several types of components install with the activation of the Content Governance \[sn\_cg\] plugin, including tables, user roles, and scheduled jobs.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

**Note:** The Content Governance \[sn\_cg\] plugin activates the sn\_cda.min\_admin\_count system property \[sys\_properties.list\]. This property prevents you from deleting your only Governance admin user by requiring a minimum number \(default is two\) of active users with this role.

## Roles installed

|Role title \[name\]|Description|Contains roles|
|-------------------|-----------|--------------|
|Content request user \[sn\_cg.content\_request\_user\]|Gives read and write access to content request records. This role is automatically assigned to the Content Publishing Content admin \(sn\_cd.content\_admin\) and Content manager \(sn\_cd.content\_manager\) roles.|None|
|Content items request user \[sn\_cg.content\_request\_item\_user\]|Gives read and write access to content items records. This role is automatically assigned to the Content Publishing Content admin \(sn\_cd.content\_admin\) and Content manager \(sn\_cd.content\_manager\) roles.|None|

## Tables installed

|Table|Description|
|-----|-----------|
|Content Request Item \[sn\_cg\_content\_request\_item\]|Content created from the Content Governance interface|
|Content Request \[sn\_cg\_content\_request\]|Request for content created by an employee or manager|

**Parent Topic:**[Employee Center Pro reference](emp-center-pro-reference.md)

**Related topics**  


[Approvals experience reference](approval-hub-ootb.md)

[Block content form](block-content-form.md)

[Campaign overview and Campaign analytics dashboards](../concept/ecpro-content-automation-content-pack.md)

[Components installed with Employee Center Pro](components-installed-with-employee-center-pro-1.md)

[Components installed with Content engagement](installed-content-engagement.md)

[Components installed with Content Experiences](installed-with-content-auto.md)

[Components installed with Content Publishing](installed-with-content-delivery.md)

[Components installed with Content Analytics](ecpro-installed-content-analytics-1.md)

[Content Analytics dashboards](../concept/content-analytics-dashboards.md)

[Content engagement dashboard](../concept/ec-pro-content-engagement-dashboard.md)

[Content Library Overview dashboard](../concept/content-library-overview-dashboard.md)

[Employee Center Pro widgets](employee-center-pro-widgets-list.md)

[Feedback Analytics dashboard](../concept/ex-fdback-board.md)

[Feedback configuration form](ex-feedback-new-record.md)

[Feedback definition form](fdbck-dfnition-record.md)

[Link content form](link-content-form.md)

[Location Consent form](location-consent-form.md)

[Notification content form](notification-content-form.md)

[Properties installed with Content Experiences](properties-installed-with-content-auto.md)

[Properties installed with Content Governance](properties-installed-content-governance.md)

[Properties installed with Content Publishing](properties-with-content-delivery.md)

[Schedule appointment form](schedule-appointment-form.md)

