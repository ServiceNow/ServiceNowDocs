---
title: Process Mining release notes
description: Version history for the Process Mining application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-nowintel-process-optimization.html
release: store
topic_type: reference
last_updated: "2026-05-05"
reading_time_minutes: 15
breadcrumb: [ServiceNow Store - Platform Analytics release notes, ServiceNow Store release notes]
---

# Process Mining release notes

Version history for the Process Mining application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 29.7.9 - May 2026 \(Australia\)**
    -   No configuration changes required. All improvements take effect automatically.
        -   Now Assist Intent &amp; Activity Analysis
            -   Removed duplicate results on filtered models
            -   Improved load performance on larger datasets
        -   Project Setup — Breakdown recommendations no longer suggest breakdowns that are already configured
        -   Analyst Workbench
            -   Show Records on MDM intermodal arcs now navigates to the correct table
            -   Automated finding definitions can now be submitted with the left nav search panel open
        -   Opportunity Details Page — Removed the non-functionalViews option, which was never intended to appear here
        -   Automation Center — Newly created requests now appear immediately in theAutomation Request tab
        -   Process Mining for Playbooks — Resolved several data accuracy issues on project cards and the Analyst Workbench
-   **Version 28.9.9 - May 2026 \(Zurich\)**

    - Made the Process Mining App free on store, which was necessary as Process Mining is auto installed on all instances.

-   **Version 29.7.5 - March 2026 \(Australia\)**
    -   New:
        -   Parallel processing for playbook data introducedAnalyze ServiceNow Playbooks, including their stages and individual activities using Process Mining.
        -   Process Step filter \(Previously Transition filter\) &amp; Rule-based Findings enhancedUtilize the enhanced process step filter and rule-based findings to unlock new use cases and drive better process optimization outcomes through additional features and improved usability.
        -   Intent and Activity Analysis
            -   Enables you to efficiently summarize \(human\) agent tasks and their sequence in relation to problem types, allowing pinpointing areas for improvement and taking concrete actions to optimize their processes.
        -   Mining Agentic AI logs
            -   Create a process mining project on Agentic AI data logs by selecting the designated source from a readily available template.
        -   Integration with Task Mining
            -   Analyze the activities of workstation users to gain insights on the time they spend and the activities they perform on tasks. This helps uncover inefficiencies, standardize best practices, and identify automation opportunities, ultimately improving productivity, compliance, and process consistency.
            -   New automated findings introduced
            -   Multidimensional project filtersFilter multidimensional projects based on child breakdowns and variants.
            -   Evaluation project for security operations available
            -   Multidimensional maps are supported on the Opportunity details page and Platform Analytics components.
-   **Version 28.9.5 - March 2026 \(Zurich\)**
    -   Fixed:
        -   Ability to edit configurable values of automated findings by analysts
        -   Process steps filter prefilling issue
        -   Intermittent alert message issue on Highlights
        -   Process steps filter with multiple OR conditions
-   **Version 28.9.3 - January 2026 \(Zurich\)**

    Fixed: Filtering task progress on the process mining graph component on the PA dashboards- Mining failure when Automated findings have empty configuration values- Generating Automation opportunities issue- Opportunity details page - fixed Number of variants, average record duration and total accumulated record duration values- Ability to view process configuration when users have access to only some of the records- Date/time activity definition creation fixes- Ability to see the Global Search icon in the Process Mining Workspace despite not having the needed roles- Top 5 opportunities type graph is not displaying the improvement opportunity type with the highest records

-   **Version 27.8.1 - January 2026 \(Yokohama\)**

    Fixed: Ability to view process configuration when users have access to only some of the records- Date/time activity definition creation fixes- The top 5 opportunities type graph is not displaying the improvement opportunity type with the highest records

-   **Version 28.8.7 - September 2025 \(Zurich\)**

    Fixed: Data loss issue for rule-based findings- Domain index failures while upgrading- Pagination on Process Configuration list- Slow loading of workspace

-   **Version 27.7.4 - September 2025 \(Yokohama\)**

    Fixed: Data loss issue for Rule-based improvement opportunities- Pagination on Process Configuration list on Process Mining Workspace

