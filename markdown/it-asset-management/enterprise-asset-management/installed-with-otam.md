---
title: Installed with OT Asset Management
description: The user role components, plugins, and applications are installed with activation of the com.sn\_otam plugin.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Enterprise Asset Management reference, Enterprise Asset Management, IT Asset Management]
---

# Installed with OT Asset Management

The user role components, plugins, and applications are installed with activation of the com.sn\_otam plugin.

## Roles installed

<table id="table_fdc_514_1bc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

OT asset manager

 \[sn\_otam.ot\_asset\_manager\]

</td><td>

Manages Operational Technology-specific models and assets in the OT Asset Workspace.

</td><td>

sn\_eam.asset\_manager

</td></tr><tr><td>

OT asset technician

 \[sn\_otam.ot\_asset\_technician\]

</td><td>

Performs tasks related to Operational Technology-specific assets in the OT Asset Workspace.

</td><td>

sn\_eam.asset\_technician

</td></tr></tbody>
</table>## Plugins installed

|Name|Description|
|----|-----------|
|Asset Management \(com.snc.asset\_management\)|Provides functionalities to integrate the physical, technological, contractual, and financial aspects of information technology assets.|
|Procurement \(com.snc.procurement\)|Provides the capability to source and receive requested assets so that you can fulfill service catalog requests.|
|Enterprise model normalization \(com.sn\_eam\_core\)|Provides information related to normalization such as normalization status, model content service download, and life-cycle overview.|
|Asset Management Workspace - Recommendations \(com.sn\_itam\_recomm\)|Provides actionable recommendations for users in configurable workspaces.|
|SM Planned Maintenance \(com.snc.planned\_maintenance\)|Provides the capability to manage regular preventative maintenance of assets.|
|Work Management \(com.snc.work\_management\)|Provides the capability to manage your work orders, work order tasks, maintenance plans, and other relevant work order information.|
|Performance Analytics \(com.snc.pa\)|Provides dashboards containing actionable data visualizations that help you improve your business processes and practices.|
|Playbook Experience \(com.glide.playbook\_experience.config\)|Provides a step-by-step guidance for setting up your assets with important information.|
|Playbooks for App Engine \(com.glide.pad.license\)|Provides a simplified and task-oriented view of processes.|
|Cost Management \(com.snc.cost\_management\)|Provides options to plan and control business costs.|

## Applications installed

|Name|Description|
|----|-----------|
|Enterprise Asset Management \(com.sn\_eam\)|Manages the complete life cycle of your enterprise connected and non-connected assets.|
|Expanded Model and Asset Classes \(com.sn\_ent\)|Adds enterprise model and asset classes that extend out-of-the-box product model and asset classes within the CMDB class hierarchy. In addition, creates model categories that associate these enterprise model and asset classes with CMDB configuration item \(CI\) classes.|
|CMDB CI Class Models \(com.sn\_cmdb\_ci\_class\)|Adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and dependent relationships.|
|Asset Management Common \(com.sn\_itam\_common\)|Provides features that are common to the Hardware Asset Management, Software Asset Management, and Enterprise Asset Management applications, including the catalog item to request asset reclamation.|
|Physical Assets \(sn\_phy\_assets\)|Marker that aligns features for physical asset-based applications, including the Hardware Asset Management and Enterprise Asset Management applications.|
|Risk Heat Map \(com.sn\_risk\_heatmap\)|Provides a heatmap component that enables you to visualize the risk posture of your organization.|
|Geo Map Component \(com.sn\_geo\_map\)|Provides the capability to track the location of the assets using indoor maps.|

**Parent Topic:**[Enterprise Asset Management reference](../concept/reference-enterprise-asset-management.md)

**Related topics**  


[Domain separation and Enterprise Asset Management](../concept/domain-separation-eam.md)

[Enterprise Asset Management roles](eam-roles.md)

[Enterprise model categories and corresponding classes](enterprise-model-categories.md)

[Mandatory fields in the bulk import spreadsheets](mandatory-bulk-fields.md)

[Normalization status for enterprise models](norm-status-eam.md)

[Model fields for Enterprise Asset Management](eam-model-fields.md)

[Contract fields for Enterprise Asset Management](contract-fields-eam.md)

[Maintenance plan fields for Enterprise Asset Management](maintenance-plan-fields-eam.md)

[Maintenance schedule fields for Enterprise Asset Management](maintenance-schedule-fields-eam.md)

[Work plan fields for Enterprise Asset Management](wp-fields-eam.md)

[Work plan schedule fields for Enterprise Asset Management](work-plan-schedule-fields-eam.md)

[Expense line fields for Enterprise Asset Management](expense-line-fields-eam.md)

[Fields inherited from a parent asset group to a sub group](subgroups-parent-fields-eam.md)

[Enterprise asset disposal order stages](eamasset-disposalorder-stages.md)

[Terminology for linear assets](terms-eam.md)

[Installed with Enterprise Asset Management for Healthcare](installed-with-eam-healthcare.md)

[Asset put away task fields](put-away-task-form-eam.md)

