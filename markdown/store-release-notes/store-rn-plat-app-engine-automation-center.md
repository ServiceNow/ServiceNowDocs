---
title: Automation Center release notes
description: Version history for the App Engine Automation Center application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-plat-app-engine-automation-center.html
release: store
topic_type: reference
last_updated: "2026-04-09"
reading_time_minutes: 10
breadcrumb: [ServiceNow Store - ServiceNow AI Platform App Engine release notes, ServiceNow Store release notes]
---

# Automation Center release notes

Version history for the App Engine Automation Center application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 14.0.1 - April 2026**
    -   Automation Explorer enables you to scan your ServiceNow instance and discover relevant automations based on a targeted query using natural language. You can filter by automation type, execution time period, and application scope, then onboard high-value automations directly to Automation Center for ROI tracking.
    -   For full access to this feature, ensure that Now Assist for Automation Center is installed and that the Saving Estimator skill is activated.
    -   For setup and detailed procedure, see the Automation Center documentation.
-   **Version 13.0.1 - March 2026**
    -   Create an automation request agent
    -   An automation request agent enables you to manage automation request tasks efficiently, eliminating the need for manual intervention. This functionality is available only when the Now Assist AI Agents skill is activated and the automation request is in "In progress" state.
    -   For more information, see the Automation Center documentation.
-   **Version 12.2.0 - December 2025**
    -   Migration Accelerator now supports Blue Prism
    -   With this release, Automation Center’s Migration Accelerator enables the migration of both Blue Prism and UiPath automations into ServiceNow RPA Hub, optimizing costs and minimizing effort.
    -   You can leverage Blue Prism and UiPath automations to generate reports and migrate them directly to the ServiceNow RPA Hub server.
    -   The Insights dashboard offers comprehensive information regarding the extent of manual intervention required to fully migrate automations to ServiceNow RPA Hub. It also highlights the added value that Migration Accelerator brings to business processes by enhancing their efficiency.
    -   For further details, please refer to the product documentation.
-   **Version 9.0.5 - October 2025**

    What's fixed:

    -   Earlier, in some cases, the top 10 applications list did not show results as expected after applying a filter. Now, this issue is resolved.
    -   In Action Center, the actions were not executed if the language was changed to anything other than English. Now, the feature works with all supported languages.
    -   The Business application change widget in the Executions tab, did not show results as expected when the Department filter was used. Now, this works as expected.
    -   In the Active Automations section in the Value tab, the average process success rate displayed a value above 100% indicating a data integrity issue. This has been resolved.
-   **Version 11.0.1 - August 2025**
    -   What's New:
        -   Migration Accelerator introduced
            -   Use the Automation Center’s Migration accelerator to migrate UiPath automations to ServiceNow RPA Hub with reduced cost and effort.
            -   Using the Migration Accelerator, you can perform the following tasks with a few clicks:
                -   Generate reports with your data \(UIpath automations\).
                -   Migrate automations from your server to ServiceNow RPA Hub server.
            -   You can view the details of your automations in the Insights dashboard of Migration Accelerator. Some of the details are:
                -   The estimated time and cost saved due to this migration.
                -   The conversion rate of the migration.
                -   The complexity levels of the migrated automations.
            -   These details give you a fair idea about how much manual work is required for the automations to completely migrate to ServiceNow RPA Hub. It also showcases how the Migration Accelerator adds value to your processes by making them more efficient.
            -   For detailed information, see the product documentation.
        -   Golive checklist feature introduced
            -   This feature enables you to automatically track items that must be reviewed before publishing the automation request. Every Golive checklist is associated with an automation request.
            -   This feature ensures that you do not miss any important checks before publishing an automation request as an automation.
            -   Using this feature, you can create checklists and checklist templates. As part of this feature, a checklist template \(Automation Deployment Checklist\) is provided out of the box.
            -   Only a user who has the automation center admin role \(sn\_ac.automation\_admin\) has access to create and update a checklist and checklist template. The technical user can only view the checklist and update the states. The business user has no access to the Golive checklist.
            -   For detailed information, see the product documentation.
            -   Migration Accelerator Known Issue
                -   When a technical user or business user tries to either upload a ZIP file or provide an URL when generating the migration report, an error message is displayed in the All automations tab
                -   You can ignore the message and proceed with the next steps.
