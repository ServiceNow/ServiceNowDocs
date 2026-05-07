---
title: Changes to Australia features and products
description: Cumulative release notes summary on changes to Australia features and products.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-05-04"
reading_time_minutes: 72
breadcrumb: [Release notes summaries for Australia features, Release notes for upgrading from Zurich, Learn about the Australia release, Australia release notes]
---

# Changes to Australia features and products

Cumulative release notes summary on changes to Australia features and products.

Existing  products were updated and changed in Australia. This includes the renaming of certain buttons or features.

<table id="rn-summary-changes-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Control Tower

</td><td>

Not applicable.

</td></tr><tr><td>

AI Desktop Actions

</td><td>

-   **[Optional Application name field](https://www.servicenow.com/docs/access?context=add-details-desktop-action-ad&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The Application field in the Details tab is now optional, enabling you to save and run desktop actions without entering an application name.

-   **[Improved connectors descriptions for non-UI block desktop actions](https://www.servicenow.com/docs/access?context=desktop-actions-designer-workspace-ad&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

Descriptions for Excel, Word, PDF, and System Actions connectors are enhanced to improve accuracy and selection.


</td></tr><tr><td>

AI Search

</td><td>

-   **[Now Assist Multi-Content Response Genius Results](https://www.servicenow.com/docs/access?context=now-assist-multi-content-qna-genius-results&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

If you have Now Assist in AI Search installed, Now Assist Multi-Content Response Genius Results are supported in global and workspace search. Activating Now Assist Multi-Content Response Genius Results in global or workspace search profiles overrides all other Genius Result configurations, so that global and workspace searches only display Genius Result answers from Now Assist Multi-Content Response Genius Results. Virtual Agent topic citations from Now Assist Multi-Content Response Genius Result answers in global or workspace search open the selected topic in the Now Assist panel so the user can continue their conversation on that topic.

-   **[Search Suggestions](https://www.servicenow.com/docs/access?context=search-suggestions-overview&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Search administrators with the ais\_admin granular admin role can access all Search Suggestions tables. Assign search administrators this role to eliminate needless propagation of full admin access.

-   **[Gain insights into search behavior with a refreshed and updated Search Preview UI.](https://www.servicenow.com/docs/access?context=search-preview-ui-new&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Preview search query results using settings from a search application configuration or a search profile. Choose between keyword and hybrid search modes. Display search results as individual EVAM cards or as a JSON-format search query response object, with search and syntax highlighting. Review search query behavior and results and specify search query settings with the new Summary, Genius Results, Details, and Profile admin tools.


</td></tr><tr><td>

API

</td><td>

The following tables lists changed API classes and methods in Australia and ServiceNow Store.

</td></tr><tr><td>

Access Management

</td><td>

-   **[Query ACLs](https://www.servicenow.com/docs/access?context=query-acl-rule&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Query ACLs now load automatically during plugin installation for most platform plugins. These preconfigured ACLs reduce the need to run the QueryRangeACLAuditor tool to generate query ACLs. Store app query ACLs aren't included in preconfigured query ACLs. For more information about preconfigured query ACLs, see the [Maintenance Information \[KB2046494\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2046494) article in the Now Support Knowledge Base.

Existing custom query ACLs are preserved and loaded as inactive. To view inactive ACLs, use this command: `<INSTANCE_URL>/sys_security_acl_list.do?[query_parameters]`

QueryRangeACLAuditor tool modifications are preserved.

-   **[ACL rule types](https://www.servicenow.com/docs/access?context=acl-rule-types&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Core field and datatype ACLs are replaced with more comprehensive rules to optimize ACL volume.


-   **[Access Analyzer](https://www.servicenow.com/docs/access?context=access-analyzer&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Use ServiceNow® Access Analyzer v6.1, a tool designed for AI administrators or creators to validate the access controls configured within agentic assets \(agentic workflows and AI agents\) on the ServiceNow AI Platform.

**Important:** Access Analyzer is available in the ServiceNow Store. For more information, visit [ServiceNow Store](https://store.servicenow.com/store).


</td></tr><tr><td>

Accounts Payable Operations

</td><td>

-   **[Configure Document Intelligence using Now Assist for Accounts Payable Operations \(APO\)](https://www.servicenow.com/docs/access?context=configure-di-using-now-assis&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)**

The Document classification skill auto-classifies supplier email attachments as invoice, credit memo, or supporting documents with an AI-recommended confidence score. After the classification, separate invoice processing cases are created for invoices and credit memo with supporting documents linked to both the cases. The playbook allows you to configure the confidence threshold for auto-approval or involve AP specialists to manually review them.


</td></tr><tr><td>

Activity Management

</td><td>

-   **[Account and Contact field auto-population](https://www.servicenow.com/docs/access?context=create-crm-touchpoint&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Reduce manual data entry when creating touchpoints by automatically populating the Account and Contact fields when you select an Associated Entity and Associated Record of type Contact, Account, Lead, or Opportunity. Associated Entity and Associated Record fields become read-only after the touchpoint record is created.


</td></tr><tr><td>

Advanced Risk

</td><td>

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr><tr><td>

Agent experience for CSM

</td><td>

-   **[Editable record headers](https://www.servicenow.com/docs/access?context=csm-workspace-agent-actions&version=australia&pubname=australia-customer-service-management&ft:locale=en-US#section_hhb_1tj_23c)**

Enables agents to edit the short description of a record directly from the header field. This feature is available on the following record pages:

    -   Front-line case page
    -   CSM Interaction record page
    -   CSM default record page
-   **[Collaborate component in CSM Configurable Workspace](https://www.servicenow.com/docs/access?context=csm-config-ws-collaborate-component&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Use the Collaborate component in the contextual side panel in CSM Configurable Workspace to communicate and collaborate with stakeholders in real time to resolve cases.

-   **[SLA component on the Front-line case page](https://www.servicenow.com/docs/access?context=csm-front-line-case-page&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Use the Service Level Agreement \(SLA\) component in the contextual side panel on the Front-line case page to view SLAs. The SLA cards appear in the Record Information tab below the record information card.

-   **[Email Interaction record page enhancements](https://www.servicenow.com/docs/access?context=csm-email-interaction-record-page&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Minimize drafts to a dock at the bottom of the workspace page in the inline modeless composer. View activities in the activity feed at the top of the page in reverse order, with the newest entries displayed at the bottom.

-   **[Lookup component added to the Email Interaction record page](https://www.servicenow.com/docs/access?context=csm-email-interaction-record-page&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Enable agents to look up contacts and consumers by name, phone number, or email address and link them to a record.

-   **[Create actions on the Front-line case page](https://www.servicenow.com/docs/access?context=csm-config-ws-action-layout-groups&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Create different types of records by using the **Create** button on the Front-line case page. Selecting an action from the Create button, such as creating an incident or a knowledge gap, opens the form in a modeless dialogue.

-   **[View attachments in modeless dialogs](https://www.servicenow.com/docs/access?context=csm-front-line-case-page-modeless-dialogs&version=australia&pubname=australia-customer-service-management&ft:locale=en-US#section_sk4_drr_23c)**

Enable agents to access and review attachments in modeless dialogs instead of workspace tabs. Agents can easily view attachments while also viewing case information and drafts of emails, comments, or work notes.

-   **[Auto-dismiss alerts in CSM Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-dismiss-alerts-in-csm-configurable-workspace&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Reduce visual clutter through auto-dismissible alerts, which are enabled by default for Info, Low, and Moderate alerts, with a default timer of five seconds. Critical and High alerts remain persistent to ensure important notifications stay visible.

-   **[Maximum number of active tabs in CSM Configurable Workspace](https://www.servicenow.com/docs/access?context=csm-config-workspace-interface&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Agents can open up to 20 active tabs \(previously 10\) in CSM Configurable Workspace to handle multiple tasks simultaneously without losing context.

-   **[Open multiple lists in separate primary tabs](https://www.servicenow.com/docs/access?context=csm-config-workspace-list-views&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Agents can now open multiple lists in different CSM Configurable Workspace primary tabs, enabling seamless context switching between lists without losing their current workspace view.

-   **[Granular admin roles](https://www.servicenow.com/docs/access?context=r_RolesInstalledWithCustomerService&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Enhance security, reduce over-privileged accounts, and enable flexible, task-focused permission management by assigning granular, feature-specific roles to replace broad admin access.


</td></tr><tr><td>

Application Manager

</td><td>

-   **[Unlicensed application information](https://www.servicenow.com/docs/access?context=available-for-you-app-mgr&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

In addition to details about applications that are already licensed, the "Available for you" tab of the Application Manager now includes information about applications that haven't been procured from the ServiceNow Store yet.


</td></tr><tr><td>

Authentication

</td><td>

-   **[OAuth enhancements](https://www.servicenow.com/docs/access?context=api-inbound-and-outbound&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Following are the OAuth enhancements:

    -   Use **Opaque** or **JWT** token option for your inbound integration endpoints.
    -   Use the **Allow access only to APIs in selected scope** option to enable access to the APIs that are explicitly listed in the selected scopes for your inbound integrations.
    -   Use the OAuth Entity Resource tab for outbound integrations to configure resource parameters so they flow into the OAuth token request and are reflected in the token from your OAuth provider.

</td></tr><tr><td>

Build Agent

</td><td>

-   **[Build Agent version parity for PDIs](https://www.servicenow.com/docs/access?context=exploring-build-agent&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Personal Development Instances \(PDIs\) are now updated to match the latest Build Agent version, delivering a consistent experience across both personal and production-track instances. Developers testing and building on PDIs have access to the same capabilities available in production environments.

-   **[Updated interaction limits](https://www.servicenow.com/docs/access?context=exploring-build-agent&version=australia&pubname=australia-application-development&ft:locale=en-US)**

To provide developers more room to iterate, the following Build Agent limits have been increased:

    -   Build Agent \(Trial\): 100 prompts per instance per 30-day cycle
    -   PDIs: 25 prompts per instance per cycle
**Note:** Limits are per-instance, not per-user. Only submitted prompts, which doesn't include plan approvals, contribute to the limit.


-   **[Support for global scope](https://www.servicenow.com/docs/access?context=exploring-build-agent&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Build apps and metadata in the global scope.


</td></tr><tr><td>

Business Continuity Management

</td><td>

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


For more information, see [Business Continuity Management and ServiceNow Store](https://www.servicenow.com/docs/access?context=bcm-and-store&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US).

</td></tr><tr><td>

Case management for CSM

</td><td>

-   **[Major Issue Management](https://www.servicenow.com/docs/access?context=major-issue-management&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Case Type consistency improvements: This update ensures case type consistency when creating and managing major cases and their related child cases, improving accuracy and reducing manual correction.

    -   Create major cases automatically upon approval, and major cases now inherit the same case type as the originating case.
    -   Promote the proposed case directly to a major case I-if no account or consumer or partner exists on the originating major case.
    -   Use the major case's case type and inherit the fields defined in \(sn\_customerservice.case\_fields\_to\_sync\) property or defined through extension point for child cases.
-   **[Task plan templates](https://www.servicenow.com/docs/access?context=task-plan-templates&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Add flexible task dependency management to task plan templates, and support for attachments.

    -   Schedule offsets can be defined when creating dependencies, allowing tasks to start within a specified time period \(minutes, hours, days, or weeks\).
    -   Configure and manage task dependencies directly from task dependency list and view layouts.
    -   Built‑in validations prevent circular dependencies, ensuring task plans remain accurate and reliable.
    -   Ability to attach documents to tasks or cases.
    -   Select **Apply Template** for any published task plan templates to automatically add all document references from the original template items to the newly created tasks, ensuring seamless access for task owners to all required documents.
-   **[Case type selector for creating cases](https://www.servicenow.com/docs/access?context=create-case-of-specific-case-type&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

The case type selector is now activated by default when creating cases of these types:

    -   Interaction
    -   Account
    -   Contact
    -   Consumer
    -   Sold product
    -   Install base item
    -   Related lists: child case, case task
    -   List view
    -   Case task list view

</td></tr><tr><td>

Clone Admin Console

</td><td>

-   **[Updated clone menu navigation items](https://www.servicenow.com/docs/access?context=system-clone-landing&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

All clone-related functions are now available under the Clone Admin Console menu navigation item.

-   **[Submit a new clone even if another clone is scheduled](https://www.servicenow.com/docs/access?context=t_StartAClone&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Create an additional clone request even if there’s already a future clone for that target. This feature helps with the limitation where you can't submit another clone until all existing requests have been canceled.

-   **[Clone summary](https://www.servicenow.com/docs/access?context=t_StartAClone&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Help prevent clone conflicts with the Clone summary, which highlights clones that are scheduled in the next 30 days that involve the same target instance.

-   **[Updated authentication model](https://www.servicenow.com/docs/access?context=configure-target-instance&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Clone Admin Console now uses JWT certificate-based authentication instead of username and password authentication, improving security and simplifying cross-instance authentication.


</td></tr><tr><td>

Cloud Cost Management 10.0

</td><td>

-   **[Granular instance operator role](https://www.servicenow.com/docs/access?context=cloud-insights-roles&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Use the instance operator role to perform routine operational tasks without requiring the full admin role for basic operations. By using limited privileges in the instance operator role, you can help reduce security risks across your organization.


</td></tr><tr><td>

Code Signing

</td><td>

-   **[Guardrail process optimization and scope increase](https://www.servicenow.com/docs/access?context=signature-verification-status&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Allows you to run the guardrail scan and identify records that have missing signatures, enabling you to proactively address records that are eligible for code signing but remain unsigned. Previously, the system only checked records with existing signatures and marked them as valid or invalid, which meant records without signatures were overlooked. Now, the process starts from the signature configuration itself, every eligible record is checked to see if it has a signature. If a record is missing a signature, it's clearly identified.


</td></tr><tr><td>

Configurable Workspace

</td><td>

-   **Record List component bundle enhancements in UI Builder**

Configure these enhancements to the Record List component bundle in UI Builder:

    -   Pin columns to keep them visible while scrolling horizontally.
    -   Change the medium default size for highlighted values.
    -   View list data as a data visualization.
    -   Show a filter overview in the list header for a summary of the filters currently applied to the list.
    -   Catalog variables and questions are supported as list columns.
    -   Open lists in multiple session tabs from the list menu.
    -   Customize gallery list card layouts including images, icons, text placement, and sizing.
-   **[AI filter assist](https://www.servicenow.com/docs/access?context=use-ai-filter-assist&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

Convert everyday language into an encoded query with AI filter assist.

-   **[Track record list changes](https://www.servicenow.com/docs/access?context=use-ai-list-tracker&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

Get an AI-generated summary of recent changes made to a list without manually reviewing each record.

-   **[Grouping for related lists](https://www.servicenow.com/docs/access?context=configure-related-list-grouping&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

Configure related lists to persist selections for the Group by filter.

-   **[Predicate Builder component enhancements in UI Builder](https://developer.servicenow.com/dev.do#!/reference/next-experience/australia/now-components/now-predicate-builder/uib-setup):**

Configure these enhancements to the Predicate Builder component in UI Builder:

    -   Customize condition rows.
    -   Configure a simple filtering mechanism.
    -   Use a search term for filtering panel definitions.
    -   Configure fixed queries.
-   **[Hierarchical queries](https://www.servicenow.com/docs/access?context=data-hierarchies&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Configure a record hierarchy to create filter queries that traverse levels of hierarchy.

-   **[Dynamic queries](https://www.servicenow.com/docs/access?context=working-with-dynamic-schema&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Configure dynamic attributes and dynamic categories to create filter queries that use the dynamic schema field type.

-   **[Form component enhancements in UI Builder](https://developer.servicenow.com/dev.do#!/reference/next-experience/australia/now-components/form%20record%20page/uib-setup):**

Configure these enhancements to the Form component in UI Builder:

    -   Wrap field labels on mobile devices.
    -   Display an indicator dot on unsaved fields.
    -   Add a background color to unsaved fields to make them more noticeable.
    -   Add an address field to forms that searches, validates, and automatically fills an address.
-   **[AI indicator](https://www.servicenow.com/docs/access?context=c_FormFields&version=australia&pubname=australia-platform-user-interface&section=ai-indicator&ft:locale=en-US)**

The AI indicator is a visual cue that identifies form fields in configurable workspace and Core UI that have been updated with AI-generated content, providing a consistent and clear indication of AI involvement across the platform.

-   **[Unsaved field indicator](https://www.servicenow.com/docs/access?context=configure-unsaved-field-indicator&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

Configure the unsaved field indicator for your entire workspace experience instead of individual pages.

-   **[Background color for unsaved fields](https://www.servicenow.com/docs/access?context=configure-background-color-unsaved-indicator&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

Configure a background color to display on unsaved fields for your entire workspace experience instead of individual pages.

-   **[Background color for highlighted values](https://www.servicenow.com/docs/access?context=configure-background-color-highlighted-values&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

Configure a background color for fields with highlighted values.

-   **[Text commands for journal fields](https://www.servicenow.com/docs/access?context=configure-journal-fields-keyboard-shortcuts&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

Configure text commands that can be applied by keyboard shortcuts within journal fields.

-   **[HTML editor toolbar](https://www.servicenow.com/docs/access?context=configure-html-editor-toolbar&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

Configure toolbar options for the HTML editor within journal input fields.

-   **[Inline validation for string fields](https://www.servicenow.com/docs/access?context=format-regex-pattern-string-fields&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

Configure inline validation for string fields that formats inputs automatically, persists guidance text as a placeholder, and restricts unsupported characters.

-   **[Watch lists](https://www.servicenow.com/docs/access?context=configure-watch-list&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

Add and remove yourself and multiple records from a watch list.

-   **[Form Templates component enhancements in UI Builder](https://developer.servicenow.com/dev.do#!/reference/next-experience/australia/now-components/now-record-common-templates-connected/uib-setup)**

Configure these enhancements to the Form Templates component in UI Builder:

    -   Preview form templates before applying them to the record page.
    -   Display an alert message and confirm reuse when a selected form template is already applied to that record.
-   **[Activity Stream component enhancements in UI Builder](https://developer.servicenow.com/dev.do#!/reference/next-experience/australia/now-components/now-activity-stream-connected/uib-setup)**

Configure these enhancements to the Activity Stream component in UI Builder:

    -   Edit and delete Activity stream posts after submitting.
    -   Add knowledge base links from recommended actions to Activity stream posts.
-   **[Keyboard shortcuts for emails](https://www.servicenow.com/docs/access?context=add-response-templates-shortcut&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

Use keyboard shortcuts to open drafts, email templates, and response templates.

-   **[Attachments component enhancements in UI Builder](https://developer.servicenow.com/dev.do#!/reference/next-experience/australia/now-components/now-record-common-attachments-connected/uib-setup)**

Configure these enhancements to the Attachments component in UI Builder:

    -   Open the file viewer as a modeless dialog.
    -   Customize the attachment header, upload instructions, and menu actions in both the full and compact modes.
    -   Display the loading skeleton as a spinner or as three cards.
    -   Enable a visible drop zone for file uploads in the compact mode.
-   **[Form action layout groups for declarative actions](https://www.servicenow.com/docs/access?context=configure-da-layout-group&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

Upgrade form action layout groups to customize the order, label, and icons for declarative actions without altering the base action.

-   **[Declarative actions and UI actions on public pages](https://www.servicenow.com/docs/access?context=using-web-embeddables&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Non-logged in users may access specified declarative actions and UI actions on embedded web pages while maintaining integrity with security guidance and access control list permissions.


</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

-   **[Elevated user roles are no longer required for CMDB tasks](https://www.servicenow.com/docs/access?context=manage-cmdb&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US):**

Access to CMDB tables is no longer restricted to users with elevated privileges. Instead, for improved security, users with access privileges that are trimmed to CMDB features can complete any administrative or end-user CMDB task:

    -   CMDB tables that required the admin or itil\_admin roles are now also accessible to the sn\_cmdb\_admin user role.
    -   CMDB tables that required the itil role are now also accessible to the sn\_cmdb\_editor user role.
For more information, see the [CMDB Granular Role EPIC changes \[KB0561055\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0561055) article in the Now Support Knowledge Base.

-   **[Automatically generate de-duplication tasks for lookup and related tables](https://www.servicenow.com/docs/access?context=id-detect-dup-ci&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

Configure IRE to automatically generate de-duplication tasks for specific lookup or related tables during the identification process. You can then process those de-duplication tasks to remediate any duplications.

-   **[Remediate duplicate related items in lookup tables](https://www.servicenow.com/docs/access?context=id-detect-dup-ci&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

Configure IRE to create de-duplication tasks for duplicate related items in a lookup table, detected during a lookup-based identification. Sort which duplicates do or don't require remediation by configuring the system property **glide.identification\_engine.lookup\_match.create\_duplicate\_task\_ci.enabled**. For more information, see [Detecting duplicate CIs](https://www.servicenow.com/docs/access?context=id-detect-dup-ci&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US#section_unn_yjr_xgc).

-   **[Domain separation for key CMDB tables](https://www.servicenow.com/docs/access?context=c_DomainSeparationSetup&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

The following tables now support domain separation on instances which are configured with domain separation:

    -   Key Value \[cmdb\_key\_value\]
    -   Printer Instance \[cmdb\_print\_queue\_instance\]
    -   Software Instance \[cmdb\_software\_instance\]
    -   Client Access \[samp\_client\_access\]
    -   Oracle Options \[samp\_oracle\_options\]
Domain separation can help protect sensitive information by supporting domain-specific data segregation.

For more information about domain separation and how to activate it, see [Domain separation setup and administration](https://www.servicenow.com/docs/access?context=c_DomainSeparationSetup&version=australia&pubname=australia-platform-security&ft:locale=en-US).

-   **[CMDB Query Builder engine execution modes](https://www.servicenow.com/docs/access?context=query-builder-engine-execution-mode&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

The CMDB Query Builder expanded its support for various types of query structures that can run in V2 engine mode. Also, the performance of running queries in V2 mode is improved. Query structures that aren't supported include related list conditions, NOT operators combined with filters, certain Service Mapping relationships, and OR operators unless explicitly enabled by the **glide.cmdb.query.or\_execution\_mode** system property.


</td></tr><tr><td>

Contract Management Pro

</td><td>

-   **[Send contracts for signature using Adobe Sign without signing in](https://www.servicenow.com/docs/access?context=cncore-nss-review-request&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Send contracts for signature in Adobe Sign without requiring users to sign in to the e-signature portal. Any modifications to the signatory details and contract documents are restricted in the Adobe Sign portal and must be completed in Contract Management Pro before initiating the signature process.

-   **[Compare contract revisions in Contract Management Pro](https://www.servicenow.com/docs/access?context=cmpro-compare-docs&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Compare contract revisions of a contract document stored in external storage.

-   **[Validations for content control placement in the Microsoft Word add‑in](https://www.servicenow.com/docs/access?context=cncore-addin-add-clauses&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

See when a clause, table, or signature block is incorrectly tagged while configuring a contract template through validation messages displayed in the Microsoft Word add-in.

-   **[Improved Microsoft Word document processing](https://www.servicenow.com/docs/access?context=cncore-set-ext-app-config&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Contract Management Pro now supports processing of Microsoft Word documents larger than 10 MB. This enhancement applies to all document operations such as contract revision generation, document synchronization, and document comparison.


</td></tr><tr><td>

Customer Success Management

</td><td>

-   **[Touchpoint home page](https://www.servicenow.com/docs/access?context=account-lifecycle-touchpoint-home&version=australia&pubname=australia-acct-lifecycle-events&ft:locale=en-US)**

Internal touchpoints ensure that the internal teams are aligned on the objectives and outcomes of the engagement.


</td></tr><tr><td>

Data Management for CSM

</td><td>

-   **[Enhanced Customer Data Viewer role](https://www.servicenow.com/docs/access?context=business-stakeholder-for-csm&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

The Customer Data Viewer \(sn\_customerservice.customer\_data\_viewer\) role includes expanded access to additional data tables and menu items. These enhancements enable users to view a broader range of customer data while maintaining read-only access restrictions. With this enhancement, you can:

    -   Extend access to additional tables for the customer data viewer role
        -   Inherit household role in customer data viewer role
    -   Explore additional menu items now accessible to the customer data viewer role.

-   **[Household plugin migration to ServiceNow Store](https://www.servicenow.com/docs/access?context=activate-customer-service-household&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Starting with the Australia release, the Household family plugin \(com.snc.household\) has been migrated to the ServiceNow Store as a standalone application. Any new enhancements to this application are delivered through the Household store app. This change provides improved packaging, versioning, and deployment flexibility for B2C implementations that require household relationship management.


-   **[Guided setup access for granular admin roles](https://www.servicenow.com/docs/access?context=import-csm-accounts&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Access to foundation data steps in guided setup now aligns with CDF admin roles. This access change enables administrators to delegate specific configuration tasks to users based on their assigned roles, providing greater flexibility in managing setup responsibilities.

-   **[Extensible account code support](https://www.servicenow.com/docs/access?context=csm-account-code-account-path&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Updated the account code generation logic to support dynamic length scalability. Account codes now automatically expand from 4 digits to 5 or more as needed, ensuring unlimited account growth without manual intervention. Administrators can resolve invalid insert errors by clearing the system property to regenerate codes based on the maximum existing code.

-   **[Declarative Responsibility Framework enhancements](https://www.servicenow.com/docs/access?context=declarative-resposibility-framework&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Introduced usability and functional enhancements to the Customer Access Management \(CAM\) Declarative Responsibility Framework. These updates streamline access configuration management and improve flexibility for responsibility definitions. With this enhancement, you can now:

    -   Import or copy access configurations from one responsibility definition to another.
    -   Manage CAM-related assets through improved cleanup capabilities.
    -   Reference any field name in the Responsibility Definition field configuration.
-   **[Unified User configuration enhancements](https://www.servicenow.com/docs/access?context=configuring-unified-user&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Added a system property \(sn\_customerservice.consumer.allowed\_user\_types\) to enhance unified user management. This property specifies which user types \(classes\) can be associated with consumers.

-   **[Customer Life Cycle Management Workflows](https://www.servicenow.com/docs/access?context=customer-life-cycle-management-workflows&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Added core primitives to support price and quantity ramps, enabling flexible, time‑based changes across the sold product lifecycle. The feature delivers scalable pricing aligned with usage, simplifies post-sale workflows, and improves revenue forecasting without custom scripts.

-   **[Install base data model enhancements](https://www.servicenow.com/docs/access?context=create-install-base-item&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Improve traceability and product life cycle management with the **Install Base Identifier** field on the install base form. Base install base items are mapped directly to model categories to support industry-specific product configurations.

Added **Provider Service Org** field on the install base form to support tracking, recall workflows, and post-sale engagement with dealers and partners.

-   **[Sold product form](https://www.servicenow.com/docs/access?context=sold-product-form&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Create future‑dated subscription products in a **Pending Activation** state to improve the Add‑Order‑to‑Sold‑Product process. It also ensures lifecycle accuracy, predictable billing, and fair access for customers while improving revenue recognition for businesses.


-   **[Service Model Foundation renamed Entities](https://www.servicenow.com/docs/access?context=renamed-entities&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Renamed Service Model Foundation entities to improve clarity and maintain consistency across the platform. Review your existing configurations, scripts, or integrations that reference these entities and update them accordingly.

**Note:** The entity name changes are available in the Business Location 5.2.0 store app.


</td></tr><tr><td>

Data Privacy

</td><td>

-   **New experience**
    -   [Optional condition filter](https://www.servicenow.com/docs/access?context=dps-create-anonymization-job&version=australia&pubname=australia-platform-security&ft:locale=en-US) when running anonymization jobs to fine tune the scope of data to be anonymized.
    -   [Specific anonymization policy](https://www.servicenow.com/docs/access?context=dps-create-anonymization-policies&version=australia&pubname=australia-platform-security&ft:locale=en-US) for catalog variables to anonymize sensitive data in catalog requests.

</td></tr><tr><td>

DevOps Change Velocity

</td><td>

-   **[Enhanced JFrog integration with DevOps Change Velocity](https://www.servicenow.com/docs/access?context=devops-jfrog-connect-workspace&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Gather JFrog evidence seamlessly and create change records automatically using the improved JFrog integration with DevOps Change Velocity.


-   **[Bearer authentication in JFrog](https://www.servicenow.com/docs/access?context=devops-jfrog-connect-workspace&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Connect to JFrog using the secure bearer token authentication to comply with JFrog’s updated security policies.


-   **[HTTP proxy for Docker](https://www.servicenow.com/docs/access?context=servicenow-custom-actions-for-gitlab&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Connect to DevOps Change Velocity through HTTP proxy settings using environment variables in your Docker deployment for instances that run a proxy server.

-   **[Health scan enhancements](https://www.servicenow.com/docs/access?context=run-health-scan-check&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**
    -   Identify any callback processing issues in your instance.
    -   Identify any access control rule \(ACL\) that is incorrectly associated with a role in your instance.
    -   Verify whether all DevOps tables are present in your instance and confirm whether all metadata in sys\_\* tables is present.
    -   Verify whether all DevOps roles in your instance contain all expected roles, including inherited roles.
-   **[Auto close without Change Management - State Model \[Legacy\] plugin](https://www.servicenow.com/docs/access?context=dev-ops-change-acceleration&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Change requests can now be auto-closed without requiring you to install the Change Management - State Model \[Legacy\] plugin.


</td></tr><tr><td>

Developer Sandboxes

</td><td>

-   **[Upgrade enhancements](https://www.servicenow.com/docs/access?context=dev-sbx-clone-upgrade-info&version=australia&pubname=australia-application-development&ft:locale=en-US)**

After an upgrade, Developer Sandboxes now recreates the sandboxes on an instance and automatically backs up update sets to the base instance.

-   **[Queuing for successive sandbox creation](https://www.servicenow.com/docs/access?context=allocating-sandboxes&version=australia&pubname=australia-application-development&ft:locale=en-US)**

To improve performance, Developer Sandboxes has implemented queuing when multiple sandboxes are created in succession.

-   **[SSO support for vanity URLs](https://www.servicenow.com/docs/access?context=dev-sbx-general-guidelines&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Instances with vanity URLs can now support Single Sign-On \(SSO\).

-   **[Schema change for shared tables isolates the table](https://www.servicenow.com/docs/access?context=dsb-installed-with&version=australia&pubname=australia-application-development&ft:locale=en-US)**

To ensure configuration consistency, if you make a schema change, such as adding a column, to a shared table, the table now becomes an isolated table on the sandbox that initiated the schema change.

-   **[New vibe coding documentation](https://www.servicenow.com/docs/access?context=vibe-coding-landing&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Documentation is now available that introduces vibe coding, which is a natural language approach to application development in ServiceNow, including how to get started, when to use it, and how it fits within the broader suite of AI-powered development tools.


</td></tr><tr><td>

Dispute Content Pack for US Regulations

</td><td>

-   **[Enhanced SLA Definitions for Reg E and Reg Z](https://www.servicenow.com/docs/access?context=using-the-dispute-content-pack-for-us-regulation&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

Improve regulatory adherence in your dispute workflow with the following enhancements to Reg E and Reg Z SLA definitions, ensuring timely dispute resolution and reducing regulatory risk exposure:

    -   SLA tracking now anchors to the dispute report date instead of the case creation date.
    -   SLA timelines for Reg Z are updated to require the financial institution to resolve the dispute within two complete billing cycles or 90 calendar days from the dispute report date.

</td></tr><tr><td>

Dispute Rules Content Pack for Mastercard

</td><td>

-   **[Dispute Rules Content Pack for Mastercard chargeback eligibility rules updates](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

Determine the eligibility of a selected transaction for chargeback through chargeback eligibility rules transformed into technical formulas.

New ineligibility conditions have been added across all five existing RC 4808 Authorization sub-categories:

    -   Required Authorization Not Obtained \(RANO\)
    -   Expired Chargeback Protection Period \(ECPP\)
    -   Stand-in or X-Code Approval after Issuer Decline \(SIXCAID\)
    -   CAT 3 Devices \(CAT3D\)
    -   Transit First Ride Risk Framework Claims \(TFRR\)
Expanded eligibility rules for the following fraud dispute reason codes:

    -   RC 4837 \(No Cardholder Authorization\)
    -   RC 4849 \(Questionable Merchant Activity\)
    -   RC 4870 \(Chip Liability Shift\)
    -   RC 4871 \(Chip Liability Shift – Lost/Stolen/NRI Fraud\)
-   **[Dispute Rules Content Pack for Mastercard intake questionnaire updates](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

Benefit from the dispute questionnaire provided through Dispute Rules Content Pack for Mastercard with some modified questions and added hard stop alerts. Questionnaire questions include RC 4853 Failed Travel Merchant – Intra-EEA and Domestic European Transactions Only as an additional display condition.


</td></tr><tr><td>

Dispute Rules Content Pack for Visa

</td><td>

-   **[Updated questions for the dispute questionnaire](https://www.servicenow.com/docs/access?context=exploring-the-dispute-rules-content-pack-for-visa&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

Added four new agent-facing questions to the dispute questionnaire under the authorization \(11\) and consumer disputes \(13\) categories. These questions map to the following reason codes:

    -   11.1 - Card recovery bulletin or exception file
    -   11.2 - Declined authorization
    -   11.3 - No authorization or late presentment
    -   13.6 - Credit not processed
    -   13.7 - Cancelled merchandise or services
-   **[Visa Resolve Online \(VROL\) version 26.1 updates](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

Updated the dispute questionnaire provided through the Dispute Rules Content Pack for Visa to align with Visa Resolve Online \(VROL\) release 26.1 revision changes.

-   **[Updated chargeback eligibility rules for Visa reason codes 10.1, 10.2, 10.3, 10.4, 13.1, 13.2, 13.3, and 13.4](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

The chargeback eligibility rules for eight Visa reason codes have been updated to reflect Visa Chargeback Guide v1.1. The rules engine evaluates disputes automatically against the updated criteria; no manual configuration is required. Disputes that do not meet the updated eligibility criteria are flagged as ineligible before submission.

-   **[Updated dispute intake questionnaire for fraud disputes involving non-fiat currency and NFTs](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

The fraud dispute intake questionnaire now includes a conditional question for disputes involving non-fiat currency or NFT transactions, such as cryptocurrency and digital token purchases. When the transaction is identified as a digital asset purchase, dispute agents and cardholders are asked to confirm whether the cardholder claims they were deceived into sending the asset to a fraudulent recipient. The question is shown only when relevant and is cleared automatically when it does not apply. This supports accurate eligibility evaluation without requiring agents to manually identify digital asset transaction types.

-   **[Updated dispute intake questionnaire for RC 13.3 \(Not as Described\) disputes involving non-fiat currency and NFTs](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

The consumer dispute intake questionnaire for RC 13.3 now includes an additional question for disputes involving non-fiat currency or NFT purchases. After confirming whether the asset received matched the description at the time of purchase, dispute agents and cardholders are asked whether there is evidence that the merchant guaranteed or promised the asset would increase in value. This question determines whether a specific dispute right applies, and appears only after the preceding NFT description question is answered.


</td></tr><tr><td>

Domain Separation

</td><td>

-   **Dot-Walk Scoping Bypass Compliance \(DIRS0000335\)**

Domain Separation has been updated to comply with the platform-wide dot-walk scoping bypass directive \(DIRS0000335\). Customers who have customizations involving dot-walk queries on domain-separated tables should review their configurations after upgrading.

-   **Java 21 Runtime Support**

Domain Separation has been validated and updated to run on the Java 21 runtime introduced in the Australia release. Deprecated Java APIs have been removed from the Domain Separation codebase. No action is required for customers — this update is included automatically with the Australia upgrade.


</td></tr><tr><td>

Enterprise Architecture

</td><td>

-   **[Granular admin role changes in Enterprise Architecture](https://www.servicenow.com/docs/access?context=eaw-gran-admin-role-changes&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)**

Added the granular level admin role \(sn\_apm.apm\_admin\) to the following system properties in the Enterprise Architecture:

    -   **sn\_apm\_trm.is\_product\_life\_cycle\_tech\_debt\_enabled**: Make this property false to disable calculating level 2 technical debt.
    -   **glide.ui.sn\_apm\_trm\_product\_request\_activity.fields**: TRM Product Request activity formatter fields.
    -   **sn\_apm\_trm.noOfPublishersPerTRMPage**: The number of publishers to show per page.
    -   **glide.ui.sn\_apm\_trm\_product\_lifecycle\_request\_activity.fields**: TRM Product Lifecycle Request activity formatter fields.
    -   **sn\_apm.noOfSoftwareModelsPerTPMPage**: The number of software models to show per page. This property is used for client-side pagination.
    -   **sn\_apm.discoveryModelProductTypesForTPMSuggestions**: Product types of discovery models to consider for TPM software suggestions.
    -   **sn\_apm.noOfSDLCComponentPerTPMPage**: The number of Agile Development components to show per page.
    -   **glide.ui.cmdb\_ci\_business\_app\_activity.fields**: Business application activity formatter fields.
    -   **sn\_apm.startRangeOfTPMLifecycle**: The number of years before the current date is included when displaying software model lifecycle phases in the TPM timeline.
    -   **sn\_apm.endRangeOfTPMLifecycle**: The number of years beyond the current date is included when displaying software model lifecycle phases in the TPM timeline.
    -   **noOfBusinessAppsPerTPMPage**: The number of business applications to show per page.

-   **[Enhancements to the My certifications section](https://www.servicenow.com/docs/access?context=manage-requests-certs-assessments&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)**

View only the certifications that are relevant to you in the **My certifications** tab on the Enterprise Architecture Workspace home page.


-   **[Enhancements to the Application Portfolio](https://www.servicenow.com/docs/access?context=eaw-work-with-application-portfolio&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)**

Business applications with the Retired state or Lifecycle stage as End of life are no longer displayed in the Business Portfolio section.


</td></tr><tr><td>

Enterprise Asset Management

</td><td>

-   **[Multiple assets and asset groups in a work order](https://www.servicenow.com/docs/access?context=create-eam-work-order-task&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

A work order and work order task can now be created for asset groups in addition to individual assets. Additionally, the sn\_eam.enterprise\_asset\_manager role can add more assets to tasks while they're in the draft stage. When technicians start the task, they can take action on all included assets. The Deploy Asset, Swap Asset, and Remove Asset actions within work order tasks support multiple assets and asset groups.

-   **[Shutdown and Startup work types](https://www.servicenow.com/docs/access?context=create-eam-work-order-task&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

The **Shutdown** and **Startup** work types available in the work order tasks enable you to manage asset shutdown and restart tasks.

-   **[Multiple calibration playbooks](https://www.servicenow.com/docs/access?context=complete-eam-work-order&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

When a calibration work order is created for multiple assets or an asset group, the system generates a separate calibration playbook for each asset in the Affected assets list.

-   **[Multiple condition lines](https://www.servicenow.com/docs/access?context=perform-condition-assessment-webui&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

When an asset condition work order is created for multiple assets or an asset group, the system generates a separate condition line for each asset in the Affected assets list. All condition lines must be evaluated before the work order can be completed.


</td></tr><tr><td>

External Content Connectors

</td><td>

-   **[Sitemap support in the Webcrawler external content connector](https://www.servicenow.com/docs/access?context=webcrawler-external-content-connector&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Retrieve content and links from URLs found in sitemaps defined for your web source system when running content crawls for the Webcrawler external content connector. A content crawl only retrieves sitemap URLs that include the crawl's starting point URL.

-   **[Start point links for scheduled partial content crawls](https://www.servicenow.com/docs/access?context=create-content-crawl-external-content-connector&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

View the start point for a scheduled partial content crawl via a link in its entry in the the external content connector's list of crawls.

-   **[Start point links in partial content crawl history entries](https://www.servicenow.com/docs/access?context=review-crawl-ext-cont-connector&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

View the start point for a scheduled partial content crawl via a link in its crawl history entries.

-   **[Limited Role-Based Access Control \(RBAC\) support in the Atlassian](https://www.servicenow.com/docs/access?context=atlassian-confluence-cloud-external-content-connector&version=australia&pubname=australia-platform-administration&ft:locale=en-US) Confluence Cloud external content connector**

Map source system user and group permissions assigned via RBAC roles to users in your ServiceNow AI Platform instance.


</td></tr><tr><td>

Field Service Management

</td><td>

-   **[ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home)**

The following plugins are planned for deprecation in the C release. Beginning with the Australia release this plugin will be migrated to a store application. Upgrade your instance to Australia or later release versions and the store applications will be automatically installed.

Beginning with the Australia release, the following applications have been moved to the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home). Any application enhancements will be delivered through the related store app.

    -   [Advanced Appointment Booking](https://www.servicenow.com/docs/access?context=appintment-booking-day-level-config&version=australia&pubname=australia-field-service-management&ft:locale=en-US) \(com.snc.advanced\_appointment\_booking\)
    -   [Field Service Contractor Management](https://www.servicenow.com/docs/access?context=configuring-fsm-contractor-management&version=australia&pubname=australia-field-service-management&ft:locale=en-US) \(com.snc.fsm\_contractor\_management\)
    -   [Field Service Marketplace](https://www.servicenow.com/docs/access?context=configuring-contractor-marketplace&version=australia&pubname=australia-field-service-management&ft:locale=en-US) \(com.snc.fsm\_marketplace\)
    -   [Field Service Territory Planning](https://www.servicenow.com/docs/access?context=configuring-territory-planning-fsm&version=australia&pubname=australia-field-service-management&ft:locale=en-US) \(com.snc.fsm\_territory\_planning\)
    -   Field Service Advanced Capacity and Reservations management \(com.snc.fsm\_advanced\_capacity\_management\)
    -   [Field Service Capacity and Reservations Management](https://www.servicenow.com/docs/access?context=configuring-capacity-management&version=australia&pubname=australia-field-service-management&ft:locale=en-US) \(com.snc.fsm\_capacity\_management\)
    -   [Field Service with Service Locations Support](https://www.servicenow.com/docs/access?context=Configuring-service-location&version=australia&pubname=australia-field-service-management&ft:locale=en-US) \(com.snc.fsm\_service\_locations\)
    -   [Technician driven sales with Field Service](https://www.servicenow.com/docs/access?context=create-opportunity&version=australia&pubname=australia-field-service-management&ft:locale=en-US) \(com.snc.fsm\_technician\_sales\)
    -   [Schedule Optimization](https://www.servicenow.com/docs/access?context=schedule-optimization-engine-plugin&version=australia&pubname=australia-field-service-management&ft:locale=en-US) \(com.snc\_schedule\_optimization\)
    -   [Field Service Quality Management](https://www.servicenow.com/docs/access?context=config-quality-mgmt&version=australia&pubname=australia-field-service-management&ft:locale=en-US)
    -   [Field Service Mobile Agent](https://www.servicenow.com/docs/access?context=setting-up-field-service-mobile-agent&version=australia&pubname=australia-field-service-management&ft:locale=en-US)
    -   Map Integrations for Field Service \(com.snc.app\_fsm\_map\_integr\)
    -   Beans.ai plugin \(com.sn\_beans\_ai\_spoke\)
    -   [Intelligent Task Recommendations](https://www.servicenow.com/docs/access?context=activate-intelligent-task-recommendation&version=australia&pubname=australia-field-service-management&ft:locale=en-US) \(sn\_fsm\_task\_rec\)
    -   [Field Service Management Scheduling Automations](https://www.servicenow.com/docs/access?context=activate-intraday-scheduling-plugin&version=australia&pubname=australia-field-service-management&ft:locale=en-US) \(sn\_fsm\_sched\_flws\)
    -   Application Common Configuration \(sn\_app\_cmn\_config\): This is a component of Dispatcher Workspace.
    -   Intelligent Task Recommendations \(sn\_task\_recommend\): This is a component of Intelligent Task Recommendations.
-   **[Google maps ID](https://www.servicenow.com/docs/access?context=r_PropInstallWFieldServMgmnt&version=australia&pubname=australia-field-service-management&ft:locale=en-US)**

The **google.maps.map\_id** system property enables Field Service Management to use Google Maps for cloud-based map styling, vector mapping, and advanced markers. You must obtain your own map ID.


</td></tr><tr><td>

Financial Services Card Operations

</td><td>

-   **[Automated document submission in Mastercard transaction dispute process](https://www.servicenow.com/docs/access?context=chargeback-stage-mastercard&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

Streamline the submission of supporting documents to Mastercard in the Mastercard Dispute Management workflow through document attachment and validation. Attached files are automatically checked against Mastercard requirements for file type and size. This update reduces the need for manual intervention, minimizes rework, and helps avoid rejection risk.

-   **[New subflow and action to support Card data security](https://www.servicenow.com/docs/access?context=card-data-security&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

Support attaching documents to a specified table record using the following subflow and action in Card data security:

    -   Attach Document to Table Record
    -   Attach Tokenized Document to Table Record

</td></tr><tr><td>

Financial Services Operations Core

</td><td>

-   **[Case type selector](https://www.servicenow.com/docs/access?context=csm-case-type-select-modals&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Filter service definitions using the case type selector in FSO with the predefined CSM implementation. For upgraded instances, existing agent criteria and customer condition data is automatically migrated from the deprecated FSO tables to the CSM tables during upgrade. No manual migration is required.

To configure agent criteria or customer conditions for the case type selector, use the following CSM tables:

    -   `sn_csm_case_types_service_user_criteria`: for agent criteria
    -   `sn_csm_case_types_service_customer_criteria`: for customer conditions

</td></tr><tr><td>

Financial Services Operations Integration with Mastercard

</td><td>

-   **[Updated subflows](https://www.servicenow.com/docs/access?context=financial-services-operations-integration-with-mastercard-subflows&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

The following subflows were updated to support integration with the Card data security application:

    -   Mastercom - Look up Case Documents
    -   Mastercom - Look up Chargeback Documents

-   **[Updated subflows for the Mastercard document attachment and validation enhancement](https://www.servicenow.com/docs/access?context=financial-services-operations-integration-with-mastercard-subflows&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

The following subflows were updated to support the document attachment and validation enhancement:

    -   Mastercom - Create Case Filing
    -   Mastercom - Create Chargeback
    -   Mastercom - Take Action on Case
    -   Mastercom - Update Chargeback

</td></tr><tr><td>

Financial Services Operations Integration with Visa

</td><td>

-   **[Updated subflows](https://www.servicenow.com/docs/access?context=components-installed-with-the-financial-services-operations-integration-with-visa&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

The following subflows have been updated to support integration with the Card data security application:

    -   Look up Associated Transactions
    -   Look up Dispute Pre Arbitration Details
    -   Look up Dispute Filing Details
    -   Look up Dispute Response Details
    -   Look up Dispute Pre Arbitration Response Details

</td></tr><tr><td>

Identity

</td><td>

-   **[Role masking in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

Use role masking for AI agents and agentic workflows to limit the inherited roles during tool execution, verifying that AI agents run with restricted privileges, minimizing potential security risks and helping prevent unintended actions.

-   **[User management enhancements](https://www.servicenow.com/docs/access?context=t_CreateAUser&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

User management enhancements:

    -   Configure AI agents or AI users by selecting the `AI` option from the Identity type drop-down menu.
    -   Use the ai\_user\_admin role for creating, editing, and role management of AI users. Use this role to view, create, edit, assign roles to, and delete users with the identity type as `AI`.
    -   Use the Identity sub-type field to categorize the identity type while creating a user.
    -   Use the new date and time formats based on the user's preference while creating users.
-   **[Federated ID](https://www.servicenow.com/docs/access?context=federated-id&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Use Federated ID to uniquely identify roles across multiple instances. Federated ID provides a unique identifier for roles, making it easier to manage and track them across instances.

-   **[Machine Identity Console](https://www.servicenow.com/docs/access?context=machine-identity-console&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

View the Inbound API Integration Usage dashboard under the Machine Identity Console's Unique API calls page to access statistics for requesters and their API calls.


-   **[Scripting Governance Tool](https://www.servicenow.com/docs/access?context=scripting-governance&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Manage user permissions for scripting on the ServiceNow AI Platform from the enhanced scripting governance tool.


</td></tr><tr><td>

Impact

</td><td>

-   **[Use Guided Setup for Impact Store Application configuration](https://www.servicenow.com/docs/access?context=guided-setup-impact-in-app&version=australia&pubname=australia-impact&ft:locale=en-US)**

The Impact Guided Setup provides a more efficient, streamlined way for you to configure the Impact Store Application. For information about how to upgrade, see [Configure the Impact Store Application](https://www.servicenow.com/docs/access?context=configuring-impact-platform&version=australia&pubname=australia-impact&ft:locale=en-US).


</td></tr><tr><td>

Import and Export

</td><td>

-   **The mssql-jdbc.7.4.1.jre8 jar file is no longer part of the MID Server distribution**

If you have a JDBC data source integration that uses this jar file \(that is, any MSSQL connections\) install this jar file or the vendor recommended jar file according to KB0862383.


</td></tr><tr><td>

Industrial Process Manager

</td><td>

-   **[Admin role dependency](https://www.servicenow.com/docs/access?context=granular-admin-roles&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Several new granular admin roles were added to enable developers to complete administrative configuration tasks without requiring the full admin role.


</td></tr><tr><td>

Instance Scan

</td><td>

-   **[Scan execution of inactive and base system checks](https://www.servicenow.com/docs/access?context=hs-sys-properties&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

You can now execute scans on inactive checks by setting the glide.scan.inactive\_records property to true. Add and enable glide.scan.base\_system\_records property to execute scans on base system checks.


</td></tr><tr><td>

Key Management

</td><td>

-   **[Updated workflow for creating cryptographic modules](https://www.servicenow.com/docs/access?context=create-cryptographic-module&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Use the streamlined workflow designed for faster, easier creation of cryptographic modules.

-   **[SecurityUtils Enhancements](https://www.servicenow.com/docs/access?context=GlideSecurityUtilsScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

The SecurityUtils API has been enhanced to help prevent cross-site scripting attacks, including methods to sanitize and escape input.


</td></tr><tr><td>

Localization Workspace

</td><td>

-   **[Cancel translation requests, delete draft requests, and review archived requests from the landing page](https://www.servicenow.com/docs/access?context=lw-status-synchronization&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Monitor and control your requests on the landing page with functions to cancel translation requests, delete draft requests, and review archived requests.

-   **[View the translation method from the translation request summary](https://www.servicenow.com/docs/access?context=lw-status-synchronization&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

View the translation method, such as TMS or machine translation, from the translation request summary. The summary is available from the My Requests list on the landing page.

-   **[Use intelligent due date suggestions based on the size and scope of your requests](https://www.servicenow.com/docs/access?context=lw-estimate&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Use intelligent due date suggestions, which provide an estimated completion date for your translations, based on the size and scope of your translation request. You can accept the suggested due date when submitting your request.


</td></tr><tr><td>

MID Server

</td><td>

-   **[MID Server supports PowerShell 7 for Discovery](https://www.servicenow.com/docs/access?context=powershell-remoting&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)**

MID Server now supports PowerShell 7, while maintaining backward compatibility with PowerShell 5.1. This update enhances security, accelerates onboarding, and reduces deployment blockers through improved runtime detection and comprehensive test coverage.

-   **[Configure the MID Server for CyberArk CCP](https://www.servicenow.com/docs/access?context=t_ConfigureTheMIDServerForCyberArkCCP&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

MID Server's CyberArk integration adds a REST-based CCP option alongside the existing AIM SDK method, providing flexible, interchangeable integration choices. This additional option can reduce dependency overhead and enables you to choose between the AIM SDK and REST-based approaches according to your requirements.

-   **[Smart Workload Manager in clusters](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

MID Servers in a cluster now assign jobs based on the true load, using a variety of criteria. The smart workload manager continuously evaluates the queue size, execution time, CPU usage, and buffer size. The manager then assigns tasks to ensure that no server is overloaded.

-   **[MID Server is bundled with Java Runtime Environment 21](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

MID Server comes bundled with Java Runtime Environment version 21.0.7 and requires a minimum JRE version 17.0.10. The installer automatically configures Java 21.0.7 to run in your environment. If you have installed your own JRE, see the **Important information for upgrading MID Server to Australia** section to ensure your JRE is compatible.


</td></tr><tr><td>

Mobile Platform

</td><td>

-   **[Enhanced prelogin page customization](https://www.servicenow.com/docs/access?context=branded-landing-page&version=australia&pubname=australia-mobile&ft:locale=en-US)**

Configure the placement of the branded landing page login button to be either in the top menu header or as a part of the web page. Integrating the button into a web page helps you to implement a secure flow that addresses issues like short authentication session lifetimes.

-   **[Tone in Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-mobile-va&version=australia&pubname=australia-mobile&ft:locale=en-US)**

Adjust the Virtual Agent tone and response lengths in Assistant Designer.

-   **[Suggested actions](https://www.servicenow.com/docs/access?context=using-enhanced-chat-mobile&version=australia&pubname=australia-mobile&ft:locale=en-US)**

Configure suggested actions across all agentic workflows.

-   **[Input form screen buttons](https://www.servicenow.com/docs/access?context=servicenow-lens-mobile&version=australia&pubname=australia-mobile&ft:locale=en-US)**

Enable up to two top action buttons on mobile device input forms that have the **Screen presentation** attribute.

-   **[Markdown support for tables in Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-mobile-va&version=australia&pubname=australia-mobile&ft:locale=en-US)**

Render tables in Virtual Agent with markdown support to keep table sizing consistent.

-   **[Turn off mobile impersonation](https://www.servicenow.com/docs/access?context=mobile-impersonate-2&version=australia&pubname=australia-mobile&ft:locale=en-US)**

Configure the **impersonationEnabled** property to turn off mobile impersonation functionality. With this property, administrators can hide the impersonation option from the mobile app, regardless of assigned user roles.


</td></tr><tr><td>

Next Experience Components

</td><td>

<table id="table_comp_list"><thead><tr><th>

Component

</th><th>

Enhancement

</th></tr></thead><tbody><tr><td>

Activity Stream

</td><td>

-   Enable users to edit or delete journal posts.
-   Add a dropdown with check boxes for author names using the Posted by filter that enables users to filter posts by author, select all, or clear all. Users can also filter for any AI-generated posts.

</td></tr><tr><td>

Alert

</td><td>

-   Enable keyboard focus to move to the alert when it appears.
-   Add AI variants with updated color palettes for generative AI workflows.

</td></tr><tr><td>

Alert list

</td><td>

Enable keyboard focus to move to the **Show alerts** button when the alert list appears.

</td></tr><tr><td>

Button

</td><td>

Add AI variants with updated color palettes for generative AI workflows.

</td></tr><tr><td>

Button iconic

</td><td>

Add AI variants with updated color palettes for generative AI workflows.

</td></tr><tr><td>

Button circular

</td><td>

Add AI variants with updated color palettes for generative AI workflows.

</td></tr><tr><td>

Calendar

</td><td>

-   Hide time zone dropdown in the calendar header.
-   Hide time lapsed indicator or time zone indicators.
-   Add section-based time zones.

</td></tr><tr><td>

Card base container

</td><td>

Add AI variants with updated color palettes for generative AI workflows.

</td></tr><tr><td>

Checklist

</td><td>

-   Edit or delete items on hover.
-   Edit checklist items inline.
-   Edit, delete, and reorder checklist items.
-   Configure empty state checklists to add new items.

</td></tr><tr><td>

Dropdown

</td><td>

Add AI variants with updated color palettes for generative AI workflows.

</td></tr><tr><td>

Dropdown list

</td><td>

The mobile version uses the sheet component instead of a popover.

</td></tr><tr><td>

Form

</td><td>

-   Place each form field label in line with the input field and adjacent to other field labels using the “Tabbed” \(horizontal\) layout.
-   Highlight form fields with unsaved changes using a background color, in addition to the existing field indicator, which is now selected by default.

</td></tr><tr><td>

Form Templates

</td><td>

-   Show that the preview option displays modal preview to help agents understand all the fields affected when they apply a particular template.
-   Alert to inform users if a template has already been applied to a record.

</td></tr><tr><td>

Highlighted value

</td><td>

-   Enter additional text to display in a popover when the highlighted value is selected.
-   Add AI variants with updated color palettes for generative AI workflows.

</td></tr><tr><td>

Icon

</td><td>

Support for theme-specific custom icon uploads.

</td></tr><tr><td>

Input

</td><td>

Display persistent placeholder text to guide users in entering data in the correct format.

</td></tr><tr><td>

Kanban

</td><td>

Use keyboard shortcuts to drag and drop cards between columns and rows.

</td></tr><tr><td>

List selector

</td><td>

Disable the selection feature for a chosen array of list selector items.

</td></tr><tr><td>

Node map

</td><td>

-   Use radial layout to arrange nodes in a ring-like pattern.
-   Use content slots to add components.
-   Disable node dragging.

</td></tr><tr><td>

Schedule recurrence

</td><td>

-   Automatically update all recurring events in a series.
-   Fill in event details using AI.

</td></tr><tr><td>

Split button

</td><td>

Add AI variants with updated color palettes for generative AI workflows.

</td></tr><tr><td>

Tabs

</td><td>

Hide padding on the sides of each tab for horizontal \(Top\) tab position, to provide more room for additional tabs.

</td></tr></tbody>
</table><table id="table_data_visualizations"><thead><tr><th>

Chart

</th><th>

Enhancement

</th></tr></thead><tbody><tr><td>

Bar \(including Pareto\)

</td><td>

-   Show or hide a tooltip that displays on hover showing the percentage of total for a data point.
-   Removed the display setting for Height, which can be configured in the **UI Builder Styles** tab.
-   Align title horizontally to the **Start**, **Center**, or **End**. The default is **Start**.
-   Set the line of truncation to 2 or 3 lines instead of truncating long titles after 1 line.
-   Wrap long titles to a second line, instead of truncating.
-   Hide the refresh action that is available to users in the More options menu.
-   Show incomplete periods for a data snapshot indicator when selecting Metric.
-   Enable Auto aggregation to have the most appropriate aggregation level determined based on the selected date range, applied date filters, or data availability.

</td></tr><tr><td>

Box plot

</td><td>

-   Align the title horizontally to the **Start**, **Center**, or **End**. The default is **Start**.
-   Set the line of truncation to 2 or 3 lines instead of truncating long titles after 1 line.
-   Wrap long titles to a second line, instead of truncating.
-   Hide the refresh action that is available to users in the More options menu.

</td></tr><tr><td>

Bubble

</td><td>

-   Show or hide a tooltip that displays on hover showing the percentage of total for a data point.
-   Align the title horizontally to the **Start**, **Center**, or **End**. The default is **Start**.
-   Set the line of truncation to 2 or 3 lines instead of truncating long titles after 1 line.
-   Wrap long titles to a second line, instead of truncating.
-   Hide the refresh action that is available to users in the More options menu.

</td></tr><tr><td>

Dial

</td><td>

-   Align the title horizontally to the **Start**, **Center**, or **End**. The default is **Start**.
-   Set the line of truncation to 2 or 3 lines instead of truncating long titles after 1 line.
-   Wrap long titles to a second line, instead of truncating.
-   Hide the refresh action that is available to users in the More options menu.
-   Show incomplete periods for a data snapshot indicator when selecting Metric.
-   Enable Auto aggregation to have the most appropriate aggregation level determined based on the selected date range, applied date filters, or data availability.

</td></tr><tr><td>

Gauge

</td><td>

-   Align the title horizontally to the **Start**, **Center**, or **End**. The default is **Start**.
-   Set the line of truncation to 2 or 3 lines instead of truncating long titles after 1 line.
-   Wrap long titles to a second line, instead of truncating.
-   Hide the refresh action that is available to users in the More options menu.
-   Show incomplete periods for a data snapshot indicator when selecting Metric.
-   Enable Auto aggregation to have the most appropriate aggregation level determined based on the selected date range, applied date filters, or data availability.

</td></tr><tr><td>

Geomap

</td><td>

-   Show or hide a tooltip that displays on hover showing the percentage of total for a data point.
-   Align the title horizontally to the **Start**, **Center**, or **End**. The default is **Start**.
-   Set the line of truncation to 2 or 3 lines instead of truncating long titles after 1 line.
-   Wrap long titles to a second line, instead of truncating.
-   Hide the refresh action that is available to users in the More options menu.

</td></tr><tr><td>

Heatmap

</td><td>

-   Show or hide a tooltip that displays on hover showing the percentage of total for a data point.
-   Align the title horizontally to the **Start**, **Center**, or **End**. The default is **Start**.
-   Set the line of truncation to 2 or 3 lines instead of truncating long titles after 1 line.
-   Wrap long titles to a second line, instead of truncating.
-   Hide the refresh action that is available to users in the More options menu.
-   Show incomplete periods for a data snapshot indicator when selecting Metric.
-   Enable Auto aggregation to have the most appropriate aggregation level determined based on the selected date range, applied date filters, or data availability.

</td></tr><tr><td>

Indicator Scorecard

</td><td>

-   Align the title horizontally to the **Start**, **Center**, or **End**. The default is **Start**.
-   Set the line of truncation to 2 or 3 lines instead of truncating long titles after 1 line.
-   Wrap long titles to a second line, instead of truncating.
-   Hide the refresh action that is available to users in the More options menu.

</td></tr><tr><td>

Pie/Donut

</td><td>

-   Show or hide a tooltip that displays on hover showing the percentage of total for a data point.
-   Align the title horizontally to the **Start**, **Center**, or **End**. The default is **Start**.
-   Set the line of truncation to 2 or 3 lines instead of truncating long titles after 1 line.
-   Wrap long titles to a second line, instead of truncating.
-   Hide the refresh action that is available to users in the More options menu.
-   Show incomplete periods for a data snapshot indicator when selecting Metric.
-   Enable Auto aggregation to have the most appropriate aggregation level determined based on the selected date range, applied date filters, or data availability.

</td></tr><tr><td>

Pivot table

</td><td>

-   Align the title horizontally to the **Start**, **Center**, or **End**. The default is **Start**.
-   Set the line of truncation to 2 or 3 lines instead of truncating long titles after 1 line.
-   Wrap long titles to a second line, instead of truncating.
-   Hide the refresh action that is available to users in the More options menu.
-   Show incomplete periods for a data snapshot indicator when selecting Metric.
-   Enable Auto aggregation to have the most appropriate aggregation level determined based on the selected date range, applied date filters, or data availability.

</td></tr><tr><td>

Single score

</td><td>

-   Align the title horizontally to the Start, Center, or End. The default is Start.
-   Wrap chart elements instead of truncating.
-   Align the title horizontally to the **Start**, **Center**, or **End**. Default is **Start**.
-   Set the line of truncation to 2 or 3 lines instead of truncating long titles after 1 line.
-   Wrap long titles to a second line, instead of truncating.
-   Hide the refresh action that is available to users in the More options menu.
-   Show incomplete periods for a data snapshot indicator when selecting Metric.
-   Enable Auto aggregation to have the most appropriate aggregation level determined based on the selected date range, applied date filters, or data availability.

</td></tr><tr><td>

Time series

</td><td>

-   Removed the display setting for Height, which can be configured in the **UI Builder Styles** tab.
-   Show or hide a tooltip that displays on hover showing the percentage of total for a data point.
-   Align the title horizontally to the **Start**, **Center**, or **End**. The default is **Start**.
-   Align all chart content to the starting edge, center, or ending edge of the visualization.
-   Set the line of truncation to 2 or 3 lines instead of truncating long titles after 1 line.
-   Wrap long titles to a second line, instead of truncating.
-   Hide the refresh action that is available to users in the More options menu.
-   Show incomplete periods for a data snapshot indicator when selecting Metric.
-   Enable Auto aggregation to have the most appropriate aggregation level determined based on the selected date range, applied date filters, or data availability.

</td></tr></tbody>
</table>|App shell|Enhancement|
|---------|-----------|
|Agent Workspace app shell|Configure alt text for a ServiceNow or customer logo button.|

</td></tr><tr><td>

Next Experience Developer \(NED\) Tools

</td><td>

-   **Events tab in the Next Experience Inspector**

Exclude filters in the Events tab to filter out specific events.

-   **Components tab in the Next Experience Inspector**

Use the journal section in the Components tab to get a log of state updates, property updates, actions dispatched, and actions handled.


</td></tr><tr><td>

Notifications

</td><td>

-   **[Sending email using Microsoft Graph](https://www.servicenow.com/docs/access?context=send-email-using-ms-graph&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Connect Microsoft email accounts using Microsoft Graph within the ServiceNow instance for sending outbound emails.

-   **[Email threading for inbound reply email](https://www.servicenow.com/docs/access?context=c_InboundEmailActions&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Enable classification of inbound emails by using the thread-index header for emails originating from Microsoft or Microsoft Outlook ecosystem.

-   **[Column Level Encryption for email attachments](https://www.servicenow.com/docs/access?context=cle-for-email-attachments&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Attachments from inbound emails are now encrypted when stored in CLE-enabled tables and decrypted when sent in outbound emails, ensuring secure access without requiring scripting.

-   **[Enable push notifications for logged-out users](https://www.servicenow.com/docs/access?context=enable-notifications-logged-out-users&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Push notifications can now be configured to be sent to users even when they are logged out, ensuring critical updates are not missed.


</td></tr><tr><td>

Now Assist

</td><td>

-   **[Now Assist Conversational Help](https://www.servicenow.com/docs/access?context=conversational-help-skills&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The discovery of Conversational Help Skills from Now Assist panel is no longer configured as auto-enabled.


</td></tr><tr><td>

Now Assist AI Agents

</td><td>

-   **[Create an external AI agent with the Agent2Agent protocol](https://www.servicenow.com/docs/access?context=create-a2a-agent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

Use the A2A Protocol integration for creating external agents in the AI Agent Studio to connect with the ServiceNow AI Platform.

-   **[Updates to platform agentic workflows](https://www.servicenow.com/docs/access?context=platform-use-cases&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

Several platform agentic workflows have seen updates to how they work and what configurations are available for AI admins. [Analyze task trends](https://www.servicenow.com/docs/access?context=incident-trends&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) and [Identify ways to improve service](https://www.servicenow.com/docs/access?context=service-improvement&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) now have post-analysis actions, including the option to download analysis and ask additional information. [Generate my work plan](https://www.servicenow.com/docs/access?context=generate-work-plan&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) can run as a scheduled job.

-   **[Agentic evaluation offer issue tracing and suggested optimizations](https://www.servicenow.com/docs/access?context=agentic-evals&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

After an automated evaluation of an agentic AI asset, you can receive a list of issues and suggested optimizations to address those issues. Issues come with individual record node-by-node traces to pinpoint the exact source of problems. Optimizations are suggested, and you can apply them and run a reevaluation from a single guided flow.


</td></tr><tr><td>

Now Assist for Configuration Management Database \(CMDB\)

</td><td>

-   **[New role required for the Create configuration item agentic workflow](https://www.servicenow.com/docs/access?context=na-cmdb-awf-ci-creator&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

The sn\_cmdb\_admin role is now required to use the 'Create configuration item' agentic workflow \(was sn\_cmdb\_editor\).

-   **Skills now also require the now\_assist\_panel\_user role**

AI skills that execute in the Now Assist panel now require both the cmdb\_dedup\_admin and now\_assist\_panel\_user roles.


</td></tr><tr><td>

Now Assist for Creator

</td><td>

-   **[Use the app generation skill to generate apps](https://www.servicenow.com/docs/access?context=sns-app-gen-use-app-gen-skill&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Build Agent is the default setting for app generation in ServiceNow Studio. To continue using the app generation skill, change the setting in ServiceNow Studio.


</td></tr><tr><td>

Now Assist for FSM

</td><td>

-   **Create Work Order AI agent performance improvements**

The Create Work Order AI agent was optimized to reduce latency and improve response times. Inter-agent communication was streamlined to minimize redundant processing during work order creation.


</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Renaming the Incident assist skill](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

The incident assist skill has been renamed to **\[DEPRECATED\] Incident assist**.

-   **[Renaming demo voice AI agents](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

The voice AI demo agents have been renamed as primers.

-   **[Skills activated by default in Now Assist for ITSM](https://www.servicenow.com/docs/access?context=using-now-assist-for-itsm&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

For new Now Assist for IT Service Management \(ITSM\) users, the following skills are activated by default:

    -   Resolution notes generation
    -   Knowledge generation
    -   Chat reply recommendation
-   **[Editing change request skills using Now Assist Skill Kit \(NASK\)](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-change-risk-skill&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Easily edit the change request risk explanation and change request summarization skill prompts and inputs directly in the Now Assist Skill Kit \(NASK\).

-   **[Configuration item details for suggest configuration items for a change request workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-suggest-configuration-items-for-a-change-request&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Provide details such as class, location, and environment to find configuration items \(CIs\) relevant to a change request while using the suggest configuration items for a change request agentic workflow from the Now Assist panel.

-   **[Role masking for change risk explanation skill](https://www.servicenow.com/docs/access?context=supporting-information-now-assist-itsm&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Enhance security for the change request risk explanation skill by enabling admins to limit roles that are inherited by the user.

-   **[Virtual agent topics available as demo data](https://www.servicenow.com/docs/access?context=itsm-va-prebuilt-topics&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

The Virtual Agent topics listed in this table have been renamed and are now available as demo data.

    |Existing name|Updated name|
    |-------------|------------|
    |Add Comment To incident|\(DEMO\) Add Comment To incident-LLM|
    |Approve Sysapproval Approver|\(DEMO\) Approve Sysapproval Approver-LLM|
    |Change Password|\(DEMO\) Change Password \(Template\) - LLM|
    |Check IT Ticket Status|\(DEMO\) Check IT Ticket Status \(Template\)|
    |Close incident|\(DEMO\) Close incident-LLM|
    |Explain change risk|\(DEMO\) Explain change risk|
    |Mark incident Unresolved|\(DEMO\) Mark incident Unresolved-LLM|
    |Open IT Ticket|\(DEMO\) Open IT Ticket \(Template\)-LLM|
    |Reject Sysapproval Approver|\(DEMO\) Reject Sysapproval Approver-LLM|
    |Reset Password|\(DEMO\) Reset Password \(Template\) - LLM|
    |Resolve incident|\(DEMO\) Resolve incident-LLM|
    |Unlock Account|\(DEMO\) Unlock Account \(Template\) - LLM|
    |View And Add Comments|\(DEMO\) View And Add Comments-LLM|


</td></tr><tr><td>

Now Assist for Legal Service Delivery \(LSD\)

</td><td>

-   **[Summarize a legal request or matter by using Now Assist for Legal Service Delivery \(LSD\)](https://www.servicenow.com/docs/access?context=now-assist-lsd-summarize-case&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Summarization now includes data from extended practice area tables, providing context‑rich summaries for your legal requests and matters.


</td></tr><tr><td>

Now Assist in Contract Management

</td><td>

-   **[Configure use case mappings for metadata and obligation extraction](https://www.servicenow.com/docs/access?context=cmpro-na-usecase-mappings-me&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Clear the **Contracts created from contract request** check box on the use case mapping forms for the contract metadata extraction and contract obligation extraction skills to extract metadata and obligations form signed contracts that are uploaded directly on a contract record.

-   **[Conversational contract search and insights Workflow](https://www.servicenow.com/docs/access?context=cmpro-agentic-use-conv-search&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

The Now Assist powered conversational search feature's improved experience enables you to:

    -   View results in a listing view, making it easier to scan, compare, and navigate contract information.
    -   Open contract documents directly from the search results and perform an in‐document search.
The conversational search feature does not support searching within contract documents that are scanned PDFs.


</td></tr><tr><td>

Now Assist in Document Intelligence

</td><td>

-   **[Now Assist in Document Intelligence skills are now turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading: Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

-   **[Document and visual insights AI agent enhancements](https://www.servicenow.com/docs/access?context=document-and-visual-insights-ai-agent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

Tools used by the document and visual insights AI agent are consolidated to improve performance.

-   **[Changes to limitations](https://www.servicenow.com/docs/access?context=now-assist-document-intelligence-limitations&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The file size limit for uploading a file using the attachment summarization feature is changed from 10MB to 20MB.

-   **[Add a tool](https://www.servicenow.com/docs/access?context=add-a-tool&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

Document and visual intelligence capabilities used to leverage extraction, question answering, and summarization for skills created with Now Assist Skill Kit is available to users with the appropriate role\(s\).


</td></tr><tr><td>

Now Assist in Platform Analytics

</td><td>

-   **[Explore data from protected scopes](https://www.servicenow.com/docs/access?context=enable-aide-secure-scope-apps&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Provide access to protected application scopes to AI Data Explorer and Query Generation, and you can use data from those application tables in explorations. \(Query Generation bundle 5.2\)

-   **[Improvements to how segments are handled](https://www.servicenow.com/docs/access?context=querygen-segments&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

    -   Manual segments are re-ranked to take priority over automatically generated segments.
    -   Prompt changes made to better support manual segments.
    -   More segments are passed to the LLM to increase the chance of the correct segment getting selected. Twelve segments are passed instead of three.
    -   Segments longer than 2000 characters are dropped to prevent context window bloat.
\(Query Generation bundle 5.2\)

-   **[Customize semantic metadata in configuration tables](https://www.servicenow.com/docs/access?context=customize-semantic-metadata&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Customize semantic descriptions and usage instructions in the table and column configuration tables. Unlike the previous method of editing Entity and Dimension records, these changes can be transferred between instances through update sets.

-   **[View recommended actions](https://www.servicenow.com/docs/access?context=expl-view-recommended-actions&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

AI Data Explorer can suggest actions based on the insights that it generates in an exploration.

-   **[Ask questions about FX currency data](https://www.servicenow.com/docs/access?context=qg-supported-query-operations&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Query Generation now supports the FXCurrency \(Currency 2\) data type. This means that you can use AI Data Explorer to explore financial operations data, including those within Source-to-Pay Operations.

-   **[Benefit from improvements to segments](https://www.servicenow.com/docs/access?context=querygen-segments&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Segments are reusable definitions in Query Generation that provide non-obvious context to assist the semantic layer or LLM to select the correct dimension and values. Users can create manual segments via a new form. A scheduled job synchronizes manual and autogenerated segments. This job also cleans up segments to help surface the correct segments and reduce noise.

Manual segments are re-ranked to take priority over automatically generated segments.

Domain separation is also now supported, with a Domain field on the Segments table. Segments based on reports and filters inherit the source domain. Manual segments have domains that are passed up to the Segments table on synchronization. Segments are not supported for indicator sources or modules on domain-separated instances.


</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>

 

</td></tr><tr><td>

Operational Resilience

</td><td>

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr><tr><td>

Operational Technology Incident Management

</td><td>

-   **[Admin role dependency](https://www.servicenow.com/docs/access?context=granular-admin-roles&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Several new granular admin roles have been added, which enable developers to complete administrative configuration tasks without requiring the full admin role.


</td></tr><tr><td>

Operational Technology Manager

</td><td>

-   **[Use CMDB groups to add OT context to IT CIs](https://www.servicenow.com/docs/access?context=use-cmdb-groups-it-ot-conversion&version=australia&pubname=australia-operational-technology&ft:locale=en-US)**

When you use CMDB groups to add OT context to IT CIs, you can no longer create an Automated IT OT Bulk Contextualization record with more than one CMDB group.

-   **[Automated IT OT Bulk Contextualization - Using CMDB groups scheduled job](https://www.servicenow.com/docs/access?context=use-cmdb-groups-it-ot-conversion&version=australia&pubname=australia-operational-technology&ft:locale=en-US)**

The **Automated IT OT Bulk Contextualization - Using CMDB groups** scheduled job can only process 10,000 CIs at one time. If you have more than 10,000 CIs, the remaining CIs will be processed in the next job run.

-   **[Admin role dependency](https://www.servicenow.com/docs/access?context=granular-admin-roles&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Several new granular admin roles were added to enable developers to complete administrative configuration tasks without requiring the full admin role.


</td></tr><tr><td>

Order Management

</td><td>

-   **[Managing inflight order for site projects](https://www.servicenow.com/docs/access?context=inflight-offering-somt&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Use the OM integration with SPM for in-flight orders to support projects for site and maintain program project and sub-project hierarchy.


</td></tr><tr><td>

Performance Analytics

</td><td>

-   **[Explore native data snapshots indicators with KPI Details](https://www.servicenow.com/docs/access?context=kpi-details-targets&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

KPI Details supports data snapshots indicators that you create, not only those that are enabled from classic indicators. The following features have been created for or extended to native data snapshots indicators:

    -   Subscriptions for alerts on targets and thresholds, which can be set from the targets and thresholds panels
    -   Adjustable filtering by breakdown, calendar, or time series aggregation
    -   Hierarchical breakdowns, with scores rolled up to parent elements
    -   Customizable score formatting options, such as precision and abbreviation
-   **[View data trends in data snapshots as data accumulates](https://www.servicenow.com/docs/access?context=create-ds-automated-indicator&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

When you select a field by which to trend a data snapshots automated indicator, you have the option to show the trend for incomplete collection periods. This feature shows the trend as it develops for live data without having to wait for the end of the collection period. You can set this behavior either on the automated data snapshot indicator record or in a time series data visualization for a data snapshot indicator.

-   **[Collect data snapshots scores with confidence](https://www.servicenow.com/docs/access?context=tables-unlimited-breakdowns&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Data mining for data snapshots scores has the following improvements:

    -   Collect scores for tables with any volume of records.
    -   The system accurately and automatically handles data gaps when data mining is disabled.
    -   You are warned of the implications before you manually disable data mining \(score collection\).
-   **[Activate data snapshots in more cases and with better information](https://www.servicenow.com/docs/access?context=activate-unlimited-breakdowns&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**
    -   Activate indicators without active data collector jobs.
    -   Activate indicators regardless of underlying record volume. For example, the `INSERT_VOLUME_EXCEEDED` error no longer occurs.
    -   If the activation fails because of scripted breakdowns, the scripted breakdowns are listed in the failure message.
    -   Generic parsing errors have been rewritten into specific, categorized messages.

</td></tr><tr><td>

Performance Analyzer

</td><td>

-   **Deep linking**

Save and share links that replicate the same view for others.

-   **Group by variant**

Aggregate pages with data grouped by variant help you to identify performance issues.

-   **Filter client interaction lists**

Filters for client interaction lists enable you to investigate user-specific performance issues.

-   **Waterfall view**

The waterfall view displays which macroponent is associated with server-side calls to help you trace API calls to specific UI components.


</td></tr><tr><td>

Platform Analytics experience

</td><td>

-   **[Manage Platform Analytics in the improved Analytics Overview page](https://www.servicenow.com/docs/access?context=analytics-center&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Quickly discover artifacts, access relevant information and key metrics, and take actions to manage the health of the library. The Analytics Overview page \(formerly Analytics Center\) acts as a one-stop shop and entry point for role-specific access to all important information related to Platform Analytics.

-   **[Platform Analytics experience is enabled by default for all users on upgrade to Australia](https://www.servicenow.com/docs/access?context=par-workspace&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Create content entirely within Platform Analytics.

-   **[Take role-based tours](https://www.servicenow.com/docs/access?context=guided-tours&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

Role-based guided tours are added to the Platform Analytics Migration Center and the Dashboards and Data Visualizations library pages.

-   **[Filter dashboards by string field values](https://www.servicenow.com/docs/access?context=create-select-filter-workspace&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Filter data by the contents of string-type fields with a single-select or multiple-select filter.

-   **[View the percentage each data segment contributes to the total](https://www.servicenow.com/docs/access?context=create-dv-donut-ac&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Enable the **Show % of total in tooltip** option to show the percentage each data point contributes to the total alongside absolute values in the tooltip. Applies to time series, bar, bubble, donut, geomap, and heatmap visualizations.

-   **[Explore native data snapshots indicators in KPI Details](https://www.servicenow.com/docs/access?context=kpi-details&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**
    -   Employ intraday analysis with granularity based on work shifts.
    -   Customize score formatting options.
    -   Adjust breakdowns, calendar, and aggregation periods while exploring an indicator.
    -   Set up subscriptions for alerts on targets and thresholds directly from the targets and thresholds panels.
    -   Define hierarchical breakdowns with scores rolled up to parent elements.
-   **[Create hierarchical filters for Industrial Connected Workforce indicators](https://www.servicenow.com/docs/access?context=create-hierarchical-filter&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Create multilevel filters with roll-up aggregation across nested organizational structures, which moves from site, to plan, to department, to functional location.

-   **[Download data visualizations as CSV or Excel files](https://www.servicenow.com/docs/access?context=export-data-vis-from-dboard&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

As a viewer, you now can download any data visualization, not only a List, as a CSV or XLS file.

-   **[Automatically set the aggregation period of data snapshots indicator trend lines](https://www.servicenow.com/docs/access?context=config-dv-time-series-ind-data&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Set the **Aggregation period** field in the **Trend by** settings to Auto so ****, the system automatically selects the aggregation period of data snapshot indicator trend lines based on the date range and business calendar.

-   **[Automatic aggregation of date-filtered data based on date range](https://www.servicenow.com/docs/access?context=create-date-filter-workspace&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Filter dashboards by business calendar and have the system infer the appropriate aggregation level at runtime. If you put a time series data visualization on a dashboard with a date filter, the aggregation of shown data adjusts automatically depending on the selected date range. This adjustment applies to both table and data snapshots indicator data.

-   **[Create custom data visualization filters with an improved condition builder](https://www.servicenow.com/docs/access?context=filter-dv-condition-builder&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

When creating a data visualization for table data, you can create a custom filter when you specify the data source. The condition builder for the custom filter now has menus of fields, operators, values, and related tables.

-   **[Hide the Refresh action on data visualizations](https://www.servicenow.com/docs/access?context=create-dv-sing-sc-ac&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

In the Headers and Borders section of data visualizations, use the **Show refresh option** check box to hide the **Refresh** icon ![](../image/refresh-icon.jpg) in the Configuration settings of data visualizations. Data visualizations on cached dashboards never have the Refresh icon.

-   **[Migration Center enhancements](https://www.servicenow.com/docs/access?context=data-migration&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**
    -   As an analytics manager, migrate any Core UI dashboard to Platform Analytics in the Dashboard library.
    -   Edit migrated content before activating it in the Platform Analytics experience.
    -   Activate content selectively.
    -   Total views of Core UI reports and other widgets are now migrated along with the Core UI content.
-   **[Dashboard element enhancements](https://www.servicenow.com/docs/access?context=edit-db-elements-in-ac&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Moving and resizing dashboard elements no longer opens the configuration panel.

-   **[Enhanced scheduled exports](https://www.servicenow.com/docs/access?context=schedule-export-dboards-data-viz&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

When scheduling the email of dashboards or data visualizations, limit recipients based on reference qualifiers.


</td></tr><tr><td>

Playbook

</td><td>

-   **[Required role update](https://www.servicenow.com/docs/access?context=user-access-playbooks&version=australia&pubname=australia-build-workflows&ft:locale=en-US)**

Any tasks that previously required only the admin role now require the playbook.admin role instead.

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr><tr><td>

Process Mining

</td><td>

-   **[Automated finding names updated](https://www.servicenow.com/docs/access?context=automated-findings&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

The following automated finding names have been updated to include "Transition" in the name:

    -   Slow duration \(Transition\)
    -   Extreme duration \(Transition\)
-   **[Role names changed](https://www.servicenow.com/docs/access?context=components-installed&version=australia&pubname=australia-now-intelligence&section=po-roles&ft:locale=en-US)**

Role names in Process Mining that previously included "optimization" have been updated to use the term "mining" instead. For example, the sn\_process\_optimization\_admin role has been renamed sn\_process\_mining\_admin.


</td></tr><tr><td>

Product Catalog Management and Pricing Management

</td><td>

-   **[Product catalog interface enhancement](https://www.servicenow.com/docs/access?context=using-product-catalog&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Quickly identify products with derived pricing through product tiles that display a message stating that the product price varies. Pricing is calculated and updated automatically based on selections made.


-   **[Derived pricing enhancements](https://www.servicenow.com/docs/access?context=configuring-related-product-pricing&version=australia&pubname=australia-order-management&ft:locale=en-US)**
    -   The Derived Pricing Matrix supports the following enhancements:
        -   Conditions defined on product offering fields for both source and target product offerings
        -   Predefined formulas for specifying prices for target product offerings and using floor and ceiling price controls to maintain acceptable price ranges
    -   Visibility into how the final price for derived products is determined.
    -   Support for account-level scope, which uses both cart items and sold products when calculating derived prices.
-   **[Price and quantity ramp enhancements](https://www.servicenow.com/docs/access?context=defining-products-with-ramps&version=australia&pubname=australia-order-management&ft:locale=en-US)**
    -   Enable sales agents to create custom ramp type segments for quotes. Agents can view the cumulative price of product offers across all ramp segments.
    -   View ramps inside the CPQ Configurator.
    -   Enable sales agents to create ramps for quotes with amendments, contract renewals, and cancellations.
-   **[Delta pricing enhancement](https://www.servicenow.com/docs/access?context=net-pricing-sp-contracts&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Show the delta pricing view in the CPQ Configurator during modify and amend flows.

-   **[Configurable pricing plan enhancement](https://www.servicenow.com/docs/access?context=configuring-pricing-plan&version=australia&pubname=australia-order-management&ft:locale=en-US)**

The Floor and Ceiling Calculation step in the default pricing plan applies the minimum and maximum prices for a product or service to help avoid pricing that isn't competitive or results in poor margins.


</td></tr><tr><td>

Project Portfolio Management

</td><td>

[Australia Patch 2](../quality/australia-patch-1.md)

-   **[Demand summarization skill enhancements](https://www.servicenow.com/docs/access?context=demand-summary-demand-classic&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

The demand summarization skill incorporates data from related entities when generating a summary. In addition to demand record fields, the summary includes insights from demand tasks, cost plans, monetary and non-monetary benefit plans, resource assignments, and work notes. The generated summary covers business requirements, timeline, risks, stakeholder comments, cost, effort, monetary and non-monetary benefits, and ROI.

-   **[Next Experience for Demand Management](https://www.servicenow.com/docs/access?context=demand-workspace&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

The new Next Experience for Demand Management provides a unified layout, guided stages, improved navigation, and enhanced capabilities such as Playbooks and Docs integration. As you move to Next Experience for Demand Management, you’ll find it easier to create, review, and manage demands with a cleaner layout and guided actions. The classic UI is still available, but new improvements will appear in the workspace.

Next Experience for Demand Management is available with the Strategic Portfolio Management \(SPM\) Standard and Pro licenses.


</td></tr><tr><td>

Public Sector Digital Services

</td><td>

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr><tr><td>

Quote Management

</td><td>

-   **[Enhancements to price ramps on quote lines](https://www.servicenow.com/docs/access?context=add-price-ramps-on-a-quote-line-item&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Modify active ramp segments on amendment quotes to better manage pricing changes over time.

    -   Split an active ramp segment into multiple shorter segments within the original term, with the system automatically assigning the correct line types and effective dates for each resulting segment.
    -   Merge split segments back into the original ramp while the quote is in draft state.
    -   Remove segments that are no longer needed.
    -   Edit the quantity in the product configurator. The quantity field for the last ramp segment of configurable and bundled products is read-only.
-   **[Quote approvals](https://www.servicenow.com/docs/access?context=explore-advanced-approval-for-sales&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Build on existing quote approval workflows with greater control and flexibility

    -   Receive automated reminder notifications for pending approvals steps based on reminder schedules configured by your administrator.
    -   View the escalated approver on the approval step card when an approval step is escalated, so you can clearly identify who is responsible for the next action.
    -   Add ad-hoc approvers to an approval request outside the configured approval workflow when additional review is needed.
    -   Override an approval to advance a quote when permitted by your organization's approval configuration.

See [Advanced Approval Management release notes](../sales-order-management/advanced-approval-management-for-sales-rn.md) for more information.

</td></tr><tr><td>

Security Center

</td><td>

-   **[Security Hardening tool Updates](https://www.servicenow.com/docs/access?context=security-hardening-settings&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

The security Hardening tool has been updated to the latest Instance Security Hardening Settings V7.


</td></tr><tr><td>

Security Incident Response

</td><td>

-   **[Assign groups in PIR user assignment rules](https://www.servicenow.com/docs/access?context=create-pir-assignment-rules&version=australia&pubname=australia-security-management&ft:locale=en-US)**

User Assignment Rules for Post-Incident Review \(PIR\) assessments in the SIR module now support group-based assignment in addition to individual user selection. You can configure assignment rules using groups. The PIR automatically reflects group membership updates without requiring manual edits to the assignment rules configuration.


</td></tr><tr><td>

Self-service and omnichannel engagement for CSM

</td><td>

-   **[Customer Service Portal Base](https://www.servicenow.com/docs/access?context=configure-csm-service-portals&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Starting with the Australia release, the Customer Service Portal Base plugin \(com.snc.csm\_portal\_base\) has been migrated to the App Store as a standalone application. Future enhancements are delivered through the Customer Service Portal Base store app. This change improves packaging, versioning, and deployment flexibility for implementations that require portal framework, responsive design, case management, knowledge integration, and community features. The store app also includes email integration, translation support, attachment handling, and mobile enhancements.

-   **[Subscriptions and Activity Feed Framework](https://www.servicenow.com/docs/access?context=actsub-api&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

Starting with the Australia release, the Subscriptions and Activity Feed Framework plugin \(com.snc.subscriptions\_activity\_feed\) has been migrated to the App Store as a standalone application. Future enhancements are delivered through the Subscriptions and Activity Feed Framework store app. This change improves packaging, versioning, and deployment flexibility for implementations that require subscription framework, activity tracking, notification preferences, or context management.

-   **[Walk-Up for CSM](https://www.servicenow.com/docs/access?context=csm-walkup-experience&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Starting with the Australia release, the Walk-up for CSM plugin \(com.snc.walkup\_for\_csm\) has been migrated to the App Store as a standalone application. Future enhancements are delivered through the Walk-up for CSM store app. This change improves packaging, versioning, and deployment flexibility for implementations that require subscription framework, activity tracking, notification preferences, or context management.


</td></tr><tr><td>

Service Catalog

</td><td>

-   **[Use UI Policy tab to add and manage the UI policies](https://www.servicenow.com/docs/access?context=create-ui-policies-in-catalog-builder&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

Previously, when creating or editing a question in Catalog Builder, users could define UI policies or dynamic behavior by selecting the UI policies icon \(![UI policies icon](../../product/service-catalog-management/image/dyn-beh-quest.png)\). This option has been removed. Now, users must directly use the UI Policy tab to add and manage the UI policies \(actions, conditions, scripts, and other required details\) to the catalog item.


</td></tr><tr><td>

Service Operations Workspace for ITSM

</td><td>

-   **[Configure reference field auto-load behavior from SOW Admin Center](https://www.servicenow.com/docs/access?context=admin-center-sow&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Use the Reference field auto-load behavior option from the SOW Properties section of the SOW Admin Center to configure the **Reference search on click ** \(**ref\_search\_on\_click**\) UX page property. The option enables you to configure the automatic searching of field value results displayed for reference fields such as Configuration item, Service offering, and Service.

-   **[Recent list links in SOW record](https://www.servicenow.com/docs/access?context=view-inc-record-info-contextual-sidepanel&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Selecting the Recent incidents, Recent interaction, or Recent tasks links from the Record information side panel of a SOW record displays the 10 most recent records irrespective of their timeline instead of showing the records from last seven days. You can select the **View All** option to view additional records as well.


</td></tr><tr><td>

ServiceNow AI Lens

</td><td>

No changes in this release.

</td></tr><tr><td>

ServiceNow AI Platform core feature

</td><td>

-   **[Country setting added to Language and Region preferences](https://www.servicenow.com/docs/access?context=next-experience-language-preferences&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

Users can select their country from the Next Experience language and region preferences.

-   **[New options for date and time format in the User record](https://www.servicenow.com/docs/access?context=user&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Users can select from new options for Date format and Time format in the User record.

-   **[Control whether date and time formats reflect the user locale by default](https://www.servicenow.com/docs/access?context=set-localization-props&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Configure date and time formats to reflect the user locale when no date or time format has been selected in user preferences through the **glide\_i18n.date.default\_to\_locale** system property.

-   **[Control how to set the language for guest users](https://www.servicenow.com/docs/access?context=set-localization-props&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Use a guest user's IP address to set their language through the **glide\_i18n.ip\_geolocation** system property.

-   **[Activate additional choices for countries](https://www.servicenow.com/docs/access?context=activate-country-choices&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Activate additional choices for countries in the Next Experience language and region preferences or in a User record.

-   **[ECMAScript 2021 \(ES12\) JavaScript mode supports additional scripting features](https://www.servicenow.com/docs/access?context=javascript-engine-feature-support&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

Use additional scripting features in applications or scripts that use the ECMAScript 2021 \(ES12\) JavaScript mode.

-   **[JavaScript engine updated with changes from the Rhino engine](https://www.servicenow.com/docs/access?context=updates-javascript-engine&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

The JavaScript engine on the ServiceNow AI Platform was updated to incorporate changes from the open-source Rhino JavaScript engine.

-   **[New Normalization Data Services system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Create duplicate records in core\_company extension tables by setting the **com.glide.acl\_check\_all\_filter\_on\_new** system property to true to reference account records.

-   **[System properties secured by default](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Glide properties that can impact instance security are set to secure values by default. For more information about which system properties are affected and why, see the [Glide Property Hardening \[KB1982254\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1982254) article in the Now Support Knowledge Base.

-   **[Tracking records in unauthenticated users' sessions](https://www.servicenow.com/docs/access?context=web-embeddables&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Track records created, modified, or deleted by unauthenticated users to enable session-based ACL access on public forms, portals, or workflows.

-   **[Manage guest user access to records](https://www.servicenow.com/docs/access?context=web-embeddables&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Restrict guest user access to records they created or updated during their current session using the 'is in session' condition builder on the ACL form for Sys ID fields.

-   **[Session-based guest access](https://www.servicenow.com/docs/access?context=web-embeddables&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Manage REST GraphQL security with path-based ACLs that are enforced without needing to require authentication for access to an API.


-   **[Support duplicate company names across core\_company extension tables](https://www.servicenow.com/docs/access?context=enhanced-nds-for-duplicate-records&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Avoid normalization conflicts when creating records with the same company name in both the Company \[core\_company\] table and its extension tables, such as Customer Account \[customer\_account\], using the **glide.cmdb.canonical.use\_base\_core\_company\_only** property. It ensures that uniqueness enforcement applies only to base core\_company records.


</td></tr><tr><td>

ServiceNow SDK

</td><td>

-   **[Flow API supports Service Catalog triggers and actions](https://www.servicenow.com/docs/access?context=fluent-flow-api&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Use triggers and actions related to Service Catalog with the Flow API.

-   **[Access Control List API supports protection policies](https://www.servicenow.com/docs/access?context=acl-api-now-ts&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Control whether someone can view or edit an access control list \(ACL\) with the protectionPolicy property in an ACL object.

-   **[Keys updated for static assets in full-stack applications](https://www.servicenow.com/docs/access?context=building-applications-source-code&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Static UX Assets \[sys\_ux\_lib\_asset\] in full-stack applications have updated keys in the `keys.ts` file. UX Asset sys\_ids aren’t changed.


</td></tr><tr><td>

ServiceNow Studio

</td><td>

-   **[Preview an app file in ServiceNow Studio](https://www.servicenow.com/docs/access?context=preview-app-file&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Files with preview capabilities open directly in preview mode in ServiceNow Studio, bypassing the record view. This change reduces the number of steps required to view file content and keeps developers focused on their work without manual mode switching.


-   **[Integrated tab groupings](https://www.servicenow.com/docs/access?context=qs-open-apps-files-across-scopes&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Integrated tabs are no longer color-coded or grouped by scope. You can see a list of the open files by selecting the more actions icon and selecting **Show Opened Editors**.

-   **[Build Agent in ServiceNow Studio](https://www.servicenow.com/docs/access?context=build-agent-in-servicenow-studio&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Build Agent is the default setting for AI-assisted app generation in ServiceNow Studio. You can change this setting in the ServiceNow Studio user preferences menu.


</td></tr><tr><td>

Smart Assessment Engine

</td><td>

-   **[Create an assessment template category](https://www.servicenow.com/docs/access?context=sae-asmnt-template-category-create&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

Allow one or more roles to access a template category with the multiselect **Category Roles** field.


</td></tr><tr><td>

Software Asset Management

</td><td>

-   **[Granular configuration admin roles](https://www.servicenow.com/docs/access?context=sam-installed-components&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Use granular admin roles, such as sam\_admin and sam\_integrator, to complete administrative configuration tasks without requiring the full admin role. By using limited admin privileges that provide access to only certain tasks, you can help reduce security risks across your organization.


</td></tr><tr><td>

Source-to-Pay Operations Integrations

</td><td>

-   **[Source-to-Pay integration with SAP](https://www.servicenow.com/docs/access?context=source-to-pay-sap-integration&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)**
    -   Enhanced integration to support data retrieval from SAP ECC, SAP OData, and SAP HANA RFC using the updated Buyer Group staging process.
    -   Enhanced integration to support Read-Only security directives to strengthen data protection, applying required field-level changes in alignment with the Read-only field remediation guidelines to ensure compliance and consistency across integrations.
    -   Updated entity naming convention from Department to Buyer Groups for improved standardization.
-   **[Source-to-Pay integration with SAP Ariba](https://www.servicenow.com/docs/access?context=source-to-pay-integration-sap-ariba&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)**
    -   Enhanced integration to support fetch shipment details from SAP Ariba.
    -   Updated entity naming convention from Department to Buyer Groups for improved standardization.
-   **[Source-to-Pay integration framework](https://www.servicenow.com/docs/access?context=source-to-pay-integration-framework&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)**
    -   Enhanced the Purchase Requisition Line \(PRL\) outbound staging table to improve data completeness and consistency for outbound Purchase Requisition integrations.
    -   Performance optimizations have been applied to the Purchase Order \(PO\) transform map to improve efficiency and scalability when processing high‑volume PO data.

</td></tr><tr><td>

Strategic Planning

</td><td>

[Australia Patch 2](../quality/australia-patch-1.md)

-   **[Demand summarization skill enhancements](https://www.servicenow.com/docs/access?context=demand-summary-demand-classic&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

The demand summarization skill incorporates data from related entities when generating a summary. In addition to demand record fields, the summary includes insights from demand tasks, cost plans, monetary and non-monetary benefit plans, resource assignments, and work notes. The generated summary covers business requirements, timeline, risks, stakeholder comments, cost, effort, monetary and non-monetary benefits, and ROI.


</td></tr><tr><td>

Subscription Management

</td><td>

-   **[Now Assist usage excludes demo data](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Demonstration instances are excluded from the total Now Assist usage count to improve tracking of Assist consumption. The accrual time field displays when Now Assist data was last accrued.

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Now Assist usage measurement is evolving. Update Subscription Management to version 6.1 or later on all instances to avoid mixed measurement states. For more information, see [Now Assist Usage - Overview &amp; New Measurement Logic: January 2026 \[KB2704710\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710) on the Now Support Knowledge Base.

-   **[Streamlined user-based subscription allocation](https://www.servicenow.com/docs/access?context=managing-user-subscriptions-v2&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

To simplify the Subscription Management experience, the manual allocation workflow for user-based subscriptions has been removed for administrators who have never used it. Administrators who have manually allocated user-based subscriptions before can still make manual allocations.

-   **[Hidden user-based subscription allocations](https://www.servicenow.com/docs/access?context=subscriptions-overview-v2&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

To help prevent inaccuracy when allocations aren't complete, allocation details for user-based subscriptions are now hidden from the Subscription Management overview. Contact your account executive for user-based subscription allocation details.


</td></tr><tr><td>

Telecommunications Customer 360

</td><td>

-   **[Products](https://www.servicenow.com/docs/access?context=c360-products-card&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**
    -   Filter the list of sold products displayed by product characteristic values.
    -   Modify configurations, suspend, resume, or disconnect one or more sold products and their services.
-   **[Customer history](https://www.servicenow.com/docs/access?context=c360-inter-history-card&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

The **Interaction history** card has been renamed to **Customer history**. Phone interactions, chat messages, cases, contracts, work orders, and other activity types that have been configured are displayed.


</td></tr><tr><td>

Telecommunications Service Operations Management \(TSOM\)

</td><td>

-   **SD-WAN Discovery connectors [SD-WAN data model](https://www.servicenow.com/docs/access?context=sd-wan-data-model&version=australia&pubname=australia-telecom-service-ops&ft:locale=en-US)**

Enable comprehensive SD-WAN visibility by leveraging new Telecom Discovery connectors. Standardize data processing through the SD-WAN Data Model integrated into the Telecom Discovery Builder Framework ETL pipeline.


-   **[Discrepancy identification – types of discrepancies](https://www.servicenow.com/docs/access?context=discrepancy-identification-types-of-discrepancies&version=australia&pubname=australia-telecom-service-ops&ft:locale=en-US)**

Enhance discovery accuracy and data quality with SD-WAN-specific discrepancy audits that validate discovery results against the CMDB. Reconcile discrepancies manually or automatically using the remediation engine. When the audit detects a newly discovered CI not present in the CMDB, a single follow-on task is created at the equipment level for streamlined resolution.


</td></tr><tr><td>

Third-party Risk Management

</td><td>

-   **[Simplified third-party element process](https://www.servicenow.com/docs/access?context=tprm-workflow-in-workspace&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

After upgrading to version 22.0.1, third‑party elements are now linked to a single third party and can no longer be shared across third parties. Scoring rollups calculate results from element‑level assessments rather than entity records.


-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr><tr><td>

Threat Intelligence Security Center

</td><td>

-   **[MITRE ATT&amp;CK Technique Extraction Rules](https://www.servicenow.com/docs/access?context=mitre-extraction-rules&version=australia&pubname=australia-security-management&ft:locale=en-US) and [View extracted MITRE ATT&amp;CK Techniques](https://www.servicenow.com/docs/access?context=mitre-extraction-method&version=australia&pubname=australia-security-management&ft:locale=en-US)**

Enabled MITRE-ATT&amp;CK extraction rules for RSS feed to map and associate MITRE-ATT&amp;CK techniques.


-   **[View RSS Feeds](https://www.servicenow.com/docs/access?context=define-rss-feeds&version=australia&pubname=australia-security-management&ft:locale=en-US)**

Enhanced the RSS feed schema and parsers to support additional fields, including tags, taxonomies, status, and expiration time.


-   **[Export intelligence data](https://www.servicenow.com/docs/access?context=tisc-export-observables&version=australia&pubname=australia-security-management&ft:locale=en-US), [Sharing of Outbound Intelligence Records from GUI](https://www.servicenow.com/docs/access?context=tisc-create-intel-records-lib&version=australia&pubname=australia-security-management&ft:locale=en-US), and [Add to TAXII Collections from Library List View](https://www.servicenow.com/docs/access?context=tisc-obs-add-taxii-collects&version=australia&pubname=australia-security-management&ft:locale=en-US)**

Enhanced STIX 2.1 export to include Traffic Light Protocol \(TLP\) definitions applied to intelligence objects as TLP 2.0 marking definition objects. For more information, see [Marking Definition](https://www.servicenow.com/docs/access?context=marking-definition&version=australia&pubname=australia-security-management&ft:locale=en-US).


-   **[System properties for TISC Reports](https://www.servicenow.com/docs/access?context=reports-system-properties&version=australia&pubname=australia-security-management&ft:locale=en-US)**

The system property `sn_sec_tisc.reporting.email_template_sn_sec_tisc_case` is no longer supported in TISC. It has been renamed to `sn_sec_tisc.default_report_email_template`, effective with the latest release.


-   **[Configure custom MISP API feed](https://www.servicenow.com/docs/access?context=tisc-premium-misp&version=australia&pubname=australia-security-management&ft:locale=en-US)**

Enhanced MISP API feed ingestion to handle events when the published timestamp is greater than the modified timestamp.


-   **[Define Vulnerability](https://www.servicenow.com/docs/access?context=define-vulnerability&version=australia&pubname=australia-security-management&ft:locale=en-US) and [Access the Vulnerability Entities](https://www.servicenow.com/docs/access?context=access-the-vulnerability-entities&version=australia&pubname=australia-security-management&ft:locale=en-US)**

Enhanced the vulnerability schema to support additional vulnerability intelligence fields related to CVSS scoring, exploit details, and remediation information.


</td></tr><tr><td>

UI Builder

</td><td>

-   **[Use pages across experiences](https://www.servicenow.com/docs/access?context=use-across-pages&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Share and reuse pages across workspaces without switching contexts or rebuilding content to help save time and simplify maintenance.


</td></tr><tr><td>

Visa Spoke

</td><td>

-   **[Card data security updates](https://www.servicenow.com/docs/access?context=visa-spoke&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

The following spoke actions have been updated to support integration with the Card data security application:

    -   Look up Associated Transaction List
    -   Look up Image
    -   Look up Report Output
    -   Download and Attach Image
-   **[VROL release 26.1 updates](https://www.servicenow.com/docs/access?context=visa-spoke&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

Updated the following Visa Spoke actions to align with VROL release 26.1 revision changes. These changes support dispute agents and admins in processing disputes accurately:

    -   Submit Exception Request Builder
    -   Submit Fraud Bundle Dispute Questionnaire
    -   Look up Dispute Financial Details Request Builder
    -   Look up Dispute Financial Details Response Parser
    -   Submit Fraud Report Request Builder
    -   Look up Fraud Report Details Response Parser
    -   Look up Fraud Report Details Request Builder
    -   Look up Transaction Details Request Builder
    -   Look up Dispute Details Request Builder
    -   Look up Dispute Details Response Parser
    -   Look up Dispute Filing Details Response Parser
    -   Look up Transaction Details Response Parser
    -   Look up Transaction Details from Case Response Parser
    -   Look up All Transaction Details Response Parser
    -   Create Dispute Pre Arbitration Response
    -   Look up Dispute Pre Arbitration Details Request Builder
    -   Look up Dispute Pre Arbitration Response Details Request Builder
    -   Look up Dispute Pre Arbitration Details Response Parser
    -   Look up Dispute Response Details Request Builder
    -   Submit Dispute Questionnaire
    -   Look up Dispute Pre Arbitration Response Details Response Parser
    -   Look up Dispute Response Details Response Parser
    -       -   Initiate Dispute from Transaction or Case
    -   Create Dispute Pre Arbitration

</td></tr><tr><td>

Vulnerability Response

</td><td>

-   **[Vulnerability Response assignment rules](https://www.servicenow.com/docs/access?context=vr-assignment-rules&version=australia&pubname=australia-security-management&ft:locale=en-US)**

The sn\_vul.rerun\_task\_rules system property for rerunning assignment rules was changed to sn\_sec\_rem.rerun\_task\_rules. Users must activate this property \(set to 'true'\) to rerun assignment rules.

-   **[Improved vulnerability assessment workflows](https://www.servicenow.com/docs/access?context=vr-ws-vuln-assessment&version=australia&pubname=australia-security-management&ft:locale=en-US)**
    -   CI filtering for vulnerability assessments: You can now filter which configuration items are included in a vulnerability assessment using a condition builder.
    -   Business Application population on AVITs: AVITs created from SBOM assessment results now include Business Application information, helping you understand application impact and prioritize remediation.
    -   Priority roll‑down from vulnerability assessments: Updates to the priority of a vulnerability assessment now automatically roll down to associated VITs and AVITs, ensuring consistent prioritization based on the highest severity.
-   **[Remediation task rule execution mode](https://www.servicenow.com/docs/access?context=sem-grouping-multiple-findings-remediation-tasks-processing&version=australia&pubname=australia-security-management&ft:locale=en-US)**

You can now choose how remediation task rules are evaluated during ingestion. The new Match First execution mode evaluates rules sequentially and applies only the first matching rule, assigning each finding to exactly one remediation task. The default Match All mode continues to evaluate all applicable rules.

-   **[Enhanced Compensatory controls](https://www.servicenow.com/docs/access?context=requesting-approving-risk-reduction&version=australia&pubname=australia-security-management&ft:locale=en-US)**

When new vulnerable items are ingested and associated with a remediation task that already has an approved compensating control, the reduced risk rating is now automatically inherited by those new vulnerable items.


</td></tr><tr><td>

Zero Copy Connector for ERP

</td><td>

-   **[Improved ETL data extractions](https://www.servicenow.com/docs/access?context=set-up-erp-integration-connection&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

The ETL process was refactored from Flow Designer to script includes for better performance and reliability.

-   **[Zero Copy Connector for ERP Data Products renamed to Content Packs](https://www.servicenow.com/docs/access?context=erp-canvas-available-content-packs&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

All ERP Data Products, such as Enterprise Data Foundation, Quote to Cash, and Source to Settle are renamed to Content Packs.

-   **[Zero Copy Connector for ERP Enterprise Data Foundation content pack](https://www.servicenow.com/docs/access?context=erp-canvas-enterprise-data-foundation-content-pack&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

Additional models, including Vendor Bank Details, Vendor Location Details, and Vendor Contact Details are added to the content pack for use when interacting with an SAP system.


</td></tr><tr><td>

Zero Copy Connectors

</td><td>

-   **[Apache Iceberg primary connector](https://www.servicenow.com/docs/access?context=apache-iceberg-primary-zcc&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

The Apache Iceberg connector is now certified as a primary connector.

-   **[Primary connectors in preview](https://www.servicenow.com/docs/access?context=primary-connectors-zcc&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

Primary connectors that are still being enhanced to include all planned functionality are now marked with a Preview label. These connectors are fully supported by ServiceNow®.

-   **[Australia Patch 1](../quality/australia-patch-1.md)**

[Amazon S3 Tables connector — Preview](https://www.servicenow.com/docs/access?context=primary-connectors-zcc&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)

The Amazon S3 Tables connector is now available with a Preview label, indicating that enhancements are ongoing. This connector is fully supported by ServiceNow®.

-   **[Australia Patch 1](../quality/australia-patch-1.md)**

[Apache Iceberg connector — Preview](https://www.servicenow.com/docs/access?context=primary-connectors-zcc&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)

The Apache Iceberg connector is now available with a Preview label, indicating that enhancements are ongoing. This connector is fully supported by ServiceNow®.

-   **[Australia Patch 2](../quality/australia-patch-2.md)**

[Teradata](https://www.servicenow.com/docs/access?context=teradata-zcc&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)

The Teradata connector now supports Bearer Token and OAuth authentication methods.

-   **[Australia Patch 2](../quality/australia-patch-2.md)**

[Apache Iceberg](https://www.servicenow.com/docs/access?context=apache-iceberg-primary-zcc&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)

The Apache Iceberg connector now supports S3-compatible object storage systems.


</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Australia features](../release-notes-summaries.md)

