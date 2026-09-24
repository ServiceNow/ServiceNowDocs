---
title: Configuring Change Management
description: You can configure various aspects of Change Management based on the specific requirements of your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/configure-change-management.html
release: brazil
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Change Management, IT Service Management]
---

# Configuring Change Management

You can configure various aspects of Change Management based on the specific requirements of your organization.

The ITSM guided setup provides a sequence of tasks that help you configure Change Management on your ServiceNow instance. To open ITSM guided setup, navigate to **Guided Setup** &gt; **ITSM Guided Setup**. For more information about using the guided setup interface, see [Using guided setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/guided-setup.md).

-   **[Change Management plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/change-plugins.md)**  
You can activate one or more of the Change Management plugins if they are not already active. Some plugins include demo data.
-   **[Standard change catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/c_StandardChangeCatalogPlugin.md)**  
Standard changes are pre-approved, low risk changes with a proven history of success. The standard change catalog contains the changes that have been approved by the Change Management application as standard changes.
-   **[Enhanced Change data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/change-data-model.md)**  
The enhanced Change data model supports better categorization, change model linkage, and role-based access to change templates. This new data model does not impact the existing standard change catalog and no migration of existing standard changes is required.
-   **[Create a Change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/create-a-change-model.md)**  
Create change models to configure the states and transitions to match your organization's change processes.
-   **[ITIL change process assignment for change models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/itil_change_process_models.md)**  
The change model specifies which ITIL change process it represents: Normal, Standard, or Emergency. The change is still governed by the model.
-   **[Scaled change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/scaled-change-overview.md)**  
Scaled Change extends change management to complex environments with many configuration items. A single Scaled Change generates and coordinates child change records for every affected configuration item. It uses scheduling intelligence, conflict detection, and approval workflows to keep large-scale changes on track from planning through closure.
-   **[Change schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/change-schedule.md)**  
The Change Schedules landing page provides a view of schedules that are categorized under **Pinned Schedules**, **Your Schedules**, and **All Schedules**. The grouping of schedules provides easy access to your most required schedules and saves your time from searching through all the schedules in the system.
-   **[Configure ability to copy a change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/configure-copy-change-request.md)**  
You can configure the ability to copy a change request record and its details using system properties.
-   **[Create a change request template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/create-a-change-request-template.md)**  
You can create a template that can be used to create change requests with pre-defined supporting tasks. Templates simplify the process of submitting new records by populating fields automatically.
-   **[Create a change request assignment rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/t_DefineAnAssignRuleForChange.md)**  
You can define assignment rules to automate the process of assigning change requests to the appropriate group or individual.
-   **[Add a new change request type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/t_AddNewChangeType.md)**  
You can add a new change type to your change process. There are several processes involved with adding a change type. These processes include managing script includes and workflows.
-   **[Extend or disable multiple CI association](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/t_ExtendMultipleCIAssociation.md)**  
The ability to associate multiple CIs to a task can be extended to other types of tasks. You can also disable multiple CI association from the related lists on change request records.
-   **[State model and transitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/c_ChangeStateModel.md)**  
Change Management offers a state model to move and track change requests through several states.
-   **[Conflict detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/c_ConflictDetection.md)**  
Conflict detection identifies potential scheduling conflicts for a change request based on the configuration items, and planned start and end date or the change. If a scheduling conflict exists, conflict detection also checks any related blackout or maintenance schedules and other active change requests to determine the scheduling conflict.
-   **[Change lockdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/change-lockdown.md)**  
Change lockdown allows change managers to pause all or a subset of in-flight change requests. Use it during major unplanned IT, critical, or financial events.
-   **[Compliance dynamic schema](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/compliance-dynamic-schema.md)**  
Compliance dynamic schema stores the risk and compliance details of a change as name and value pairs in a single field. This avoids adding a column to the Change Request table for each detail.
-   **[Change success score](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/change-success-score.md)**  
Use team historical data for insights into team performance. The score value helps you to determine how likely the team is to complete your change request without issues.
-   **[Predictive Intelligence for Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/change-mgmt-intelligent-solutions.md)**  
The Predictive Intelligence for Change Management capability uses machine-learning algorithms to suggest standard templates, identify similar incidents, and enhance risk assessment for the change.
-   **[Applying CSDM guidelines to Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/itsm-change-use-case-product-view.md)**  
Change Management lets you control every aspect of the IT change process from creation to approval. When you have accurate information, you can minimize risks to your business and avoid conflicts with scheduling. The goal of this product view is to help you to understand how Change Management key entities work with the core CSDM framework.

**Parent Topic:**[Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/c_ITILChangeManagement.md)