-   **Version 9.0.1 - May 2025**
    -   Domain separation supported for Automation Center
    -   Domain separation is supported for Automation Center.  Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
    -   Action Center encounters challenges due to process separation in flows. In Action Center, the domain data from both global and current session domains is displayed.
    -   The summary execution table displays data about executions of the automations for the domain where they are created and not where they are executed. For example, if an automation is created in the parent domain and executed in the child domain, it will display the data in the parent domain. You cannot see this execution data in the child domain.
    -   Automation requests created from Service portal are listed under Requests tab
    -   In the previous releases, when you created an automation request from the Service portal, the automation request was visible only from Automation Center. From this release, any automation request created from Service portal is visible from the Requests tab of the Service portal as well as from Automation Center.
-   **Version 8.0.2 - February 2025**
    -   New: Connection Manager: Connection Manager enables you to import data from a third-party tool into Automation Center tables by correctly mapping and testing the data import. This process is highly efficient and requires just a few clicks. For detailed information, see the Automation Center documentation.
    -   New: Ability to display Integration Hub data in Automation Center dashboard: Information from Integration Hub is now available for viewing and analysis in the Automation Center dashboard. The details are displayed in the Overview and Executions dashboards of the Automation Center Workspace for the technical user and administrator.
-   **Version 7.0.8 - December 2024**
    -   For the Client-Callable Script Include \(CCSI\) sandbox access directive, there were issues affecting the security control. The issue is fixed by adding a field to the Script Includes to explicitly denote opting Script Includes into the sandbox.
    -   Previously, when a technical user navigated from Kanban board, Request board, or Task board to list view, there was an error message. This was caused due to a role-based issue. This issue is now fixed.
    -   There was an issue that caused the technical users to not be able to map automations to the automation requests. This issue is now fixed.
    -   Business users were not able to navigate to Automation Center dashboard. An error message was displayed. Now, business users can navigate to Automation Center dashboard.
-   **Version 7.0.2 - September 2024**
    -   Fixed:
        -   The look and feel of the application is improved for better user experience.
        -   The Granular Integration related list was available even without enabling granular integration. From this version, the Granular Integration related list will be available only after enabling granular integration.
        -   An empty table was installed when Automation center plugin was activated. This has been fixed such that no empty table is created.
        -   Due to an upgrade of the Data Visualization component of the underlying platform, certain widgets were out of place. This misplacement and malfunctioning is fixed now.
-   **Version 7.0.1 - August 2024**
    -   What's new:
        -   New filter in Kanban Board: Filter the requests based on the request type in addition to date, priority, and department. You can choose to filter by automation requests, action requests, or review requests.
        -   Ability to map multiple automation records with one automation request: Map multiple automations with a single automation record.
        -   View data from a more granular level in the Overview dashboard: Enable granular integration in the automations. This will allow you to view the cost saved and time saved data in the Active Automations widget from the item level making it more accurate for ServiceNow RPA. ServiceNow RPA Hub \(10.0.0\) or later is required for this feature
-   **Version 6.0.1 - May 2024**
    -   New:
        -   Action Center introduced: Action Center lists all actions created to fix repeated issues that cause automations to fail in Automation Center. Action Center provides the following benefits:
            -   Manage and execute actions to solve issues that cause automations to fail.
            -   Fix common repeated issues without any dependence on the administrator.
        -   Create actions, action requests, and review requests in Automations Center: You can now create actions, action requests, and review requests in Automation center. A business user can create an action request that will enable the business user to fix issues that cause automations to fail. The technical user or system administrator will then create actions for the business user.
        -   Review requests are created by a developer to review automations by the COE team. This will enable the developer to understand the efficiency and effectiveness of the automation.
    -   Updated:
        -   Kanban Board updated: Earlier, the Automation Center Kanban board provided an easy access to view and manage only automation requests and automation tasks. In addition to automation requests and automation tasks, Kanban Board now provides access to view and manage action requests and review requests.
