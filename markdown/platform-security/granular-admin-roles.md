---
title: Granular admin roles
description: Granular admin roles enables you to verify proper access management by assigning roles that define user permissions and responsibilities. By doing so, organizations can maintain security, enforce conformance, and optimize their operations effectively.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 38
keywords: [Granular admin roles, admin roles, ServiceNow admin roles, admin, roles, access management, assigning roles, maintain security, enforce conformance]
---

# Granular admin roles

Granular admin roles enables you to verify proper access management by assigning roles that define user permissions and responsibilities. By doing so, organizations can maintain security, enforce conformance, and optimize their operations effectively.

Roles are a fundamental part of managing access and maintaining security within your instance. They define what you can see and do, verifying that you have the appropriate level of access based on your responsibilities. By assigning the correct roles to the users, organizations can safeguard sensitive data, enforce conformance, and streamline operations.

To optimize access management within the ServiceNow AI Platform, consider adopting granular admin roles. This approach enables you to assign specific permissions to developers or users who perform minor administrative tasks, without granting them unrestricted access to the full admin role.

**Note:**

-   Users who are assigned with admin role previously will have its granular admin roles assigned based on the product or module that they had access to earlier.
-   Each product within the ServiceNow AI Platform has its own set of granular admin roles. To determine the appropriate roles for your administrators or developers, refer to the specific product documentation.
-   You can assign the Instance operator \(`instance_operator`\) role for users who handle day-to-day operations without elevated system configuration privileges. Assign this role to users who need to:
    -   Check logs and diagnose problems
    -   Perform routine maintenance
    -   Keep workflows running smoothly
-   Granular admin roles are separate from the existing admin role and must be assigned independently.

By adopting granular admin roles, you can create a more secure and efficient access management system that aligns with your organization's needs.

<table id="table_granular-roles" class="custom-rows"><thead><tr><th>

Product

</th><th>

Role Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Access Analyzer

</td><td>

access\_analyzer\_admin

</td><td>

Role required to use access-analyzer application.

</td></tr><tr><td>

AE - StreamConnect

</td><td>

message\_replication\_admin

</td><td>

Role required to access all IntegrationHub stream replication features, enable setup and connection to message brokers, and configure message stream replications.

</td></tr><tr><td>

AE - StreamConnect

</td><td>

stream\_connect\_admin

</td><td>

Role required to manage Stream Connect-related settings for subscriptions, topics, and other configurations.

</td></tr><tr><td>

Agent Chat

</td><td>

awa\_admin

</td><td>

Role required to access granular AWA capabilities.

</td></tr><tr><td>

Agent Chat

</td><td>

interaction\_admin

</td><td>

Role required to access granular interaction configuration capabilities.

</td></tr><tr><td>

AI Agents

</td><td>

sn\_aia.admin

</td><td>

Role required to access and update Agentic AI tables.

</td></tr><tr><td>

AI Search

</td><td>

ais\_admin

</td><td>

Role required to manage and view AI Search and NowAssist for Search tables, properties, and configurations.

</td></tr><tr><td>

AI Virtual Agent

</td><td>

sn\_nowassist\_admin.nsa\_admin

</td><td>

Role required to enable your requesters to have a streamlined, conversational experience that is based on generative AI as they submit a catalog item request in Virtual Agent.

</td></tr><tr><td>

App Governance

</td><td>

sn\_aemc.aemc\_admin

</td><td>

Role required to have feature admin access for App Engine Management Center and includes scan\_user.

</td></tr><tr><td>

App Governance

</td><td>

sn\_app\_summary.app\_summary\_admin

</td><td>

Role required to have feature admin access for App Summary.

</td></tr><tr><td>

App Governance

</td><td>

sn\_deploy\_pipeline.deployment\_pipeline\_admin

</td><td>

Role required to have feature admin access for Deployment Pipeline.

</td></tr><tr><td>

App Governance

</td><td>

sn\_pipeline.pipeline\_admin

</td><td>

Role required to have feature admin access for Pipeline.

</td></tr><tr><td>

Application Vulnerability Response

</td><td>

sn\_vul.app\_sec\_manager

</td><td>

Role required for security managers. It is also required for application owners who manage penetration test assessment requests. By default, this role contains granular roles for third-party integration configuration and is required for full read, write, and delete permission on all AVR records and rules.

</td></tr><tr><td>

Alumni Center

</td><td>

sn\_asc.admin

</td><td>

Role required to create and manage profiles and features related to an alumni.

</td></tr><tr><td>

Audit, History and Journal

</td><td>

audit\_admin

</td><td>

Provides write and delete access to sys\_audit. Manual record modifications should be avoided. For bulk deletions, use system jobs rather than direct deletion.

</td></tr><tr><td>

Authentication

</td><td>

adaptive\_auth\_policy\_admin

</td><td>

Role required to configure adaptive authentication policies and filters, as well as update or delete those created by the role. Additionally, policies and filters created by other users and default configurations are available in read-only mode.

</td></tr><tr><td>

Authentication

</td><td>

adpative\_auth\_admin

</td><td>

Role required to access and modify Adaptive Authentication configurations, including creating and adjusting policies, managing policy contexts, and configuring filter criteria. Additionally, users can enable or disable adaptive authentication policies as needed. The role also grants access to modify Multi-Factor Authentication \(MFA\) settings, enabling users to enforce MFA and adjust MFA factor policies.

</td></tr><tr><td>

Authentication

</td><td>

custom\_url\_admin

</td><td>

Role required to configure new custom URLs for the instance, as well as to delete or modify existing custom URL configurations.

</td></tr><tr><td>

Authentication

</td><td>

password\_policy\_admin

</td><td>

Role required to configure and manage the password policies in the instance. Users with this role can create, manage, and enable or disable existing and new password policies.

</td></tr><tr><td>

Authentication

</td><td>

sso\_config\_admin

</td><td>

Role required to access all configurations related to Single Sign-On authentication within the instance. Grants the capability to create and modify feature configurations for SSO SAML, OIDC, Digest, and Certificate-Based Authentication in the instance.

</td></tr><tr><td>

Authentication

</td><td>

user\_authn\_admin

</td><td>

Role required to access and modify all user login-specific configurations, such as Single Sign-On \(SSO\), Account Recovery, Adaptive Authentication, MFA, and Password Policy.

</td></tr><tr><td>

Authentication Factors

</td><td>

auth\_factors\_admin

</td><td>

Role required to configure authentication for voice agent environments, with the factors that first identify the caller, then authenticate them before granting access.

</td></tr><tr><td>

Career Conversations

</td><td>

sn\_egd\_act.admin

</td><td>

Role required to configured all Career Conversations features, including auto closure of conversations and setting up integrations with Microsoft Outlook.

</td></tr><tr><td>

CMDB Admin

</td><td>

sn\_cmdb\_admin

</td><td>

Role required to configure the application and to create, read, write, and delete records in tables.

 Provides the highest level of access to tools and UIs within CMDB Workspace and other store apps such as CMDB Coverage, including full access to the Configuration item \[cmdb\_ci\] table. A CMDB Admin, for example, can set policies in the CI Class Manager and application service requirements.

 CMDB Admin can also modify default config records under the default identifier or the default identifier itself.

</td></tr><tr><td>

Code Assist Experience

</td><td>

background\_script\_admin

</td><td>

Role required to manage background scripts.

</td></tr><tr><td>

Code Assist Experience

</td><td>

now\_assist\_code\_admin

</td><td>

Role required to manage the Now Assist for code generation settings in system\_properties.

</td></tr><tr><td>

Code Assist Experience

</td><td>

now\_assist\_code\_rag\_admin

</td><td>

Role required to manage the Retrieval for code generation app.

</td></tr><tr><td>

Collaborative Work Management

</td><td>

sn\_cwm.cwm\_admin

</td><td>

Role required to update Collaborative Work Management \(cwm\) properties and reports.

</td></tr><tr><td>

Configuration Compliance

</td><td>

sn\_vulc.admin

</td><td>

Role required for full read, write, and delete permission on all Configuration Compliance records and rules.

</td></tr><tr><td>

Container Vulnerability Response

</td><td>

sn\_vul\_container.vulnerability\_admin

</td><td>

Role required for complete access to the Container Vulnerability Response \(CVR\) application and its records. Role required to configure third-party integrations and rules in Container Vulnerability Response.

</td></tr><tr><td>

Contract Management Pro

</td><td>

sn\_cm\_core.contract\_admin

</td><td>

Role required for administrative access to Contracts Core and underlying data.

</td></tr><tr><td>

Contract Management Pro - Contract Workspace

</td><td>

sn\_cm\_workspace.admin

</td><td>

Role required to change the Contract Workspace for Contract Management Pro to fit into the business or user requirements.

</td></tr><tr><td>

Contract Management Pro - Contracts Dashboard

</td><td>

sn\_cm\_pa.pa\_admin

</td><td>

Role required to activate and configure the Analytics Pack for Contract Management Pro application.

</td></tr><tr><td>

Contract Management Pro - Now Assist in Contract Management

</td><td>

sn\_cm\_gen\_ai.ai\_contract\_admin

</td><td>

Role required for administrative access to the Now Assist in Contract Management application.

