---
title: Strategic Planning release notes
description: The ServiceNow Strategic Planning application helps you accomplish end-to-end planning using a single workspace. Strategic Planning was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 11
---

# Strategic Planning release notes

The ServiceNow® Strategic Planning application helps you accomplish end-to-end planning using a single workspace. Strategic Planning was enhanced and updated in the Australia release.

## Strategic Planning highlights for the Australia release

-   Create and manage demands from the Next Experience for Demand Management in Strategic Planning. Guide demand managers and users through predefined stages and actions for each demand process using Playbooks in Next Experience for Demand Management.
-   Link AI systems to a demand using a playbook activity in Next Experience for Demand Management. Generate a concise summary of a demand using the demand summarization skill.
-   Use boards in Strategy and Goals to group and manage strategic priorities and objectives for your organization. Use the goal insights skill to generate insights for goals to gain predictive, actionable visibility into goal health.
-   Send notifications to target owners or contributors to ensure timely updates of target actuals. Define targets across multiple organizational levels with the Assigned entity field in the target form.
-   Consistent financial reporting across all baselines by support of investment currency on migrated financial baselines.
-   Simplified user experience and focus on investment level financials view on investment currency fields for new customers. Complete and accurate currency data in all financial baselines for existing customers are now upgraded to include investment currency values.

See [Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/alignment-planner-workspace-landing-page.md) for more information.

**Important:** Strategic Planning is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **Epic status assessment**

    Automatically evaluate epic health across six risk dimensions using the Epic status assessment skill in Enterprise Agile Planning. Now Assist analyzes story health, blocked stories, dependencies, progress, timeline, and ownership to return a red, yellow, or green status with plain-English reasoning. Portfolio managers can quickly assess epic risks without manually reviewing stories, timelines, and assignments by selecting the **Epic status** button on the epic record page.

-   **[AI-generated insights for portfolio plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/view-portfolio-insights.md)**

    Gain AI-generated insights for planning items within a portfolio plan using the Portfolio insights skill. Identify planning items that are delayed beyond their planned end date, have delayed starts, or have misalignments between planned and approved dates. View AI-generated top root causes and recommended actions for each insight category to help address delays and misalignments effectively.

    Users with the sn\_align\_core.apw\_admin role assigned can configure severity scoring for planning items to control how the Portfolio insights skill classifies insight severity as Critical, Medium, or Low.

-   **[Story generation for epics in Agile Development 2.0 and EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/generate-stories-quickly-for-eap-and-agile-2-0.md)**

    Generate a complete user story, including title, description, and acceptance criteria, directly from an epic instead of creating one. By providing one or two lines of context, you can generate a story and edit inline before saving. This skill is available in both Agile Development 2.0 and EAP.

-   **[Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/demand-workspace.md)**

    Next Experience for Demand Management delivers a unified experience for managing strategic and operational demands in Strategic Planning. This Next Experience interface consolidates demand creation, assessment, collaboration, and conversion in one place, eliminating context switching and reducing reliance on the classic Demand Workbench.

-   **[Create and manage demands in Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/use-demands-dmnd-wpc.md)**
    -   Create and manage a demand in Next Experience for Demand Management using guided tabs that help you define alignment, estimate costs, and confirm readiness as you build out the demand.
    -   Collaborate on demands through Docs, with execution and planning synced.
    -   View, add, and edit cost plans and budgeting details using related lists.
-   **[Use Playbooks in Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/use-playbooks-in-dw.md)**

    Help teams manage demands with greater structure and consistency using Playbook in Next Experience for Demand Management.

    Playbooks enable you to define multiple governance processes across the organization using a low‑code/no‑code configuration experience. Create clear stages and guided activities from demand intake to completion by using a default playbook or creating a custom playbook to support your organization’s multiple demand management processes.

-   **[Associate AI systems with demands in Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/use-playbooks-in-dw.md)**

    Use a playbook activity in Next Experience for Demand Management to associate AI systems with a demand. You can link impacted systems and add new ones directly within the demand workflow.

-   **[Summarize demands with demand summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/summarize-demand-in-demand-workspace.md)**

    Generate a concise, structured summary of any demand using the demand summarization skill through the **Summarize** button in the demand form. The skill reviews the demand fields and helps create a clear summary of the demand.

