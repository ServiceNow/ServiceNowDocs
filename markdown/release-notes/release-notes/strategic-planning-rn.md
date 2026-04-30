---
title: Strategic Planning release notes
description: The ServiceNow Strategic Planning application helps you accomplish end-to-end planning using a single workspace. Strategic Planning was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 12
---

# Strategic Planning release notes

The ServiceNow® Strategic Planning application helps you accomplish end-to-end planning using a single workspace. Strategic Planning was enhanced and updated in the Xanadu release.

## Strategic Planning highlights for the Xanadu release

-   Show or hide the features of your portfolio plan so you share only the most important data with your stakeholders.
-   Update actuals and track the progress of your targets in daily, weekly, monthly, quarterly, or yearly intervals with the enhanced target breakdown feature.
-   Filter the planning items and roadmap bars with multi-value fields, such as tags, business applications, and business capabilities.
-   Create rich-text documents to store and manage artifact information for planning items and Agile teams in EAP.
-   Create scenarios to simulate changes to the portfolio plan, compare scenarios for visualizing trade-off decisions, and approve a scenario to revise the live plan.
-   View the cost plans, expense lines, budget, and financial baselines of sub-projects at the parent project level. View the financial performance of a project using the rolled-up planned and actuals costs in the widgets of parent projects.
-   Select a primary attribute to populate resource criteria automatically from the resource assignments of the prioritized planning items, and view the team's capacity in the Capacity Planning screen.

