---
title: Install Enterprise Asset Management
description: Request the Enterprise Asset Management application from the ServiceNow Store so that you can track and manage your enterprise assets.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configuring Enterprise Asset Management, Enterprise Asset Management, IT Asset Management]
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

Provides functionalities to integrate the physical, technological, contractual, and financial aspects of information technology assets. See [Asset Management](https://www.servicenow.com/docs/access?context=c_AssetManagement&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information on asset management.

</td></tr><tr><td>

Procurement\(com.snc.procurement\)

</td><td>

Provides the capability to source and receive requested assets so that you can fulfill service catalog requests. See [Procuring enterprise assets](../concept/procuring-assets.md) for more information on procurement.

</td></tr><tr><td>

Field Service Management \(com.snc.work\_management\)

</td><td>

Provides the capability to manage work orders and related tasks. See [Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US) for more information on Field Service Management.

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

Provides the capability to manage regular preventative maintenance of assets. See [Planned Maintenance](https://www.servicenow.com/docs/access?context=c_SMPlanMaint&version=yokohama&pubname=yokohama-service-management-for-the-enterprise&ft:locale=en-US) for more information on Planned Maintenance.

</td></tr><tr><td>

Physical Assets\(com.sn\_phy\_assets\)

</td><td>

Marker that aligns features for physical asset-based applications, including the Hardware Asset Management and Enterprise Asset Management applications.

</td></tr><tr><td>

Indoor Mapping for Assetscom.sn\_ima

</td><td>

Provides the capability to track the location of the assets using indoor maps.

</td></tr><tr><td class="sub-head" colspan="2">

Applications

</td></tr><tr><td>

Expanded Model and Asset Classes

</td><td>

Adds enterprise model and asset classes that extend out-of-the-box product model and asset classes within the CMDB class hierarchy. In addition, creates model categories that associate these enterprise model and asset classes with CMDB configuration item \(CI\) classes. See [Expanded Model and Asset Classes Store application](../concept/enterprise-model-asset-classes-app.md) for more information on this application.

</td></tr><tr><td>

CMDB CI Class Models

</td><td>

Adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and dependent relationships. See [CMDB CI Class Models store app](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) for more information on this application.

</td></tr><tr><td>

Asset Management Common

</td><td>

Provides features that are common to the Hardware Asset Management, Software Asset Management, and Enterprise Asset Management applications, including the catalog item to request asset reclamation.

</td></tr><tr><td>

GRC: Risk Heatmap

</td><td>

Provides a heatmap component that enables you to visualize the risk posture of your organization. See [Risk heatmap for classic risk assessment](https://www.servicenow.com/docs/access?context=risk-heatmap-classic-risk-assessment&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US) or [Operational risk heatmap for Advanced Risk Assessment in the Risk Workspace](https://www.servicenow.com/docs/access?context=risk-heatmaps-in-ws&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US) for more information on risk heatmaps.

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

