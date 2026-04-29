---
title: Install Enterprise Asset Management
description: Request the Enterprise Asset Management application from the ServiceNow Store so that you can track and manage your enterprise assets.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Enterprise Asset Management, IT Asset Management]
---

# Install Enterprise Asset Management

Request the Enterprise Asset Management application from the ServiceNow® Store so that you can track and manage your enterprise assets.

## Before you begin

Role required: sys\_admin

## About this task

The following plugins and applications are automatically installed with the ServiceNow Enterprise Asset Management application:

<table id="table_x2t_k4z_ssb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Plugins

</td></tr><tr><td>

Asset Management\(com.snc.asset\_management\)

</td><td>

Provides functionalities to integrate the physical, technological, contractual, and financial aspects of information technology assets. See [Asset Management](https://www.servicenow.com/docs/access?context=c_AssetManagement&version=australia&pubname=australia-it-service-management&ft:locale=en-US) for more information on asset management.

</td></tr><tr><td>

Procurement\(com.snc.procurement\)

</td><td>

Provides the capability to source and receive requested assets so that you can fulfill service catalog requests. See [Procuring enterprise assets](../concept/procuring-assets.md) for more information on procurement.

</td></tr><tr><td>

Field Service Management \(com.snc.work\_management\)

</td><td>

Provides the capability to manage work orders and related tasks. See [Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&version=australia&pubname=australia-field-service-management&ft:locale=en-US) for more information on Field Service Management.

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

Provides the capability to manage regular preventative maintenance of assets. See [Planned Maintenance](https://www.servicenow.com/docs/access?context=c_SMPlanMaint&version=australia&pubname=australia-service-management-for-the-enterprise&ft:locale=en-US) for more information on Planned Maintenance.

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

</td></tr><tr><td class="sub-head" colspan="2">

Applications

</td></tr><tr><td>

Expanded Model and Asset Classes

</td><td>

Adds enterprise model and asset classes that extend out-of-the-box product model and asset classes within the CMDB class hierarchy. In addition, creates model categories that associate these enterprise model and asset classes with CMDB configuration item \(CI\) classes. See [Expanded Model and Asset Classes](../concept/enterprise-model-asset-classes-app.md) for more information on this application.

</td></tr><tr><td>

CMDB CI Class Models

</td><td>

Adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and dependent relationships. See [CMDB CI Class Models store app](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) for more information on this application.

</td></tr><tr><td>

Asset Management Common

</td><td>

Provides features that are common to the Hardware Asset Management, Software Asset Management, and Enterprise Asset Management applications, including the catalog item to request asset reclamation.

</td></tr><tr><td>

GRC: Risk Heatmap

</td><td>

Provides a heatmap component that enables you to visualize the risk posture of your organization. See [Risk heatmap for classic risk assessment](https://www.servicenow.com/docs/access?context=risk-heatmap-classic-risk-assessment&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US) or [Operational risk heatmap for Advanced Risk Assessment in the Risk Workspace](https://www.servicenow.com/docs/access?context=risk-heatmaps-in-ws&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US) for more information on risk heatmaps.

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
</table>## Procedure

1.  From a web browser, go to the [ServiceNow Store](https://store.servicenow.com/).

2.  Log in using your HI credentials.

3.  In the search bar, enter `Enterprise Asset Management` and then select **Search**.

4.  Select the result called **ServiceNow Enterprise Asset Management**.

5.  On the ServiceNow Enterprise Asset Management page, select **Request Install**.

    The ServiceNow Request for App Installation - ServiceNow Enterprise Asset Management dialog box opens.

6.  In the dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Instance Name|Name of the instance on which you want to install the application. After you enter the instance name, select **Validate Instance** to verify that the instance exists.|
    |Reason for request|Reason for requesting the application.|

7.  Select **Request**.

8.  Select **Close**.


## Result

If your request is approved, you will receive an email with detailed instructions on how to install the application.

## What to do next

Install the application according to the instructions in the email.

