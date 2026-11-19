---
title: Plan the CSM Agent Workspace migration
description: Some configurations transfer directly to CSM Configurable Workspace, some need to be adapted, and some must be rebuilt. Understand the full scope of the migration before you start.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/migration-plan.html
release: zurich
topic_type: concept
last_updated: "2026-11-13"
reading_time_minutes: 9
breadcrumb: [Migrating to CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Plan the CSM Agent Workspace migration

Some configurations transfer directly to CSM Configurable Workspace, some need to be adapted, and some must be rebuilt. Understand the full scope of the migration before you start.

Reproducing CSM Agent Workspace exactly as it was doesn't take advantage of the improvements in CSM Configurable Workspace. Use the following table to identify the configurations your agents depend on most and prioritize those in your migration order.

**Note:** Because CSM Agent Workspace and CSM Configurable Workspace can coexist on the same instance, you can pilot the new workspace with a smaller agent group before switching everyone over.

## Check which configurations carry over

To address the most commonly required changes first, start with form headers and ribbons, which are quick wins because the tables are shared. Then migrate highlighted values, UI actions, chrome header settings, and the New Record menu. Rebuild landing pages last because they require the most work.

|Configuration|What happens when you migrate|Action required|
|-------------|-----------------------------|---------------|
|[Ribbons](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-form-ribbons.md)|Ribbon settings are shared between both workspaces. Ribbon widgets carry over, but legacy ribbon configurations don't. Add ribbon settings to a ribbon configuration for them to appear in CSM Configurable Workspace.|Verify only|
|[Form headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-form-headers.md)|Existing form headers are accessible without modification but must be linked to the CSM Configurable Workspace configuration. A base system configuration record is provided.|Verify only|
|[Lists and list categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-lists.md)|List configurations carry over. Verify role-based audience access after migration. In CSM Configurable Workspace, audience access uses a separate many-to-many applicability table.|Verify only|
|[Agent Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-agent-assist.md)|Agent Assist settings carry over. Verify the search source configuration after migration.|Verify only|
|[Activity stream](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-activity-stream.md)|The activity stream works in CSM Configurable Workspace but uses a different component. Map legacy parameters to UI Builder component parameters.|Verify only|
|[Forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-forms.md)|Workspace form configurations work without modification, but the two workspaces handle form components differently. In CSM Agent Workspace, the form component includes the header, UI action bar, and activity stream. In CSM Configurable Workspace, these are separate components.|Verify only|
|[Agent Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-agent-chat.md)|Agent Chat configurations work with CSM Configurable Workspace. Some parameters are hidden in UI Builder and can't be configured there.|Carries over|
|[Declarative actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-form-declarative-actions.md)|Custom declarative actions must be converted to the UXF Client Action type and have corresponding add-on event mappings defined.|Action needed|
|[Global search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-search-config.md)|Global search uses a different configuration table in CSM Configurable Workspace \(sys\_ux\_page\_property\). Verify your search source configuration after migration.|Action needed|
|[Email Composer and Email Viewer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-compose-preview-email.md)|No legacy table equivalent exists. Configure the Email Composer and Email Viewer components in UI Builder.|Action needed|
|[Customer Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-custom-central.md)|Customer Central was available in CSM Agent Workspace on interaction records only, and existing configurations carry over. CSM Configurable Workspace extends Customer Central to case, account, contact, and consumer records. Use the guided setup to configure the additional record types.|Verify only|
|Playbook action cards|Declarative action playbook cards carry over without modification.|Carries over|
|Search sources|Existing search source configurations carry over.|Carries over|
|[Service catalogs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/csm-config-workspace-set-up.md)|Agents can submit service catalog requests on behalf of customers from the workspace. Both workspaces use the Service Workspace Portal for these requests, so your catalog configuration carries over. To verify, navigate to **All** &gt; **Service Portal** &gt; **Portals**, open **Service Workspace Portal**, and check that the **Catalogs** related list includes the catalogs your agents need. To make another catalog available, add it to the **Catalogs** related list. If you can't edit the **Catalogs** related list, switch to the Service Catalog - Service Workspace application. Encourage self-service, and reserve agent-submitted requests for exceptional scenarios.|Carries over|
|Form templates|Existing form templates carry over and are accessible in CSM Configurable Workspace. Decide which form templates agents need, including the fields to prepopulate, the conditions to meet, and the users or groups who can access each template. To choose fields to prepopulate, identify the ones agents use most. Tables with standard fields, such as Order and Major Case, are good candidates for prepopulation.|Carries over|
|[Response templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-response-templates.md)|Response templates aren't available in CSM Agent Workspace, so there's nothing to carry over. Configure them in CSM Configurable Workspace after migration.|Action needed|
|[Highlighted values](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-form-highlights.md)|Highlighted values aren't linked to the CSM Configurable Workspace configuration automatically. They don't appear until you complete the migration steps.|Action needed|
|[New Record menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-new-record-menu.md)|The sys\_aw\_new\_menu\_item approach doesn't exist in CSM Configurable Workspace. Rebuild the menu using the chrome\_tab UX page property.|Action needed|
|[Landing pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-landing-pages.md)|CSM Agent Workspace landing pages use a limited UI Builder and can't be reused directly. Rebuild them in the full UI Builder.|Action needed|
|[UI actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-form-ui-actions.md)|UI actions must have the **Format for Configurable Workspace** check box selected before they appear.|Action needed|
|[Chrome header settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-chrome-header.md)|CSM Agent Workspace uses check boxes on the workspace record. CSM Configurable Workspace uses the chrome\_header UX page property in JSON.|Action needed|
|[Form layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-form-layout.md)|Review existing form layouts and set or create a view specifically for the workspace.|Action needed|
|[Contextual side panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-contextual-side-panel.md)|Review existing side panel configurations and rebuild or reconfigure them in UI Builder.|Action needed|
|[Client scripting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-client-scripts.md)|Review each client script. Scripts that manipulate the DOM don't work in CSM Configurable Workspace.|Action needed|
|DOM manipulation|Not supported. Rebuild customizations using UI Builder components.|Not supported|
|Jelly scripting|UI macros, UI pages, and formatters that use Jelly scripting don't appear in CSM Configurable Workspace. Rebuild them in UI Builder through a page collection page.|Not supported|

**Note:** Changes to your CSM Agent Workspace configuration can also affect CSM Configurable Workspace, and the reverse is also true. Test in both workspaces after any configuration change until your migration is complete.

## Major Case Management

If your agents use Major Case Management in CSM Agent Workspace, decide whether they need to access it from CSM Configurable Workspace. Major Case Management configurations, such as lists, filters, fields, processes, and access controls, don't move automatically. Review them so that major case managers don't have to switch between the Core UI and the workspace. Use manager-specific lists and form layouts so that major case managers don't see information that's more relevant to agents. For more information, see [Configure major issue management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/configure-major-issue-management.md).

## Set migration goals and design the workspace for agents

Define what you want your agents to achieve before you configure anything, and use those goals to guide every configuration decision. Agents know which parts of CSM Agent Workspace slow them down and which parts they rely on, so involve agents or team leads when you set goals.

Define the key performance indicators \(KPIs\) that you're optimizing for, such as first contact resolution rate, average handle time, and customer satisfaction \(CSAT\) scores. Make sure that each workspace element you configure, such as lists, landing pages, and agent assist features, aligns with these KPIs.

-   Write goals as measurable outcomes. For example, write "Reduce the steps to create a case from the landing page" rather than a general statement such as "Make the workspace faster."
-   Map each goal to a specific feature in CSM Configurable Workspace before you start migrating.
-   Define your agent groups, such as frontline agents and team managers, and identify whether each group needs a different page layout or different features. You use these groups to set up audiences in UI Builder.

|Goal|Configuration to prioritize|
|----|---------------------------|
|Reduce the average resolution time for high-priority cases|Add a gauge visualization to the [landing page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-landing-pages.md) that shows the percentage of cases that met their SLAs over the past seven days.|
|Reduce case creation time|Set up the [New Record menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-new-record-menu.md) so that agents can create cases in one click. Configure form templates to prepopulate common fields.|
|Surface customer history without switching tabs|Configure the [contextual side panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-contextual-side-panel.md) so that agents see customer history on the record page.|
|Reduce missed SLA deadlines|Configure the ribbon to show the SLA timer. Set up case action status to highlight cases approaching their deadline.|
|Faster wrap-up after each interaction|Configure interaction wrap-up so that agents can log outcomes and close interactions quickly.|
|Tailor the workspace per agent group|Create [landing page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-landing-pages.md) variants in UI Builder. For example, create an agent landing page that shows assigned cases and an agent manager landing page that shows team-level analytics.|

