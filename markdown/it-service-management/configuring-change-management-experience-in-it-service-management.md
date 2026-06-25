---
title: Configuring Simplified Change Management
description: Configure Change Management through a guided experience that walks you through the core setup areas required to make Change Management operational.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/configuring-change-management-experience-in-it-service-management.html
release: australia
topic_type: concept
last_updated: "2026-04-30"
reading_time_minutes: 6
breadcrumb: [Configuring the fulfiller experience in Simplified IT Service Management, Configure integrations and ITSM experiences in Simplified IT Service Management, Configure and integrate, Simplified IT Service Management, IT Service Management]
---

# Configuring Simplified Change Management

Configure Change Management through a guided experience that walks you through the core setup areas required to make Change Management operational.

The setup provides an opinionated, wizard-driven experience with defaults pre-applied in some steps. Rather than building your configuration from scratch, you can configure by exception, accepting defaults where they apply and customizing only where your organization's needs differ.

## Simplified Change Management overview

Simplified Change Management offers the core functionality of the full Change Management application. It's purpose-built for organizations that need a fast, low-friction path to change governance without the complexity of an enterprise-scale deployment.

Compared to the standard Change Management application, the simplified experience reduces scope in three key ways:

-   **Fewer change types to configure**

    The standard change application supports a wide range of change types with individually configurable workflows, risk models, and approval chains. Simplified change focuses on the most common change patterns—Standard, Normal, and Emergency with prebuilt workflows that work with the base system, so you aren't required to design approval logic before you can go live.

-   **Opinionated defaults instead of open-ended configuration**

    The full change application gives you complete control over every configuration parameter, which requires significant ServiceNow expertise to set up correctly. Simplified change makes those decisions for you using defaults based on common practices. You only need to act where your organization's requirements genuinely differ from the defaults.

-   **Guided setup instead of open configuration**

    The standard change application is configured through multiple administration modules spread across the platform. Simplified change consolidates all required setup into a single, step-by-step guided setup experience within the Configuration Console, so you know what to configure next and can track your progress in one place.


Simplified Change Management is intended for organizations that are new to ServiceNow change governance, are transitioning from spreadsheet or email-based change tracking, or need to reach an operational state quickly without a dedicated implementation team. If your organization requires advanced workflow customization, complex multi-stage CAB structures, or integration with enterprise release management tools, the full Change Management application may be a better fit.

## Configuration areas

Navigate the setup across the core configuration areas within the Configuration Console, each accessible from the **ITSM fulfiller experience** &gt; **Change Management** section. You can move through the areas in any order, skip an area and return to it later as needed.

-   **Team roles**

    Defines who can approve, build, or review a change by mapping individuals and groups to their respective roles in the change process. For more information, see [Configure team roles for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-team-roles-for-change-management.md).

-   **Risk configuration**

    Establishes how risk is assessed for change requests. Pre-configured risk assessment questions, responses, and score ranges are provided as defaults, allowing organizations to start with a working risk model and refine it over time as their change governance matures. For more information, see [Configure risk for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-risk-change-mgmt.md).

-   **Change Advisory Board \(CAB\)**

    Configures the CAB structure that governs change approvals. Admins define CAB membership, meeting schedules, and the types of changes that require CAB review. Default CAB role mappings are pre-applied to reduce initial setup effort. For more information, see [Configure Change Advisory Board for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-cab-change-management.md).

-   **Change models**

    Specifies the templates and workflows used for each type of change—Standard, Normal, and Emergency. Base system change models are included as defaults. Admins can modify existing models or create new ones to reflect their organization's change types and workflows. For more information, see [Configure change models for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-change-models-scm.md).

-   **Change schedules**

    Defines the maintenance windows and blackout periods that control when changes can be implemented. Default schedules are provided as a starting point and can be customized to align with the organization's operational calendar and service availability requirements. For more information, see [Configure schedules for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-schedules-for-simplified-change-management.md).

-   **Notifications**

    Configures when and how stakeholders are notified about change activity, approvals, and completions. Default notification rules cover the most common communication touchpoints in the change lifecycle and can be extended or suppressed based on organizational preferences. For more information, see [Configure notifications for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-notifications-for-simplified-change-management.md).


## Roles required

You must have the Change Management Setup Administrator \(sn\_itsm\_chg\_admin.admin\) role to configure all the sections of the Change Management setup. This role contains the following roles that can be assigned for access to specific sections:

|Role|Description|
|----|-----------|
|sn\_itsm\_chg\_admin.team\_roles\_config|Grants access to configure team roles and group assignments.|
|sn\_itsm\_chg\_admin.risk\_config|Grants access to configure risk assessment questions, scoring, and risk threshold bands.|
|sn\_itsm\_chg\_admin.cab\_config|Grants access to configure Change Advisory Board membership, meeting schedules, and approval policies.|
|sn\_itsm\_chg\_admin.change\_models\_config|Grants access to configure change models, approvals, and change type behaviors.|
|sn\_itsm\_chg\_admin.change\_schedules\_config|Grants access to configure change windows, blackout periods, and maintenance schedules.|
|sn\_itsm\_chg\_admin.notification\_config|Grants access to configure notifications.|

**Note:** The parent role \(sn\_itsm\_chg\_admin.admin\) uses the dotted suffix pattern, while child roles follow a underscore suffix pattern \(for example, sn\_itsm\_chg\_admin.team\_roles\_config\). This is an intentional naming convention, not a typo.

-   **[Configure team roles for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-team-roles-for-change-management.md)**  
Assign the right people to the right roles in Change Management so your team can approve, implement, and manage changes with the correct access. Team roles control who can approve, build, or review a change.
-   **[Configure risk for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-risk-change-mgmt.md)**  
Set up risk assessment questions, scoring thresholds, and risk levels so that the system can automatically evaluate the risk of a proposed change and route it to the appropriate approval workflow. Configuring risk helps your organization make consistent, data-driven decisions about change requests without requiring ITIL expertise.
-   **[Configure Change Advisory Board for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-cab-change-management.md)**  
Set up your Change Advisory Board \(CAB\) in the setup wizard to define who reviews and approves significant changes before they are implemented.
-   **[Configure change models for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-change-models-scm.md)**  
Configure the change models that control how Normal, Standard, Emergency, and Change Registration changes are processed in Simplified Change Management.
-   **[Configure schedules for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-schedules-for-simplified-change-management.md)**  
Create and manage blackout and maintenance schedules for Change Management to control when changes are permitted or blocked across your organization.
-   **[Configure notifications for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-notifications-for-simplified-change-management.md)**  
Add and manage notifications for Change Management to keep users informed about approvals, status updates, and task assignments at key steps in the change process.

**Parent Topic:**[Configuring the fulfiller experience in Simplified IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configuring-fulfiller-experience-ai-native-itsm.md)