-   **Version 26.16.14 - September 2025 \(Xanadu\)**

    Fixed: Data loss of Rule-based Improvement opportunities and auditing

-   **Version 28.8.2 - August 2025 \(Zurich\)**
    -   Opportunity details page
        -   This page provides detailed improvement opportunity context and surfaces key drivers behind process patterns that accelerate decision-making and prioritization of process changes.
        -   Idle time analysis Analyze where cases are waiting to be assigned to agents by tracking and analyzing the time during which the case is assigned to a team but not yet to an agent. Idle time analysis helps identify inefficiencies, such as delays in task assignment or workflow bottlenecks, and helps improve coordination and reduce waiting time within processes. Idle time analysis must be configured in the process configuration.
    -   Touchpoint analysis
        -   Identify where and how human involvement occurs in a process by using touchpoint analysis. Analyzing the fields that involve human involvement helps you improve your processes, enhancing performance and reducing operational costs. Touchpoint analysis enables you to analyze the workload of transitions and cases. Touchpoint analysis must be configured in the process configuration.
    -   Enhanced data security
        -   Mark a project as restricted to help protect sensitive data and avoid security breaches. Restricted project data is available only to the owner and the users with whom the project is shared. - Share a Process Mining project Share projects through a link that remains unchanged even when the project is updated and remined. - Creation of automation requests and CIMs simplified When creating an automation or Continual Improvement Management \(CIM\) request from Process Mining, mandatory fields are pre-populated, reducing friction and accelerating time-to-action.
    -   Process Mining integrated with ServiceNow playbook
        -   Process Mining has been integrated with ServiceNow playbook. After analyzing and identifying a process for improvement, export the process to playbook and add subflows or triggers to analyze and refine the flow.
        -   Use the Playbooks icon on the Process Mining Analyst Workbench to export up to 5 routes of a project to ServiceNow playbook. This feature is enabled by Now Assist.
-   **Version 27.7.2 - July 2025 \(Yokohama\)**
    -   Fixed:
        -   Project setup's overview page loading issue for performance analytics projects
        -   Using contextual activity in the transition's context
        -   Shows relevant errors after mining
        -   Edit option on Evaluation projects
        -   Evaluation project copy accessible for no-role users
        -   Multitable inter-entity occurrence count
-   **Version 26.16.12 - July 2025 \(Xanadu\)**
    -   Fixed:
        -   Project setup's overview page loading issue for performance analytics projects
        -   Process configuration visibility when imported from content packs
        -   Evaluation project fixes
        -   Multitable inter-entity arcs appear when collapsed
        -   Automated Improvement opportunities filter icon issues
-   **Version 27.6.3 - May 2025 \(Yokohama\)**
    -   Fixed:
        -   Evaluation project issues
        -   Transitions with OR condition, 0-second maximum constraint issue
        -   Duplicate child tables in use cases in project creation
        -   Top 3 KPIs by \# records widget issue
        -   Histogram popup percentage values
        -   Project setup transition filters to now allow Process Start and End
        -   Archived project's activity grouping by default is fixed
-   **Version 26.16.8 - March 2025 \(Xanadu\)**
    -   Fixed:
        -   Ability to edit transitions
        -   Transitions constraint max duration set to zero issue
        -   Applied filter count and RCA issues
        -   Evaluation project fixes
        -   Security fix
