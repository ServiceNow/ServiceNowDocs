---
title: Components installed with Enterprise Asset Management
description: Several types of components are installed with activation of the com.sn\_eam plugin, including user roles, plugins, and applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/installed-with-eam.html
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: reference
last_updated: "2026-06-08"
reading_time_minutes: 7
breadcrumb: [Enterprise Asset Management reference, Enterprise Asset Management, IT Asset Management]
---

# Components installed with Enterprise Asset Management

Several types of components are installed with activation of the com.sn\_eam plugin, including user roles, plugins, and applications.

## Roles installed

<table id="table_o23_ynl_xsb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Enterprise asset manager

 \[sn\_eam.enterprise\_asset\_manager\]

</td><td>

This role has access to all Enterprise Asset Management features except administrative functions.

</td><td>

-   wm\_initiator
-   sn\_eam.enterprise\_mobile\_user
-   sn\_eam.enterprise\_asset\_creator
-   sn\_eam.enterprise\_asset\_technician
-   sn\_eam.asset\_manager
-   inventory\_user
-   contract\_manager
-   procurement\_user
-   cmdb\_query\_builder
-   cmdb\_read
-   plan\_maint\_admin
-   wm\_task\_initiator

</td></tr><tr><td>

Enterprise admin

 \[sn\_eam.enterprise\_admin\]

</td><td>

This role has full access to the Enterprise Asset Management application as well as the OT Asset Workspace.

</td><td>

-   inventory\_admin
-   catalog\_manager
-   report\_user
-   sn\_eam.enterprise\_asset\_manager
-   asset
-   procurement\_admin
-   sn\_ent.classification\_manager
-   sn\_otam.ot\_asset\_manager

</td></tr><tr><td>

Enterprise technician \[enterprise\_asset\_technician\]

</td><td>

This role is for users who perform work tasks and update asset records as part of the asset lifecycle. This role has access to the following enterprise asset tasks: -   all RMA tasks except the Prepare task
-   all recall tasks
-   all disposal tasks
-   all loaner tasks except the Prepare task
-   enterprise asset audit
-   lease-end Collection, Preparation, and Shipment tasks

</td><td>

-   sn\_eam.enterprise\_mobile\_user
-   sn\_eam.enterprise\_asset\_editor
-   sn\_ent.classification\_reader
-   canvas\_user
-   sn\_eam.asset\_technician

</td></tr><tr><td>

Enterprise mobile user

 \[sn\_eam.enterprise\_mobile\_user\]

</td><td>

This role has access to scan assets from a mobile application as well as dispose assets from a mobile application.

</td><td>

none

</td></tr><tr><td>

Agent\[wm\_agent\]

</td><td>

This role is for users who perform work on enterprise assets and record details in the corresponding work orders and work order tasks.**Note:** The wm\_agent role must contain an additional role such as enterprise\_asset\_manager, enterprise\_asset\_technician, or any other role to log into the Enterprise Asset Management.

</td><td>

none

</td></tr></tbody>
</table>## Granular roles installed

<table id="table_b1n_5km_k3c"><thead><tr><th>

EAM functionality

</th><th>

Granular admin role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Shipment

</td><td>

asset\_integration\_admin

</td><td>

Provides write access to the Ignore stale check \[ignore\_stale\_check\] column in the Shipment \[sn\_itam\_common\_shipment\] table.

</td></tr><tr><td>

Carrier integration

</td><td>

asset\_integration\_admin

</td><td>

Provides access to the Carrier Integration Profile \[sn\_itam\_carrier\_int\_profile\] table to perform the following tasks:-   Create carrier integration profiles
-   View reports

</td></tr><tr><td>

Contract renewal

</td><td>

contract\_system\_admin

</td><td>

Provides Write access to the **sn\_itam\_common.sn\_contract\_enable\_renewal\_flow** system property.

</td></tr><tr><td>

ITAM AI agents

</td><td>

asset\_aia\_admin

</td><td>

Provides access to read, write, delete, and report on the ITAM AI Agents Log \[itam\_aia\_log\] table.

</td></tr><tr><td>

Common Hardware Asset Management and Enterprise Asset Management tables

</td><td>

sn\_eam.enterprise\_admin

</td><td>

Provides access to the following tables:-   RFID Connection Attributes \[sn\_itam\_common\_rfid\_conn\_attr\]
-   RFID Stage Asset \[sn\_itam\_common\_rfid\_stg\_asset\]
-   Repair order \[sn\_itam\_common\_repair\_order\]
-   Repair order line \[sn\_itam\_common\_repair\_orderline\]
-   Asset order \[sn\_itam\_common\_asset\_order\]
-   Asset order line \[sn\_itam\_common\_asset\_orderline\]
-   Loaner Asset Order \[sn\_itam\_common\_loaner\_asset\_order\]

</td></tr></tbody>
</table>## Plugins installed

<table id="table_x2t_k4z_ssb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Asset Management\(com.snc.asset\_management\)

</td><td>

Provides functionalities to integrate the physical, technological, contractual, and financial aspects of information technology assets. See [Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/c_AssetManagement.md) for more information on asset management.

</td></tr><tr><td>

Procurement\(com.snc.procurement\)

</td><td>

Provides the capability to source and receive requested assets so that you can fulfill service catalog requests. See [Procuring enterprise assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/procuring-assets.md) for more information on procurement.

</td></tr><tr><td>

Field Service Management \(com.snc.work\_management\)

</td><td>

Provides the capability to manage work orders and related tasks. See [Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/fsm-application-landing-page.md) for more information on Field Service Management.