</td></tr><tr><td>

Cloud Accelerate-Cloud Workspace

</td><td>

sn\_itom\_cam.cw\_admin

</td><td>

Role required to provision cloud accounts, add an unmanaged cloud account and update cloud account details.

</td></tr><tr><td>

Cloud Accelerate-CSC

</td><td>

sn\_cmp.cloud\_service\_user.root\_admin

</td><td>

Role required to manage stacks and resource filters.

</td></tr><tr><td>

Cloud Accelerate - CSC

</td><td>

sn\_cmp.cloud\_admin

</td><td>

Role required to setup Google Cloud Platform and Microsoft Azure Cloud on Cloud Services Catalog, setup cloud accounts for VMware, Specify the credentials that CSC Terraform Connector, work with stacks, view Cloud Service Requests in Cloud Admin Portal, view and utilize the Cloud Root Cause Analysis reports, debug and troubleshoot Cloud API Trail, create custom tags for cloud resources, Store the Azure service principal credentials in the instance.

</td></tr><tr><td>

Cloud Accelerate - CPG

</td><td>

sn\_cmp.cmp\_root\_admin

</td><td>

Role required to create scan schedules, CI finder mapping, policies by using condition builder, flows, or script, a policy set, resource collectors and view the dashboard and audit issue reports to run remediation and scan configurations.

</td></tr><tr><td>

Creator Studio

</td><td>

sn\_creatorstudio.configuration\_admin

</td><td>

Role required to provide admin privileges for the Creator Studio. The roles contains the following Creator Studio granular admin roles:-   sn\_creatorstudio.task\_admin
-   sn\_creatorstudio.app\_configurator
-   sn\_creatorstudio.reports\_viewer

</td></tr><tr><td>

Creator Studio

</td><td>

sn\_creatorstudio.task\_admin

</td><td>

Role required to grant users access to change several fields on the Request Task table or a table that extends Request Task.This role contains the following:-   Table-level access for sn\_creatorstudio\_task: Create, Write, Delete
-   Field-level access for:
    -   sn\_creatorstudio\_task.request\_type, which enables you to change the associated form
    -   sn\_creatorstudio\_child\_task.parent, which enables you to change the parent table for any subtask tables created from a task activity added to an app's playbook.

</td></tr><tr><td>

CSM - CRM Foundation

</td><td>

entitlement\_admin

</td><td>

Role required to access the entitlement table.

</td></tr><tr><td>

CSM - Case Management

</td><td>

sn\_csm\_case\_type.config\_admin

</td><td>

Role required to create, view, update and delete records in the Case type \[`sn_case_type`\]​ table.

</td></tr><tr><td>

CSM - Case Management

</td><td>

sn\_customerservice.case\_admin

</td><td>

Role required to create, view, update and delete records in the Customer Service Case \[`sn_customerservice_case`\]​ table.

</td></tr><tr><td>

CSM - Case Management

</td><td>

sn\_case\_line.admin

</td><td>

Role required to create, view, update and delete records in the Case Line \[`sn_case_line`\]​ table.

</td></tr><tr><td>

CSM - Case Management

</td><td>

sn\_csm\_case\_digest.admin

</td><td>

Role required to delete record in the Case Digest \[`sn_csm_case_digest_task`\] table​. ​Also, can create, view, update and delete records in the Case Digest Configuration \[`sn_csm_case_digest_config`\]​ table.

</td></tr><tr><td>

CSM - Case Management

</td><td>

sn\_task\_plan.admin

</td><td>

Role required to create, view, update and delete records in the Task Plan tables.​

</td></tr><tr><td>

CSM - Case Management

</td><td>

sn\_complaint.admin

</td><td>

Role required to create, view, update and delete records in the Complaint tables.​

</td></tr><tr><td>

CSM - Case Management

</td><td>

sn\_onboarding.admin

</td><td>

Role required to create, view, update and delete records in the Onboarding tables.​

</td></tr><tr><td>

CSM - Case Management

</td><td>

sn\_csm\_ppm.admin

</td><td>

Role required to create, view, update and delete records in the Project Portfolio Management tables.​

</td></tr><tr><td>

CSM - Case Management

</td><td>

sn\_action\_status.admin

</td><td>

Role required to create, view, update and delete records in the Action Status tables.​

</td></tr><tr><td>

CSM - Case Management

</td><td>

sn\_uib\_dyn\_rel\_rec.admin

</td><td>

Role required to create, view, update and delete records in the UIB Dynamic Related Records tables.​

</td></tr><tr><td>

CSM - Case Management

</td><td>

sn\_cs\_sm.admin

</td><td>

Role required to create, view, update and delete records in the Customer Service with Service Management tables.​

</td></tr><tr><td>

CSM - CRM Foundation

</td><td>

sales\_agreement\_admin

</td><td>

Role required to have full access to all sales agreement tables.

</td></tr><tr><td>

CSM - CRM Foundation

</td><td>

service\_contract\_admin

</td><td>

Role required to have full access to all contract tables.

</td></tr><tr><td>

CSM - CRM Foundation

</td><td>

sn\_crm\_customer\_access\_management\_admin

</td><td>

Role required to have admin access to customer access management configuration tables, including related party configurations, responsibility definitions, and responsibility access configurations.

</td></tr><tr><td>

CSM - CRM Foundation

</td><td>

sn\_crm\_escalation\_admin

</td><td>

Role required to have admin access to all escalations and related configuration tables.

</td></tr><tr><td>

CSM - CRM Foundation

</td><td>

sn\_crm\_foundation\_admin

</td><td>

Role required to have admin access to CRM configurations, including escalations, query rules, and customer access management. It also contains sn\_crm\_foundation\_data\_manager role.

</td></tr><tr><td>

CSM - CRM Foundation

</td><td>

sn\_cs\_queryrules.admin

</td><td>

Role required to have admin access to all query rules.

</td></tr><tr><td>

CSM - CRM Foundation

</td><td>

sn\_install\_base.install\_base\_admin

</td><td>

Role required to have granular admin access for Install base and related features.

</td></tr><tr><td>

CSM - CRM Foundation

</td><td>

sn\_l2c\_core.admin

</td><td>

Role required to have full access to Lead to Cash Core metadata tables, modules, and application.

</td></tr><tr><td>

CSM - CRM Foundation

</td><td>

sn\_prm.enterprise\_partner\_admin

</td><td>

Role required to have admin access for partner relationship management.

</td></tr><tr><td>

CSM - CRM Foundation

</td><td>

sn\_crm\_sequence.admin

</td><td>

Role required to give full access to sequence records and its related data.

</td></tr><tr><td>

CSM - CRM Foundation

</td><td>

sn\_l2c\_core.admin

</td><td>

Role required to have full access to Lead to Cash Core metadata tables, modules, and application.

</td></tr><tr><td>

CSM - CRM Foundation

</td><td>

sn\_tmt\_core.admin

</td><td>

Role required to have full access to Sales and Service Core API tables.

</td></tr><tr><td>

CSM - Omni

</td><td>

sn\_openframe.admin

</td><td>

Role required to have granular admin access to Open frame tables and properties.

</td></tr><tr><td>

CSM - Self Service

</td><td>

actsub\_admin

</td><td>

Role required to access Subscription and Activity Feed Framework related tables and modules.

</td></tr><tr><td>

CSM - Self Service

</td><td>

sn\_communities.admin

</td><td>

Role required to access Communities related tables and modules.

</td></tr><tr><td>

CSM - Self Service

</td><td>

sn\_csm\_ec.ec\_admin

</td><td>

Role required to have granular admin access for engagement messenger tables and Rest APIs.

</td></tr><tr><td>

CSM - Self Service

</td><td>

sn\_csm\_walkup.walkup\_admin

</td><td>

Role required to access CSM Walkup Experience tables and modules.

</td></tr><tr><td>

CSM - Self Service

</td><td>

sn\_embeddable\_core.emb\_admin

</td><td>

Role required to have granular admin access for web embeddables admin experience.

</td></tr><tr><td>

CSM - Self Service

</td><td>

sn\_ext\_usr\_reg\_admin

</td><td>

Role required to have granular admin access for External user registration.

</td></tr><tr><td>

CSM - Self Service

</td><td>

sn\_gamification.admin

</td><td>

Role required to access Gamification related tables and modules.

</td></tr><tr><td>

CSM - Self Service

</td><td>

sn\_otp\_support\_util\_admin

</td><td>

Role required to have granular admin access for OTP Support Util.

</td></tr><tr><td>

CSM - Base Entities

</td><td>

csm\_admin

</td><td>

Role required to access to all CSM features and data.

</td></tr><tr><td>

CSM - Base Entities

</td><td>

sn\_res\_shaper.admin

</td><td>

Role required to perform create, update, and delete operations for the Resolution Shaper Config table \(sys\_resolutionshaper\_config\).

</td></tr><tr><td>

CSM - Customer Central

</td><td>

sn\_customer\_central\_admin

</td><td>

Role required to access all Customer Central features and data.

</td></tr><tr><td>

Customer Success Management

</td><td>

sn\_acct\_lc.customer\_success\_application\_admin

</td><td>

