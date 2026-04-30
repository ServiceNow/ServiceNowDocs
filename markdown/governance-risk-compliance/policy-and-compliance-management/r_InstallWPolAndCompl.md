---
title: Components installed with Policy and Compliance Management
description: Reference topics provide additional information about components that are installed with the activation of the Policy and Compliance Management plugin. These components include tables, user roles, and properties.Roles are added with activation of GRC: Policy and Compliance Management.Tables are added with activation of GRC: Policy and Compliance Management.The access control limitations \(ACLs\) or no role conditions with snc\_internal role \(or no role\) is replaced with sn\_grc.business\_user role to control the access level of different users to compliance tables and also to track their usage.Properties are added with activation of GRC: Policy and Compliance Management.
locale: en-US
release: yokohama
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 12
breadcrumb: [Policy and Compliance Management reference, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Components installed with Policy and Compliance Management

Reference topics provide additional information about components that are installed with the activation of the Policy and Compliance Management plugin. These components include tables, user roles, and properties.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

**Parent Topic:**[Policy and Compliance Management reference](../concept/reference-data-policy-compliance.md)

## Roles installed with GRC: Policy and Compliance Management

Roles are added with activation of GRC: Policy and Compliance Management.

<table id="table_adh_2dw_s3b"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Compliance Administrator\[sn\_compliance.admin\]

</td><td>

Contains the reader, user, manager, and admin roles in sn\_grc scopes, and the reader, user, and manager roles in the Policy and Compliance Management application. In addition to the inherited permissions, the compliance admin can delete authority documents, citations, policies, control objectives, and controls.

</td><td>

-   sn\_compliance.manager
-   sn\_grc.admin

</td></tr><tr><td>

Attestation Creatorsn\_compliance.attestation\_creator

</td><td>

Role used for creating the GRC attestation metric type, as well as exception questionnaires.

</td><td>

assessment\_admin

</td></tr><tr><td>

Compliance Developer\[sn\_compliance.developer\]

</td><td>

Contains the reader, user, manager, admin, and developer roles in sn\_grc scopes, and the reader, user, manager, and admin roles in the Policy and Compliance Management application. In addition to the inherited permissions, the compliance developer can create article templates and edit scripts.

</td><td>

-   sn\_compliance.admin
-   sn\_grc.developer

</td></tr><tr><td>

Compliance Manager\[sn\_compliance.manager\]

</td><td>

Contains the reader, user, and manager roles in sn\_grc scopes, and the reader and user roles in the Policy and Compliance Management application. In addition to the inherited permissions, the compliance manager can create authority documents, citations, control objectives, and controls.

</td><td>

-   sn\_compliance.user
-   sn\_grc.manager
-   sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer

</td></tr><tr><td>

Compliance Reader\[sn\_compliance.reader\]

</td><td>

Contains the reader role in sn\_grc scopes. In addition to the inherited permissions, the compliance reader can be assigned indicators templates, indicators, and issues.

</td><td>

-   sn\_grc.reader
-   survey\_reader

</td></tr><tr><td>

Compliance User\[sn\_compliance.user\]

</td><td>

Contains the reader and user roles in sn\_grc scopes, and the reader role in the Policy and Compliance Management application. In addition to the inherited permissions, the compliance user can be assigned controls and create policies, and has read-only access to the Risk Management application and modules. The compliance user can also create control objectives.

</td><td>

-   sn\_compliance.reader
-   sn\_grc.user
-   sn\_risk.reader
-   survey\_reader
-   vendor\_reader

</td></tr><tr><td>

Corporate compliance analyst \[sn\_compliance\_ws.corporate\_compliance\_analyst\]

</td><td>

Contains the reader and user roles in sn\_grc scopes, and the reader role in the Compliance Workspace.

</td><td>

-   sn\_compliance.user
-   sn\_audit.user

</td></tr><tr><td>

Corporate compliance manager \[sn\_compliance\_ws.corporate\_compliance\_manager\]

</td><td>

Contains the reader, user, and manager roles in sn\_grc scopes, and the reader and user roles in the Compliance Workspace.

</td><td>

-   sn\_compliance.manager
-   sn\_compliance\_ws.corporate\_compliance\_analyst
-   sn\_audit.manager

</td></tr><tr><td>

IT compliance manager \[sn\_compliance\_ws.it\_compliance\_manager\]

</td><td>

Contains the reader, user, and manager roles in sn\_grc scopes, and the reader and user roles in the Compliance Workspace.

</td><td>

-   sn\_compliance.manager
-   sn\_audit.manager

</td></tr><tr><td>

Rationalize process writer \[sn\_reco\_template.rationalization\_process\_writer\]

</td><td>

Contains the reader and user roles in sn\_reco\_template scopes and is needed for rationalization process for creation and editing.

</td><td>

-   sn\_reco\_template.rationalization\_process\_reader
-   sn\_reco\_template.recommendation\_writer

</td></tr><tr><td>

Rationalize process reader \[sn\_reco\_template.rationalization\_process\_reader\]

</td><td>

Contains the reader and user roles in sn\_reco\_template scopes and is reader role for rationalization process.

</td><td>

sn\_reco\_template.recommendation\_reader

</td></tr><tr><td>

Compliance GenAI User \[sn\_grc\_shared\_genai.compliance\_gen\_ai\_user\]

</td><td>

Contains the reader and user roles in sn\_grc\_shared\_genai scopes and is needed for generating recommendation in rationalization process.

</td><td>

 

</td></tr></tbody>
</table>## Tables installed with Policy and Compliance Management

Tables are added with activation of GRC: Policy and Compliance Management.

<table id="table_qlq_g3m_vs"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Authority Document\[sn\_compliance\_authority\_document\]

</td><td>

Extends the Document \[sn\_grc\_document\] table and stores all Authority Documents.

</td></tr><tr><td>

Control\[sn\_compliance\_control\]

</td><td>

Extends the Item \[sn\_grc\_item\] table and stores all controls.

</td></tr><tr><td>

Policy\[sn\_compliance\_policy\]

</td><td>

Extends the Document \[sn\_grc\_document\] table and stores all policies.

</td></tr><tr><td>

Article Template\[sn\_compliance\_article\_template\]

</td><td>

Used to format the policy text contained in a policy record when publishing the policy to the knowledge base \(KB\).

</td></tr><tr><td>

Citation\[sn\_compliance\_citation\]

</td><td>

Extends the Content \[sn\_grc\_content\] table and stores all citations.

</td></tr><tr><td>

Policy exception risk rating mapping \[sn\_compliance\_policy\_exception\_risk\_rating\_mapping\]

</td><td>

Stores the mapping details of the risk assessment rating with the policy exception risk rating.

</td></tr><tr><td>

Policy to Entity Type\[sn\_compliance\_m2m\_policy\_profile\_type\]

</td><td>

Extends Document to Entity Type \[sn\_grc\_m2m\_document\_profile\_type\] and is a many-to-many relationship table that is used to manage the relationships between policies and entity types.

</td></tr><tr><td>

Control Objective to Citation\[sn\_compliance\_m2m\_statement\_citation\]

</td><td>

Many-to-many relationship table that is used to manage relationships between control objectives and their related citations.

</td></tr><tr><td>

Control Objective to Entity Type\[sn\_compliance\_m2m\_statement\_profile\_type\]

</td><td>

Extends Content to Entity Type \[sn\_grc\_m2m\_content\_profile\_type\] and is a many-to-many relationship table that is used to manage the relationships between control objectives and entity type.

</td></tr><tr><td>

Control objective\[sn\_compliance\_policy\_statement\]

</td><td>

Extends the Content \[sn\_grc\_content\] table and stores all control objectives.

</td></tr><tr><td>

Control objective requirement\[sn\_compliance\_policy\_stmt\_requirement\]

</td><td>

Stores the requirement number and the requirement description of a control objective requirement.

</td></tr><tr><td>

Control objective to Control objective requirement\[sn\_compliance\_m2m\_policy\_stmt\_policy\_stmt\_rqmt\]

</td><td>

Many-to-many relationship table that is used to manage relationships between control objective and control objective requirement.

</td></tr><tr><td>

Control requirement\[sn\_compliance\_control\_requirement\]

</td><td>

Stores the requirement number of control

</td></tr><tr><td>

Control to Control requirement\[sn\_compliance\_m2m\_control\_control\_requirement\]

</td><td>

Many-to-many relationship table that stores the control and control requirement details. The **Implementation status** field gives the information whether the requirement is inherited or self implemented.

</td></tr><tr><td>

Requirement selection\[sn\_compliance\_hybrid\_selection\]

</td><td>

Stores the selections of control requirements. It contains the details of control requirements, control objective, entity, and authorization package.

</td></tr><tr><td>

Policy exception\[sn\_compliance\_policy\_exception\]

</td><td>

Stores all policy exceptions.

</td></tr><tr><td>

Policy to Policy Statement\[sn\_compliance\_m2m\_policy\_policy\_statement\]

</td><td>

Many-to-many relationship table that is used to manage relationships between policy and control objectives.

</td></tr><tr><td>

Control to entity \[sn\_compliance\_m2m\_control\_entity\]

</td><td>

Extends Item to entity \[sn\_grc\_m2m\_entity\_item\] table.

</td></tr></tbody>
</table>**Note:** All additional tables installed by the dependent plugins are also needed for Policy and Compliance Management.

## GRC business user role to control access of compliance tables

The access control limitations \(ACLs\) or no role conditions with snc\_internal role \(or no role\) is replaced with sn\_grc.business\_user role to control the access level of different users to compliance tables and also to track their usage.

-   **GRC business user \(sn\_grc.business\_user\) role**

    GRC business user role is granted to users who could perform any GRC operations. It is also granted to users with snc\_internal role who have performed all operations like creating policy exception, issues, and responding to attestations, acknowledgements, and other operations. This role comes with installing GRC Profiles plugin.

-   **GRC business user – lite \(sn\_grc.business\_user\_lite\) role**

    Users who could do limited operations with snc\_internal role are considered as lite operators. Such users are given the GRC business user – lite \(sn\_grc.business\_user\_lite\) role so as to track the lite usage of compliance tables using the role. This role is granted through explicit roles plugin, GRC: Business User – Lite, which can be installed by users with maint access or ServiceNow support teams.


For more information on install, upgrade, and role assignments, see [GRC Business User Role \[KB0864247\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0864247) article in the Now Support Knowledge Base.

**Note:** You must log in to Now Support to view the articles.

The access limitations of users with GRC business user role and other roles for different compliance tables and other related tables are listed herewith. For more information, see the [Security tightenings for GRC: Policy and Compliance Management \[KB1112315\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1112315) article in the Now Support Knowledge Base.

-   **Control Objective**
    -   Users with GRC business user or business user lite role can read all control objectives.
    -   If GRC: Audit Management application is installed and the control objective has a published policy associated to it, then users with external auditor role can read such control objectives.
    -   Users with business user lite have read access to report an issue or policy exception.
-   **Policy**
    -   Users with GRC business user or business user lite role can read all policies.
    -   If GRC: Audit Management application is installed, users with external auditor role can read all published policies.
    -   Users with business user lite have read access to policies so as to create policy exceptions.
-   **Policy to Control Objective M2M**
    -   Users with GRC business user or business user lite role can read a policy to control objective M2M record.
    -   If GRC: Audit Management application is installed, users with external auditor role can read a policy to control objective M2M record if the policy is published.
-   **Control \[sn\_compliance\_control\]**
    -   Users with GRC business user or business user lite role can view a control.
    -   If GRC: Audit Management application is installed, users with external auditor role can read a control.
-   **Assessment Instance \[asmt\_assessment\_instance\]**
    -   Users with GRC business user and business user lite role can view attestations that are assigned to them.
    -   ServiceNow users with GRC business user or business user lite role can take assessments.
    -   Users with GRC business user or business user lite role can view My Grouped Attestations module.
    -   Users with GRC business user and business user lite role can view Group Assessment UI and Ungroup Assessment UI actions.
    -   Users with GRC business user and business user lite role can view **My Attestations** option in GRC application menu.
-   **Assessment Metric Type \[asmt\_metric\_type\]**

    User role is set to GRC business user or business user lite if the evaluation is attestation, the table is Policy Exception, and the role is empty.

-   **Control Overview report**

    User with GRC reader role can view the control overview report.

-   **Issue \[sn\_grc\_issue\]**
    -   **Report and View issues in Service Portal**

        Users with GRC business user role can report an issue and view their reported issues in Service Portal. GRC business user is the minimum role required to view **My Issues** in the Service Portal.

    -   **Read**

        Users with the following roles can view an issue:

        -   GRC user \(sn\_grc.user\) role
        -   GRC business user or business user lite role. Furthermore, the user must fulfil any one of the following conditions:
            -   **Assigned to** field in the issue is the user.
            -   **Assigned to** of the parent issue is the user or **Assignment group** of the parent issue is one of the user's groups.
            -   **Assignment group** is one of the user's groups. Additionally, the user must also have the GRC business user role.
            -   **Issue manager** is the user.
            -   **Issue manager group** is one of the groups that belong to the logged in user.
            -   **Control/Risk** of the issue has an owner and the owner is the user.
            -   Issue is created by the logged in user.
            -   Issue is created out of an issue triage opened by the user.
            -   Logged in user is the assignee or watchlist user on a remediation task for the issue.
            -   If GRC: Audit Management is installed, you are an external auditor only; and an auditor on a closed engagement that had control test issues or other issues, can view only those issues.
    -   **Write**

        If the user with the business user role is also the user designated in the **Assigned to** field, then the user can edit:

        -   Name
        -   Description
        -   Issue manager
        -   Issue manager group
        -   Action plan
        -   State
        -   Parent issue
        -   Additional comments
        -   Work notes
        -   Response
        -   Explanation
        If the user with the business user lite role is also the user designated in the **Assigned to** field, then the user can edit:

        -   Issue manager
        -   Issue manager group
        -   State
        -   Parent issue
        -   Additional comments
        -   Work notes
        -   Response
        -   Explanation
        **Note:** If users with business user and business user lite roles have reported an issue, then they can add comments to the issue. However, a GRC user can edit all issues.

    -   **View My Open Issues**

        Users with a minimum role of a GRC business user or business user lite can view their open issues.

    -   **Issue grouping**

        Issue grouping is only open to users with GRC user role.

    -   **Send information**

        A minimum of GRC business user or business user lite role is required to send information for the issue.

-   **Issue Source \[sn\_grc\_issue\_source\]**

    A minimum of GRC business user role is required to view and edit the Issue Source table.

-   **Remediation task \[sn\_grc\_task\]**
    -   User in the **Assigned to** field of the Remediation task table must have a minimum of GRC business user or business user lite role.
    -   For read access, users who have a remediation task assigned to them or who are the watchlist users on the remediation task must have a GRC business user or business user lite role. The **Assigned to** user of the issue, the issue manager of the issue, or any user with GRC manager \(sn\_grc.manager\) role can view a remediation task.
    -   **My Open Remediation Tasks** is visible to users with a minimum role of GRC business user or business user lite.
-   **My Indicator Task \[sn\_grc\_indicator\_task\]**

    Users with GRC business user or business user lite role can access My Indicator Tasks.

-   **Policy Acknowledgement**

    Users with GRC business user or business user lite role can:

    -   Acknowledge policies from ServiceNow AI Platform UI and Service Portal.
    -   View **My Acknowledgements** menu option in Service Portal.
    -   View Acknowledgement instances \[sn\_compliance\_policy\_acknowledgement\_instance\] that are assigned to them.
-   **Policy Exception \[sn\_compliance\_policy\_exception\]**

    Users with GRC business user or business user lite role can:

    -   Raise Policy Exceptions from ServiceNow AI Platform and Service Portal.
    -   View policy exception. Users with read access include users who requested policy exception, are present in watch list, and are verification approvers, final approvers, impacted control owners, and compliance managers.

For more information, see:

-   [GRC Business user role \[KB0864247\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0864247) article in the Now Support Knowledge Base.
-   [Governance, Risk, and Compliance License Compliance update \[KB1096178\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1096178) article in the Now Support Knowledge Base.

## Properties installed with GRC: Policy and Compliance Management

Properties are added with activation of GRC: Policy and Compliance Management.

<table id="table_ght_bmm_vs"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Entity hierarchy based scoringsn\_compliance.entity\_hierarchy\_based\_scoring

</td><td>

-   **Type**: true or false
-   **Default value**: false
-   **Location**: **All** &gt; **Policy and Compliance** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Trigger control attestations based on the created or updated date of the last completed attestation sn\_compliance.attestation\_run\_reference\_date\_field

</td><td>

-   **Type**: string
-   **Default value**: Created date, Updated date
-   **Location**: **All** &gt; **Policy and Compliance** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

States for which the control is active \(the first state is the default active state\)sn\_compliance.active\_states

</td><td>

Compliance administrators can change this setting.-   **Type**: string
-   **Default value**: draft, assess, review, monitor
-   **Location**: **Policy and Compliance** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

States for which control is inactive \(the first state is the default inactive\)sn\_compliance.closed\_states

</td><td>

Compliance administrators can change this setting.-   **Type**: string
-   **Default value**: retired
-   **Location**: **Policy and Compliance** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Name of the assessment metric type that is used for attestationssn\_compliance.default\_attestation

</td><td>

System administrators can change this setting.-   **Type**: string
-   **Default value**: GRC Attestation
-   **Location**: **Policy and Compliance** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

sn\_compliance.glide.script.block.client.globals

</td><td>

-   **Type**: true or false
-   **Default value**: false
-   **Location**: **Policy and Compliance** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Name of the knowledge base used to publish Policy articlessn\_compliance.knowledge\_base

</td><td>

Compliance administrators can change this setting.-   **Type**: string
-   **Default value**: Governance, Risk, and Compliance
-   **Location**: **Policy and Compliance** &gt; **Administration** &gt; **Properties**

</td></tr><tr id="smart-assessment"><td>

Enable smart assessments on controlsn\_compliance.enable\_smart\_assessments

</td><td>

Property that enables the assessment of controls using the non-classic assessment engine.-   Type: true or false
-   Default value: false

</td></tr></tbody>
</table>