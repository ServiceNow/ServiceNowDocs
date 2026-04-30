---
title: Roles installed with Risk Management
description: Roles are added with activation of GRC: Risk Management.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Components installed with Risk Management, Reference, Risk Management, Governance, Risk, and Compliance]
---

# Roles installed with Risk Management

Roles are added with activation of GRC: Risk Management.

<table id="table_gtf_wpk_qjb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Risk Reader\[sn\_risk.reader\]

</td><td>

In addition to the inherited permissions, the risk reader has read-only access rights to the Risk application and modules. The risk reader can do the following in the GRC scope:-   Act on issues assigned to him.
-   Have read access to all Indicator templates.
-   Can act on indicator tasks assigned to them.
-   Have read-access to indicators.
-   Have read-access to entities.

The risk reader can do the following in the Risk Management application:

-   Act on the Remediation tasks assigned to them.
-   Have read-access to risks.
-   Take old risk assessment.
-   Have read-access to risk statement and risk framework.
-   Perform advanced risk assessment.
-   Create risk events.
-   Work on risk event tasks and issues.
-   Access all risk events and risk dashboards.
-   Have read-access to feedback.

</td><td>

-   sn\_grc.reader
-   survey\_reader
-   sn\_rvw\_feedback.reader

</td></tr><tr><td>

Risk User\[sn\_risk.user\]

</td><td>

Contains the reader and business user roles in sn\_grc scope, and the reader role in the Risk Management application and business user role in the sn\_grc scope. In addition to the inherited permissions, the risk user can view:-   entity types
-   entities
-   risks
-   remediation tasks
-   control
-   control objectives
-   policy exceptions

The risk user can also create risks. The risk user can be assigned risks and has read-only access to the Policy and Compliance Management application and modules. Risk user can do everything that the risk reader can do. The risk reader can do the following in the Risk Management application:

-   Work on risk acceptance tasks and remediation tasks.
-   Create risks.
-   Access the Advanced Risk related dashboards.
-   Have read-access to the risk identification functionality of Advanced Risk and can take assessment related to risk identification.
-   Create assessment scope.

</td><td>

-   sn\_grc.user
-   sn\_compliance.reader
-   sn\_risk.reader
-   survey\_reader
-   sn\_grc.business\_user
-   sn\_risk\_advanced.ara\_creator

</td></tr><tr><td>

Risk Manager\[sn\_risk.manager\]

</td><td>

Contains the reader, user, and manager roles in sn\_grc scope, and the reader and user roles in the Risk Management application. In addition to the inherited permissions, the risk manager can do the following in the GRC scope-   Create issues and issue ratings.
-   Create entity, entity types, and entity classes and class rules.
-   Create content references.
-   Create indicators and indicator templates.
-   Have read-access to entity tier.

In the Risk Management application, the risk manager can:

-   Create risk frameworks
-   Create risk statements
-   Create risks
-   Create risk event response template.
-   Create risk identifications and can view the dashboard related to risk identification.
-   Create remediation tasks.
-   Create assessment scheduler.
-   Associate risk statements to Information objects using Associate risk statements module.

</td><td>

-   sn\_grc.manager
-   sn\_risk.user

</td></tr><tr><td>

Risk Admin\[sn\_risk.admin\]

</td><td>

Contains the reader, user, manager, and admin roles in sn\_grc scopes, and the reader, user, and manager roles in the Risk Management application. In addition to the inherited permissions, in the GRC scope, the risk admin can create an entity tier. In the Risk Management application, the risk administrator can:-   Delete risk frameworks.
-   Delete entity, tables, indicator, risks, issues, tasks.
-   Create risk statements and risks.
-   Modify admin properties.
-   Modify risk criteria.
-   Create causes and consequences of risk event.
-   Access to risk, advanced risk related properties.
-   Create risk identification configuration.
-   Create a risk assessment methodology, all types of factors.
-   Perform administrative activities.
-   Configure a feedback integration setup for any record type.

</td><td>

-   sn\_grc.admin
-   sn\_risk.user
-   sn\_risk.manager
-   sn\_grc\_appr.admin
-   sn\_rvw\_feedback.admin

</td></tr><tr><td>

Assessment Creator\[sn\_risk.asmt\_creator\]

</td><td>

The assessment creator is used for creating GRC risk assessment metric types.

</td><td>

assessment\_admin

</td></tr><tr><td>

GRC Business User\[sn\_grc.business\_user\]

</td><td>

Users with this role can perform the following tasks:-   Take risk assessment.
-   Create risk response tasks.
-   View risk statements.
-   View risk assessment scope.
-   View and report risk events.
-   Work on assigned risk event tasks.
-   View indicator supporting data.
-   Respond to indicator tasks.
-   Respond to risk identification questionnaire.
-   Respond to metrics data tasks.
-   Report issues.
-   Submit issue triage requests.
-   Work on assigned remediation tasks.
-   Work on assigned issues.
-   If there is an integration with Project Portfolio Management:
    -   View the Project Risk Overview dashboard
    -   Create risks from library.
    -   Elevate enterprise risks.
    -   Initiate any object assessment.

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with Risk Management](r_InstallWRisk.md)