Role required to have granular admin access for customer success management tables and server-side access.

</td></tr><tr><td>

Data Streaming

</td><td>

hermes\_admin

</td><td>

Role required to have access for all Hermes related configuration and maintenance.

</td></tr><tr><td>

Data Streaming

</td><td>

idr\_admin

</td><td>

Role required to have access for all IDR related configuration and maintenance.

</td></tr><tr><td>

Data Streaming

</td><td>

data\_mgmt\_tools\_admin

</td><td>

Role required to enable administrators to perform basic Data Management tasks.

</td></tr><tr><td>

Digital End-User Experience

</td><td>

sn\_dex.admin

</td><td>

Role required to manage user access to DEX, manage the applications that are being monitored, and handle onboarding or offboarding-related tasks. Used also to troubleshoot any issues that arise within the application.

</td></tr><tr><td>

Document Intelligence

</td><td>

platform\_ml\_di.admin, sn\_docintel.admin

</td><td>

Role required to have granular admin access for Document Intelligence \(docintel\) capabilities.

</td></tr><tr><td>

Document Management

</td><td>

document\_admin

</td><td>

Role required to manage system properties, security ACLs, and security ACL roles. Manage PDF generation, document conversion and document viewer BASE SYSTEM plugins.

</td></tr><tr><td>

Document Management

</td><td>

platform\_document\_management\_admin

</td><td>

Provides access to perform Create, Read, Update and Delete operations to the Documents, references, versions, lists and list entry tables.

</td></tr><tr><td>

Employee Center Outlook Add-in

</td><td>

sn\_outlook\_addin.outlook\_addin\_setup

</td><td>

Role required to set up and manage the Employee Center Outlook Add-in, including access to the sn\_outlook\_addin.portal.suffix system property, modules, UI actions, and app application files.

</td></tr><tr><td>

Employee Center Pro

</td><td>

sn\_hr\_sp.esc\_admin

</td><td>

Role required to have read and write access to the feedback task table, Employee Center version 37 onwards.

</td></tr><tr><td>

Employee Profile

</td><td>

sn\_employee.admin

</td><td>

Role required to create and manage employee profiles.

</td></tr><tr><td>

Encryption

</td><td>

security\_admin

</td><td>

Role required to perform security operations as an admin.

</td></tr><tr><td>

Encryption

</td><td>

sn\_kmf.admin

</td><td>

Role required to have admin and security admin access to be sn\_kmf.admin. Can assign sn\_kmf.cryptographic\_manager or sn\_kmf.cryptographic\_auditor role to other users and has read, write, and execution permissions for key operations.

</td></tr><tr><td>

Enterprise Architecture

</td><td>

sn\_apm.apm\_admin

</td><td>

Role required to administer Enterprise Architecture features and configurations

</td></tr><tr><td>

Event Management

</td><td>

evt\_mgmt\_admin

</td><td>

Role required to have full access to configure Event Management, including event rules, field mapping, alert management rules, and more.

</td></tr><tr><td>

External Content Connectors

</td><td>

sn\_ext\_conn.xcc\_admin

</td><td>

Role required for management of external content connector configuration settings. Can create, read, update, and delete connectors, schedule and run connector crawls, and view crawl logs and analytics.

</td></tr><tr><td>

Flow Designer UI

</td><td>

flow\_admin

</td><td>

Role required to have admin access for all flow designer tables.

</td></tr><tr><td>

Flow Engines

</td><td>

flow\_admin

</td><td>

Role required to work with backend tables of flow\_designer.

</td></tr><tr><td>

FSC-Accounts Payable Invoice Processing

</td><td>

sn\_ap\_apm.admin

</td><td>

Role required to have admin access for Accounts Payable Invoice Processing.

</td></tr><tr><td>

FSC-Accounts Payable Invoice Processing

</td><td>

sn\_ap\_apm.invoice\_tolerance\_admin

</td><td>

Role required to configure tolerances in Accounts Payable Invoice Processing.

</td></tr><tr><td>

FSC-Accounts Payable Invoice Processing

</td><td>

sn\_ap\_cm.admin

</td><td>

Role required to have admin access for Invoice case management.

</td></tr><tr><td>

FSC - Finance Case Management

</td><td>

sn\_fin\_ops.admin

</td><td>

Role required to access all the features and capabilities of Finance Case Management, including Finance Operations workspace.

</td></tr><tr><td>

FSC - Integrations

</td><td>

sn\_fcms\_intg.admin

</td><td>

Role required to have administrative access for the ERP Integration Framework, inheriting sn\_fcms\_intg.integration\_user and granting admin-level access to manage integration configurations, data, and operations.

</td></tr><tr><td>

FSC - Purchase Order Management

</td><td>

sn\_poem\_core.admin

</td><td>

Role required to have admin access for Purchase Order Management.

</td></tr><tr><td>

FSC - SLO

</td><td>

sn\_slm.admin

</td><td>

This role provides full administrative access to manage supplier-related processes and includes elevated permissions such as`sn_slm.manager`, `decision_table_admin`,`sn_fin.supplier_payment_info_write`,`sn_vdr_risk_asmt.vendor_assessor`, and`sn_shop.shopper`. Users who need complete control over supplier management, vendor assessments, payment information, and related workflows across the SLM application.

</td></tr><tr><td>

FSC - SLO

</td><td>

sn\_kpi.admin

</td><td>

Provides full administrative access to manage and configure all aspects of the KPI Framework, including creating, editing, deleting KPIs, and configuring KPI definitions.

</td></tr><tr><td>

FSC - SPO

</td><td>

sn\_fin.finance\_admin

</td><td>

Role required to generate fiscal and accounting periods.

</td></tr><tr><td>

FSC - SPO

</td><td>

sn\_shop.procurement\_administrator

</td><td>

Role required to access the primary data and administration sections of the Purchase Automation module.

</td></tr><tr><td>

FSC - SPO

</td><td>

sn\_shop.shopping\_hub\_admin

</td><td>

Role required to access all modules of the Source-to-Pay Common Architecture application.

</td></tr><tr><td>

FSC - SPO

</td><td>

sn\_spend\_psd.psd\_admin

</td><td>

Role required to configure and make changes to system properties, such as creating request types and categories.

</td></tr><tr><td>

FSC - SPO

</td><td>

sn\_spend\_sdc.admin

</td><td>

Role required to access Service Task and Service Request tables, which extends to Procurement Case Management, as well as other infrastructure that forms the foundation of Finance and Supply Chain Workflows products.

</td></tr><tr><td>

FSM - Plan Schedule

</td><td>

dynamic\_scheduling\_admin

</td><td>

Role required to perform administration configuration for Dynamic Scheduling Application.

</td></tr><tr><td>

FSM - Plan Schedule

</td><td>

sn\_task\_recommend.task\_rec\_admin

</td><td>

Role required to have granular admin access for Intelligent Task Recommendations \(sn\_task\_recommend\) plugin.

</td></tr><tr><td>

FSM - Plan Schedule

</td><td>

timecard\_admin

</td><td>

Role required to have write access to all time cards, otherwise users only have access to their own timecards.

</td></tr><tr><td>

FSM - Plan Schedule

</td><td>

sn\_task\_grouping.admin

</td><td>

Role required to have admin access for Task Grouping Feature.

</td></tr><tr><td>

FSM - Plan Schedule

</td><td>

wm\_admin

</td><td>

Role required to have admin access for Work Order Management users.

</td></tr><tr><td>

Gen AI Controller

</td><td>

global\_genai\_admin

</td><td>

Role required to have access to certain GenAI tables that are hosted in the global domain.

</td></tr><tr><td>

Grants Management

</td><td>

sn\_gsm\_grnt\_mgmt.grant\_admin

</td><td>

Role required to provide delegated admin access to the Grants Management application.

</td></tr><tr><td>

GRC

</td><td>

sn\_rec\_pg\_vertical.admin

</td><td>

Role required to have admin access for Record - vertical.

</td></tr><tr><td>

GRC - AI Risk and Compliance Management

</td><td>

sn\_ai\_case\_mgmt.ai\_case\_admin

</td><td>

Role required to have admin access for AI Case Management.

</td></tr><tr><td>

GRC - AI Risk and Compliance Management

</td><td>

sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_admin

</td><td>

Role required to have admin access for AI Risk and Compliance Management.

</td></tr><tr><td>

GRC - AI Risk and Compliance Management

</td><td>

sn\_privacy.admin

</td><td>

Role required to be responsible for configuring privacy management solution as a Privacy Admin.

</td></tr><tr><td>

GRC - Corp Compliance

</td><td>

sn\_audit.admin

</td><td>

Role required to have admin access for Audit related plugins.

</td></tr><tr><td>

GRC - Corp Compliance

</td><td>

sn\_compliance.admin

</td><td>

Role required to have admin access for GRC Compliance related plugins.

</td></tr><tr><td>

GRC - Corp Compliance

</td><td>

sn\_grc.admin

</td><td>

Role required to have admin access for GRC core-related plugins.

</td></tr><tr><td>

GRC - Corp Compliance

</td><td>

sn\_grc\_advanced.evidence\_admin

</td><td>

Role required to access Evidence-related objects as a feature role.

