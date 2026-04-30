---
title: Security Analyst Workspace properties
description: These system properties are used to configure the Security Analyst Workspace.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Configure the Security Analyst Workspace, Install and configure Security Incident Response, Security Incident Response setup, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Analyst Workspace properties

These system properties are used to configure the Security Analyst Workspace.

There are two types of properties:

-   Properties that are typically not modified like sys\_ids and product keys.
-   Properties that are modified as required like long poll intervals and user interface configurations.

**Note:** The Security Analyst Workspace properties are located at this location: **Security Incident** &gt; **Analyst Workspace Setup** &gt; **Analyst Workspace Properties**.

<table id="table_ftv_dry_hhb"><thead><tr><th>

Property Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Fields that are hidden by default in the response task banner.

 sn\_app\_secops\_ui.form.excluded\_fields.response\_task

</td><td>

-   **Type**: string
-   **Default value**:
    -   number
    -   short description
    -   comments
    -   work\_notes
    -   comments\_and\_work\_notes
    -   work\_notes\_list
    -   automation\_activity

</td></tr><tr><td>

Fields that are hidden by default in the incident banner.

 sn\_app\_secops\_ui.form.excluded\_fields.incident

</td><td>

-   **Type**: string
-   **Default value**:
    -   number
    -   short description
    -   comments
    -   work\_notes
    -   comments\_and\_work\_notes
    -   work\_notes\_list
    -   automation\_activity
    -   security\_tags

</td></tr><tr><td>

Background color style is applied to the fields listed here.

 sn\_app\_secops\_ui.form.color\_coded\_fields

</td><td>

-   **Type**: string
-   **Default value**:
    -   business criticality
    -   impact
    -   priority
    -   risk\_score
    -   severity

</td></tr><tr><td>

If true, tables extended from the sn\_si\_task base response task table, will also have access to email templates created for the base response task table.

 sn\_app\_secops\_ui.extend.base.response\_task.email\_templates

</td><td>

-   **Type**: true \| false
-   **Default value**: true

</td></tr><tr><td>

Sets the width of each summary field in each response task banner.

 sn\_app\_secops\_ui.task\_summary.single\_summary.width.response\_task

</td><td>

-   **Type**: integer
-   **Default value**: 10

</td></tr><tr><td>

Sets the width of each summary field in each incident banner.

 sn\_app\_secops\_ui.task\_summary.single\_summary.width.incident

</td><td>

-   **Type**: integer
-   **Default value**: 15

</td></tr><tr><td>

Sets a limit on the number of summary fields allowed in the incident banner.

 sn\_app\_secops\_ui.task\_summary.single\_summary.limit.incident

</td><td>

-   **Type**: integer
-   **Default value**: 12

</td></tr><tr><td>

Sets a limit on the number of summary fields allowed in the response task banner.

 sn\_app\_secops\_ui.task\_summary.single\_summary.limit.response\_task

</td><td>

-   **Type**: integer
-   **Default value**: 12

</td></tr><tr><td>

Sets a limit on the number of summary fields allowed in the first line of the incident banner.

 sn\_app\_secops\_ui.task\_summary.single\_summary.limit.incident.first\_line

</td><td>

-   **Type**: integer
-   **Default value**: 3

</td></tr><tr><td>

Comma separated list of fields that may have user photos.

 sn\_app\_secops\_ui.form.user\_fields

</td><td>

-   **Type**: string
-   **Default value**:
    -   affected\_user
    -   caller
    -   sys\_updated\_by
    -   sys\_created\_by
    -   opened\_by
    -   closed\_by
    -   submitted\_by

</td></tr><tr><td>

Sets the width of each summary field in each incident peek view.

 sn\_app\_secops\_ui.task\_summary.single\_summary.width.incident\_peek

</td><td>

-   **Type**: integer
-   **Default value**: 13.5

</td></tr><tr><td>

Comma separated list of fields that display time.

 sn\_app\_secops\_ui.form.time\_fields

</td><td>

-   **Type**: string
-   **Default value**:
    -   opened\_at
    -   sys\_created\_on
    -   sys\_updated\_on

</td></tr><tr><td>

Controls the frequency \(in milliseconds\) at which the sighting search results are refreshed.

 sn\_app\_secops\_ui.poller\_interval.search\_action

</td><td>

-   **Type**: integer
-   **Default value**: 30000

**Minimum**: 15000


</td></tr><tr><td>

Controls the frequency \(in milliseconds\) at which the count or query data is refreshed.

 sn\_app\_secops\_ui.poller\_interval.related\_list

</td><td>

-   **Type**: integer
-   **Default value**: 30000

**Minimum**: 15000


</td></tr><tr><td>

Controls the frequency \(in milliseconds\) at which the result data is refreshed \(for the playbook\).

 sn\_app\_secops\_ui.poller\_interval.playbook\_tasks

</td><td>

-   **Type**: integer
-   **Default value**: 30000

**Minimum**: 15000


</td></tr><tr><td>

ID for the Security Operations Integration - Isolate Host workflow.

 sn\_app\_secops\_ui.workflow.id.isolate\_host

</td><td>

-   **Type**: string
-   **Default value**: d72041f1ff203200c68c84648e94fa5e

</td></tr><tr><td>

ID for the Security Operations Integration -Watchlist workflow.

sn\_app\_secops\_ui.workflow.id.publish\_to\_watchlist

</td><td>

-   **Type**: string
-   **Default value**: 35800c0eff343200c68c84648e94fa85

</td></tr><tr><td>

ID for the Security Operations Integration - Block Request workflow.

 sn\_app\_secops\_ui.workflow.id.block\_request

