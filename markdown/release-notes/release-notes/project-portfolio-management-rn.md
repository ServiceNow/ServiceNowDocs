---
title: Project Portfolio Management release notes
description: The ServiceNow Project Portfolio Management application enables you to create and manage a wide range of planning items from a few small tasks to large portfolios of projects. Project Portfolio Management was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
---

# Project Portfolio Management release notes

The ServiceNow® Project Portfolio Management application enables you to create and manage a wide range of planning items from a few small tasks to large portfolios of projects. Project Portfolio Management was enhanced and updated in the Australia release.

## Project Portfolio Management highlights for the Australia release

-   Update the idea and demand-related system properties by using the idea\_admin or pps\_admin roles.
-   Link AI systems to demands in Demand Management.
-   Generate a concise summary of a demand by using the demand summarization skill.

See [Explore Project Portfolio Management](https://www.servicenow.com/docs/access?context=explore-project-portfolio-management&version=australia&pubname=australia-it-business-management&ft:locale=en-US) for more information.

## New in the Australia release

-   **[Admin role enhancements in Demand Management](https://www.servicenow.com/docs/access?context=c_DemandManagement&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**
    -   Enabling all users to create ideas with a minimum read role added to the **com.snc.idea.universal\_request.copy\_fields** system property.
    -   The **com.snc.idea.universal\_request.copy\_fields** system property can be updated only by users with the idea\_admin or pps\_admin roles.
    -   Help ensure that only authenticated users have access to the bubble chart workbench through the UserIsAuthenticated condition added to the bubble chart workbench ACL \(access control list\).
-   **[Associate AI systems with demands in Demand Management](https://www.servicenow.com/docs/access?context=associate-ai-systems-with-demands&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

    Add and manage AI system associations directly from the **AI Associations** tab in Demand Management. You can select impacted AI systems or create AI systems using related links directly within the demand workflow.

-   **[Summarize demand records with the demand summarization skill](https://www.servicenow.com/docs/access?context=demand-summary-demand-classic&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

    Generate a concise, structured summary of any demand using the demand summarization skill through the **Summarize** button in the demand form. The skill reviews the demand fields and helps create a clear summary of the demand.

-   **[Admin role enhancements in Project Management](https://www.servicenow.com/docs/access?context=r_InstalledWithProjectManagement&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

    The Project properties can be edited only by users with the pps\_admin role.

-   **[Admin role enhancements in Innovation Management](https://www.servicenow.com/docs/access?context=innovation-management-landing&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**
    -   The write role has been added for the **idea.notification.sender.email** and**com.snc.innovation\_management.im\_editor\_attachment\_tag\_id** system properties.
    -   The **idea.notification.sender.email** and **com.snc.innovation\_management.im\_editor\_attachment\_tag\_id** system properties can be added or updated only by users with idea\_admin roles.

## UI changes

-   **[Demand Management UI changes](https://www.servicenow.com/docs/access?context=demand-form&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**
    -   The **Start date** and **Due date** column labels have been renamed **Planned start date** and **Planned end date**, respectively. This change is applicable only for new installations of the Australia version. To ensure continuity, if you’re upgrading to the Australia release from an earlier release, you’ll continue to see the prior labels.
    -   If you have the AI Control Tower plugin installed and the investment type of the demand is set to artificial intelligence:
        -   The **AI Associations** section in the Demand form is displayed. The following fields are included:
            -   **Product**: Enables you to select the product or system that the demand relates to.
            -   **Impacted AI systems**: Links the impacted AI systems with the demand. You can select existing AI systems from the list or remove systems that are no longer relevant.
        -   An option to create an AI system under Related Links in the Demand form is available for users with the sn\_ai\_steward role.

## Changed in this release

-   **[Next Experience for Demand Management](https://www.servicenow.com/docs/access?context=demand-workspace&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

    The new Next Experience for Demand Management provides a unified layout, guided stages, improved navigation, and enhanced capabilities such as Playbooks and Docs integration. As you move to Next Experience for Demand Management, you’ll find it easier to create, review, and manage demands with a cleaner layout and guided actions. The classic UI is still available, but new improvements will appear in the workspace.

    Next Experience for Demand Management is available with the Strategic Portfolio Management \(SPM\) Standard and Pro licenses.


## Removed in this release

-   For Demand Management:
    -   The permission to edit the value of the **dmn\_stakeholder\_register.number** field in the Stakeholder Register \[dmn\_stakeholder\_register\] table has been removed for the admin role.
    -   The admin role ACL has been removed for the bubble chart workbench.
    -   The duplicate app module that was created for the admin role has been removed.

## Deprecated features

-   Starting with Australia release, Scenario Planning for PPM \(com.snc.ppm\_scenario\_planning\) is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

    Alternatively, Strategic Planning Workspace \(for SPM pro users\) or Portfolio Planning Workspace \(for SPM standard users\) provides the Scenario Planning capability. For details, see [Scenario planning in Strategic Planning](https://www.servicenow.com/docs/access?context=scenario-planning-in-strategic-planning&version=australia&pubname=australia-it-business-management&ft:locale=en-US) or [Scenario planning in Portfolio Planning](https://www.servicenow.com/docs/access?context=scenario-planning-in-portfolio-planning&version=australia&pubname=australia-it-business-management&ft:locale=en-US).

-   Starting with Australia release, the Project Status Report \(com.sn\_store\_ppm.mobile\) is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. Alternatively, Project Workspace provides the Status Report capability.
-   Starting with Australia release, the PMO dashboard is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. Alternatively, Execution dashboard provides the PMO dashboard capability.
-   Starting with Australia release, the Investment Portal is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. Alternatively, Portfolio Planning Workspace provides the Investment Portal capability.
-   Starting Australia, Project Workbench is no longer deployed, enhanced, supported or available for activation. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

## Activation information

Project Portfolio Management is a ServiceNow AI Platform feature that is available with activation of the PPM Standard \(com.snc.financial\_planning\_pmo\) plugin. For details, see [Activate PPM Standard \(Project Portfolio Management\)](https://www.servicenow.com/docs/access?context=t_ActivateProjectPortfolioSuiteWithFinancials&version=australia&pubname=australia-it-business-management&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Project Workspace](https://www.servicenow.com/docs/access?context=project-workspace-landing-page&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

    The Project Workspace application provides an intuitive user experience that enables project managers to plan and manage their projects.


**Parent Topic:**[Strategic Portfolio Management release notes](it-business-management-rn-landing.md)

