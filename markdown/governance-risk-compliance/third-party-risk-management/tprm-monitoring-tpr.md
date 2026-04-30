---
title: Monitoring your third-party risk
description: You can monitor the potential risks that are associated with your third-party relationships by using the Third-party Risk Management application. An ongoing monitoring process can help you regularly assess the third party's performance and adherence to the agreed-upon terms.
locale: en-US
release: zurich
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Third-party Risk Management, Governance, Risk, and Compliance]
---

# Monitoring your third-party risk

You can monitor the potential risks that are associated with your third-party relationships by using the Third-party Risk Management application. An ongoing monitoring process can help you regularly assess the third party's performance and adherence to the agreed-upon terms.

## Ongoing monitoring and review

You can monitor and review the performance of your third parties with Vendor Management Workspace. For example, you can regularly assess whether the third party is adhering to the agreed-upon terms.

**Note:** The Vendor Management Workspace is designed for users with the Third-party risk \(TPR\) manager \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\], TPR assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\], and Third-party assessment reviewer \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\] roles.

## Viewing risk reports and other information

Starting with version 21.1.x, the legacy horizontal tab-based layout in the Vendor Management Workspace has been replaced by a structured vertical navigation panel. This design introduces:

-   Grouped Related Lists: Organizes access to third-party records, assessments, and dashboards into logical sections.
-   Clearer Workflows: Navigation is streamlined to support risk management processes and dependency tracking for third parties and engagements.
-   Consistent Availability: The vertical panel is accessible across all internal user roles, ensuring a unified experience for managing vendor risk and resilience.

For more information on configuring related lists, see [Configure related lists for vertical navigation on record pages](../task/config-related-list-vert-nav.md).

You can view the risk reports for all third parties and engagements by navigating to **Workspaces** &gt; **Vendor Management Workspace** and then selecting the **Risk** tab to open the workspace to the home page. For more information, see [Viewing third-party risk reports](unified-vrm-workspace.md).

You can also view the status and all current information for a third party or engagement by navigating to **Workspaces** &gt; **Vendor Management Workspace**. On the **Risk** tab, select the home page icon ![](../../grc-workspace-vrm/image/icon-tprm-ws-home.png).

As shown in the following example, you can select any number in the Third-party risk overview section to open a list of third parties or engagements with that risk rating value. You can then select a third party or engagement.

![Sequence showing the selections needed to view a third party or engagement. For the text description, refer to the text that preceded this example.](../../grc-workspace-vrm/image/tprm-ws-dd-list-third-parties.png "How to open a third party or engagement page by risk rating")

For more information, see [Get an overview of a third party](../../grc-workspace-vrm/concept/tprm-ws-tp-working-on.md).

## TPRM personalized dashboards

Monitor and analyze your assessment data at various levels using the Third-party insights dashboard and TPRM custom analytics dashboard. If you have the TPR manager \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] or TPR assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] role, you can create and share your own dashboards and reports. TPR managers can also customize report layouts, widgets, and data views to prioritize key metrics and workflows that align with your individual roles and risk programs. These dashboards provide you and your team with tailored insights and deliver relevant information at a glance, improving your decision-making process. You can view TPRM personalized dashboards by navigating to **Workspaces** &gt; **Vendor Management Workspace** and selecting the dashboard page icon ![](../../grc-workspace-vrm/image/icon-tprm-ws-dashboard.png). For more information, see [Monitoring assessment data using TPRM dashboards](tprm-monitor-dashboards.md).

## Due diligence processes

You can view the status of the following due diligence processes from the Due diligence request record page:

-   Request process
-   Inherent Risk Questionnaire \(IRQ\) process
-   Third-party risk assessment process
-   Approval process
-   Contract risk process

To access the Due diligence request record page, you can select the DDR number for any due diligence request. For more information about the due diligence process, see [Monitoring the due diligence request process](../../grc-workspace-vrm/concept/tprm-ws-dd-mgt-pg-overview.md).

## Managing fourth-nth parties

You can use Third-party Risk Management to help identify, understand, and manage risks that are related to third parties dependent on the services of fourth-nth parties. Monitoring fourth-nth parties can help ensure that they adhere to the same security and compliance standards as the primary third party. For more information about fourth-nth parties, see [Monitoring your fourth-nth parties](tprm-monitor-fourth-parties.md).

## Managing third-party elements

You can monitor third-party elements through scalable scoring models, relationship analysis, and due diligence workflow integration as part of the third-party element collection process. Monitoring third-party elements and leveraging that information can help with conducting more informed risk assessments as part of your third-party risk program. For more information about third-party elements, [Monitoring third-party elements](tprm-monitor-tp-elements.md).

## Managing Smart assessment templates

After upgrading to version 22.0.1 and installing the Unified Content Management application, TPR managers \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] can view a centralized library of smart assessment templates aligned with global regulations and industry standards. From the unified content management module in the Vendor Management Workspace you can activate and update templates. You can access the unified content module by navigating to **Workspaces** &gt; **Vendor Management Workspace**, select the unified content management icon ![](../image/unified-content-mgmt-icon.png) and then navigate to **Smart assessment templates**. For more information, see [Managing TPRM SAE templates with Unified Content Management](tprm-integrating-ucm.md) and [Sample questionnaires](../../grc-workspace-vrm/reference/tprm-questionnaire-types.md).

## Viewing managed activities

An engagement only consumes one license, regardless of whether there’s one managed activity or many managed activities per contract year. Managed activity usage is triggered only when an activity is initiated. You can view your managed activities for verification purposes with the Usage analytics activities \[sn\_vdr\_risk\_asmt\_ua\_activity\] table. This read-only table stores a record whenever a managed activity occurs. You must have the Third-party assessment reviewer \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\] role to view this table. You can access the Usage analytics activities table by navigating to **All** &gt; **Third Party Risk Management** &gt; **Administration** &gt; **Managed Activity Analytics**. For more information, see [Tracking a managed activity](tprm-managed-activity.md).

**Note:** The Usage analytics activities \[sn\_vdr\_risk\_asmt\_ua\_activity\] table is only available to those users that have purchased the Third-party Risk Management application and have access to the Due diligence management application. To see the instructions for downloading a GRC application from the ServiceNow® Store, see [Download a GRC application from the ServiceNow Store for the first time](../../grc-common/task/download-grc-first-time.md).

