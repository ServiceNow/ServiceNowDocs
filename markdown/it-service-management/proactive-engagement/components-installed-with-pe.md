---
title: Components installed with Proactive Engagement
description: Several types of components are installed with activation of the Proactive Engagement application \(com.snc.self\_remediation\_framework\), including user roles.
locale: en-US
release: australia
product: Proactive Engagement
classification: proactive-engagement
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Proactive Engagement, Digital End-User Experience, IT Service Management]
---

# Components installed with Proactive Engagement

Several types of components are installed with activation of the Proactive Engagement application \(com.snc.self\_remediation\_framework\), including user roles.

## Roles installed with ServiceNow Proactive Engagement

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see Find components installed with an application.

<table id="table_zbn_zhs_xbc"><thead><tr><th>

Role title \[name\]

</th><th>

Contains Roles

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_pren.solution\_provider

</td><td>

sn\_pren.issue\_registry\_template\_write

</td><td>

This persona is responsible for creating the Issue registry template, Resolution, and Resolution prompt records.

</td></tr><tr><td>

sn\_pren.engagement\_admin

</td><td>

sn\_pren.issue\_registry\_write

 sn\_pren.experience\_issue\_read

 sn\_pren.issue\_registry\_template\_write

</td><td>

-   This persona is responsible for deploying the Issue registry templates.
-   Configuring the engagement settings, notification channels and fallback.
-   Create a custom resolution and notification for an existing template.

 **Note:** SOW user role is required to access the Proactive Engagement workbench.

</td></tr><tr><td>

sn\_pren.issue\_registry\_template\_write

</td><td>

None

</td><td>

Can create/edit/read/delete the -   Issue Registry Template records
-   Resolution records
-   Notification Content records

</td></tr><tr><td>

sn\_pren.issue\_registry\_write

</td><td>

None

</td><td>

Can create/edit/read/delete the -   Issue Registry
-   Issue Registry Template records
-   Resolution records
-   Notification Content records

</td></tr><tr><td>

sn\_pren.solution\_provider

</td><td>

None

</td><td>

Can read Experience Issue records

</td></tr></tbody>
</table>## Tables installed

<table id="table_kvc_l53_dxb"><thead><tr><th>

Table

</th><th>

Table name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Proactive engagement provider

</td><td>

sn\_pren\_provider

</td><td>

Record used to maintain the details of the DEX solution provider such as name and provider code. As of today, we only have Servicenow as the provider.

</td></tr><tr><td>

Issue Registry Templates

</td><td>

sn\_pren\_issue\_registry\_template

</td><td>

This table stores all the end-user issues for which a customer could potentially engage the end-user to self-solve in case of an issue occurrence. Issue registry template records can either come from a third-party DEX/DEX provider or be created directly by the customer, with a reference to the provider. This table specifies the resolution for the issue and how the end user should be engaged, and it holds descriptive fields for the issue, such as Short Description and Description. Additionally, it contains a Unique Issue Code, which is a combination of the Provider Code and Issue Code, ensuring uniqueness across all template records for a customer.

</td></tr><tr><td>

Issue Registries

</td><td>

sn\_pren\_issue\_registry

</td><td>

This table holds all the issues that the customer has chosen for end-user self-solution. An Issue Registry record is created by deploying the Issue Registry template record. Simply having the Issue Registry template record does not make the issue eligible for self-solving; the Engagement Admin must deploy the template to create the Issue Registry record.

 The table stores all the configurations deployed by the customer, including details on whether a custom resolution and notification were configured by the customer, engagement settings, notification channel settings, fallback options, and template parity status.

</td></tr><tr><td>

Resolutions

</td><td>

sn\_pren\_resolution

</td><td>

Record used to store the resolutions configured to be executed when a threshold breach occurs, as per the metric rule configuration. This record could include a self-help instruction with defined steps, a URL with a specified link, a remedial action with a reference to the configured remedial action, or of type incident creation.

</td></tr><tr><td>

Notification content

</td><td>

sn\_pren\_notification\_content

</td><td>

Record used to maintain the notification settings such as notification prompt message and resolution consent prompt

</td></tr><tr><td>

Experience Issues

</td><td>

sn\_pren\_experience\_issue

</td><td>

Experience issue record is created once the engagement is initiated with the end-user. This stores data such as user info, **State** of the resolution execution, end reason state, fallback result \(if triggered\), investigative details, etc. This record will be the source of truth for any proactive engagement with end-user.

</td></tr><tr><td>

Experience issue alert

</td><td>

sn\_pren\_experience\_issue\_m2m\_alert

</td><td>

Record used to create a log of the alert that caused experience issue. This is a mapping table between alert and experience issues, with details on count of throttled users and throttling reason.

</td></tr></tbody>
</table>**Parent Topic:**[Proactive Engagement reference](../proactive-engagement-reference.md)

