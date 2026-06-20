---
title: Combined Common Core release notes for upgrades from Xanadu to Zurich
description: Consolidated page of all release notes for Common Core from Xanadu to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-xanadu-zurich/zurich-xanadu-commoncore-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 11
breadcrumb: [Products combined by family]
---

# Combined Common Core release notes for upgrades from Xanadu to Zurich

Consolidated page of all release notes for Common Core from Xanadu to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Common Core release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Common Core to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Common Core.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Entity Based Access](https://servicenow-staging.fluidtopics.net/access?context=entity-based-access&family=yokohama&ft:locale=en-US)**

Implement data segregation and detailed access management so that users can access only the permitted data through entity-based access. Administrators can grant access to an entity's related records by adding users or user groups or by using entity user fields for entity-based access configuration. You can enhance your data security and minimize the risk of unnecessary data exposure while ensuring that only authorized users can access an entity's related records.

-   **[Gen AI issue summarization](https://servicenow-staging.fluidtopics.net/access?context=generate-grc-issue-resolution&family=yokohama&ft:locale=en-US)**

Optimize the GRC issue resolution agentic AI workflow in the Integrated Risk Management application to help your issue managers and analysts resolve GRC issues with AI agents in the Now Assist panel. This workflow makes the issue resolution process more efficient by introducing targeted solutions for key steps in the issue management life cycle.

-   **[Gen AI issue summarization](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-irm&family=yokohama&ft:locale=en-US)**

Summarize an issue by using the Now Assist for IRM application to provide quicker context gathering and contextual awareness. You can quickly analyze the issue records, including the description, activity log, and remediation tasks, and then generate a concise summary that provides you with a concise context of the issue to help you resolve it. Check your entitlements to determine whether you have access to issue summarization.

-   **[Searching user groups to understand the licensing treatment](https://servicenow-staging.fluidtopics.net/access?context=grc-licensing-summary-dashboard&family=yokohama&ft:locale=en-US)**

Use the enhanced GRC licensing summary dashboard to understand the licensing treatment of users that are added to the group by roles that are mapped or assigned to the group.

-   **[Overview of an agency record](https://servicenow-staging.fluidtopics.net/access?context=regulatory-agency-library-rcm&family=yokohama&ft:locale=en-US)**

View the pie charts that depict the total number of emails that are sent to the various regulatory domains. On the overview page of a regulatory agency, you can view the domains where the maximum number of emails were sent and access the Emails Tracker page directly from an agency record. You can also filter and display only the relevant emails that were sent to a specific agency.

-   **[Document designer integration](https://servicenow-staging.fluidtopics.net/access?context=configuring-audit-word-based-templates&family=yokohama&ft:locale=en-US)**

Update and add content by using Microsoft 365 for ServiceNow Reporting, which is now integrated with the Document designer application. You can insert data and reports into a Microsoft Word document.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Entity based record access update utility guided experience](https://servicenow-staging.fluidtopics.net/access?context=entity-based-access-playbook&family=zurich&ft:locale=en-US)**

Apply entity-based access \(EBA\) restrictions at the record level by using guided assistance in the entity based record access update utility. Guided assistance consists of a four-step process:

    1.  Define the scope for the relevant entities
    2.  Scope the record types
    3.  Apply the conditions to each record type to refine the scope
    4.  Review the selected records before you execute and initiate the update
See the execution logs for a status after each update. You can get the details about the impacted records, applied scopes, and outcomes.

-   **[\[Placeholder link text to key report-a-grc-issue\]](https://servicenow-staging.fluidtopics.net/access?context=report-a-grc-issue&family=zurich&ft:locale=en-US)**

The report a GRC issue AI agent is now available in the Employee Center, enabling employee users to report issues through a guided conversational experience. As users respond to prompts, the agent structures the issue and recommends relevant controls, entities, and policies based on the input provided. The AI agent helps ensure that the issue is well-defined and enriched with contextual information before it's submitted.

-   **[Entity based record access rules to secure new records](https://servicenow-staging.fluidtopics.net/access?context=continuous-monitoring-of-entity-based-access&family=zurich&ft:locale=en-US)**

Configure entity-based record access rules on record types to ensure that access restrictions are applied automatically to secure new records or modified records related to entities with active EBA configurations.

-   **[\[Placeholder link text to key continuous-monitoring-of-entity-based-access\]](https://servicenow-staging.fluidtopics.net/access?context=continuous-monitoring-of-entity-based-access&family=zurich&ft:locale=en-US)**

Maintain seamless access for users and groups referenced in record fields when entity-based access restrictions are applied. This feature enables users and groups referenced in a record’s user or group fields to access the records they are associated with. By configuring record-level user access at the table or record type level, it reduces administrative overhead and streamlines EBA adoption with minimal disruption.

-   **[Deactivation of entity-based access configuration](https://servicenow-staging.fluidtopics.net/access?context=deactivating-entity-based-access&family=zurich&ft:locale=en-US)**

Deactivate the entity-based access configuration, enabling the system to automatically assess the records that it impacts. If entity-based access configuration is restricting a record, the access restrictions are removed. If other configurations also apply to the record, the restrictions remain in place and only the selected configuration is deactivated.

-   **[\[Placeholder link text to key functional-domain-bulk-update\]](https://servicenow-staging.fluidtopics.net/access?context=functional-domain-bulk-update&family=zurich&ft:locale=en-US)**

Apply or remove domain-specific tags across multiple records at once. This streamlines workspace management by letting you quickly filter and organize records, for example, you can exclude non-privacy-tagged items in the Privacy Workspace for a more focused, efficient view.

-   **[Entity record page enhancements](https://servicenow-staging.fluidtopics.net/access?context=entities-in-risk-ws&family=zurich&ft:locale=en-US)**

The Entity type and Downstream Risks \(now renamed as Risks\) related lists on the Entity record page have been converted to UIB pages, providing a more intuitive and modern interface. The Downstream Risks related list has been moved to the dedicated Risks page, featuring organized tabs for Directly related risks, Suggested risks, and All risks.

**Note:** You may experience issues with custom actions that emit events on the Risks or Entity type related lists on the Entity record page. To ensure a smooth transition and adopt these changes, refer to [KB2593527](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2593527) for detailed guidance.

-   **[Model Text Protocol \(MCP\) Client](https://servicenow-staging.fluidtopics.net/access?context=mcp-client&family=zurich&ft:locale=en-US)**

Enable users of the ServiceNow® AI Agent Studio to access tools that are hosted externally and published using an MCP Server via the Model Context Protocol Client application.

Authenticate users with the MCP Server to add the MCP tool to an AI agent.

-   **[Create an AI agent](https://servicenow-staging.fluidtopics.net/access?context=configure-next-best-action-agent&family=zurich&ft:locale=en-US)**

The **Add** button on the **AI agents** tab is added as a drop-down providing different agent types for AI agent creation:

    -   Chat
    -   External
-   **[Configure ACLs for AI agents and agentic workflows](https://servicenow-staging.fluidtopics.net/access?context=aia-security-implementation&family=zurich&ft:locale=en-US)**

Configure the Access Control Lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.

-   **[\[Placeholder link text to key configuration-of-tasks\]](https://servicenow-staging.fluidtopics.net/access?context=configuration-of-tasks&family=zurich&ft:locale=en-US)**

Easily manage which configurations appear on the My Tasks page by marking them Active or Inactive. This gives you flexibility to enable or disable configurations without manual intervention, simplifying administration and improving control. An Active/Inactive flag has also been introduced in the My Choice table for enhanced configuration management.


-   **[\[Placeholder link text to key what-is-an-entity\]](https://servicenow-staging.fluidtopics.net/access?context=what-is-an-entity&family=zurich&ft:locale=en-US)**

Entity names in GRC now automatically update when the associated CI name changes. This enhancement improves data consistency, reduces manual effort, and ensures alignment between CI and Entity records without requiring custom automation.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Common Core features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Column Organization](https://servicenow-staging.fluidtopics.net/access?context=create-an-audit-report-template&family=yokohama&ft:locale=en-US)**

You can select and reorder columns when adding a table into your template by using the Document designer Microsoft Word add-in. You can now organize your content better to meet your reporting needs.

-   **[Create content configurations](https://servicenow-staging.fluidtopics.net/access?context=create-content-configurations&family=yokohama&ft:locale=en-US)**

You can add up to 20 columns in a table and content block by using the Document designer application. You now have more flexibility with customizing your table and content block to meet your reporting needs.


-   **[Some Now Assist skills are turned on by default](https://servicenow-staging.fluidtopics.net/access?context=now-assist-skills-on-by-default&family=yokohama&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Changes to Now Assist usage measurement](https://servicenow-staging.fluidtopics.net/access?context=monitoring-now-assist-usage&family=yokohama&ft:locale=en-US)**




</td></tr><tr><td>

Zurich

</td><td>

-   **[States in the entity based record access update utility](https://servicenow-staging.fluidtopics.net/access?context=eba-configuration-states&family=zurich&ft:locale=en-US)**

A new Preview state has been added to the record access update utility life cycle. You can now review the estimated number of impacted records before you apply the restrictions. This step helps you to validate the selected scope, assess potential impacts, and make adjustments, if needed. It also adds an extra layer of control and reduces the risk of unintended access changes.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Common Core features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Common Core features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

The template data relationship table has been removed and deprecated for the Document designer application.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Common Core.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

Install Integrated Risk Management and Now Assist for IRM by requesting them from ServiceNow Store. 

</td></tr><tr><td>

Zurich

</td><td>

Install Integrated Risk Management and Now Assist for IRM by requesting them from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Common Core we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Common Core we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Common Core, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Common Core we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Common Core we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   Generate a GRC issue action plan by using the agentic AI workflow.
-   Segregate data by entities and granular access management when using entity-based access.
-   Summarize an issue by using generative AI to provide quicker context gathering and contextual awareness. With this feature, you can improve the efficiency and productivity of your analysts on GRC issues.
-   Use the enhanced GRC licensing summary dashboard to understand the licensing treatment for users that are added to the group by roles that are mapped or assigned to the group.
-   Select a user record on the licensing summary dashboard and select the role hierarchy to see all the parent roles that are assigned to the user and their role hierarchies.
-   Monitor the email activity from the Overview page for regulatory agencies.
-   Update and add content by using Microsoft 365 for ServiceNow Reporting, which is now integrated with the Document designer application.
-   Add up to 20 columns in a table and in a content block by using the Document designer application.
-   Select and reorder columns by using the Document designer Microsoft Word add-in while creating templates.

 [Yokohama Patch 11](https://servicenow-staging.fluidtopics.net/access?context=yokohama-patch-11&family=yokohama&ft:locale=en-US)

-   Some Now Assist skills are now turned on by default.
-   Review changes to Now Assist usage measurements.

 For detailed documentation, see [Common GRC features](https://servicenow-staging.fluidtopics.net/access?context=common-grc-features&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

-   Use the report a GRC issue AI agent in the Employee Center to report issues through a guided conversational experience.
-   Ensure seamless access for users and groups referenced in user fields on records by leveraging entity-based access restrictions through record attribute user access configuration. Minimize manual effort, reduce administrative overhead, and enable entity-based access with minimal disruption.
-   Configure which task and tab settings appear in My Tasks by marking them Active or Inactive in the applicable table for easier management. Use the Active/Inactive flag in the GRC choice table to control visibility.
-   Automatically sync and maintain entity names in GRC with associated CI names to improve data consistency and reduce manual effort.
-   Authenticate users with the MCP Server to add a Model Context Protocol tool to AI agents using the Model Context Protocol Client.
-   Create ACLs for AI agents and agentic workflows to customize who can discover and trigger AI agents and agentic workflows.
-   Generate control recommendations for each regulatory alert to address compliance requirements. Use these suggestions to save time, minimize manual effort, and ensure a consistent response to regulatory changes.
-   Apply access restrictions at the record level by using the record access update utility in guided assistance. You can also preview the impacted record counts before updating and review the results and execution logs after the update.
-   Apply access restrictions automatically to newly created or modified records using entity-based record access rules.
-   Deactivate the entity-based access configurations.
-   Enable entity-based access on custom GRC tables.

 For detailed documentation, see [Common GRC features](https://servicenow-staging.fluidtopics.net/access?context=common-grc-features&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-xanadu-zurich/rn-combined-intro.md)