-   **[Strategy and Goals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/strategy-goals-landing-page.md)**

    Use boards in Strategy and Goals to organize and manage your organization’s strategic priorities and objectives. A board is a collection of strategic plans, priorities, objectives, and key results based on your selected filter criteria—helping you stay focused and manage them effectively.

    -   Managing boards:
        -   Create boards step by step, choosing whether to base them on strategic plans, priorities, goals, or both. Define what items to display using advanced filter conditions.
        -   Build boards tailored to specific goals by entity type and entity, ensuring focus on the goals that matter most.
        -   Share boards with stakeholders to align efforts and drive shared outcomes.
        -   Add boards to your favorites for faster navigation.
    -   Managing strategy and goals using boards:
        -   Create and organize strategic plans, strategic priorities, goals, and key results in a single, focused view.
        -   Associate work or planning items with goals or targets to align your current or future work with your strategic priorities, helping your team achieve goals and targets efficiently.
        -   As the goal or process owner, send notifications to target owners or contributors to ensure timely updates of target actuals.
        -   Target owners and contributors receive reminder notifications for check-in updates before the due date.
        -   With Now Assist for Strategic Portfolio Management \(SPM\), generate measurable targets for your goals to reduce the effort of defining clear success criteria, and gain actionable insights to identify at‑risk goals, assess forecasted status, and act on AI‑driven recommendations.
-   **[AI-generated insights for goals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/generate-insights-for-goal.md)**
    -   Generate AI‑powered insights using the goal insights skill to gain predictive, actionable visibility into goal health. By analyzing the goal, goal targets, subgoals, and aligned work, the system delivers data‑driven insights that help goal owners and contributors manage risks proactively and improve goal outcomes. Insights include AI-forecasted status, confidence of achieving the goal, targets at risk, and aligned work or recommendations that have been delayed or stalled.
    -   View the AI-forecasted status for goals and targets in the grid, generated automatically via the Goal insights generation scheduled job, along with the rationale for the generated status.
    -   Configure run frequency and set of goals to run the Goal insights generation scheduled job as need. The job is inactive by default.
-   **[Portfolio plan goals enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/managing-goals-in-alignment-planner-workspace.md)**
    -   Owners and contributors are notified when they’re mentioned in a goal, target, or when comments are added.
    -   Define targets across multiple organizational levels with the Assigned entity field in the target form. This enables targets created at higher levels \(for example, Company\) to be directly assigned to lower levels \(for example, Business Unit, Department\), eliminating redundant subgoal creation, and streamlining overall goal management.
-   **[Portfolio plan enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/create-portfolio-plans-in-alignment-planner-workspace.md)**
    -   Visualize planning items in lanes with the new Kanban tab in the Planning page and access the Hierarchy tab directly from the same location. These tabs replace the previous access point in the Prioritization tab, offering a more streamlined way to view and manage planning items.
    -   Save filter views specific to the Kanban tab and the Hierarchy tab without affecting views in the Prioritization tab.
    -   View planning items in the new Hierarchy tab on the Planning page, now sorted using global rank when available. Drag and drop is supported for lowest‑level items, enabling you to rerank them within their groups.
    -   Share a portfolio plan using the Copy link option. This provides access to existing users who have access to the portfolio plan.
    -   Expand or collapse portfolio plan header to maximize screen space while planning.
    -   Edit the default view within a portfolio plan and save changes using the Save view option.
-   **[Hierarchy tab for EAP teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/eap-hierarchy-tab.md)**

    Gain visibility into how your work connects to broader organizational goals by viewing the complete work item hierarchy directly in the EAP workspace. Expand any epic to see its capabilities, features, and stories across Solution Trains, ARTs, and Agile Teams without switching between multiple screens or running separate reports.

    Customize your view by selecting which columns appear in the hierarchy grid and adjusting column widths to match your workflow. Your column preferences persist across sessions, so your configured view is ready each time you return.

-   **[Open EAP work items in new browser tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/using-eap.md)**

    Open work items from the EAP Backlog and Hierarchy pages in a new browser tab, so you never lose your context. Right-click any work item, or use the item options menu, to open its full details in a separate tab. This feature lets you review and compare multiple work items side by side without losing your current view.

-   **[Admin role enhancements in Feedback](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/product-feedback/components-installed-with-product-feedback.md)**

    The read role sn\_align\_core.pf\_read and write role sn\_align\_core.apw\_admin are added to the following system properties in Feedback and Product idea:

    -   sn\_apw\_advanced.product\_feedback\_allowed\_non\_planning\_items\_for\_link\_item
    -   sn\_apw\_advanced.product\_feedback\_product\_idea\_filters
    -   sn\_apw\_advanced.product\_feedback\_feedback\_filters
    -   sn\_apw\_advanced.feedback.idea\_feedback\_queue\_address
