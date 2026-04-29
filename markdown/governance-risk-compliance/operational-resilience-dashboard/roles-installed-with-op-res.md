---
title: Roles installed with Operational Resilience
description: Several types of roles are installed with the Operational Resilience application.
locale: en-US
release: australia
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Operational Resilience reference, Operational Resilience, Governance, Risk, and Compliance]
---

# Roles installed with Operational Resilience

Several types of roles are installed with the Operational Resilience application.

## Roles that are installed with Operational Resilience

**Note:** For more information on roles and FAQs, see [KB0555605](https://support.servicenow.com/nav_to.do?uri=/kb%3Fid=kb_article_view&sysparm_article=KB0555605).

<table id="table_rnp_cm2_4tb"><thead><tr><th>

Role name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Operational Resilience administrator\[sn\_oper\_res.admin\]

</td><td>

The Operational Resilience administrator is responsible for:-   Configuring scenarios
-   Setting up entity types, entity filters, and reporting pillars based on dashboard requests from the business teams.
-   Customizing reports on the Operational Resilience dashboard.

 The Operational Resilience administrator should have the ITIL role to add the CMDB relationship between the service and the process.

The Operational Resilience administrator role contains the following roles:

-   sn\_grc.admin
-   sn\_oper\_res.manager
-   Contains sn\_grc\_case\_mgmt.grc\_case\_admin, who inherits the ability to set up the vulnerability type, state models, vulnerability assessment templates, and document templates.

</td></tr><tr><td>

Operational Resilience Manager\[sn\_oper\_res.manager\]

</td><td>

The Operational Resilience Manager is responsible for:-   Ensuring operational resilience in the organization using the dashboards and reports
-   Reviewing reports on the Operational Resilience dashboard, as well as supporting data.

The Operational Resilience Manager role contains the following roles:

-   sn\_grc.manager
-   sn\_compliance.reader
-   sn\_oper\_res.user
-   sn\_risk.reader
-   Contains sn\_grc\_case\_mgmt.grc\_case\_manager, who inherits the ability to submit operational vulnerability \(A type of case\).

</td></tr><tr><td>

Operational Resilience User\[sn\_oper\_res.user\]

</td><td>

The Operational Resilience User is responsible for:-   Reviewing reports on the Operational Resilience dashboard, as well as supporting data.
-   Completing impact tolerance and test plans for individuals assigned to the service impact analysis.

 The Operational Resilience User can access the Vulnerability Response data.

The Operational Resilience User role contains the following roles:

-   sn\_incident.read
-   sn\_grc.reader
-   task\_editor
-   Contains sn\_grc\_case\_mgmt.grc\_case\_business\_user, who can be assigned tasks or issues in the operational vulnerability.

</td></tr><tr><td>

sn\_oper\_res.operational\_resilience\_business\_user

</td><td>

Submits "Report operational vulnerability" from the employee center from: instancename/esc?id=emp\_taxonomy\_topic&amp;topic\_id=14aedd93a314121051b1ab18951e6150&amp;in\_context=true

</td></tr><tr><td>

BCM and Operational Resilience Administrator \[sn\_oper\_res.bcm\_opres\_admin\]

</td><td>

The BCM and Operational Resilience Administrator role contains the following roles: -   sn\_oper\_res.bcm\_opres\_manager
-   sn\_oper\_res.admin

</td></tr><tr><td>

BCM and Operational Resilience Manager \[sn\_oper\_res.bcm\_opres\_manager\]

</td><td>

The BCM and Operational Resilience Manager role contains the following roles: -   sn\_oper\_res.bcm\_opres\_user
-   sn\_oper\_res.manager

</td></tr><tr><td>

BCM and Operational Resilience User \[sn\_oper\_res.bcm\_opres\_user\]

</td><td>

The BCM and Operational Resilience User role has the following permissions:-   Can read the BCM UIB Workspace.
-   Cannot access the IRM reports or data.

The BCM and Operational Resilience User role contains the following roles: -   sn\_bcm.viewer
-   sn\_oper\_res.user

</td></tr><tr><td>

IRM Operational Resilience User \[sn\_oper\_res.irm\_opres\_user\]

</td><td>

The Integrated Risk Management \(IRM\) Operational Resilience User role cannot access the BCM reports and data. It contains:

-   sn\_grc.reader
-   sn\_oper\_res.user

 The following user roles are contained only when policy and compliance management and risk management are installed:

-   sn\_compliance.reader
-   sn\_risk.reader

</td></tr><tr><td>

IRM Operational Resilience Administrator \[sn\_oper\_res.irm\_opres\_admin\]

</td><td>

The IRM Operational Resilience Administrator role contains the following roles: -   sn\_oper\_res.irm\_opres\_manager
-   sn\_oper\_res.admin

</td></tr><tr><td>

IRM Operational Resilience Manager \[sn\_oper\_res.irm\_opres\_manager\]

</td><td>

The IRM Operational Resilience Manager role contains the following roles: -   sn\_oper\_res.irm\_opres\_user
-   sn\_oper\_res.manager

</td></tr></tbody>
</table><table id="table_mqg_zbg_zzb"><thead><tr><th>

Roles

</th><th>

Family

</th><th>

Comments

</th></tr></thead><tbody><tr><td>

sn\_oper\_res.admin

</td><td>

IRM

</td><td>

None

</td></tr><tr><td>

sn\_oper\_res.manager

</td><td>

IRM

</td><td>

None

</td></tr><tr><td>

sn\_oper\_res.user

</td><td>

IRM

</td><td>

The sn\_oper\_res.user role is required to access Vulnerability profile records.

</td></tr><tr><td class="sub-head" colspan="2">

New roles introduced

</td><td>

 

</td></tr><tr><td>

sn\_oper\_res.bcm\_opres\_admin

</td><td>

BCM

</td><td rowspan="3">

The sn\_bcm.viewer role is required to access the BCM Configurable Workspace.​

 A user with the sn\_oper\_res.bcm\_opres\_user+ role can access both Operational Resilience Workspace and BCM Configurable Workspace.

</td></tr><tr><td>

sn\_oper\_res.bcm\_opres\_manager

</td><td>

BCM

</td></tr><tr><td>

sn\_oper\_res.bcm\_opres\_user

</td><td>

BCM

</td></tr><tr><td>

sn\_oper\_res.irm\_opres\_admin

</td><td>

IRM

</td><td rowspan="3">

A user with the sn\_oper\_res.irm\_opres\_user+​ role can access the Operational Resilience Workspace, but cannot access the Compliance Workspace and Risk Workspace. ​

 Extra roles are needed to access the Compliance Workspace and Risk Workspace.

</td></tr><tr><td>

sn\_oper\_res.irm\_opres\_manager

</td><td>

IRM

</td></tr><tr><td>

sn\_oper\_res.irm\_opres\_user

</td><td>

IRM

</td></tr></tbody>
</table>## Roles created for BCM Professional and IRM Professional

-   The following roles are created for the BCM Professional users:

    **Note:** When the app-grc-bcm-lite applications are not installed, the users with these roles are counted as operators.

    -   sn\_oper\_res.bcm\_opres\_admin
    -   sn\_oper\_res.bcm\_opres\_manager
    -   sn\_oper\_res.bcm\_opres\_user
-   The following roles are created for the IRM Professional users:

    **Note:** When the app-grc-bcm-lite applications are not installed, the users with these roles are counted as operators.

    -   sn\_oper\_res.irm\_opres\_admin
    -   sn\_oper\_res.irm\_opres\_manager
    -   sn\_oper\_res.irm\_opres\_user​
-   When the following Lite applications are installed, the users with the sn\_oper\_res.bcm\_opres\_user, sn\_oper\_res.irm\_opres\_user, or sn\_oper\_res.user roles are counted as Lite operators.
    -   BCM Lite application: app-grc-bcm-lite \(Plugin id: com.snc.app\_grc\_bcm\_lite\)​
    -   IRM Lite application: app-grc-business-user-lite \(Plugin id: com.sn\_grc\_lite\)​
-   The sn\_oper\_res.admin, sn\_oper\_res.manager, and sn\_oper\_res.user roles are included in IRM.

## Roles required for accessing the Workspaces

A user with one of the following roles can access the Operational Resilience Workspace and BCM Configurable Workspace:

-   sn\_oper\_res.bcm\_opres\_user​
-   sn\_oper\_res.bcm\_opres\_manager​
-   sn\_oper\_res.bcm\_opres\_admin

​A user with any following role can access the Operational Resilience Workspace:

-   sn\_oper\_res.irm\_opres\_user
-   sn\_oper\_res.irm\_opres\_manager
-   sn\_oper\_res.irm\_opres\_admin

A user with one of the following roles can access the Risk Workspace:

-   sn\_risk\_workspace.business\_op\_risk\_manager​
-   sn\_risk\_workspace.IT\_risk\_manager​
-   sn\_risk\_workspace.operatonal\_risk\_manager​

A user with one of the following roles can access the Compliance Workspace:

-   sn\_compliance\_ws.corporate\_compliance\_analyst​
-   sn\_compliance\_ws.corporate\_compliance\_manager​
-   sn\_compliance\_ws.it\_compliance\_manager​

## Roles used for reporting the incidents

The following roles are used for reporting incidents in the Digital resilience incident reporting module.

|Role|Description|
|----|-----------|
|sn\_dri\_inc\_rptg.digital\_resilience\_incident\_admin|Role for setting up administrative and Digital resilience incident activities.|
|sn\_dri\_inc\_rptg.digital\_resilience\_incident\_manager|Role for creating Operational Resilience and Digital resilience incident activities.|
|sn\_dri\_inc\_rptg.digital\_resilience\_incident\_user|Role for participating in Operational Resilience and Digital resilience incident activities.|

## Plugin dependencies for BCM Professional

For BCM Professional, the following mandatory applications are installed with Operational Resilience.![BCM plugins.](../image/bcm-required-plugins.png)

-   Business Continuity Planning \(com.snc.bcm.app\_bcm\_planning\)
-   Business Impact Analysis \(com.snc.bcm.app\_bcm\_bia\)
-   Crisis Management \(com.snc.bcm.app\_bcm\_exercise\)
-   Data Relationships Framework \(com.sn\_app\_grc\_relationship\_config\)
-   Optional: Vulnerability Response \(com.snc.vulnerability\)

## Plugin dependencies for IRM Professional

For IRM Professional, the following mandatory applications are installed with Operational Resilience.![IRM plugins.](../image/irm-required-plugins.png)

-   Advanced Risk Assessment \(com.sn\_risk\_advanced\)
-   Data Relationships Framework \(com.sn\_app\_grc\_relationship\_config\)
-   Policy and Compliance Management \(com.sn\_compliance\)
-   Risk Management \(com.sn\_risk\)
-   Optional: Vulnerability Response \(com.snc.vulnerability\)