</td><td>

-   **Type**: string
-   **Default value**: 11a6a5270b9032008f9108e3c5673a24

</td></tr><tr><td>

ID for the sn\_si\_analyst user role.

 sn\_app\_secops\_ui.roles.id.sn\_si.write

</td><td>

-   **Type**: string
-   **Default value**: 66878663ff123100158bffffffffff8d

</td></tr><tr><td>

ID for the sn\_si\_read user role.

 sn\_app\_secops\_ui.roles.id.sn\_si.read

</td><td>

-   **Type**: string
-   **Default value**: ae878663ff123100158bffffffffff8e

</td></tr><tr><td>

ID for the sn\_si\_admin user role.

 sn\_app\_secops\_ui.roles.id.sn\_si.admin

</td><td>

-   **Type**: string
-   **Default value**: 22878663ff123100158bffffffffff8d

</td></tr><tr><td>

ID for the Microsoft Exchange - Perform Email Search and Delete workflow.

 sn\_app\_secops\_ui.email.phishing.manual.workflow

</td><td>

-   **Type**: string
-   **Default value**: ed9f289cc310220031fbdccdf3d3aeb4

</td></tr><tr><td>

ID for the Add to Deny list custom action under the Explore tab in the Security Analyst Workspace.

 sn\_app\_secops\_ui.explore.action.direct.id.deny\_list

</td><td>

-   **Type**: string
-   **Default value**: DENY\_e9bd0ac50b632200263a089b37673a0b

</td></tr><tr><td>

ID for the Add to Allow list custom action under the Explore tab in the Security Analyst Workspace

 sn\_app\_secops\_ui.explore.action.direct.id.allow\_list

</td><td>

-   **Type**: string
-   **Default value**: ALLOWLIST\_e9bd0ac50b632200263a089b37673a0b

</td></tr><tr><td>

ID for the Run Threat Lookup UI Action.

 sn\_app\_secops\_ui.explore.action.id.run\_threat\_lookup

</td><td>

-   **Type**: string
-   **Default value**: da5ff4420b540300263a089b37673ae7

</td></tr><tr><td>

ID for the Threat Lookup integration capability.

 sn\_app\_secops\_ui.explore.capability.id.threat\_lookup

</td><td>

-   **Type**: string
-   **Default value**: 39344d4f0b273200263a089b37673ab1

</td></tr><tr><td>

ID for the Observable Enrichment custom action under the Explore tab in the Security Analyst Workspace.

 sn\_app\_secops\_ui.explore.action.id.observable\_enrichment

</td><td>

-   **Type**: string
-   **Default value**: OBS\_ENRICHMENT\_54e2f5d60b5003009f66e94685673a1e

</td></tr><tr><td>

ID for the Enrich Observable integration capability.

 sn\_app\_secops\_ui.explore.capability.id.observable\_enrichment

</td><td>

-   **Type**: string
-   **Default value**: 9ad183640b1003009f66e94685673af4

</td></tr><tr><td>

ID for the Publish to Watchlist UI Action.

 sn\_app\_secops\_ui.explore.action.id.publish\_to\_watchlist

</td><td>

-   **Type**: string
-   **Default value**: 8ee94002ff743200c68c84648e94faf9

</td></tr><tr><td>

ID for the Block Request UI Action.

 sn\_app\_secops\_ui.explore.action.id.block\_request

</td><td>

-   **Type**: string
-   **Default value**: 7158f6e40b2032008f9108e3c5673adf

</td></tr><tr><td>

ID for the Run Sightings Search UI Action.

 sn\_app\_secops\_ui.explore.action.id.sightings\_search

</td><td>

-   **Type**: string
-   **Default value**: 43f91a6f0b032200b97c67d985673a2c

</td></tr><tr><td>

ID for the Create Child Security Incident UI Action.

 sn\_app\_secops\_ui.explore.action.id.create\_child\_incident

</td><td>

-   **Type**: string
-   **Default value**: 5a6882645363530099d5ddeeff7b1272

</td></tr><tr><td>

ID for the Add Security Annotation UI Action.

 sn\_app\_secops\_ui.explore.action.id.add\_security\_annotation

</td><td>

-   **Type**: string
-   **Default value**: 1e3a3e723b5332005a9149a4d2efc4eb

</td></tr><tr><td>

ID for the CI Enrichment Custom Action under the Explore tab in the Security Analyst Workspace.

 sn\_app\_secops\_ui.explore.action.id.ci\_enrichment

</td><td>

-   **Type**: string
-   **Default value**: CI\_ENRICHMENT\_54e2f5d60b5003009f66e94685673a1e

</td></tr><tr><td>

ID for the Isolate Host UI Action.

 sn\_app\_secops\_ui.explore.action.id.isolate\_host

</td><td>

-   **Type**: string
-   **Default value**: d6244e0aff203200c68c84648e94fad3

</td></tr><tr><td>

ID for the Add Multiple Observables UI Action.

 sn\_app\_secops\_ui.explore.action.id.multiple\_observable

</td><td>

-   **Type**: string
-   **Default value**:138de478d78322007a6de294de6103aa

</td></tr><tr><td>

Product key for ag-Grid-Enterprise.

 sn\_app\_secops\_ui.ag-grid-license

</td><td>

-   **Type**: string
-   **Default value**:ServiceNow\_ServiceNow\_5Devs2\_August\_2018\_\_MTUzMzE2NDQwMDAwMA==cedabe1c76ccf28f23aec398ec32997d

</td></tr></tbody>
</table>