</td></tr><tr><td>

GRC - Corp Compliance

</td><td>

sn\_grc\_reg\_change.it\_admin

</td><td>

Role required to have IT admin access for GRC: reg change management plugin and set up integrations with third-party regulatory intelligence providers.

</td></tr><tr><td>

GRC - Corp Compliance

</td><td>

sn\_grc\_taxonomy.taxonomy\_admin

</td><td>

Role required to have admin access for GRC: Taxonomy.

</td></tr><tr><td>

GRC - Formula builder

</td><td>

sn\_fb\_connected.admin

</td><td>

Role required to have admin access for formula builder application.

</td></tr><tr><td>

GRC - Operational resilience

</td><td>

sn\_oper\_res.admin

</td><td>

Role required to create and delete some operational resilience activities.

</td></tr><tr><td>

GRC - Operational resilience

</td><td>

sn\_oper\_res.irm\_opres\_admin

</td><td>

Role required to create and delete both operational resilience activities and IRM activities.

</td></tr><tr><td>

HRSD - Case and Knowledge Management

</td><td>

sn\_hr\_core.admin

</td><td>

Role required to have full HR administrator access — can configure all HR settings, assign roles, and access all HR data.

</td></tr><tr><td>

HRSD - Case and Knowledge Management

</td><td>

sn\_hr\_er.admin

</td><td>

Role required tohave full administrator access to ER module configuration, case management, and setup.

</td></tr><tr><td>

HRSD - Case and Knowledge Management

</td><td>

sn\_em.admin

</td><td>

Role required to access and configure all areas within Evidence Management.

</td></tr><tr><td>

HRSD - Case and Knowledge Management

</td><td>

sn\_interview\_temp.admin

</td><td>

Role required to access, read, create, and edit interview question templates, template tags, and Employee Relations properties.

</td></tr><tr><td>

HRSD - Case and Knowledge Management

</td><td>

sn\_hr\_ef.admin

</td><td>

Role required to assign EDM roles, search, read, create, or update employee documents, and manage administration including retention periods, retention policies, security policies, and document types

</td></tr><tr><td>

HRSD - Case and Knowledge Management

</td><td>

sn\_sp\_admin\_ws.admin

</td><td>

Role required to access workspace and see a consolidated view of the demand and consumption of services offered to customers.

</td></tr><tr><td>

HRSD - Case and Knowledge Management

</td><td>

sn\_hr\_ra.admin

</td><td>

Role required to configure HR related Recommended Context tables to show different recommendations in HR Agent

</td></tr><tr><td>

HRSD - Employee Journey Management

</td><td>

sn\_ja.admin

</td><td>

Role required to create and manage all Journey Accelerator components, tables, and data.

</td></tr><tr><td>

HRSD - Employee Journey Management

</td><td>

sn\_hr\_le.admin

</td><td>

Role required to create, manage, and add users to groups within Lifecycle Events.

 Can access:

 -   Guided Setup
-   Manage Owner Groups
-   Manage Roles
-   LE UI Configuration
-   Onboarding Executive Dashboard
-   Onboarding Executive View

</td></tr><tr><td>

HRSD - Employee Journey Management

</td><td>

sn\_hr\_le\_pa.admin

</td><td>

Lifecycle Events Performance Analytics Admin role for the scoped application.

 -   Access and modify the Lifecycle Events PA content packs.
-   Edits Performance Analytics properties.
-   Accesses Admin Console.
-   Launch Dependency Assessment.

</td></tr><tr><td>

HRSD - Employee Journey Management

</td><td>

sn\_jny.admin

</td><td>

Role required to create and manage all Journey designer and Journey Accelerator configurations and features.

</td></tr><tr><td>

HRSD-Employee Journey Management

</td><td>

sn\_ja.admin

</td><td>

Role required to create and manage all Journey Accelerator components, tables, and data.

</td></tr><tr><td>

HRSD-Employee Journey Management

</td><td>

sn\_hr\_le.admin

</td><td>

Role required to create, manage, and add users to groups within Lifecycle Events.

 Can access:

 -   Guided Setup
-   Manage Owner Groups
-   Manage Roles
-   LE UI Configuration
-   Onboarding Executive Dashboard
-   Onboarding Executive View

</td></tr><tr><td>

HRSD-Employee Journey Management

</td><td>

sn\_hr\_le\_pa.admin

</td><td>

Lifecycle Events Performance Analytics Admin role for the scoped application.

 -   Access and modify the Lifecycle Events PA content packs.
-   Edits Performance Analytics properties.
-   Accesses Admin Console.
-   Launch Dependency Assessment.

</td></tr><tr><td>

HRSD-Employee Journey Management

</td><td>

sn\_jny.admin

</td><td>

Role required to create and manage all Journey designer and Journey Accelerator configurations and features.

</td></tr><tr><td>

HRSD - Hiring Experiences

</td><td>

sn\_ta\_hiring\_core.admin

</td><td>

Role required to have super admin access to the Hiring Experiences environment.

</td></tr><tr><td>

HRSD - Hiring Experiences

</td><td>

sn\_ta\_tp.talent\_profile\_admin

</td><td>

Role required to have admin access to set up Talent Profile.

</td></tr><tr><td>

HRSD - Talent Experience

</td><td>

sn\_egd\_core.admin

</td><td>

Role required to have admin access for talent development core.

</td></tr><tr><td>

HRSD - Talent Experience

</td><td>

sn\_egd\_shared\_lib.admin

</td><td>

Role required to have admin access for the shared library across HR.

</td></tr><tr><td>

HRSD - Talent Experience

</td><td>

sn\_hr\_lm.admin

</td><td>

Role required to track HR license usage by customer as an admin.

</td></tr><tr><td>

HRSD - Talent Experience

</td><td>

sn\_td\_na.admin

</td><td>

Role required to have admin access for Now Assist for talent.

</td></tr><tr><td>

Health and Safety

</td><td>

sn\_ohs\_im.admin

</td><td>

Role required to have admin access for Health and Safety applications.

</td></tr><tr><td>

Identity

</td><td>

agent\_role\_config\_admin

</td><td>

Role required to access and modify Agent role configurations \(role masking\).

</td></tr><tr><td>

Identity

</td><td>

mi\_admin

</td><td>

Role required to have admin access for Machine Identity Console. It's a high privilege as it contains other admin roles, assign carefully.

</td></tr><tr><td>

Identity

</td><td>

privileged\_role\_config\_admin

</td><td>

Role required to configure which roles are designated as privileged in the system.

</td></tr><tr><td>

Identity

</td><td>

role\_delegator\_admin

</td><td>

Role required to have admin access for Role delegation feature.

</td></tr><tr><td>

Identity

</td><td>

scim\_client\_config\_admin

</td><td>

Role required to access and modify SCIM client configurations.

</td></tr><tr><td>

Identity

</td><td>

scim\_config\_admin

</td><td>

Role required to access and modify SCIM provider-related configurations such as SCIM extension schema and SCIM system properties.

</td></tr><tr><td>

IH Core

</td><td>

connection\_admin

</td><td>

Role required to have access to Connections \[sys\_connection\] and Credentials \[discovery\_credentials\] table.

</td></tr><tr><td>

IH Core

</td><td>

credential\_admin

</td><td>

Role required to have access to Credentials \[discovery\_credentials\] table.

</td></tr><tr><td>

IH Core

</td><td>

ih\_process\_sync\_admin

</td><td>

Role required to create, edit, or delete Process Sync related tables.

</td></tr><tr><td>

Industrial Connected Workforce

</td><td>

sn\_icw.application\_admin

</td><td>

Role required to have application admin access for Industrial Connected Workforce.

</td></tr><tr><td>

Inbound web services

</td><td>

web\_service\_admin

</td><td>

Role required for administrative access to create Scripted REST and GraphQL operations.

</td></tr><tr><td>

Inbound web services

</td><td>

web\_service\_configuration\_admin

</td><td>

Role required to manage Web Service configurations for REST, GraphQL, and SOAP services, including behavior and security settings. To learn more, see Web Service configurations.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_appss.admin

</td><td>

Role required to create, update, delete, and read request types, inputs, outputs, and definitions.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_bom.admin

</td><td>

Role required to have access to all the banking data entities, plus admin privileges as the banking admin.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_bom.service\_definition\_admin

</td><td>

Role required to have full access to the service definition records as the FSO service definition admin.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_bom\_clo\_b2b.admin

</td><td>

Role required to have access to all Business customers' life-cycle operations data and admin privileges.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_bom\_clo\_b2c.admin

</td><td>

Role required to have access to all personal customers life-cycle operations data and admin privileges related to personal customers life-cycle operations.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_bom\_compl.admin

</td><td>

Role required to have access to all complaint operations data and admin privileges as the Financial Services Complaint Admin.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_bom\_credit\_asmt.admin

</td><td>

Role required to have access to all credit assessment data and admin privileges.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_bom\_credit\_card.admin

</td><td>

Role required to have access to all credit card service tasks and admin privileges.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_bom\_deposit\_b2b.admin

</td><td>

Role required to have access to all Business Deposit Operations data and admin privileges.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_bom\_deposit\_b2c.admin