-   **[Financials for planning items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/using-financials-spw.md)**
    -   Migration of financial baselines:
        -   Migrate the financial baselines of projects, which includes investment currency support.
        -   While migration, financial baselines will now include actuals, costs, benefits, and budget values from the project currency to the investment currency.
    -   Streamlined currency fields while using multicurrency:
        -   New and existing customers will now see only investment currency fields in demand and project records.
        -   Planned costs, actual costs, planned benefits, actual benefits, and budget fields are included in the financial baselines.

## UI changes

-   **[Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/demand-workspace.md)**
    -   The Demands icon ![](../../product/spw-demand/images/demands-icon.png) has been added to the Strategic Planning L1 menu to open the All Demands home page.
    -   The **State** field on the **All Demands** page has been color-coded for each state value.
    -   The **Playbook**, **Details**, and **Docs** tabs have been added to the L2 menu of each demand to clearly and consistently group information.
        -   The **Details** tab has been added to add and manage demand information such as financials and resource assignments.
        -   The **Playbook** tab has been added to define clear stages and guided activities to read and follow. Selecting the name of a stage or activity navigates you to that stage or activity in the playbook. The **Skip**, **Update**, and **Mark Complete** options have been added to the activities of the playbook.
        -   The **Docs** tab has been added to view and manage the documentation on the demand.
    -   If you have the AI Control Tower plugin installed and the investment type of the demand is set to artificial intelligence:
        -   The **AI Associations** section in the Demand details is displayed. The following fields are included:
            -   **Product**: Enables you to select the product or system that the demand relates to.
            -   **Impacted AI systems**: Links the impacted AI systems with the demand. You can select existing AI systems from the list or remove systems that are no longer relevant.
        -   The **AI Checkpoint** stage is added to the demand default playbook. This stage includes the **Product** and **Impacted AI systems** fields.
        -   The **Create AI System** option is added to the **Details** page of a demand for users with the sn\_ai\_steward role.
-   **[Changes to Target form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/target-form-egm.md)**

    The following fields have been added to the Target form to support defining targets at multiple organizational levels.

    -   **Assigned entity**
    -   **Company**
    -   **Business Unit**
    -   **Department**
    -   **Portfolio**
    -   **Product model**
    -   **Value stream**
    -   **Initiative**
    -   **Strategic Program**
-   **[Changes to Strategic Priority form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/goal-framework/strategic-priority-form.md)**

    The **Status** field has been added to the Strategic Priority form, enabling you to set the status of a strategic priority as **None**, **Green**, **Yellow**, or **Red**.

-   **[Hierarchy and List views in Prioritization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/managing-backlog-alignment-planner-workspace.md)**

    The **Kanban** and **Hierarchy** views have been removed from the Prioritization page and are now available as separate tabs in the Planning page. This change improves navigation by consolidating all planning-related views in one place.


## Changed in this release

[Australia Patch 2](../quality/australia-patch-1.md)

-   **[Demand summarization skill enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/demand-management/demand-summary-demand-classic.md)**

    The demand summarization skill incorporates data from related entities when generating a summary. In addition to demand record fields, the summary includes insights from demand tasks, cost plans, monetary and non-monetary benefit plans, resource assignments, and work notes. The generated summary covers business requirements, timeline, risks, stakeholder comments, cost, effort, monetary and non-monetary benefits, and ROI.


## Activation information

Install Strategic Planning by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-control-tower-landing.md)**

    ServiceNow AI Control Tower enables you to track and monitor all your strategic priorities, goals, targets, planning items, and execution items—projects and demands categorized as Artificial Intelligence in the Strategic Planning Workspace.

-   **[Now Assist for Strategic Portfolio Management \(SPM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/now-assist-spm.md)**

    Now Assist enables you to use generative AI skills in multiple SPM apps. With Now Assist for SPM, summarize product feedback, create stories for epics, generate concise project summaries, rephrase content for docs, create demands through a conversational experience, and quickly gain insights into projects.

-   **[Digital Product Release Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-workspace.md)**

    ServiceNow Digital Product Release Workspace helps product managers track the planning items associated with the product enhancements that are defined in the Strategic Planning Workspace using the Digital Product lens.


**Parent Topic:**[Strategic Portfolio Management release notes](it-business-management-rn-landing.md)

