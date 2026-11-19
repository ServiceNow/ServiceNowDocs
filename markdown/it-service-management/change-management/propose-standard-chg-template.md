---
title: Propose a standard change template
description: Propose a new standard change template when you identify a need while creating a change request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-service-management/change-management/propose-standard-chg-template.html
release: yokohama
product: Change Management
classification: change-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Create a standard change task template, Standard change catalog, Configure, Change Management, IT Service Management]
---

# Propose a standard change template

Propose a new standard change template when you identify a need while creating a change request.

## Before you begin

Role required: itil, admin

## About this task

As an IT technician, you can propose a new change template for a change request that you frequently create. This new template is later sent for approval to the change management team, which reviews the request and approves the template as part of the approval process.

**Tip:** In Service Operations Workspace, select the \[Omitted image "list-gray.png"\] Alt text: List icon, and then select **Change Standard Templates** to propose new template. For more information, see 

## Roles for standard change proposals

The following roles apply to standard change proposal templates:

-   `itil`: Submit a new standard change proposal template.
-   `change_manager`: Review and approve the submitted proposals.
-   `sn_change_write`: Create and edit standard change templates.
-   `admin`: Perform all standard change proposal actions.

For the complete role list, see [Components installed with ITSM Roles - Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-service-management/change-management/installed-with-cm-itsm-roles.md).

## Procedure

1.  You can propose a standard change template by navigating to **Change** &gt; **Standard Change** &gt; **Standard Change Catalog** &gt; **Template Management** &gt; **Propose a new Standard Change Template** and filling in the fields on the form.

    |Field|Description|
    |-----|-----------|
    |Short description|Short description of the standard change proposal template.|
    |Requester|User who requests the standard change template.|
    |Category|Category under which the template is published. For example, Server Standard Changes.|
    |Assigned to|User assigned to change requests created from the standard change template.|
    |Configuration item|Configuration item affected by change requests created from the standard change template.|
    |Sample Change Requests|Change requests provided as samples for the change that you propose. The Change Management team reviews the requests as a part of the approval process.|
    |Change Request values|Default field values applied to change requests created from the standard change template. The available fields are governed by the catalog properties. For more information, see[Configure standard change catalog properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-service-management/change-management/t_ConfigureTheStandardChangeCatalog.md)|

2.  Select **Save**.

    The proposal is created with the status **New**.

3.  Select **Request Approval**.

    After you submit the proposal, the status changes to **In Progress** and the Change Management team reviews the sample change requests. The team either approves or rejects the template.

    When the team approves or rejects the template, the system automatically notifies members of the Change Management group. The proposal remains in **In Progress** status until the review is complete.

    -   **Approved:** The template publishes to the Standard Change Catalog and is set to available for creating standard change requests.
    -   **Rejected:**The proposal reverts to **New** status for modifications.
4.  Create a standard change template from a change that exists by completing the following steps.

    1.  Navigate to **Change** &gt; **Open** and select the change whose information you want to use in the standard change template.

    2.  Open the form context menu and select **Propose a Standard Change Template**.

    **Note:**

    -   Any change tasks that are included with the change also get copied to the new standard change proposal. The fields copied from both the change and change tasks are defined in the [Standard Change Properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-service-management/change-management/t_ConfigureTheStandardChangeCatalog.md).
    -   By default, approval records are created for members of the Change Management group.
    Alternatively, as a change manager, create and submit a standard change proposal that can be utilized as a template to draft a standard change request that occurs frequently and is of low risk. By default, the basic standard change proposal workflow sends approval records to members of the change management group where the members verify and modify the records, as appropriate. Navigate to **Change** &gt; **Standard Change** &gt; **My Proposals**. Select **New**, fill the form, and then select **Submit**.

    To view standard change templates, users must have the appropriate roles. Users with the following roles can view the standard change templates:

    -   admin
    -   change\_manager
    -   sn\_change\_write
    -   itil

## Result

A new template record is created for use.

**Parent Topic:**[Create a standard change task template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-service-management/change-management/create-a-standard-change-task-template.md)