</td><td>

Role required to have access to all personal deposit operations data and admin privileges.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_bom\_fraud.admin

</td><td>

Role required to have access to all Fraud Operations data and admin privileges.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_bom\_kyc.admin

</td><td>

Role required to have access to all Business KYC operations data and admin privileges.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_bom\_loan.b2c\_admin

</td><td>

Role required to have access to all loan operations data and admin privileges.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_bom\_loan\_b2b.admin

</td><td>

Role required to have access to all Business loan operations data and admin privileges.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_bom\_pa.admin

</td><td>

Role required to have access to all the banking data entities as the performance analytics admin, plus admin privileges.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_bom\_payment.admin

</td><td>

Role required to have access to all payment operations data and admin privileges.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_bom\_po.admin

</td><td>

Role required to have admin privileges.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_bom\_remote.admin

</td><td>

Role required to have access to all remote data and admin privileges as the FSO Remote Tables and Lookup Admin.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_bom\_treasury.admin

</td><td>

Role required to have access to all treasury operations data and admin privileges related to treasury operations.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_data\_sec.admin

</td><td>

Role required to have access to the Tokenizer Resource Configuration table and admin privileges.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_doc\_processor.admin

</td><td>

Role required to have access to all document entities and admin privileges.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_evnt\_inq.admin

</td><td>

Role required to have admin access for Event Inquiry.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_fso\_intg\_friss.admin

</td><td>

Role required to manage the flows for FRISS integration.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_fso\_intg\_jha.admin

</td><td>

Role required to manage the flows for JHA integration.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_ins\_claim.admin

</td><td>

Role required to have access to all Insurance Claims Core tables and admin privileges.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_ins\_claim\_cml.admin

</td><td>

Role required to have access to all Commercial claim operations data and admin privileges.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_ins\_claim\_indl.admin

</td><td>

Role required to have access to all Individual Life claim operations data and admin privileges.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_ins\_claim\_pers.admin

</td><td>

Role required to have access to all Personal claim operations data and admin privileges.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_ins\_gen\_claim.admin

</td><td>

Role required to have access to all Insurance claims operations data and admin privileges.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_ins\_group\_life.admin

</td><td>

Role required to have access to all Group Life and Disability Servicing data and admin privileges.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_ins\_group\_uw.admin

</td><td>

Role required to have access to all Group Life and Disability Underwriting operations data and admin privileges.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_ins\_indiv\_life.admin

</td><td>

Role required to have access to all Individual Life Servicing operations data and admin privileges.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_ins\_indiv\_uw.admin

</td><td>

Role required to have access to all individual life insurance underwriting operations data and admin privileges.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_ins\_policy\_b2b.admin

</td><td>

Role required to have access to all Commercial policy operations data and admin privileges.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_ins\_policy\_b2c.admin

</td><td>

Role required to have admin access for Personal lines policy cases.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_ins\_siu.admin

</td><td>

Role required to have access to all SIU data and admin privileges.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_ins\_underwrite.admin

</td><td>

Role required to have access to all insurance underwriting operations data and admin privileges.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_ins\_uw\_b2b.admin

</td><td>

Role required to have access to all Insurance commercial underwriting operations data and admin privileges.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_jha\_spoke.admin

</td><td>

Role required to have admin access for JHA.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_payment\_card.admin

</td><td>

Role required to create, read, write, and delete Payment Card records.

</td></tr><tr><td>

Industry Banking

</td><td>

sn\_req\_criteria.admin

</td><td>

Role required to have access to all the service request criteria data entities as the admin.

</td></tr><tr><td>

Information Request Playbook

</td><td>

sn\_gsm\_info\_req.admin

</td><td>

Role required to provide delegated admin access to the Information Request Playbook application.

</td></tr><tr><td>

IntegrationHub - Finance and Operations Spoke

</td><td>

sn\_ms\_fin\_ops\_spk.admin

</td><td>

Role required to have admin access for the Microsoft Dynamics 365 for Finance and Operations Spoke.

</td></tr><tr><td>

IntegrationHub - Finance and Operations Spoke

</td><td>

sn\_onedrive\_spoke.Microsoft\_OneDrive\_Admin

</td><td>

Role required to have admin access for the Microsoft Dynamics 365 for Finance and Operations Spoke.

</td></tr><tr><td>

IntegrationHub - Finance and Operations Spoke

</td><td>

sn\_uipath\_spoke.uipath\_admin

</td><td>

Role required to have admin access for UiPath spoke tables.

</td></tr><tr><td>

ITAM

</td><td>

asset\_licensing\_admin

</td><td>

Role required to have granular admin access for ITAM licensing capabilities.

</td></tr><tr><td>

ITAM

</td><td>

asset\_recommendation\_admin

</td><td>

Role required to have granular admin access for Recommendations capabilities.

</td></tr><tr><td>

ITAM

</td><td>

asset\_system\_admin

</td><td>

Role required to have granular admin access for Asset management capabilities.

</td></tr><tr><td>

ITAM

</td><td>

asset\_task\_admin

</td><td>

Role required to have access to create and delete for asset task table.

</td></tr><tr><td>

ITAM

</td><td>

contract\_system\_admin

</td><td>

Role required to have granular admin access for Contract capabilities.

</td></tr><tr><td>

ITAM

</td><td>

procurement\_system\_admin

</td><td>

Role required to have granular admin access for Procurement capabilities.

</td></tr><tr><td>

ITAM - CCM

</td><td>

sn\_cld\_intg\_core.cloud\_integrations\_admin

</td><td>

Role required to configure Billing Download jobs and Price Sheet Download jobs.

</td></tr><tr><td>

ITAM - CCM

</td><td>

sn\_cld\_intg\_core.read

</td><td>

Role required to give access to all the persons for a specific table \(this is strictly for internal purpose and won’t be exposed to the customer\).

</td></tr><tr><td>

ITAM - CCM

</td><td>

sn\_cld\_spend\_core.spend\_admin

</td><td>

Role required to have access to spend dashboards and tables.

</td></tr><tr><td>

ITAM - CCM

</td><td>

sn\_clin\_core.insights\_admin

</td><td>

Role required to have complete access to whole application as a super user and access to modify scripts and flows.

</td></tr><tr><td>

ITAM - EAM

</td><td>

sn\_eam.enterprise\_admin

</td><td>

Role required to have access to entire enterprise application.

</td></tr><tr><td>

ITAM - EAM

</td><td>

asset\_aia\_admin

</td><td>

Role required to have access to ITAM agents capabilities.

</td></tr><tr><td>

ITAM - EAM

</td><td>

asset\_integration\_admin

</td><td>

Role required to have access to integration capabilities.

</td></tr><tr><td>

ITAM - HAM

</td><td>

asset\_aia\_admin

</td><td>

Role required to have access to ITAM agents capabilities.

</td></tr><tr><td>

ITAM - HAM

</td><td>

asset\_integration\_admin

</td><td>

Role required to have access to integration capabilities.

</td></tr><tr><td>

ITAM - HAM

</td><td>

sn\_hamp.ham\_system\_admin

</td><td>

Role required to have granular admin access for Advanced Shipment Notification \(ASN\).

</td></tr><tr><td>

ITAM - SAM

</td><td>

sam\_admin

</td><td>

Role required to have access to the entire Software Asset Management application.

</td></tr><tr><td>

ITAM - SAM

</td><td>

sam\_integrator

</td><td>

Role required to create and manage SaaS integration profiles.

</td></tr><tr><td>

ITOM - Agent Framework

</td><td>

agent\_client\_collector\_admin

</td><td>

Role required to have admin privileges for management of the agent client collector store application.

</td></tr><tr><td>

ITOM - CA

</td><td>

sn\_\_itom\_ccg.admin

</td><td>

Role required to have admin access for Cloud Configuration Governance set of apps.

</td></tr><tr><td>

ITOM - Cloud Configuration Governance

</td><td>

sn\_cmp.cloud\_root\_admin

</td><td>

Role required to have admin access for Cloud Provisioning and Governance set of Apps.

</td></tr><tr><td>

ITOM - Cloud Configuration Governance

</td><td>

sn\_itom\_cam.cw\_admin

</td><td>

Role required to have admin access for Cloud Workspace Application.

</td></tr><tr><td>

ITOM - Certificate Inventory and Management

</td><td>

sn\_disco\_certmgmt.pki\_admin

</td><td>

Role required to have granular admin access for Certificate Inventory and Management.

</td></tr><tr><td>

ITOM - Certificate Inventory and Management

</td><td>

sn\_disco\_firewall.firewall\_admin

</td><td>

Role required to change non-standard attributes \(not present in the original firewall\) for a firewall record like, status, purpose, etc. The attributes present in the firewall are immutable.

</td></tr><tr><td>

ITOM - Certificate Inventory and Management

</td><td>

sn\_itom\_licensing.admin

</td><td>

Role required to configuration access for ITOM/OT SU Licensing.

</td></tr><tr><td>

ITOM - Tag Governance

</td><td>

sn\_itom\_tag.tag\_governance\_admin

</td><td>

Role required to have granular configuration access for Tag Governance.

</td></tr><tr><td>

ITOM - Discovery