-   **Version 27.6.1 - February 2025 \(Yokohama\)**

     

    -   New:
    -   Process configuration builder:  Configure and view the process configurations efficiently using the new comprehensive process configuration builder.
    -   Content pack importer for process configurations: Import and customize the content pack process configuration templates to activate new features. Content pack process configuration templates are now read-only.
    -   Process Mining evaluation projects for HR and CSM: Ability to try out the sample mining and limited features available for HR and CSM without an entitlement. You can purchase a license for the advanced features.
    -   Enhanced Process Mining Engine
        -   Key updates include:
            -   Defining integer fields as activity definitions.
            -   Grouping journal fields to identify how quickly an agent reacted to an assigned case.
            -   Defining the order of simultaneous activities on the graph.
    -   API for accessing Process Mining data: Create, mine, and access Process Mining data via an API \(ProcessMiningIntegrationAPI\).
    -   Usability improvements introduced:
        -   View the improvement opportunities on the Summary and Insights page as a card view or list view.
        -   Rename the scheduled tasks that help to identify and view a specific result.
    -   Changed:
    -   ACLs update: The ACL rules have been updated for broader visibility on the try-out version while also increasing the security.
        -   No Process Mining role is required to access a shared project and to generate Platform Analytics insights for some tables.
        -   Breakdowns/activity definitions are blocked for certain users based on the column access.
    -   Performance improvements:
        -   Introduced lazy loading of improvement opportunities and variants for faster workspace loading.
        -   Introduced applying a transition filter before mining to reduce scope of data and speed up the mining process.
    -   Enhanced transition filters: The enhanced transition filters now provide more flexibility and precision in filtering the process map by providing the following:
        -   Ability to use OR clause on steps to create a more complex and nuanced criteria for process transitions.
        -   Include predicates like "is empty" and "is not empty" allowing for more refined control over the conditions under which transitions occur, ensuring that workflows are both comprehensive and adaptable to a variety of scenarios.
        -   Ability to select more than one value with a single click that contains a specific text.
-   **Version 26.16.6 - January 2025 \(Xanadu\)**
    -   Fixed:
        -   Fixed Edit transitions
        -   Fixed editing project filter on evaluation projects from guided setup
        -   Fixed disabling "Automation Discovery" for evaluation Project
        -   Fixed Repetition filter for nodes with high repetitions
        -   Removed additional fields from contextual conditions
        -   Fixed results for RCA to apply in the workbench
        -   Fixed Summary and Insights page: Time series Y axis labels, Top 3 KPIs by \# records &amp; opportunities widget stats
        -   Evaluation project RCA/Clustering is not being disabled with more than 100 records
        -   Summary and Insights Improvement Opportunities list: action items stuck in loading
        -   Removed protection policy from left navigation modules/menu
        -   Opening finding definitions not generated link to the correct page
-   **Version 25.7.1 - January 2025 \(Washington DC\)**

    Fixed: Summary and Insights tab Improvement Opportunities list-action items stuck in loading.

-   **Version 26.16.1 - November 2024 \(Xanadu\)**
    -   Fixed:
        -   Guided project setup: Tables list was not loading on the Set Objectives page after Washington to Xanadu upgrade.
        -   Guided project setup: Set Objectives page keeps loading occasionally.
        -   Work notes analysis: Occasionally fails to run due to incorrect ACL.
        -   Rule-based findings: Not all impacted KPIs are shown.
        -   Advanced transitions with constraints: Not giving results for valid conditions.
        -   Clustering results popup: Popup not appearing occasionally.
        -   Archived data source: List of Values drop-down did not show "No results found" in the archived data source.
        -   Repetition or duration histogram: No duration histogram for arcs.
        -   Root Cause Analysis \(RCA\) for Improvement Opportunities: Not able to select any leading influencer to open in the workbench.
        -   Automated Findings: Opening an automated finding in the workbench opens the entire model instead of the improvement opportunity.
        -   Content Packs: Review and Mine page does not load for project shipped as part of a content pack.
-   **Version 25.6.13 - September 2024 \(Washington DC\)**

    Fixed: Addressed the slow loading of Project Guided Setup - Set Objectives page- Analysts can now edit the project's Rule-Based/Automated Improvement opportunity definitions- Automation request option is usable after installing the Automation Center plugin- Process Mining Map Dashboard Widget issues with the wrong theme.

-   **Version 26.13.1 - August 2024 \(Xanadu\)**
    -   Process mining evaluation project for the Incident table.
    -   Sample mining on sub-production instance enabled by default.
    -   Process graph enhanced with perspective: filter the process mining graph by the activity definitions you want to view.
    -   Guided setup for findings: Configure and view automated and rule-based finding definitions efficiently.
    -   Pre-configured use cases for approval and SLA Breach analysis.
    -   Variation analysis into summary and insights page.
    -   Increase the length of the displayed node in the process graph.
    -   Option to filter out incoming or outgoing arcs on the process map.
    -   Ability to view records on the analyst workbench process mining component.
    -   Transition work notes analysis: Create a cluster of records with similar work notes to understand the actual transition reason.
    -   Guided setup for the project:
        -   Ability to toggle between include and excludeall AD values, including the search option
        -   Select and configure multiple breakdowns at once
        -   Dot. walk for activity definitions
        -   Configure compound events
