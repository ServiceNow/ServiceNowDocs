---
title: Using Playbooks for Public Sector Digital Services
description: A playbook provides government service agents with step-by-step guidance through the life cycle of a public service request case. Use Playbooks to fulfill requests for license and permits, government records and other public information, or non-emergency service requests.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Using Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Using Playbooks for Public Sector Digital Services

A playbook provides government service agents with step-by-step guidance through the life cycle of a public service request case. Use Playbooks to fulfill requests for license and permits, government records and other public information, or non-emergency service requests.

A playbook takes a workflow and breaks it into multiple stages or lanes. Each stage in a playbook includes one or more activities, or steps, for you to complete. Stages can also include automated activities, such as auto-sending an email to a customer when a stage or activity is complete. When using a playbook, you can:

-   View the playbook stages and activities.
-   Select an activity and perform the work to complete that activity.
-   Mark an activity as complete and move to the next activity or stage.
-   Complete the stages and activities to resolve the case.

The following applications are available with Public Sector Digital Services that enable you to create and use playbooks:

-   [Grants Management](psds-using-grants-management-playbook.md)
-   [Social Benefits Playbook](psds-using-sb-playbooks.md)
-   [License and Permit Playbook](psds-using-lp-playbooks.md)
-   [Information Request Playbook](psds-using-ir-playbooks.md)
-   [Service Request Playbook](psds-using-sr-playbooks.md)

The corresponding playbook for each case type automatically appears in the **Playbook** tab when you create an public service request case as an agent in the CSM Configurable Workspace, or when a constituent puts in a request through the Government Service Portal.

The workflows for a type of case and the activities that you need to resolve these cases are in the playbook. By using a playbook, you can visualize the entire life cycle of the public service case workflow.

![License Permit Playbook.](../image/lpr-example.png)

## Playbook stages

Each playbook contains four stages \(Intake, Review, Process, and Decision\) and several activities in each stage. Below is a diagram illustrating the base playbook workflow. This workflow can be modified to match a specific public service request use case, depending on what your agency offers.

The base Playbook workflow stages are listed in the following table.

|Task|Description|
|----|-----------|
|Intake|Guides you through the record creation process by capturing the details of the request and assigning it to the right agent.|
|Review|Acts as a checkpoint for duplicate cases and provides you with an opportunity to review the case details.|
|Process|Guides you through the activities for request fulfillment.|
|Decision|Captures and communicates the decision and any supporting information to the constituent and any other agents or involved parties.|

## Playbook layout

A playbook is made up of several areas, including the playbook life cycle, the playbook work area, and the contextual side panel. The activity view determines how the stages and activities appear in the playbook.

The default activity view for Playbooks in Public Sector Digital Services is the process-based experience view. This view, which is shown in the following example, shows constituent or business information and case task information at the forefront of the playbook work area as you work on it.

The process-based playbook layout shows the following features:

-   A horizontal stage picker that gives the agent a complete view of the entire process and where they currently are in that process. Agents can use the stage picker to track their overall progress as they work on cases.
-   Record information on the left side of the page, such as the contact information that is always available.
-   Related records in the contextual side panel supported by the dynamic related records component.

![Agent workspace view of the License and Permit Playbook life cycle, case record information, and license request details, shown in the Process-based experience view.](../image/lp-request-process-based-layout.png "Playbook layout with the Process-based Experience")

The following table shows the components shown in the Playbook workspace.

<table id="table_vqh_ygn_b1c"><thead><tr><th>

Playbook area

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Playbook header

</td><td>

-   Appears at the top of the playbook.
-   Shows the title of the playbook and a horizontal stage picker that displays progress through the playbook stages.
-   Includes a filter that you can use to filter the activities by the assigned user or the activity status.
-   Includes the Playbook Actions menu that you can use to select the playbook-level and activity-level actions.

</td></tr><tr><td>

Playbook Lifecycle

</td><td>

