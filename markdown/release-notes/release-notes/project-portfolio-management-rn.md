---
title: Project Portfolio Management release notes
description: The ServiceNow Project Portfolio Management application enables you to create and manage a wide range of planning items from a few small tasks to large portfolios of projects. Project Portfolio Management was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
---

# Project Portfolio Management release notes

The ServiceNow® Project Portfolio Management application enables you to create and manage a wide range of planning items from a few small tasks to large portfolios of projects. Project Portfolio Management was enhanced and updated in the Zurich release.

## Project Portfolio Management highlights for the Zurich release

-   Synchronize resource assignment dates with the project end dates, and end resource assignments automatically when a project reaches its end date.
-   Manage all project-specific resource assignments in one place by accessing the resource page directly from Project Workspace.
-   Identify similar demand records based on contextual similarity in the name, description, and business case content using the identify similar records Now Assist skill.
-   Convert demands to Enterprise Agile Planning \(EAP\) entities, such as Epic, Feature, or Capability, directly from Demand Management.

See [Project Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/c_ProjectPortfolioSuite.md) for more information.

## New in the Zurich release

-   **[Managing projects with Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/use-projects-pw.md)**
    -   End resource assignments when a project ends, view assignment details, and synchronize assignment dates with project dates.
    -   Access and edit the resource details directly from the Resource page without switching between views.
-   **[Identify similar records using Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/identify-similar-demand-records.md)**

    Detect similar existing demand records when creating or editing a demand using the identify similar records skill. This skill compares the **Name**, **Description**, and **Business Case** fields for contextual similarity.

-   **[Convert demands to EAP entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/t_CrtArtftDmdMnu.md)**

    Convert your demand records quickly to Enterprise Agile Planning \(EAP\) entities, such as Epic, Feature, or Capability. When you convert a demand, the system generates a new record of the selected entity type, replicates common fields from the demand, and moves the demand to the Approved state.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Project Workspace UI changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/update-resource-assignment-pw.md)**

    The following items were added to Project Workspace:

    -   Resource page to access and manage resource assignments.
    -   **Sync all** button to synchronize project dates for all the resource assignments.
-   **[Demand Management UI changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/demand-form.md)**
    -   The Artificial Intelligence value has been added to the **Investment Type** field of the Demand form so you can choose AI as an investment type.
    -   Three values, EAP Epic, EAP Feature, and EAP Capability, have been added to the **Type** field in the Demand form. These options are available only when the value in the **Category** field is set to **Strategic**.
    -   An option to create the selected type of EAP entity has been added under Related Links in the Demand form. This option is available when the demand is in the Draft state and until an EAP entity is created.
    -   The EAP Details section has been added to the Demand form. This section is displayed after the demand is in the Draft state and includes two fields:

        -   **Team**: Choose a team for the EAP entity.
        -   **Converted to**: Name of the created EAP entity after it's generated.
        After the EAP entity is created, both fields are set to read only.

    -   The following items have been added to the demand form and are available if you have the identify similar records Now Assist skill activated:
        -   The **Identify similar demands** button, which identifies and displays similar demands.
        -   The Similar Demands related list, which displays the list of similar demand records identified by Now Assist.

## Deprecations

-   **[Resource Management reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/c_UsingResourceManagementReports.md)**

    Starting with the Zurich release, Resource Management reports are deprecated. You can start using the interactive Overview dashboard in Resource Management Workspace to work on reporting.

    For more information on the Overview dashboard, see [Using Resource Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/using-rmw.md#section_v4k_rtg_1fc).

-   **[Resource Management classic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/c_ResourceManagement.md)**

    Starting with the Zurich release, the Resource Allocation workbench and Capacity planning overview are removed from the product navigation of Resource Management for new customers.


## Activation information

Project Portfolio Management is available with activation of the PPM Standard \(com.snc.financial\_planning\_pmo\) plugin. For more information on activation, see [Activate PPM Standard \(Project Portfolio Management\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/t_ActivateProjectPortfolioSuiteWithFinancials.md).

Install Strategic Spend Tracking for PPM by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/project-workspace-landing-page.md)**

    See the Project Workspace documentation for more details about using ServiceNow Workspace in Next Experience.

-   **[Use Resource Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/using-rmw.md)**

    You can use Resource Management Workspace to manage resource assignments as a replacement for Allocation workbench.

-   **[Capacity Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/using-cap-plan-spw.md)**

    Use the Capacity in Strategic Planning Workspace to generate user capacity as a replacement for Capacity planning overview.

-   **[ServiceNow Otto for Strategic Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/now-assist-spm.md)**

    Now Assist enables you to use generative AI skills in multiple SPM apps. With ServiceNow Otto for SPM, identify similar demand records to avoid duplication and redundancy.


**Parent Topic:**[Strategic Portfolio Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/it-business-management-rn-landing.md)