</td><td>

discovery\_admin

</td><td>

Role required to access the "Discovery" and "Discovery Definition" applications to configure, monitor, and run Discovery operations.

</td></tr><tr><td>

ITOM - Leap

</td><td>

sn\_itom\_leap.leap\_admin

</td><td>

Role required to have admin access to leap application, enabling users to activate skills and create artifacts.

</td></tr><tr><td>

ITSM - FE

</td><td>

sn\_sow\_admin.sn\_sow\_admin

</td><td>

Role required to oversee service operations workspace-related configurations as `sn_sow_admin` and help customer admin to configure product features and maintain organizational policies.

</td></tr><tr><td>

ITSM - Incident Management

</td><td>

sn\_incident\_admin

</td><td>

Role required to configure all Incident Management features including incident management properties.

</td></tr><tr><td>

ITSM - Major Incident Management

</td><td>

sn\_mim\_admin

</td><td>

Role required to configure all Major Incident Management features including major incident properties and trigger rules.

</td></tr><tr><td>

ITSM - Incident Communications Management

</td><td>

sn\_iam\_admin

</td><td>

Role required to configure all Incident Communications Management features including creating, editing, or canceling incident communication plan, communication task, and managing contact information. Additionally, this role can administrate all Incident Communications Management capabilities.

</td></tr><tr><td>

ITSM - Contact Management

</td><td>

sn\_contact\_admin

</td><td>

Role required to configure all Contact Management features including creating and editing contact definitions, contact responsibilities, configuration of MI users, recipient lists, and groups.

</td></tr><tr><td>

ITSM - Task Communications Management

</td><td>

sn\_tcm\_admin

</td><td>

Role required to configure all Task Communications Management features including communication plans and tasks.

</td></tr><tr><td>

ITSM - Task Outage

</td><td>

sn\_task\_outage\_admin

</td><td>

Role required to configure all Task Outage features including the mapping between the Task \[task\] table and the Outage \[cmdb\_ci\_outage\] table.

</td></tr><tr><td>

ITSM - Change Management

</td><td>

sn\_change\_admin

</td><td>

Role required to configure Change Management features and system properties.

</td></tr><tr><td>

Journey Accelerator

</td><td>

sn\_ja.admin

</td><td>

Role required to create and manage all Journey Accelerator components, tables, and data.

</td></tr><tr><td>

Journey Designer

</td><td>

sn\_jny.admin

</td><td>

Role required to create and manage all Journey designer and Journey Accelerator configurations and features.

</td></tr><tr><td>

Key Management Framework

</td><td>

sn\_kmf.admin

</td><td>

Role required to assigns roles to other users to perform operations around the ServiceNow Key Management Framework.

</td></tr><tr><td>

Knowledge management

</td><td>

knowledge\_Admin

</td><td>

Role required to have admin access for Knowledge management.

</td></tr><tr><td>

Lifecycle Events

</td><td>

sn\_hr\_le.admin

</td><td>

Role required to create, manage, and add users to groups within Lifecycle Events.

</td></tr><tr><td>

Localization Framework

</td><td>

localization\_admin

</td><td>

Role that manages the Localization Framework application. This role is also used in Localization Workspace.

</td></tr><tr><td>

LSD - Legal Request Management

</td><td>

sn\_lg\_ops.legal\_admin

</td><td>

Role required for administrative access to all legal apps and the underlying data.

</td></tr><tr><td>

LSD - Legal Request Management

</td><td>

sn\_lg\_ops.request\_admin

</td><td>

Role required for administrative access to the Legal Request module with full access to data.

</td></tr><tr><td>

LSD - Legal Request Management

</td><td>

sn\_lg\_ops.legal\_assignment\_rules\_admin

</td><td>

Role required for administrative access to the Assignment Rules module in legal apps.

</td></tr><tr><td>

LSD - Legal Request Management

</td><td>

sn\_lg\_ops.legal\_catalog\_admin

</td><td>

Role required for administrative access to the Catalog administration module in legal apps.

</td></tr><tr><td>

LSD - Legal Request Management

</td><td>

sn\_lg\_ops.legal\_notification\_admin

</td><td>

Role required for administrative access to the Notifications module in legal apps to configure email notifications.

</td></tr><tr><td>

LSD - Legal Matter Management

</td><td>

sn\_lg\_matter.matter\_admin

</td><td>

Role required for the administrative access to legal matters and the underlying data.

</td></tr><tr><td>

LSD - Legal Content Review

</td><td>

sn\_lg\_cont\_review.admin

</td><td>

Role required for administrative access to the Legal Content Review feature and its underlying data.

</td></tr><tr><td>

LSD - Legal Digital Forensics

</td><td>

sn\_lg\_forensics.forensics\_admin

</td><td>

Role required for administrative access to the Legal Digital Forensics app and full access to the underlying data.

</td></tr><tr><td>

LSD - Legal Investigations

</td><td>

sn\_lg\_investigate.admin

</td><td>

Role required for administrative access to the Legal Investigations app and full access to the underlying data.

</td></tr><tr><td>

LSD - Legal Simple Privacy

</td><td>

sn\_lg\_simple\_priva.privacy\_admin

</td><td>

Role required for administrative access to the Legal Simple Privacy app and full access to the underlying data.

</td></tr><tr><td>

LSD - Gifts and Entertainment Compliance

</td><td>

sn\_lg\_gifts.gifts\_admin

</td><td>

Role required for administrative access to the Gifts &amp; Entertainment app and full access to the underlying data.

</td></tr><tr><td>

LSD - Legal Conflict of Interest

</td><td>

sn\_lg\_coi.coi\_admin

</td><td>

Role required for administrative access to the Legal Conflict of Interest app and full access to the underlying data.

</td></tr><tr><td>

LSD - Legal Hold Notification

</td><td>

sn\_Ig\_hold.legal\_hold\_admin

</td><td>

Role required for administrative access to the Legal Hold Notification app and full access to the underlying data.

</td></tr><tr><td>

LSD - Now Assist for Legal Service Delivery

</td><td>

sn\_lg\_gen\_ai.admin

</td><td>

Role required for administrative access to the Now Assist for Legal Service Delivery application.

</td></tr><tr><td>

LSD - Contract Management Pro for Legal Service Delivery

</td><td>

sn\_lg\_cnt.contract\_admin

</td><td>

Role required for administrative access to the Contract Management Pro for Legal Service Delivery app and full access to the underlying data.

</td></tr><tr><td>

LSD - Advanced Work Assignment for Legal Service Delivery

</td><td>

sn\_lg\_awa.admin

</td><td>

Role required for administrative access to the Advanced Work Assignment for for Legal Service Delivery applications.

</td></tr><tr><td>

LSD - Legal Counsel Center

</td><td>

sn\_lg\_cf\_workspace.admin

</td><td>

Role required to change the Legal Counsel Center Workspace for Legal Request Management to fit into the business or user requirements.

</td></tr><tr><td>

LSD - External Legal Service Center

</td><td>

sn\_lg\_ext\_portal.ext\_admin

</td><td>

Role required for administrative access to the External Legal Service Centre application and full access to underlying data.

</td></tr><tr><td>

LSD - Legal and Contracts Common Utilities

</td><td>

sn\_lco\_cmn.admin

</td><td>

Role required for administrative access to Legal and Contracts Common Utilities records.

</td></tr><tr><td>

Mobile

</td><td>

mobile\_admin

</td><td>

Role required to configure mobile applications.

</td></tr><tr><td>

Notification

</td><td>

email\_admin

</td><td>

Role required to perform resend email and reprocess inbound email functionality.

</td></tr><tr><td>

Notification

</td><td>

email\_bounce\_admin

</td><td>

Role required to administer email bounce functionality.

</td></tr><tr><td>

Notification

</td><td>

email\_digest\_admin

</td><td>

Role required to monitor email digest.

</td></tr><tr><td>

Notification

</td><td>

notification\_admin

</td><td>

Role required to configure notifications.

</td></tr><tr><td>

Notification

</td><td>

notification\_category\_admin

</td><td>

Role required to configure notification category.

</td></tr><tr><td>

Notification

</td><td>

notification\_classification\_admin

</td><td>

Role required to configure notification classification.

</td></tr><tr><td>

Notification

</td><td>

portal\_notification\_pref\_admin

</td><td>

Role required to configure sys\_recipient\_user\_mapping table.

</td></tr><tr><td>

Notification

</td><td>

push\_admin

</td><td>

Role required to manage push notifications.

</td></tr><tr><td>

Notification

</td><td>

smime\_certificate\_admin

</td><td>

Role required to administer SMIME public certificate.

</td></tr><tr><td>

Notify

</td><td>

notify\_setup\_admin

</td><td>

Role required to configure Notify features and system properties.

</td></tr><tr><td>

Now Assist - CSM

</td><td>

sn\_customerservice\_agent

</td><td>

Role required to enable Now Assist for CSM Gen AI skills for customer service agents. It grants access to all Now Assist for CSM skills such as Generate Resolution Notes, Case Summarization, and Chat Summarization.

</td></tr><tr><td>

Now Assist - CSM

</td><td>

sn\_customerservice.consumer\_agent

</td><td>