See [Strategic Planning](https://www.servicenow.com/docs/access?context=alignment-planner-workspace-landing-page&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US) for more information.

**Important:** Strategic Planning is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Strategic Planning to Xanadu

After upgrading to Strategic Planning v4.3.2, run the **Migrate BreakdownInterval To Checkinfrequency** scheduled job. This scheduled job migrates the existing values in the **Review frequency** and **Breakdown interval** fields to the **Check-in frequency** field in the target records. For more information on how these values are migrated for targets with different values, see [Target breakdowns migration](https://www.servicenow.com/docs/access?context=target-breakdowns-migration-spw&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

## New in the Xanadu release

-   **[Show or hide features for your portfolio plan](https://www.servicenow.com/docs/access?context=show-or-hide-the-features-for-your-portfolio-plan-spw&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

    As a portfolio manager, show or hide the features, such as Goals, Scoring, Prioritization, and Roadmap, of your portfolio plan. This capability helps you share only the portfolio plan data that matters to your stakeholders and restrict access to the other data.

-   **[Goal management enhancements](https://www.servicenow.com/docs/access?context=managing-goals-in-alignment-planner-workspace&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Create daily, weekly, or monthly target breakdowns according to how often you want to update and track the progress of the target. The target breakdowns are created based on the value selected in the **Check-in frequency** field. For example, if you select **Monthly** in the **Check-in frequency** field for a target spanning a year, then 12 monthly target breakdowns are created.
    -   Updating actuals for a target has been simplified with an enhanced UI:
        -   In the Check-in actuals window on the **Progress** tab of the target’s side panel, update the actual value of any time period or breakdown.
        -   In the **Progress** tab of the target’s side panel, view the trend of the target’s progress in a line or bar graph. You can also edit the planned target and view the check-in history of the target actuals.
    -   When creating a target, the **Target breakdown details** section of the Target modal shows the planned target values for each target breakdown in a tabular format, which helps you visualize the final target value spread across the target’s time period.
    -   On the Target form, use the **Baseline reference** field to compare future target performance with the actual value that was achieved in the last year or before the target was created.
    -   Add targets to a new goal using the **Save and add target** option on the Goal modal. Also, you can use the **Save and add new target** option to add more targets for the goal.
    -   Run the **Create Goals Demo Data with Target Breakdowns** scheduled job to create demo data with goals and target breakdowns. For more information on this scheduled job, see [Create goals demo data with target breakdowns](https://www.servicenow.com/docs/access?context=create-goals-demo-data-with-target-breakdowns&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).
    -   Create a copy of a goal or target using the **Duplicate** option from the row context menu icon \(![Row context menu icon.](../image/row-context-menu-icon.png)\). For more information, see [Create a copy of a goal or target](https://www.servicenow.com/docs/access?context=create-a-copy-of-a-goal-or-target&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).
    -   Activity stream is enabled for the targets and goals in the full details record page.
-   **[Planning enhancements](https://www.servicenow.com/docs/access?context=planning-in-spw&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Filter planning items in the Prioritization page and roadmap bars in the Roadmap page with multi-value fields, such as tags, business applications, and business capabilities.
    -   In the Child items related list of an EAP planning item, view child items associated with the epic in EAP.
    -   When you view a portfolio plan, you can copy a portfolio plan that you don't have edit access to and edit the plan as needed. For more information, see [Copy a portfolio plan](https://www.servicenow.com/docs/access?context=copy-portfolio-plan-in-strategic-planning&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).
-   **[Now Assist in Strategic Planning](https://www.servicenow.com/docs/access?context=now-assist-spm&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Generate a summary of selected text on Docs using the Planning item Gen AI Docs skill. You can summarize, elaborate, and shorten the selected content on Docs.
    -   Summarize a large volume of feedback using the multi feedback summarization skill on the Feedback page.
    -   Create a demand within the Employee Service Management \(ESC\) portal using the Now Assist conversational catalog creation capability.
    -   Summarize the complete content of a document with the Planning item Gen AI Docs skill to help save time on manual content analysis.
-   **[Collaborate using Docs in EAP](https://www.servicenow.com/docs/access?context=docs-for-eap-teams-and-planning-items&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Store the information of key artifacts and other details of planning items, such as Epics, Capabilities, and Features, directly from within the workspace.
    -   Manage team-level documentation for Agile team, ART, Solution Train, and Portfolio.
    -   Create multiple rich-text documents at each planning item level or Agile team level.
        -   Help avoid data loss and parallel editing with real-time collaboration.
        -   Tag team members to their action items.
        -   Insert media and URLs.
-   **[Docs for planning items in Strategic Planning](https://www.servicenow.com/docs/access?context=docs-for-planning-items-in-spw&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Store the information of key artifacts and other details of planning items, such as Demands, Projects, and Epics, directly from within the workspace.
    -   Create multiple rich-text documents at each planning item level.
        -   Help avoid data loss and parallel editing with real-time collaboration.
        -   Tag team members to their action items.
        -   Insert media and URLs.
-   **[Migrating from SAFe to EAP](https://www.servicenow.com/docs/access?context=migrating-from-safe-to-eap&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

    Transition from Scaled Agile Framework \(SAFe\) applications, such as Essential SAFe and Portfolio SAFe, to EAP. Use the Guided Setup module in the Strategic Planning application to execute your migration step by step.

    This migration is intended to be one-time only. Initiating the migration again later while continuing to use SAFe applications with EAP won't carry any changes made to the SAFe records that are already migrated.

-   **[Override the default planning calendar for Agile Teams](https://www.servicenow.com/docs/access?context=create-planning-calendar-type-in-eap&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

    For Agile Teams and Agile release trains \(ARTs\), the **Override planning calendar** field enables team members to change their planning calendar. The updated calendar is automatically applied to any child teams and takes effect at the beginning of the next iteration.

-   **[Persistence of personalization settings for the EAP PI planning board](https://www.servicenow.com/docs/access?context=pi-planning-eap&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

    Personalization of the settings made in the PI planning board for a team type are applied across the workspace according to user, team type, and work item type. For example, settings applied to one ART, such as enabling the Dependencies toggle, Team backlog lane, or compact cards, are applied to all ARTs in the workspace for a user.

-   **[Optimize planning using scenario planning](https://www.servicenow.com/docs/access?context=scenario-planning-in-strategic-planning&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Create scenarios in a simulated environment and adjust the prioritization and timelines of planning items.
    -   Check the alignment of planning items with goals to verify the delivery of strategic outcomes.
    -   Visualize the differences between goal alignment and trade-off decisions between scenarios by comparing scenarios side by side.
    -   Approve the best scenario as the live portfolio plan for execution and making informed decisions.
-   **[Export goals and targets data to Excel or CSV](https://www.servicenow.com/docs/access?context=export-goals-and-targets-to-excel&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

    Export goals and targets from your portfolio plan into a Microsoft Excel or CSV file to share the data and collaborate with your business stakeholders.

-   **[Export a roadmap or free-form roadmap to PowerPoint](https://www.servicenow.com/docs/access?context=export-a-portfolio-plan-to-powerpoint-strategic-planning&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

    Export a roadmap or free-form roadmap from a portfolio plan into a Microsoft PowerPoint file to share data and collaborate with your business stakeholders. The predefined template helps you generate reports for your roadmap, including roadmap milestones, item milestones, vertical lines, and horizontal lanes.

    You can export a roadmap for the maximum tenure of lanes a year at a time. You can also choose between Compact mode, which exports 25 horizontal lanes per slide, or Default mode, which exports 15 horizontal lanes per slide, when exporting your roadmap.

    You can select the data that you want to be exported into the report by editing the predefined templates or creating your own branded template. For more information, see [Create a Microsoft PowerPoint template](https://www.servicenow.com/docs/access?context=create-ppt-template&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

-   **[Plan at a high level using the Project Program lens](https://www.servicenow.com/docs/access?context=portfolio-plans-in-strategic-planning&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

    Plan at a high level by building portfolio plans for program \[pm\_program\] items using the Project Program lens. Score and prioritize the programs and track them using roadmaps.

-   **[Feedback enhancements](https://www.servicenow.com/docs/access?context=managing-product-feedback-in-strategic-planning&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Manage the feedback filter card directly from the feedback homepage by sorting, pinning, sharing, updating, or deleting it.
    -   Allow access to specific users or groups when sharing the feedback filter card, and review the users who have access to it.
-   **[Financials in Strategic Planning](https://www.servicenow.com/docs/access?context=using-financials-spw&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Migrate the existing planning items budget from the classic UI to Next Experience using the **Migrate Budget** option.
    -   As a portfolio manager, allocate and manage the budget of your planning items using the Budget vs cost view.
    -   As a project manager, compare a budget to the captured costs of your planning items and reforecast the planned costs to meet the approved budget.
    -   Compare financial baselines to view simple financials and budget.
    -   View the cost plans, expense lines, and financial baselines of sub-projects using the Financial view of a parent project.
    -   Widgets in the Cost view of parent projects display the rolled-up value of the planned costs, expense lines, budget, and variance.
    -   Create custom labor cost types and map them with a unique sys\_id to generate labor costs.

-   **[Capacity Planning in Strategic Planning](https://www.servicenow.com/docs/access?context=using-cap-plan-spw&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   Select a primary attribute to auto-select the resource criteria based on the planning items in the portfolio.
    -   Automatically generate resource capacity using a scheduled job at your desired cadence.
    -   View only prioritized planning items in the bottom tray of the Capacity Planning screen.
    -   View the total capacity, estimate, and available efforts of a resource using the heatmap view.

## UI changes

-   **[Product feedback UI changes](https://www.servicenow.com/docs/access?context=managing-product-feedback-in-strategic-planning&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   The **Share with members or group** field has been removed from the Feedback filter form.
    -   The **Share** option on the feedback filter card has been removed.
    -   The Product Feedback icon name is changed to Feedback.
    -   The most recently created records in Feedback and product idea are displayed on the top.
-   **[EAP reports and dashboards](https://www.servicenow.com/docs/access?context=using-eap-dashboard&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

    Improved widget placement in the ART and the Team dashboard pages, which enables you to view more data with less scrolling.

-   **[Goals UI changes](https://www.servicenow.com/docs/access?context=managing-goals-in-alignment-planner-workspace&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   The **List** tab and **Hierarchy** tab have been moved under the **Goals and targets** tab for a better UI experience while switching between the List and Hierarchy views on the Goals page.
    -   On the Target form, the **Breakdown interval** and **Cumulative target** fields have been removed. Also, the Fortnightly option has been removed from the **Check-in frequency** field.
    -   On the Target form, the **Cumulative target** field has been replaced with **Target value distribution field**. The field has two values to describe the target distribution: Spread linearly across the time period \(cumulative\) and Split equally across the time period \(non-cumulative\).
    -   On the Target form, the following fields form have been renamed:
        -   **Review frequency** to **Check-in frequency**
        -   **Base value** to **Start value**
        -   **Target value** to **Final target value**
        -   **Actual value** to **Actuals to date**
        -   **Review due date** to **Check-in due date**
    -   Horizontal lines have been added on the List view to differentiate one set of goals and targets from another.
    -   Vertical lines have been added on the List view to differentiate the target breakdowns with the goals and targets columns.
    -   The maximum number of characters allowed in the **Name** field has increased from 80 to 255 for the Goal \[sn\_gf\_goal\] and Target \[sn\_gf\_goal\_target\] tables.
-   **[Planning UI changes](https://www.servicenow.com/docs/access?context=copy-portfolio-plan-in-strategic-planning&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   The **Copy portfolio plan** option in the Portfolio actions menu has been renamed to **Duplicate portfolio plan**.
    -   The **Create copy** option in the Row context menu of planning items has been renamed to **Duplicate**.
-   **[Roadmap UI changes](https://www.servicenow.com/docs/access?context=copy-roadmap-in-strategic-planning&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

    The **Copy roadmap** option in the Roadmap actions menu has been renamed to **Duplicate roadmap**.

-   **[Financials UI changes](https://www.servicenow.com/docs/access?context=using-financials-spw&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   New **Budget vs. cost** toggle for project managers and product managers to view a comparison of budget and captured costs.
    -   New **Budget allocation** toggle for portfolio managers to manage a project budget.
    -   New **Approve budget** button in the budget allocation view for portfolio managers to approve budget changes.
    -   New grid view to enter and view the budget information at a fiscal period, quarterly, or yearly, and the total breakdowns by Expense Type or Cost Type.
    -   New **Project/Demand** column in the Cost view to show the mapping of cost plans to projects and sub-projects.
-   **[Capacity Planning UI changes](https://www.servicenow.com/docs/access?context=using-cap-plan-spw&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   New Resource criteria screen.
    -   New **Auto-select** and **Manual-select** options to select the attributes on the Resource criteria screen.
    -   New **Prioritized Work Item** category in the bottom tray of the Capacity Planning screen.

## Changed in this release

-   **[Break down work from a parent work item](https://www.servicenow.com/docs/access?context=breakdown-work-eap-epics-capabilities-child-work&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

    Create child work items directly from the parent record page.

    -   The **Child items** tab on the work item record page is replaced with the tabs of each associated child item. For example, the full details page of an Epic shows separate tabs for its child work items, capabilities, features, and stories, based on the EAP configuration.
    -   New button is added to each tab to create work items directly from the parent work item record page.
-   **[Enhancements to the PI planning board in EAP](https://www.servicenow.com/docs/access?context=pi-planning-eap&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

    The PI planning board displays all work assigned to the current Agile structure level as well as its child teams.

-   **[Feedback](https://www.servicenow.com/docs/access?context=product-feedback-landing&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

    The Product Feedback application name is changed to Feedback.


## Activation information

Install Strategic Planning by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Export to PowerPoint for Strategic Portfolio Management](https://www.servicenow.com/docs/access?context=export-ppt-landing-page&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

    Edit the predefined templates or create your own branded template with ServiceNow Export to PowerPoint for Strategic Portfolio Management to export roadmap data into the report.


**Parent Topic:**[Strategic Portfolio Management release notes](it-business-management-rn-landing.md)

