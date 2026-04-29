---
title: Properties installed with Recruitment workspace
description: The system properties installed with the Recruitment workspace plugin is required to configure different functionality in the Recruitment Workspace environment.
locale: en-US
release: australia
product: Recruiter Workspace
classification: recruiter-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Recruitment Workspace, Hiring Experiences, HR Service Delivery, Employee Service Management]
---

# Properties installed with Recruitment workspace

The system properties installed with the Recruitment workspace plugin is required to configure different functionality in the Recruitment Workspace environment.

These properties are available for Recruitment workspace.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_kfz_rbj_tdc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

exchange\_meeting\_user

 sn\_ta\_recruiter.exchange\_meeting\_user

</td><td>

User principal name of the Azure service account user that is used for sending calendar invites.-   Type: String
-   Other possible values:

Ignore cache: Selected


</td></tr><tr><td>

maximum\_slots\_for\_interview\_schedulingsn\_ta\_recruiter.maximum\_slots\_for\_interview\_sch

</td><td>

Restriction for the maximum number of slots that can be selected by a recruiter while scheduling interview. The maximum number available is 10.-   Type: Integer
-   Value: 3
-   Other possible values:

Ignore cache: Selected


</td></tr><tr><td>

state\_for\_onboarding\_mailsn\_ta\_recruiter.state\_for\_onboarding\_mail

</td><td>

State that set off the email notification trigger for onboarding.-   Type: String
-   Value: 60
-   Other possible values:

Ignore cache: Selected


</td></tr><tr><td>

block\_interviewer\_calendarsn\_ta\_recruiter.bok\_interviewer\_calendar

</td><td>

Calendar blocker for the interviewer while scheduling interviews.-   Type: true \| false
-   Value: true
-   Other possible values:

Ignore cache: Selected


</td></tr><tr><td>

duplicate\_allowed\_fieldssn\_ta\_recruiter.duplicate\_allowed\_fields

</td><td>

Replicable fields while duplicating a job requisition.-   Type: String
-   Value: job\_title, preferred\_job\_title, seniority\_level, compensation\_range, position\_count, primary\_location, hiring\_manager, cost\_center,department, employment\_type, working\_hours, travel\_requirement, relocation\_support, immigration\_sponsorship, min\_yrs\_experience, minimum\_qualification, certification, required\_skills, preferred\_skills, preferred\_companies, job\_description
-   Other possible values:
    -   Read roles: sn\_ta\_hiring\_core.admin
    -   Write roles: admin

</td></tr><tr><td>

enable\_outlook\_integrationsn\_ta\_recruiter.enable\_outlook\_integration

</td><td>

Property to enable the outlook integration for Interview scheduling.-   Type: true \| false
-   Value: true
-   Other possible values:
-   Ignore cache: Selected

</td></tr></tbody>
</table>**Parent Topic:**[Recruitment Workspace reference](../concept/recruitment-workspace-reference.md)