Role required to enable Now Assist for CSM Gen AI skills for customer service agents. It grants access to all Now Assist for CSM skills such as Generate Resolution Notes, Case Summarization, and Chat Summarization.

</td></tr><tr><td>

Now Assist for HR Service Delivery

</td><td>

sn\_hr\_gen\_ai.admin

</td><td>

Role required to configure and manage Now Assist for HR Service Delivery.

</td></tr><tr><td>

Now Assist for HR Service Delivery

</td><td>

sn\_hr\_ai\_agents.admin

</td><td>

Role required to configure and manage the HR Service Delivery AI Agent collection.

</td></tr><tr><td>

Now Assist for HR Service Delivery

</td><td>

sn\_hr\_aia\_voice.admin

</td><td>

Role required to configure and manage voice agents in the HR Service Delivery AI Agent collection.

</td></tr><tr><td>

Now Assist - TMT

</td><td>

sn\_tmt\_agentic\_ai.app\_admin

</td><td>

Role required to manage the Telecommunications Media and Technology AI agent collection.

</td></tr><tr><td>

Now Assist for Vulnerability Response

</td><td>

aia-admin

</td><td>

Role required for administrative access to Now Assist for Vulnerability Response.

</td></tr><tr><td>

On-Call Scheduling

</td><td>

sn\_on\_call\_admin

</td><td>

Role required to configure On-Call Scheduling features and system properties.

</td></tr><tr><td>

Operational Technology - CMDB

</td><td>

cmdb\_ot\_admin

</td><td>

Role required to manage all OT CMDB tables and records as an admin.

</td></tr><tr><td>

Operational Technology - ISA

</td><td>

cmdb\_ot\_isa\_admin

</td><td>

Role required to manage all ISA Equipment Model records and Equipment Model Template records as an admin.

</td></tr><tr><td>

Operational Technology - Industrial Process Health

</td><td>

ot\_health\_admin

</td><td>

Role required to have admin access to Industrial process health application and related functions.

</td></tr><tr><td>

Operational Technology - Subnet Mapping

</td><td>

sn\_ot\_amazing\_admin

</td><td>

Role required to manage OT Subnet Mapping records in 'ot\_subnet\_mapping' table and OT Subnet Mapping properties as an admin.

</td></tr><tr><td>

Operational Technology - Change Management

</td><td>

sn\_ot\_change\_admin

</td><td>

Role required to have admin access to the OT Change Management Application and related functions.

</td></tr><tr><td>

Operational Technology - Incident Management

</td><td>

sn\_ot\_incident\_admin

</td><td>

Role required to have admin access to the OT Incident Management Application and related functions.

</td></tr><tr><td>

Operational Technology - Vulnerability Integration

</td><td>

sn\_otvr.integration\_admin

</td><td>

Role required to have admin access for OT Vulnerability Integration application.

</td></tr><tr><td>

Operational Technology - Risk Score Calculator application

</td><td>

sn\_risk\_score\_calc.admin

</td><td>

Role required to have admin access to Risk Score Calculator application and related functions.

</td></tr><tr><td>

Outlook Actionable Messages integration

</td><td>

oam\_admin

</td><td>

Role required to access and manage Outlook Actionable Messages configurations, including system properties and OAM definitions.

</td></tr><tr><td>

Password policy

</td><td>

password\_policy\_admin

</td><td>

Role required to configure password policy-related items.

</td></tr><tr><td>

Password Reset

</td><td>

password\_reset\_admin

</td><td>

Role required to configure Password Reset features and system properties.

</td></tr><tr><td>

Platform

</td><td>

source\_control\_admin

</td><td>

Role required to perform all source control functionality.

</td></tr><tr><td>

Platform

</td><td>

update\_set\_admin

</td><td>

Role required to create, delete, and manage Update Sets.

</td></tr><tr><td>

Platform

</td><td>

cds\_client\_admin

</td><td>

Role required to have admin access for client-side framework of Canonical Data Services \(CDS\).

</td></tr><tr><td>

Platform

</td><td>

cluster\_node\_admin

</td><td>

Role required to have admin access for instance node and cluster configuration \(VNCC\) related tables.

</td></tr><tr><td>

Platform

</td><td>

nds\_admin

</td><td>

Role required to have admin access for Normalization Data Services.

</td></tr><tr><td>

Platform

</td><td>

normalizer

</td><td>

Role required to have admin access for Field Normalization feature.

</td></tr><tr><td>

Platform Server - Side Scripting

</td><td>

script\_include\_admin

</td><td>

Role required to have granular access to sys\_script\_include.

</td></tr><tr><td>

Platform Server - Side Scripting

</td><td>

sys\_es\_latest\_script\_admin

</td><td>

Role required to have granular access to sys\_es\_latest\_script.

</td></tr><tr><td>

Platform Server - Side Scripting

</td><td>

sysevent\_script\_action\_admin

</td><td>

Role required to have granular access to sysevent\_script\_action\_admin.

</td></tr><tr><td>

Platform Data Fabric

</td><td>

df\_connection\_admin

</td><td>

Role required to establish connection to available data sources as a connection admin, and manage access to these connections for data steward users.

</td></tr><tr><td>

Platform Deployment Analyzer

</td><td>

deployment\_analyzer\_admin

</td><td>

Role required to access Deployment Analyzer tables to set up and see results for Deployment Analyzer. Doesn’t have access to create script includes.

</td></tr><tr><td>

Platform Dev Sandbox

</td><td>

sandbox\_manager

</td><td>

Role required to manage the life-cycle of all developer sandboxes as a Sandbox Manager.

</td></tr><tr><td>

Platform Event Processing

</td><td>

events\_admin

</td><td>

Role required to be a System Events administrator involved in the events processing feature of the system.

</td></tr><tr><td>

Platform ISM

</td><td>

response\_header\_admin

</td><td>

Role required to have read, write, create, delete, and list\_edit access for records in HTTP Response Header table \(sys\_response\_header\).

</td></tr><tr><td>

Platform Scheduler

</td><td>

app\_resource\_quota\_admin

</td><td>

Role required to configure and manage Application Resource Quotas plugin.

</td></tr><tr><td>

Platform Scheduler

</td><td>

business\_calendar\_admin

</td><td>

Role required to configure and manage plugins and features related to business calendars \(com.glide.business\_calendars, com.glide.business\_calendars.scheduled\_jobs\).

</td></tr><tr><td>

Platform Scheduler

</td><td>

system\_scheduler\_admin

</td><td>

Role required to configure and manage scheduler-related plugins and features \(com.glide.system\_scheduler, com.snc.automation, com.snc.automation\_time\_zone, com.glide.stats.scheduler\) and access Scheduled Jobs dashboard in System Events and Jobs Dashboard plugin \(com.sn\_async\_dashboard\).

</td></tr><tr><td>

Plato Predictive Intelligence

</td><td>

ml\_admin

</td><td>

Role required to have access to create and retrain classification, similarity, and clustering models.

</td></tr><tr><td>

Playbook

</td><td>

playbook.admin

</td><td>

Role required to have Playbook Admin access. Contains pd\_content\_author, pd\_operator, pd\_trigger\_author, pd\_author, playbook.localization, and pd\_cancel.

</td></tr><tr><td>

Proactive Prompts

</td><td>

sn\_pp.admin

</td><td>

Role required to create and manage all Proactive Prompts configurations and features.

</td></tr><tr><td>

Process Mining

</td><td>

sn\_process\_mining\_admin

</td><td>

Role required to have admin access only for Process Mining workspace and can do certain actions limited to process mining only.

</td></tr><tr><td>

Public Sector Digital Services

</td><td>

sn\_gsm.admin

</td><td>

Role required to provide delegated admin access to scoped applications built on the Public Sector Digital Services platform.

</td></tr><tr><td>

Role delegation

</td><td>

role\_delegator\_admin

</td><td>

Role required for role delegation.

</td></tr><tr><td>

Roles

</td><td>

user\_role\_history\_admin

</td><td>

Role required to manage perform specific role related operations.

</td></tr><tr><td>

Retail

</td><td>

sn\_retail.ro\_admin

</td><td>

Role required to create retail organization and add members to the organization.

</td></tr><tr><td>

SBOM

</td><td>

sn\_sbom\_core.admin

</td><td>

Role required to create, read, edit data, and upload Software Bill of Materials \[SBOMs\]. This role is required for access to the SBOM Core modules in your instance. It inherits the roles from the Data Model for SBOM application.

</td></tr><tr><td>

Search

</td><td>

ais\_admin

</td><td>

Role required to administrate and configure AI Search functionality. Includes Search Applications, Search Profiles, Search Sources, Indexed Sources, and Properties necessary for administrating and configuring AI Search.

</td></tr><tr><td>

Search

</td><td>

ts\_admin

</td><td>

Role required to administrate and configure text search on an instance, enabling adjusting of ts\_weights and viewing or changing properties necessary for Text Search Administration.

</td></tr><tr><td>

Search UX

</td><td>

ais\_admin

</td><td>

Role required to migrate admin ACLs to a more granular role for ai-search-admin, semantic\_search, com.glide.search.analytics, com.glide.search.signal\_data, and com.glide.signals.