-   **Version 25.6.12 - August 2024 \(Washington DC\)**
    -   Fixed:
        -   Set objectives page very slow to load
        -   Advanced transitions - transition value empty in the condition when it is not present in latest model version
        -   Clustering results pop-up - click on 'Show records' icon is throwing error for Analyst user
-   **Version 25.6.9 - June 2024 \(Washington DC\)**
    -   Fixed:
        -   Fixed missing index on a process mining table \(performance\)
        -   Fixed scheduled task panel getting stuck on loading state
        -   Addressed the summary and insights page's widget issues
        -   Process Mining Map Component theme issues
        -   Fixed task SLA table not showing up in project guided setup
-   **Version 24.6.7 - June 2024 \(Vancouver\)**
    -   Fixes:
        -   Fixed issues in loading more items in the clustering results
        -   Fixed missing index on a process mining table \(performance\)
        -   Fixed scheduled task panel getting stuck on loading state
        -   Addressed the summary and insights page's widget issues
-   **Version 25.6.7 - March 2024 \(Washington DC\)**
    -   Fixed:
        -   Cosmetic fixes in the project builder
        -   Fixed transition filters getting overridden
        -   Blocking the selection of breakdowns with integer type and having no choices
        -   Fixed analyst not being able to create finding constraints
        -   Included total duration on arc popups
-   **Version 24.5.6 - March 2024 \(Vancouver\)**
    -   Fixed analyst not being able to create finding constraints
    -   Fixed issues related to clustering/RCA results in the node/arc popup
    -   Fixed performance issues
    -   Added total duration on arc popup
-   **Version 25.6.3 - February 2024**
    -   New
        -   Guided project setup using project builder
        -   Additional Automated Findings: pattern repetition, slow transitions, extreme arc repetitions, and extreme arc durations
            -   Project metrics dashboard with a trend line to show the average time to completion of records over time \(Time series\)and distribution of records by the time taken to reach the process end \(Histogram\)
            -   Node panel containing incoming and outgoing distribution of records via other nodes
            -   Mining engine changes with dot walked and compound activities
            -   Star node diagram on dashboard component with zoom options and filtering
            -   Mining on archived tables
            -   Performance improvements on process projects and analyst workbench load time and auto retirement of projects resulting in data cleanup
    -   Changed:
        -   KPI Dashboard configured can be viewed by toggling the project metrics dashboard
        -   Filtering on process projects
-   **Version 24.5.3 - December 2023 \(Vancouver\)**
    -   Fixed:
        -   Translation issues on the Process Configuration and Workbench page.
        -   Process Insights and Variation analysis module fixes in workforce optimization.
-   **Version 24.5.2 - November 2023 \(Vancouver\)**
    -   New:
        -   Track the number of actions taken within a project via an easy-to-interpret visual on the summary and insights page \(CIM, notes, automation requests, and saved filter sets\)
        -   Be able to update the improvement opportunity state from new to under review and archived
    -   Changed:
        -   Made the entity canvas slightly transparent to show the inter-entity arcs original and target nodes
        -   Entities do not change position on the process graph when other entities are collapsed or expanded
        -   Initial loading of graph: Outline the position of entities horizontally instead of vertically
        -   Process graph: Minimum &amp; maximum distance between entities
        -   Process graph: Remember the position of entities for the next workbench session
    -   Fixed:
        -   Advanced transition: Right side panel overlapping with advanced transition screen
        -   Advanced transition: Entity table not visible
        -   Process mining system property page not accessible
        -   Finding definitions: Not able to select process configuration/table within rule findings start or stop condition
        -   Launch process mining project from standard platform list view points user to finding definition instead of project setup
        -   Scheduled tasks: Advanced transitions scheduled tasks always show 'Directly followed By' irrespective of the actual relation used
        -   Unable to apply a Saved filter on finding definitions
        -   Inter-entity label sometimes overlaps with entity canvas
        -   Selection of entity should not result in a refresh of the entire process graph \(blinking of the graph\)