-   **Version 3.0.6 - March 2024**

    Fixed: Cost and Time saved issues is fixed for flow exections.

-   **Version 5.0.1 - February 2024**
    -   New:
        -   Introduction of Kanban Board: The Automation Center Kanban board provides an easy access to view and manage automation requests and automation tasks from one location.
        -   Integration with Document Intelligence: Automation Center integrates with Document Intelligence enabling you to get the Document Intelligence data into ServiceNow instance. You can analyze the data from Document Intelligence using Automation Center.
        -   Configuration of automation summary execution: Configure the execution summary of automation to specify how automation data is aggregated and presented on the Automation Center dashboard. You can import and configure data from various sources, such as RPA, ServiceNow flows, Document Intelligence \(DocIntel\), and others to view in the Automation Center dashboard.
    -   Updated: Track ServiceNow actions as automations: Earlier, only ServiceNow flows could be tracked as automations. From this release, ServiceNow actions can also be tracked as automations.
    -   Deprecated: Deprecated resource creation: From this release, the resource creation for every automation request is deprecated.
-   **Version 3.0.0 - August 2023**

    Changed: Renamed "Recommended Actions" contextual panel to "Recommendations" along with added options to either dismiss or view details of the recommendations.

-   **Version 2.0.3 - May 2023**
    -   Changed: New rules added for third party execution records.
    -   Fixed:
        -   In Execution Summary table, cost save per run and time save per run will capture run specific information.
        -   List View changes to identify attribute record association with robot or process.
        -   Published date issue fixed for third party applications on attribute tables.
        -   Data issue fixed for Goals widget.
-   **Version 2.0.1 - February 2023**
    -   New:
        -   Introduced Value Dashboard:
            -   Tracks goals associated with automation requests.
            -   Provides actual cost saving, time saving, average process success rate for active automations.
            -   Displays expected cost and time saving for future automations.
        -   Prioritization using ServiceNow Spotlight feature:
            -   Enables you to view automation requests by the order of priority done by Spotlight feature using the "Score" field.
            -   This is an optional opt-in feature.
        -   Enable reusability with ServiceNow Recommended Actions application:
            -   Displays any existing similar automation requests or automations to enable reusability and avoid duplicate effort.
            -   This is an optional opt-in feature.
        -   Automation Center integration with UiPath:
            -   Enables webhook integration for UiPath using Integration Hub spoke to reduce time and effort for implementation.
        -   Automation Center integration with flows:
            -   Enables use of ServiceNow Flows data in Automation Center.
            -   You can pick flows you want to track using "Automation tracker".
            -   Flows picked are automatically published as Automation CI.
        -   Publish any automation as Automation CI:
            -   It's agnostic to publish any automation \(can be 3rd party vendor also\) as Automation CI; its not limited to RPA or Flows.
-   **Version 1.1.2 - November 2022**

    Changed: Column label for Automation requests from 'Rank' to 'Score'.

-   **Version 1.1.0 - August 2022**
    -   Automation Center integrates islands of automation and delivers centralized governance and management of cross-enterprise, multi-vendor automation in a single workspace.
    -   Automation Center enables ServiceNow AI Platform owners, admins, solution architects, process analysts, and developers to view real-time metrics and analytics to understand automation performance vs. business goals, time and cost savings realized, active automations, automation pipeline, and operational health.
    -   Automation Center is uniquely capable of preventing automation failures to maximize uptime across multiple vendors​ by creating CMDB CIs for every robot and bot process with dependency mapping to business applications.
    -   Automation Center 1.0.0 is pre-integrated and works out of the box with:
        -   ServiceNow Process Mining and Service Catalog for automation discovery
        -   RPA Hub for automation executions
    -   Automation Center is a framework designed to:
        -   Support an increasing range of ServiceNow automation solutions going forward such as Integration Hub and Document Intelligence
        -   Integrate with any third-party automation technology. 1.0.0 is pre-tested with UiPath RPA.