</td></tr><tr><td>

Security Center

</td><td>

sn\_vsc.security\_center\_admin

</td><td>

Role required to have admin access for Security center store application.

</td></tr><tr><td>

Security Operations - Data Loss Prevention

</td><td>

sn\_dlir.admin

</td><td>

Role required for administrative access to the Data Loss Prevention application.

</td></tr><tr><td>

Security Operations - Security Incident Response integrations

</td><td>

sn\_si.ingestion\_profile\_admin

</td><td>

Role required to configure the plugin and to create, edit, delete, and maintain ingestion profiles.

 -   Microsoft Azure Sentinel integration
-   Splunk Enterprise Security Event Ingestion integration
-   Splunk Enterprise Event Ingestion integration
-   Cortex XSIAM by Palo Alto Networks
-   Microsoft Defender integration
-   CrowdStrike Next-Gen SIEM integration

</td></tr><tr><td>

Security Operations - Security Incident Response

</td><td>

sn\_si.admin

</td><td>

Role required for administrative access to the Security Incident Response application.

</td></tr><tr><td>

Security Operations - Now Assist for Security Incident Response

</td><td>

sn\_si.admin

</td><td>

Role required for administrative access to the Now Assist for Security Incident Response application.

</td></tr><tr><td>

Security Operations - Threat Intelligence Security Center

</td><td>

sn\_sec\_tisc.admin

</td><td>

Role required for administrative access to the Threat Intelligence Security Center application.

</td></tr><tr><td>

Security Posture Control

</td><td>

SPC Admin Group

</td><td>

Group required for full read and write access to all the records for Security Posture Control, including licensing information. Granular roles for this group include: \[sn\_sec\_caasm.analyst, sn\_sec\_caasm.caasm\_security\_admin, and sn\_sec\_spc\_core.configure\].

</td></tr><tr><td>

Service Applicant Information

</td><td>

sn\_svc\_appl\_info.admin

</td><td>

Role required to provide delegated admin access to the Service Applicant Information application.

</td></tr><tr><td>

Service Applicant Program Management

</td><td>

sn\_svc\_appl\_pgm\_mg.admin

</td><td>

Role required to provide delegated admin access to the Service Applicant Program Management application.

</td></tr><tr><td>

Service Catalog

</td><td>

catalog\_admin

</td><td>

Role required to manage the Service Catalog application, including catalogs, categories, and items, but not including scripting functions available to administrators.

</td></tr><tr><td>

Service Graph Connectors

</td><td>

admin

</td><td>

Role required to install and upgrade Service Graph Connectors, including API Service Graph Connectors. Admin users can create a connection, configure connection properties, monitor connections and data imports, run background scripts, and provide access to tables in the global scope.

</td></tr><tr><td>

Service Graph Connectors

</td><td>

sn\_cmdb\_int\_util.sgc\_admin

</td><td>

Role required to create, update, and delete connections, configure connectors using the guided setup, and read and write system properties.

</td></tr><tr><td>

Service Graph Connectors

</td><td>

cmdb\_inst\_admin

</td><td>

Role required to read all Service Graph Connector application modules, read and write system properties, and read records that are owned by other applications and are related to the functionality of Service Graph Connectors. Users with this role can create, update, and delete custom tables, scheduled imports, and data sources.

</td></tr><tr><td>

Service Level Management

</td><td>

sla\_admin

</td><td>

Role required to configure Service Level Management features and system properties.

</td></tr><tr><td>

ServiceNow Studio

</td><td>

sn\_udc.admin

</td><td>

Role required to -   Manage all ServiceNow Studio system properties, settings, and configurations.
-   Manage roles and permissions specific to ServiceNow Studio.
-   Configure the experience switcher roles across Creator Studio, ServiceNow Studio, and ServiceNow IDE.

</td></tr><tr><td>

ServiceNow Studio

</td><td>

sn\_prfrd\_tables.admin

</td><td>

Role required to configure preferred tables in your instance for Table Builder.

</td></tr><tr><td>

ServiceNow Vault

</td><td>

sn\_vault\_console.vault\_console\_admin

</td><td>

Role required to have a collection of Data Classification admin, Data Privacy admin, and CA Admin roles to execute a template flow and monitor sensitive data. To learn more, see [Configuring ServiceNow Vault](../../vault/concept/configuring-servicenow-vault.md)

</td></tr><tr><td>

ServiceNow Vault

</td><td>

sn\_vault\_console.vault\_console\_auditor

</td><td>

Role required to have a collection of Data Discovery Auditor, Data Classification Auditor, Data Privacy Auditor, and Continuous Auth Auditor roles to view the policies and metrics related to ServiceNow Vault.

</td></tr><tr><td>

ServiceNow for Teams – Core

</td><td>

sn\_now\_teams.admin

</td><td>

Role required to manage ServiceNow for Teams configurations, including system properties, Virtual Agent configuration, manifest settings, UI actions, and table-level ACLs.

</td></tr><tr><td>

Skills Foundation

</td><td>

sn\_skills\_int.admin

</td><td>

Role required to configure system settings with complete access to all the Skills Foundation features and functionality related to the employee.

</td></tr><tr><td>

Skills Foundation

</td><td>

sn\_skills\_int.job\_arch\_admin

</td><td>

Role required to view, create, update, remove, and configure the job architecture data.

</td></tr><tr><td>

Smart Operations

</td><td>

sn\_smartops.admin

</td><td>

Role required to serve as the Super Admin for Smart Operations. Has full privileges to perform all CRUD \(Create, Read, Update, Delete\) operations across Smart Operations tables, APIs, and data brokers.

</td></tr><tr><td>

Social Benefits Playbook

</td><td>

sn\_gsm\_soc\_bnfts.admin

</td><td>

Role required to provide delegated admin access to the License and Permit Playbook application.

</td></tr><tr><td>

System Engineering Core

</td><td>

openstack\_admin

</td><td>

Role required to have full administrative access to OpenStack compute, storage, and network.

</td></tr><tr><td>

System Engineering Core

</td><td>

vcenter\_admin

</td><td>

Role required to have full administrative access to vCenter: VMs, clusters, storage, and hosts.

</td></tr><tr><td>

System Logs \(Log Entry\)

</td><td>

syslog\_admin

</td><td>

Provides create/write access to Log Entry \(syslog\) records. The previous admin role ACL bindings on the syslog table are deleted and replaced with these new granular roles.

</td></tr><tr><td>

Talent Feedback

</td><td>

sn\_tf.admin

</td><td>

Role require to manage and configure all Talent Feedback modules.

</td></tr><tr><td>

Task Mining

</td><td>

sn\_tm\_core.admin

</td><td>

Role required to have admin access for Process mining application.

</td></tr><tr><td>

Third-party risk management

</td><td>

sn\_vdr\_risk\_asmt.vendor\_risk\_admin

</td><td>

Role required to have admin access for third-party risk management.

</td></tr><tr><td>

Transaction Part Metrics Logs

</td><td>

txn\_part\_metrics\_admin

</td><td>

Provides create, write, and delete access to the syslog\_transaction\_part\_metrics table. The previous admin role ACL bindings on this table are deleted and replaced with these new granular roles. New ACLs for all five operations \(read, create, write, delete, report\_view\) are introduced, each gated by the appropriate new role.

</td></tr><tr><td>

TSOM Visibility

</td><td>

tsom\_visibility\_admin

</td><td>

Role required to manage the operational tasks for the TSOM Visibility application.

</td></tr><tr><td>

TSOM Assurance

</td><td>

tsom\_assurance\_admin

</td><td>

Role required to manage the operation tasks \(includes administration\) for the TSOM Assurance.

</td></tr><tr><td>

UI Builder

</td><td>

ui\_builder\_admin

</td><td>

Role required to have admin access for UI Builder.

</td></tr><tr><td>

Usage Analytics

</td><td>

usage\_admin

</td><td>

Role required to have admin access for usage analytics.

</td></tr><tr><td>

Universal Request

</td><td>

sn\_uni\_req.ur\_admin

</td><td>

Role required to setup and configure Universal Request.

</td></tr><tr><td>

Universal Task

</td><td>

sn\_uni\_task.admin

</td><td>

Role required to have full administrator access to Universal Task — configure task types, templates, and settings.

</td></tr><tr><td>

Universal Task

</td><td>

sn\_uni\_task.emp\_form\_admin

</td><td>

Role required to manage employee forms.

</td></tr><tr><td>

Usage Insights

</td><td>

analytics\_admin

</td><td>

Role required to have admin access for Usage Insights.

</td></tr><tr><td>

User Experience-Scope

</td><td>

sn\_cda.analytics\_admin

</td><td>

Role required to have access to User Experience resources as Scope app admin.

</td></tr><tr><td>

Vulnerability Response

</td><td>

sn\_vul.vulnerability\_admin

</td><td>

Role required for complete access to the Vulnerability Response \(VR\) application and its records. Users with this role configure all VR applications and rules and can install third-party integrations.

</td></tr></tbody>
</table>-   **[Platform security granular admin roles](platsec-granular-roles.md)**  
Use granular admin roles to verify access management by assigning roles that define user permissions and responsibilities.