-   Appears in a panel on the left side of the playbook.
-   Displays a list of the activities for each stage.
-   With the horizontal stage layout, you can expand or collapse the entire list of activities for the current stage.


</td></tr><tr><td>

Playbook work area

</td><td>

-   Appears in the middle of the playbook.
-   Displays the card for the current activity.

</td></tr><tr><td>

Contextual side panel

</td><td>

-   Appears on the right side of the playbook.
-   Includes the tabs that you can use to display the following types of information:
    -   Case or case task activity stream.
    -   Ribbon information such as the case overview, customer details, timeline, and service level agreements \(SLAs\).
    -   Dynamic related records. For more information, see [Dynamic related records](psds-playbook-viewing-rel-records.md).

</td></tr><tr><td>

Case Information Contact Card

</td><td>

-   Contact information for the constituent or business that submitted the request.
-   Appears in a panel on the left side of the playbook.

</td></tr><tr><td>

Service Request Map Card

</td><td>

-   **Service Request Playbook only**
-   New component of the process-based playbook layout.
-   Appears after the intake stage, if the sn-geo-map plugin is installed, and Google API key is configured.

</td></tr><tr><td>

Items Received Card

</td><td>

-   **License and Permit Playbook only**
-   Appears on the left side of the playbook.
-   Shows licenses/permits that are active, expired, and expiring soon, and the time remaining on each one.

</td></tr></tbody>
</table>## Public Sector Digital Services Playbooks

The Public Sector Digital Services platform includes the following playbooks:

-   **[Social Benefits Playbook](psds-using-sb-playbooks.md)**

    The Social Benefits Playbook application provides an end-to-end workflow for handling requests for social benefits submitted by public sector end users. The application includes the following:

    -   Packaged playbook that deploys out of the box case types, playbooks, business logic, SLAs, notifications and more to automate workflow to orchestrate the process​ and help agents resolve requests faster and efficiently.
    -   Customizable catalog of pre-built social benefit options that constituents and businesses can choose from on the Government Service Portal.
    -   Extendable data model through service definitions.
-   **[License and Permit Playbook](psds-using-lp-playbooks.md)**

    The License and Permit Playbook application provides an end-to-end workflow for handling license and permit requests submitted by public sector end users. The application includes the following:

    -   Packaged playbook that deploys out of the box case types, playbooks, business logic, SLAs, notifications and more to automate workflow to orchestrate the process​ and help agents resolve requests faster and efficiently.
    -   Customizable catalog of pre-built license and permit request options that constituents and businesses can choose from on the Government Service Portal.
    -   Extendable data model through service definitions.
-   **[Information Request Playbook](psds-using-ir-playbooks.md)**

    The Information Request Playbook application provides an end-to-end workflow for handling public record and information requests submitted by public sector end users. The application includes the following:

    -   Service catalog of pre-built, information request options that constituents and businesses can choose from on the Government Service Portal.
    -   Automated workflow process that agents use to resolve information requests faster and efficiently.
    -   If using Advanced Work Assignment, an Information Request service channel that admins can use to automatically route information requests to designated agents.
-   **[Service Request Playbook](psds-using-sr-playbooks.md)**

    The Service Request Playbook application provides an end-to-end workflow for handling non-emergency service requests submitted by public sector end users. The application includes the following:

    -   Service catalog of pre-built, non-emergency request options that constituents and businesses can choose from on the Government Service Portal.
    -   Automated workflow process that agents use to resolve non-emergency service requests faster and efficiently.
    -   If using Advanced Work Assignment, a Service Request service channel that admins can use to automatically route non-emergency service requests to designated agents.
    -   Pre-built Virtual Agent conversation topic that enables constituents and businesses to use Virtual Agent to submit non-emergency service requests.

For more information on installing and configuring Playbooks for Public Sector Digital Services, see [Configuring Public Sector Digital Services](configuring-public-sector-digital-services.md).