-   **Version 23.2.10 - November 2023 \(Utah\)**
    -   Fixed:
        -   Process configuration form labels are not translated
        -   Finding definitions not translated
-   **Version 24.4.5 - September 2023 \(Vancouver\)**
    -   Fixed:
        -   User not able to select a table within Finding Definitions
        -   Process Insights are not visible in Workforce Optimization Manager Workspace
-   **Version 24.4.1 - August 2023 \(Vancouver\)**
    -   New:
        -   Be able to map KPI to improvement opportunities.
        -   Advanced transitions to support attributes of interests.
        -   Ability to share projects with roles.
    -   Changed:
        -   Name change: Project Optimization becomes Process Mining.
        -   Process graph: Created becomes Process Start.
        -   Process graph: Changed the solid line into an artificial line \(dashed\) for all outgoing Process Start node arcs.
        -   Improved Summary and Insights page for better improvement opportunities insights.
    -   Removed: Bottleneck variation analysis on Summary and Insights page \(available in Analyst Workbench\).
-   **Version 22.1.19 - May 2023**

    Changed: Not able to auto-run RCA for improvement opportunities.

-   **Version 23.1.3 - March 2023**
    -   Fixed:
        -   Findings definitions: Contextual condition "Performed By" fixed
        -   Advanced transition: contextual conditions with AND or OR fixed
        -   Multi-Dimensional model graph: Unexpectedly moving entities when reshuffling nodes on process graph fixed
        -   Multi-Dimensional model graph: Inter-model arcs overlap nodes fixed
-   **Version 22.1.16 - February 2023 \(Utah\)**

    Fixed: Usability improvements.

-   **Version 22.1.16 - February 2023 \(Tokyo\)**

    Fixed:

    -   Advanced transitions usability improvement
    -   Automated group by reference on child table
-   **Version 22.1.13 - November 2022**
    -   New:
        -   Artificial lines indicating end of process
        -   Select all option in variance and breakdown
    -   Changed:
        -   Intermodel slider to double dotted line including shown and hidden arcs
        -   Remove all arcs if nodes not visible in graph
        -   Be able to link/unlink automation request
-   **Version 21.1.3 - October 2022**

    Fixed: Nodes in process graph improvement

-   **Version 22.1.4 - August 2022**
    -   New:
        -   Expanded project search capabilities
        -   Historgram report on connections to find outliers quickly
        -   Mine sub-parts of the process with the custom start and stop capabilities
    -   Changed process model:
        -   Easier navigation on process map
        -   One mouse click to highlight all outgoing node connections
        -   Multi dimensional mining slider to quickly zoom in and out on table connections
        -   Easily filter among your scheduled tasks to find your completed cluster, root cause, or mine tasks
    -   Fixed:
        -   Shared user is able to add new entity in model config and New button visible for Activity and Breakdown Def
        -   Several graph rendering fixes
-   **Version 21.1.2 - June 2022**
    -   Fixed:
        -   Point the link "Setup Finding Definition" in the workbench to the right table
        -   Fix for Polaris ON/OFF
        -   Security updates
-   **Version 21.1.1 - March 2022**
    -   New:
        -   Guided setup for a quick start
        -   Open process map for a designated automation opportunity
        -   Instantly view the records behind a cluster
        -   Be able to load more clusters
        -   New metric Est. Avg time savings on insights card
    -   Fixed:
        -   After upgrading to Feb release, no records a shown after clicking on the Show records icon for a designated cluster in linked processes
        -   In the condition builder on the analyst workbench, typed chars are cut off when using the "condition" expression due to fast fresh
-   **Version 21.1.0 - February 2022**
    -   New:
        -   Launch PO within Automation Discovery
        -   Load more clusters
        -   One-click to see records in a particular cluster
        -   Process configuration to guided setup
        -   Save as function for saved filters
        -   Added the improvement opportunities metric "Avg time impact"
    -   Changed: Renamed the improvement opportunities metric "Total time savings" into "Total time impact"

