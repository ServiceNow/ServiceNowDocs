---
title: Configure change models for Simplified Change Management
description: Configure the change models that control how Normal, Standard, Emergency, and Change Registration changes are processed in Simplified Change Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/configure-change-models-scm.html
release: australia
product: IT Service Management
classification: it-service-management
topic_type: task
last_updated: "2026-05-18"
reading_time_minutes: 3
keywords: [change models, configure change model, simplified change management]
breadcrumb: [Configuring Simplified Change Management, Configuring the fulfiller experience in Simplified IT Service Management, Configure integrations and ITSM experiences in Simplified IT Service Management, Configure and integrate, Simplified IT Service Management, IT Service Management]
---

# Configure change models for Simplified Change Management

Configure the change models that control how Normal, Standard, Emergency, and Change Registration changes are processed in Simplified Change Management.

## Before you begin

The groups, assignment groups, and notification recipients you plan to assign must already exist in the system.

Role required: sn\_itsm\_chg\_admin.change\_models\_config, sn\_itsm\_chg\_admin.admin, or admin

## About this task

Simplified Change Management includes four configurable change models. Each model defines the states, approvals, and task behaviors for its change type:

-   **Normal**

    CAB-governed workflow for planned changes that require risk assessment, approvals, and post-implementation review.

-   **Standard**

    Pre-approved, low-risk, repeatable changes that use approved templates and bypass the full approval workflow.

-   **Emergency**

    Fast-track workflow for urgent changes requiring expedited authorization. Restricts who can submit and notifies stakeholders on creation.

-   **Change Registration**

    Records changes implemented outside the standard workflow. Restricts who can register and notifies stakeholders on creation.


When you activate the ITSM Change Management Admin Experience plugin \(sn\_itsm\_chg\_admin\), the simplified change models become the active defaults and the classic global models are deactivated. For more information, see [Change model defaults for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-model-defaults-for-simplified-change-management.md).

## Procedure

1.  Navigate to **Admin** &gt; **Admin Home**.

2.  From the **Manage your products** section, select **View product overview** for IT Service Management.

3.  On the Product Hub page for IT Service Management, from the **Configure your product** section, select **Configure**.

4.  On the Configuration Console page, from the navigation panel, select **ITSM fulfiller experience** &gt; **Change Management** &gt; **Change models**.

5.  From the **Change models** list, select the model to configure.

    |Model|What to configure|How to configure|
    |-----|-----------------|----------------|
    |**Normal**|Adjust availability, risk-based approvals for the Assess and Authorize states, templates, and automatic change task creation.|[Configure the Normal change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-normal-change-model-scm.md)|
    |**Standard**|Manage pre-approved templates. Availability, approval, and task settings don't apply to Standard changes.|[Configure the Standard change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-standard-change-model-scm.md)|
    |**Emergency**|Restrict submitter access, configure Authorize approvals, set up stakeholder notifications, and control automatic task creation.|[Configure the Emergency change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-emergency-change-model-scm.md)|
    |**Change Registration**|Restrict who can register external changes and configure notification recipients.|[Configure the Change Registration change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-change-registration-model-scm.md)|

6.  Expand the **Advanced configuration** section to access and adjust additional settings.

7.  After you configure all required change models, select **Mark as configured** to complete the change model configuration.


-   **[Configure the Normal change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-normal-change-model-scm.md)**  
Configure the Normal change model to define availability, approval requirements, templates, and change task behaviors.
-   **[Configure the Standard change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-standard-change-model-scm.md)**  
 Configure the Standard change model to manage the pre-defined templates that requesters use to create Standard changes.
-   **[Configure the Emergency change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-emergency-change-model-scm.md)**  
Configure the Emergency change model to define who can submit emergency changes, set up stakeholder notifications, configure approvals, and control automatic change task creation.
-   **[Configure the Change Registration change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-change-registration-model-scm.md)**  
Configure the Change Registration change model to define who can register external changes and configure stakeholder notifications.
-   **[Change model defaults for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-model-defaults-for-simplified-change-management.md)**  
When you activate the ITSM Change Management Admin Experience plugin \(sn\_itsm\_chg\_admin\), the simplified change models become the active defaults and the classic global models are deactivated.

**Parent Topic:**[Configuring Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configuring-change-management-experience-in-it-service-management.md)