</td></tr><tr><td>

Enterprise Asset Management Core\(com.sn\_eam\_core\)

</td><td>

Provides core functionalities, such as normalization, for the Enterprise Asset Management application.

</td></tr><tr><td>

Asset Management Workspace - Recommendations plugin\(com.sn\_itam\_recomm\)

</td><td>

Provides actionable recommendations for users in configurable workspaces.

</td></tr><tr><td>

SM Planned Maintenance\(com.snc.planned\_maintenance\)

</td><td>

Provides the capability to manage regular preventative maintenance of assets. See [Planned Maintenance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-management-for-the-enterprise/c_SMPlanMaint.md) for more information on Planned Maintenance.

</td></tr><tr><td>

Physical Assets\(com.sn\_phy\_assets\)

</td><td>

Marker that aligns features for physical asset-based applications, including the Hardware Asset Management and Enterprise Asset Management applications.

</td></tr><tr><td>

Indoor Mapping for Assetscom.sn\_ima

</td><td>

Provides the capability to track the location of the assets using indoor maps.

</td></tr><tr><td>

Work Management \(com.snc.work\_management\)

</td><td>

Provides the capability to manage your work orders, work order tasks, maintenance plans, and other relevant work order information.

</td></tr><tr><td>

Performance Analytics \(com.snc.pa\)

</td><td>

Provides dashboards containing actionable data visualizations that help you improve your business processes and practices.

</td></tr><tr><td>

Playbook Experience Core\(com.glide.playbook\_experience.config\)

</td><td>

Provides a step-by-step guidance for setting up your assets with important information.

</td></tr><tr><td>

Process Automation Designer for App Engine\(com.glide.pad.license\)

</td><td>

Provides a simplified and task-oriented view of processes.

</td></tr><tr><td>

Cost Management \(com.snc.cost\_management\)

</td><td>

Provides options to plan and control business costs.

</td></tr></tbody>
</table>## Applications installed

<table id="table_bty_vt3_njc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Expanded Model and Asset Classes

</td><td>

Adds enterprise model and asset classes that extend out-of-the-box product model and asset classes within the CMDB class hierarchy. In addition, creates model categories that associate these enterprise model and asset classes with CMDB configuration item \(CI\) classes. See [Expanded Model and Asset Classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/enterprise-model-asset-classes-app.md) for more information on this application.

</td></tr><tr><td>

CMDB CI Class Models

</td><td>

Adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and dependent relationships. See [CMDB CI Class Models store app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/cmdb-ci-class-models.md) for more information on this application.

</td></tr><tr><td>

Asset Management Common

</td><td>

Provides features that are common to the Hardware Asset Management, Software Asset Management, and Enterprise Asset Management applications, including the catalog item to request asset reclamation.

</td></tr><tr><td>

GRC: Risk Heatmap

</td><td>

Provides a heatmap component that enables you to visualize the risk posture of your organization. See [Risk heatmap for classic risk assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/risk-heatmap-classic-risk-assessment.md) or [Operational risk heatmap for Advanced Risk Assessment in the Risk Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/risk-heatmaps-in-ws.md) for more information on risk heatmaps.

</td></tr><tr><td>

Smart Assessment Core \(com.sn\_smart\_asmt\)

</td><td>

Foundational application that is required for the smart assessment engine to work. This is required for the Assessment designer, Assessment component and Migration tools.

</td></tr><tr><td>

sn-smart-assessment-connected \(com.sn\_smart\_assessment\_connected\)

</td><td>

Respond to assessments quickly using the Assessment response component. Its user-friendly and simple design enables users to submit assessments with more efficiency.

</td></tr><tr><td>

sn-smart-assessment-designer \(com.sn\_smart\_assessment\_designer\)

</td><td>

Create assessment templates and add instructions, questions, and reference information to an assessment template.

</td></tr><tr><td>

Basic Scoring for Smart Assessments \(com.sn\_smart\_scoring\)

</td><td>

Scoring in Smart Assessment Engine is a systematic way to evaluate responses to various questions within an assessment. By attributing scores to answers, you can translate qualitative responses into quantitative data, offering each evaluation's measurable and comparable outcome.

</td></tr><tr><td>

Smart Assessment for Mobile \(com.snc.smart\_assessment\_mobile\)

</td><td>

Application for smart assessment engine to work on mobiles.

</td></tr><tr><td>

ISA Equipment Model \(com.sn\_isa\_model\)

</td><td>

Data model for ISA-95 Equipment model entities and templates.

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Asset Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/reference-enterprise-asset-management.md)

**Related topics**  


[Domain separation and Enterprise Asset Management]()

[OT Asset Workspace roles]()

[Asset fields for enterprise assets]()

[Asset audit fields for enterprise assets]()

[Audit results]()

[Enterprise model categories and corresponding classes]()

[Mandatory fields in the bulk import spreadsheets]()

[Normalization status for enterprise models]()

[Model fields for Enterprise Asset Management]()

[Contract fields for Enterprise Asset Management]()

[Maintenance plan fields for Enterprise Asset Management]()

[Maintenance schedule fields for Enterprise Asset Management]()

[Work plan fields for Enterprise Asset Management]()

[Work plan schedule fields for Enterprise Asset Management]()

[Expense line fields for Enterprise Asset Management]()

[Fields inherited from a parent asset group to a sub group]()

[Enterprise asset disposal order stages]()

[Terminology for linear assets]()

[Scheduled jobs and tables installed with normalization of firmware models]()

[Asset put away task fields]()

