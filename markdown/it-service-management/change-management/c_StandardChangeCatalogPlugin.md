---
title: Standard change catalog
description: Standard changes are pre-approved, low risk changes with a proven history of success. The standard change catalog contains the changes that have been approved by the Change Management application as standard changes.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Change Management, IT Service Management]
---

# Standard change catalog

Standard changes are pre-approved, low risk changes with a proven history of success. The standard change catalog contains the changes that have been approved by the Change Management application as standard changes.

Users with the ITIL role can view the list of available standard changes and submit change requests.

A property controls whether the selection of a standard change request from the catalog inserts the change request record into the database. An administrator can select the **Two step** check box in Standard Change Properties. This property requires the requester to click **Submit** to insert the change request record.

Standard changes are logically grouped under specific categories. The Change Management application uses a proposal process to control which changes become available in the standard change catalog.

The standard change catalog enables you to perform the following activities:

-   Request, review, and approve standard change templates.
-   Request preapproved standard changes.
-   Determine access to standard change templates at the user level.

You can propose, modify, and retire standard change templates based on the requirements of your organization.

## Pre-approved standard changes

Submitting a change request from a standard change template ensures that pre-approved information is automatically populated in the necessary fields. Standard changes are submitted more quickly and fulfillment can be expedited.

**Note:** You cannot mass-update a set of Configuration Items \(CIs\) in standard changes. However, you can propose individual changes.

## Determine access to standard change templates at the user level

Standard change templates are logically grouped under specific categories. These categories are displayed to users based on user criteria such as user role, geographical location, and department.

**Note:** You must have read access to the standard change template. Please ensure you have the correct roles to access the templates.

-   **[Configure standard change catalog properties](../task/t_ConfigureTheStandardChangeCatalog.md)**  
Configure the standard change catalog through the standard change properties.
-   **[Create a standard change task template](../task/create-a-standard-change-task-template.md)**  
You can create a change task template to add to a standard change proposal. If the standard change proposal is approved, the related change tasks are created when the standard change request is created.
-   **[Attach files to a standard change template](../task/attach-files-change-templates.md)**  
Attach files, such as documents, spreadsheet, and images to a standard change proposal. Standard change templates copy any file attached to the template to a change request that the template creates.
-   **[Modify or retire a standard change template](../task/manage-standard-change-template.md)**  
You can modify and retire standard change templates based on your organization's requirements.

**Parent Topic:**[Configuring Change Management](configure-change-management.md)

