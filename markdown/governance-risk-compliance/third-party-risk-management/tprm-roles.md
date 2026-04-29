---
title: Roles in Third-party Risk Management
description: Roles determine permissions and access in TPRM.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Reference, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Roles in Third-party Risk Management

Roles determine permissions and access in TPRM.

## TPRM roles

<table id="table_o14_t2s_2mb"><thead><tr><th>

Friendly name \[role name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Third-party reader \[vendor\_reader\]

</td><td>

Read access to third-party contact records.

</td><td>

None

</td></tr><tr><td>

Third-party editor \[vendor\_editor\]

</td><td>

Create/update/delete third-party contact records.

</td><td>

None

</td></tr><tr><td>

Third-party assessment reviewer\[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\]

</td><td>

View assessment and questionnaire data. In addition to viewing, they can leave comments on the following tables:

-   Tiering assessment
-   Internal assessment
-   External assessment
-   Third-party risk issues
-   Third-party risk tasks
-   Third-party risk due diligence request

</td><td>

Contains:

 -   compliance\_reader
-   risk\_reader
-   task\_editor
-   vendor\_reader
-   sn\_dora\_accel.user
-   sn\_smart\_asmt.template\_reader
-   sn\_smart\_asmt.assessment\_reader
-   sn\_tprm\_genai.nowassist\_user

</td></tr><tr><td>

TPR assessor \(Third-party risk assessor\)

 \[sn\_vdr\_risk\_asmt.vendor\_assessor\]

</td><td>

-   Includes all permissions of the Third-party assessment reviewer role plus: Manage third parties, third-party contacts, external risk assessments, and issues.
-   You can set the following options for the sn\_svdp.allow\_assessor\_edit property:

    -   Enable TPR assessors to answer questions or modify responses in third-party questionnaires \(default\).
    -   Enable TPR assessors to modify responses.
    -   Don’t enable TPR assessors to answer questions or modify responses.
See [Configure TPRM properties](../task/tprm-properties-configure.md).


</td><td>

Contains:-   compliance\_reader
-   vendor\_assessment\_reviewer
-   vendor\_editor
-   vendor\_reader
-   sn\_dora\_accel.manager

</td></tr><tr><td>

TPR approver

 \[sn\_vdr\_risk\_asmt.approver\]

</td><td>

Includes all permissions of the Third-party assessment reviewer role plus: approve IRQs.

</td><td>

Contains:

-   vendor\_assessment\_reviewer
-   sn\_dora\_accel.user

</td></tr><tr><td>

TPR manager \(Third-party risk manager\)\[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\]

</td><td>

Includes all permissions of the TPR assessor role plus:

 -   Manage third-party assessment templates and scheduled assessments.
-   Manage engagements and engagement contacts.
-   Manage scoring rules for both third parties and engagements.

</td><td>

Contains:

-   vendor\_assessor
-   sn\_dora\_accel.manager

</td></tr><tr><td>

TPR admin \(Third-party risk admin\)\[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\]

</td><td>

Includes all permissions of the TPR manager role plus:

 Create and edit the following items:

 -   Third-party assessment templates
-   Risk tiering templates
-   Risk tier questionnaire templates
-   Third-party questionnaire templates
-   Document request templates
-   Post assessment automation rules

 **Note:** All the templates include both classic and SAE templates.

</td><td>

Contains:

-   vendor\_risk\_manager
-   assessment\_admin
-   sn\_dora\_accel.admin
-   sn\_smart\_asmt.assessment\_admin
-   sn\_smart\_imp\_auto.automation\_creator

</td></tr><tr><td>

Contract risk negotiator\[sn\_vdr\_risk\_asmt.contract\_negotiator\]

</td><td>

Includes all permissions of the TPR assessor role plus:

 Gives users in the legal department access to modify contract status and the start and expiration dates.

 You can add users with this role to the **Contract risk negotiators** user group. See [Add users to groups based on responsibilities](../task/tprm-groups-add-users-to.md).

</td><td>

Contains:

-   vendor\_assessor
-   sn\_dora\_accel.manager

</td></tr><tr><td>

\[vendor\_contact\]

-   Called a third-party contact when responding to an external questionnaire/task/issue for a third party.
-   Called an engagement contact when responding to a questionnaire/task/issue for an engagement.

</td><td>

You assign the third-party contact role to users at the third-party organization whose risk is being assessed. Third-party contacts are assigned the snc\_external role to give them access to resources and actions in the Third-party portal.

 **Important:** The third-party contact role should be used only for external contacts. The role prohibits access to your ServiceNow AI Platform instance and grants access only to the Third-party portal.

 You assign the **primary contact** responsibility to the third-party contact who can directly answer assessment questions or assign another contact at the third party to answer the questions. Primary contacts can manage other contacts for the third party.

</td><td>

Contains: snc\_external

</td></tr></tbody>
</table>## Roles required for accessing the Digital resilience third-party registers

A user with one of the following roles can access the Digital resilience third-party registers related modules in the Vendor Management Workspace:

-   TPRM DORA user \[sn\_dora\_accel.user\] role

    Third-party assessment reviewer and TPR approver contain this role.

-   TPRM DORA manager \[sn\_dora\_accel.manager\] role

    TPR assessor and TPR manager contain this role.

-   TPRM DORA admin \[sn\_dora\_accel.admin\]

    The TPR admin contains this role.


For more information on DORA related roles, see [Roles installed with Digital resilience third-party registers](../../grc-operational-res/reference/roles-for-drtpr.md).

## Roles required for using Smart Assessment Engine

A user with one of the following roles can view templates in the Assessment Workspace:

-   TPRM SAE template reader \[sn\_smart\_asmt.template\_reader\] role

    Third-party assessment reviewer contains this role.

-   TPRM SAE assessment reader \[sn\_smart\_asmt.assessment\_reader\] role

    Third-party assessment reviewer contains this role.


A user with one of the following roles can respond to questionnaires in the Vendor Management Workspace, GRC portal, or Third-party portal.

-   TPRM SAE internal assessment user \[sn\_vdr\_risk\_asmt.internal\_assessment\_responder\]

    This role is automatically assigned to an assigned IRQ assessor or internal assessment respondent.

    This role is required to respond to internal/IRQ assessment questionnaires using the GRC Portal.

    This role contains the following roles: sn\_grc\_business\_user, canvas\_user, and sn\_smart\_asmt.actor.

-   TPRMSAE external assessment user \[sn\_vdr\_risk\_asmt.external\_assessment\_responder\]

    This role is automatically assigned to the assigned third-party contact.

    This role is required to respond to external questionnaires using the Third-party portal.

    This contains the role: sn\_smart\_asmt.actor.


A user with the TPRM SAE admin \[sn\_smart\_asmt.assessment\_admin\] role can create SAE templates in the Vendor Management Workspace and Assessment Workspace.

Third-party admin contains this role.

A user with the sn\_smart\_imp\_auto.automation\_creator role can create post assessment impact automation rules.

Third-party admin contains this role.

**Important:** The Third-party assessment reviewer \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\] role is the minimum role that you must have to view any template that is a member of the TPRM external questionnaire, TPRM external document request, TPRM internal tiering questionnaire, and TPRM internal IRQ purposes.

For more information on SAE related roles, see [Roles installed in Smart Assessment Engine](../../assessment-engine/reference/sae-roles-defined.md).

## Roles required for using Now Assist for Third-party Risk Management \(TPRM\)

A user with the Third-party Assessment reviewer \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\] role can use the Now Assist for TPRM skills.

The TPRM GenAI User \[sn\_tprm\_genai.nowassist\_user\] role is granted to Third-party Assessment reviewers \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\] automatically after you install the Now Assist for TPRM application. For more information about a Now Assist for TPRM, see [Now Assist for Third-party Risk Management \(TPRM\)](../../grc-vendor-risk/concept/now-assist-tprm.md).

**Parent Topic:**[Third-party Risk Management reference](../../grc-vendor-risk/concept/tprm-reference.md)

**Related topics**  


[Assign TPRM roles to users and user groups](../task/tprm-roles-assign.md)

[Roles installed with Digital resilience third-party registers](../../grc-operational-res/reference/roles-for-drtpr.md)

[Roles installed in Smart Assessment Engine](../../assessment-engine/reference/sae-roles-defined.md)

