---
title: Combined Project Portfolio Management release notes for upgrades from Zurich to Brazil
description: Consolidated page of all release notes for Project Portfolio Management from Zurich to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-brazil/brazil-zurich-projectportfoliomanagement-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 15
breadcrumb: [Products combined by family]
---

# Combined Project Portfolio Management release notes for upgrades from Zurich to Brazil

Consolidated page of all release notes for Project Portfolio Management from Zurich to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Project Portfolio Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Project Portfolio Management to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Upgrade information**

Users who already have Project Portfolio Management can upgrade to PPM Standard. New users must purchase PPM Standard. For more information, see [Activate PPM Standard \(Project Portfolio Management\)](https://www.servicenow.com/docs/access?context=t_ActivateProjectPortfolioSuiteWithFinancials&family=brazil&ft:locale=en-US).


</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Project Portfolio Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Identify similar records using Now Assist](https://www.servicenow.com/docs/access?context=identify-similar-demand-records&family=zurich&ft:locale=en-US)**

Detect similar existing demand records when creating or editing a demand using the identify similar records skill. This skill compares the **Name**, **Description**, and **Business Case** fields for contextual similarity.

-   **[Convert demands to EAP entities](https://www.servicenow.com/docs/access?context=t_CrtArtftDmdMnu&family=zurich&ft:locale=en-US)**

Convert your demand records quickly to Enterprise Agile Planning \(EAP\) entities, such as Epic, Feature, or Capability. When you convert a demand, the system generates a new record of the selected entity type, replicates common fields from the demand, and moves the demand to the Approved state.


 -   **[Manage projects](https://www.servicenow.com/docs/access?context=use-projects-pw&family=zurich&ft:locale=en-US)**
    -   End resource assignments when a project ends, view assignment details, and synchronize assignment dates with project dates.
    -   Access and edit the resource details directly from the Resource page without switching between views.

</td></tr><tr><td>

Australia

</td><td>

-   **[Associate AI systems with demands in Demand Management](https://www.servicenow.com/docs/access?context=associate-ai-systems-with-demands&family=australia&ft:locale=en-US)**

Add and manage AI system associations directly from the **AI Associations** tab in Demand Management. You can select impacted AI systems or create AI systems using related links directly within the demand workflow.

-   **[Summarize demand records with the demand summarization skill](https://www.servicenow.com/docs/access?context=demand-summary-demand-classic&family=australia&ft:locale=en-US)**

Generate a concise, structured summary of any demand using the demand summarization skill through the **Summarize** button in the demand form. The skill reviews the demand fields and helps create a clear summary of the demand.


 -   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


 -   **[Admin role enhancements in Demand Management](https://www.servicenow.com/docs/access?context=c_DemandManagement&family=australia&ft:locale=en-US)**
    -   Enabling all users to create ideas with a minimum read role added to the **com.snc.idea.universal\_request.copy\_fields** system property.
    -   The **com.snc.idea.universal\_request.copy\_fields** system property can be updated only by users with the idea\_admin or pps\_admin roles.
    -   Help ensure that only authenticated users have access to the bubble chart workbench through the UserIsAuthenticated condition added to the bubble chart workbench ACL \(access control list\).
-   **[Admin role enhancements in Project Management](https://www.servicenow.com/docs/access?context=r_InstalledWithProjectManagement&family=australia&ft:locale=en-US)**

The Project properties can be edited only by users with the pps\_admin role.

-   **[Admin role enhancements in Innovation Management](https://www.servicenow.com/docs/access?context=innovation-management-landing&family=australia&ft:locale=en-US)**
    -   The write role has been added for the **idea.notification.sender.email** and**com.snc.innovation\_management.im\_editor\_attachment\_tag\_id** system properties.
    -   The **idea.notification.sender.email** and **com.snc.innovation\_management.im\_editor\_attachment\_tag\_id** system properties can be added or updated only by users with idea\_admin roles.

</td></tr><tr><td>

Brazil

</td><td>

-   **Budget Overrun insight card**

Identify portfolio plans at risk of exceeding their approved budget with the new Budget Overrun insight card in Portfolio Insights. The card compares each planning item's current fiscal year forecast against its approved budget and flags items where the forecast is higher. Flagged items include a root cause analysis — grouped by cost type and driven by factors such as rate changes, effort overruns, or foreign exchange impact — along with recommended actions like re-forecasting with finance or initiating change control.

-   **Cost Variance insight card**

Identify cost plans whose actual spend is running over or under plan for the current fiscal period with the new Cost Variance insight card in Portfolio Insights. The card flags cost plans where the variance between actual and planned costs exceeds a configurable threshold, in either direction, and groups the root causes by driver — such as rate-driven, effort or hours overrun, or actuals below plan — along with recommended next steps for each.

-   **[Copy and customize the demand summarization skill](https://www.servicenow.com/docs/access?context=clone-customize-the-demand-summarization-skill-ppm&family=brazil&ft:locale=en-US)**

Tailor demand summaries to your organization's process by copying the base demand summarization skill and customizing it with your own input fields, related entities, and prompt. When you activate a copy of the demand summarization skill, the previously active skill, either the base skill or an earlier copy, is automatically deactivated. Only one version of the skill can be active at a time.

-   **[Work with demands in Employee Hub](https://www.servicenow.com/docs/access?context=my-demands-widget-ppm&family=brazil&ft:locale=en-US)**

Create and track demands without leaving the conversation-first Employee Slate workspace. Describe the demand in a conversation to have matching catalog items identified and relevant fields prepopulated from your message, then track its status, activity, and progress using the new My Demands widget on your canvas or the standard Requests widget. Demands appear in Employee Slate only when both Project Workspace and Employee Slate Core apps are installed.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Project Portfolio Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Demand Management UI changes](https://www.servicenow.com/docs/access?context=demand-form&family=zurich&ft:locale=en-US)**
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

 -   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Project Workspace UI changes](https://www.servicenow.com/docs/access?context=update-resource-assignment-pw&family=zurich&ft:locale=en-US)**

The following items were added to Project Workspace:

    -   Resource page to access and manage resource assignments.
    -   **Sync all** button to synchronize project dates for all the resource assignments.

</td></tr><tr><td>

Australia

</td><td>

-   **[AI skills for Demand Management](https://www.servicenow.com/docs/access?context=similar-demand-identification-using-now-assist&family=australia&ft:locale=en-US)**

ServiceNow Otto introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.


 -   **[Demand summarization skill enhancements](https://www.servicenow.com/docs/access?context=demand-summary-demand-classic&family=australia&ft:locale=en-US)**

The demand summarization skill incorporates data from related entities when generating a summary. In addition to demand record fields, the summary includes insights from demand tasks, cost plans, monetary and non-monetary benefit plans, resource assignments, and work notes. The generated summary covers business requirements, timeline, risks, stakeholder comments, cost, effort, monetary and non-monetary benefits, and ROI.


 -   **[Next Experience for Demand Management](https://www.servicenow.com/docs/access?context=demand-workspace&family=australia&ft:locale=en-US)**

The new Next Experience for Demand Management provides a unified layout, guided stages, improved navigation, and enhanced capabilities such as Playbooks and Docs integration. As you move to Next Experience for Demand Management, you’ll find it easier to create, review, and manage demands with a cleaner layout and guided actions. The classic UI is still available, but new improvements will appear in the workspace.

Next Experience for Demand Management is available with the Strategic Portfolio Management \(SPM\) Standard and Pro licenses.


 -   **[Demand Management UI changes](https://www.servicenow.com/docs/access?context=demand-form&family=australia&ft:locale=en-US)**
    -   The **Start date** and **Due date** column labels have been renamed **Planned start date** and **Planned end date**, respectively. This change is applicable only for new installations of the Australia version. To ensure continuity, if you’re upgrading to the Australia release from an earlier release, you’ll continue to see the prior labels.
    -   If you have the AI Control Tower plugin installed and the investment type of the demand is set to artificial intelligence:
        -   The **AI Associations** section in the Demand form is displayed. The following fields are included:
            -   **Product**: Enables you to select the product or system that the demand relates to.
            -   **Impacted AI systems**: Links the impacted AI systems with the demand. You can select existing AI systems from the list or remove systems that are no longer relevant.
        -   An option to create an AI system under Related Links in the Demand form is available for users with the sn\_ai\_steward role.

 -   **[Australia Patch 4](https://www.servicenow.com/docs/access?context=australia-patch-4&family=australia&ft:locale=en-US)[Large language models on the ServiceNow AI Platform](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=australia&ft:locale=en-US)**

The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


</td></tr><tr><td>

Brazil

</td><td>

-   **Portfolio Insights card order**

The AI Insights panel now displays insight cards in a fixed order based on prominence and impact: Projects at risk, Budget Overrun, Cost Variance, Items past planned end date, Delayed start, and Planned versus approved misalignment. Review the most critical financial and schedule risks first.

-   **Insight explanations in Portfolio Insights**

Each card in Portfolio Insights now includes an info icon. Select the icon to open a popover with a plain-language explanation of what the insight measures and how it's calculated, so you can interpret the insight without leaving the panel.

-   **[Navigation to Project Workspace in Next Experience](https://www.servicenow.com/docs/access?context=t_CreateAProject&family=brazil&ft:locale=en-US)**

View and access Project Workspace in Next Experience when you access project workspace from the All navigation menu.

-   **[Summarize demands with the demand summarization skill](https://www.servicenow.com/docs/access?context=demand-summary-demand-classic&family=brazil&ft:locale=en-US)**

The default trigger is not set to **Automatic** for demands in any state. You can select how you want the skill to be triggered for any state.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Project Portfolio Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Project Portfolio Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Resource Management reports](https://www.servicenow.com/docs/access?context=c_UsingResourceManagementReports&family=zurich&ft:locale=en-US)**

Starting with the Zurich release, Resource Management reports are deprecated. You can start using the interactive Overview dashboard in Resource Management Workspace to work on reporting.

For more information on the Overview dashboard, see [Using Resource Management Workspace](https://www.servicenow.com/docs/access?context=using-rmw&family=zurich&ft:locale=en-US).

-   **[Resource Management classic](https://www.servicenow.com/docs/access?context=c_ResourceManagement&family=zurich&ft:locale=en-US)**

Starting with the Zurich release, the Resource Allocation workbench and Capacity planning overview are removed from the product navigation of Resource Management for new customers.


</td></tr><tr><td>

Australia

</td><td>

-   Starting with Australia release, Scenario Planning for PPM \(com.snc.ppm\_scenario\_planning\) is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

Alternatively, Strategic Planning Workspace \(for SPM pro users\) or Portfolio Planning Workspace \(for SPM standard users\) provides the Scenario Planning capability. For details, see [Scenario planning in Strategic Planning](https://www.servicenow.com/docs/access?context=scenario-planning-in-strategic-planning&family=australia&ft:locale=en-US) or [Scenario planning in Portfolio Planning](https://www.servicenow.com/docs/access?context=scenario-planning-in-portfolio-planning&family=australia&ft:locale=en-US).

-   Starting with Australia release, the Project Status Report \(com.sn\_store\_ppm.mobile\) is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. Alternatively, Project Workspace provides the Status Report capability.
-   Starting with Australia release, the PMO dashboard is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. Alternatively, Execution dashboard provides the PMO dashboard capability.
-   Starting with Australia release, the Investment Portal is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. Alternatively, Portfolio Planning Workspace provides the Investment Portal capability.
-   Starting Australia, Project Workbench is no longer deployed, enhanced, supported or available for activation. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

 -   For Demand Management:
    -   The permission to edit the value of the **dmn\_stakeholder\_register.number** field in the Stakeholder Register \[dmn\_stakeholder\_register\] table has been removed for the admin role.
    -   The admin role ACL has been removed for the bubble chart workbench.
    -   The duplicate app module that was created for the admin role has been removed.

 -   The permission to edit the value of the **dmn\_stakeholder\_register.number** field in the Stakeholder Register \[dmn\_stakeholder\_register\] table has been removed for the admin role.
-   The admin role ACL has been removed for the bubble chart workbench.
-   The duplicate app module that was created for the admin role has been removed.

</td></tr><tr><td>

Brazil

</td><td>

-   **[Planning console](https://www.servicenow.com/docs/access?context=c_TheProjectPlanningConsole&family=brazil&ft:locale=en-US)**

Starting Brazil release, Planning console is deprecated and is no longer supported. Project managers can [access Project Workspace using Next Experience](https://www.servicenow.com/docs/access?context=access-new-project-workspace&family=brazil&ft:locale=en-US) to work on project planning.

-   **Process Mining**

Starting Brazil release, Process Mining Content Pack for SPM \(`com.snc.itbm_po`\) will be migrated to Process Mining Content Pack store application. Upgrade your instance to Brazil or higher releases. For more information, see [Process Optimization](https://www.servicenow.com/docs/access?context=process-mining&family=brazil&ft:locale=en-US) documentation.

-   **Now LLM Service**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr></tbody>
</table>## Activation information

Review information on how to activate Project Portfolio Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **Activation information**

Project Portfolio Management is available with activation of the PPM Standard \(com.snc.financial\_planning\_pmo\) plugin. For more information on activation, see [Activate](https://www.servicenow.com/docs/access?context=t_ActivateProjectPortfolioSuiteWithFinancials&family=zurich&ft:locale=en-US).

Install Strategic Spend Tracking for PPM by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Project Portfolio Management is a ServiceNow AI Platform feature that is available with activation of the PPM Standard \(com.snc.financial\_planning\_pmo\) plugin. For details, see [Activate PPM Standard \(Project Portfolio Management\)](https://www.servicenow.com/docs/access?context=t_ActivateProjectPortfolioSuiteWithFinancials&family=australia&ft:locale=en-US).


</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Activate the PPM Standard plugin \(com.snc.financial\_planning\_pmo\) if you have the admin role. This plugin installs the Project Portfolio Management applications, along with their user roles and tables. For more information, see [Activate PPM Standard \(Project Portfolio Management\)](https://www.servicenow.com/docs/access?context=t_ActivateProjectPortfolioSuiteWithFinancials&family=brazil&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Project Portfolio Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Project Portfolio Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Project Portfolio Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Project Portfolio Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Project Portfolio Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   Synchronize resource assignment dates with the project end dates, and end resource assignments automatically when a project reaches its end date.
-   Manage all project-specific resource assignments in one place by accessing the resource page directly from Project Workspace.
-   Identify similar demand records based on contextual similarity in the name, description, and business case content using the identify similar records Now Assist skill.
-   Convert demands to Enterprise Agile Planning \(EAP\) entities, such as Epic, Feature, or Capability, directly from Demand Management.

 See [Project Portfolio Management](https://www.servicenow.com/docs/access?context=c_ProjectPortfolioSuite&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Update the idea and demand-related system properties by using the idea\_admin or pps\_admin roles.
-   Link AI systems to demands in Demand Management.
-   Generate a concise summary of a demand by using the demand summarization skill.

 See [Explore Project Portfolio Management](https://www.servicenow.com/docs/access?context=explore-project-portfolio-management&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   Gather and evaluate ideas, and promote accepted ideas to a demand, story, epic, or project.
-   Assess, approve, and promote demands to strategic and operational work.
-   Manage projects, programs, and portfolios, along with their resources and financials, from a single suite of applications.
-   Execute work using a traditional waterfall methodology, an Agile approach, or a hybrid of the two.

 See [Project Portfolio Management](https://www.servicenow.com/docs/access?context=c_ProjectPortfolioSuite&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-zurich-brazil/rn-combined-intro.md)

