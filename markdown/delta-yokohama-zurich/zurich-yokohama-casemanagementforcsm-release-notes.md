---
title: Combined Case management for CSM release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for Case management for CSM from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-casemanagementforcsm-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Case management for CSM release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for Case management for CSM from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Case management for CSM release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Case management for CSM to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Case management for CSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Case Management for Invoice Operations](https://servicenow-staging.fluidtopics.net/access?context=csm-invoice-operations&family=yokohama&ft:locale=en-US)**

Use the Case Management for Invoice Operations application \(com.sn\_csm\_invoice\) to create cases for multiple invoices or for specific invoice lines. Agents can use these cases to process invoice-related services such as invoice disputes or requested corrections.

-   **[Process mining](https://servicenow-staging.fluidtopics.net/access?context=process-mining&family=yokohama&ft:locale=en-US)**

Use the following features to find process improvement opportunities:

    -   Use work notes analysis to learn the operational reasons behind activity transitions. This feature is Now LLM based.
    -   Mine the configured base system project to investigate the causes and get a clear view of the long resolution times and delays.
-   **[Quick start tests for Customer Service Management](https://servicenow-staging.fluidtopics.net/access?context=quick-start-tests-csm&family=yokohama&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Customer Service Management works as expected. If you customized Customer Service Management, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Task plan templates](https://servicenow-staging.fluidtopics.net/access?context=task-plan-templates&family=zurich&ft:locale=en-US)**

Create templates that define the repeatable tasks and records that need to be created for business processes. Define the tasks, set the task order, and create conditions that determine when these tasks and records are created.

-   **[Add multiple entitlements to a case](https://servicenow-staging.fluidtopics.net/access?context=add-entitlement-to-case&family=zurich&ft:locale=en-US)**

View the available entitlements on a customer service case and associate the multiple entitlements to the case. Available entitlements are associated with the account or consumer, product, and contract selected on the case record.

-   **[Recommend service definitions based on case context](https://servicenow-staging.fluidtopics.net/access?context=csm-service-definitions&family=zurich&ft:locale=en-US)**

Recommend the most relevant services to an agent based on the record context, such as the short description or description of the interaction.

-   **[Customer Service Case Types - Enable the service selector to launch record producers](https://servicenow-staging.fluidtopics.net/access?context=csm-service-definition-catalog-items&family=zurich&ft:locale=en-US)**

Use the Service Portal record producers when your agents are creating cases in CSM Configurable Workspace. Agents can select the service definitions from the case type selector and launch the record producers.

-   **[Quick start tests for Customer Service Management](https://servicenow-staging.fluidtopics.net/access?context=quick-start-tests-csm&family=zurich&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Customer Service Management works as expected. If you customized Customer Service Management, copy the quick start tests and configure them for your customizations.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Case management for CSM features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Process mining](https://servicenow-staging.fluidtopics.net/access?context=process-config-builder&family=yokohama&ft:locale=en-US)**

Use the process mining enhancements to improve processes as needed:

    -   Removed the viewer role from all records in the Process Mining Content Pack for Customer Service Management \(CSM\).
    -   Set process configurations as read-only templates, deletable only by a process mining administrator. You can enable customers to copy the template or import specific parts into their custom configuration.
-   **[Case lines and workflows](https://servicenow-staging.fluidtopics.net/access?context=case-line-form&family=yokohama&ft:locale=en-US)**

The Case Line table \(sn\_case\_line\) includes the **Install base** and **Asset** reference fields. These fields display information based on the selected account and product.


</td></tr><tr><td>

Zurich

</td><td>

-   **[\[Placeholder link text to key sharing-task-plan-template\]](https://servicenow-staging.fluidtopics.net/access?context=sharing-task-plan-template&family=zurich&ft:locale=en-US)**

Sharing task plan templates ensures that only authorized users can access, edit, or share templates based on their role and location, preventing misuse and maintaining operational integrity. Sharing task plant template features include:

    -   Access control: Users can now provide access to task plan templates at various levels, including user, group, and service organization.
    -   Ownership Management: The Owner or an Admin can change the ownership of a Template by updating the Owner field.
    -   Global template: Task plan templates can be marked as global, making them visible to all users with read access.
    -   Form and List Layouts: Admins can view and edit form and list layouts for sharing, displaying all relevant fields.
    -   Notifications: In-app notifications are sent when access is granted, Selecting the notification opens the shared template directly.
-   **[Task plan template configurations](https://servicenow-staging.fluidtopics.net/access?context=task_plan_template_configurations&family=zurich&ft:locale=en-US)**

Admins can create configurations for task plan templates that pre-fill information when creating a new task plan template.


-   **[Filtering service definitions](https://servicenow-staging.fluidtopics.net/access?context=csm-service-definitions&family=zurich&ft:locale=en-US)**

Enable agents to filter the service definitions that are shown on the service selector in the following ways:

    -   By user, role, group, or agent
    -   By entity critera such as location, customer level, or related entities
-   **[Case lines for Case Management - Add multiple entitlements to case lines](https://servicenow-staging.fluidtopics.net/access?context=csm-case-mgmt-case-lines&family=zurich&ft:locale=en-US)**

View the available entitlements on a case line and associate the multiple entitlements to that case line. Available entitlements are associated with the contracts and entitlements that are purchased by the customer.

-   **[Targeted Communications](https://servicenow-staging.fluidtopics.net/access?context=targeted-comm-publication-workflows&family=zurich&ft:locale=en-US) and [Case Digests](https://servicenow-staging.fluidtopics.net/access?context=customer-service-case-digests&family=zurich&ft:locale=en-US) workflows**

Legacy workflows for the Targeted Communications \(com.sn\_publications\) and Case Digests \(com.sn\_csm\_case\_digest\) applications have been migrated to low-code flows in Workflow Studio. The functionality of the flows remains the same.

-   **[Classifying sensitive data](https://servicenow-staging.fluidtopics.net/access?context=dps-data-privacy-overview&family=zurich&ft:locale=en-US)**

Fields in the Customer Service Management and Targeted Communications tables are mapped to the Data Privacy data classes. For more information, see the [Data privacy overview](https://servicenow-staging.fluidtopics.net/access?context=dps-data-privacy-overview&family=zurich&ft:locale=en-US) topic in the ServiceNow® Platform Security documentation.

-   **Deny-Unless ACLs implemented on CSM tables**

Deny-Unless access control lists \(ACLs\) were implemented on CSM tables for non-authenticated users, such as users with public roles. With this minimum-security setting, only authenticated users can perform read, write, delete, or create actions on these tables. For more information about Deny-Unless ACLs, see the [Deny-Unless ACL](https://servicenow-staging.fluidtopics.net/access?context=acl-denial-behavior&family=zurich&ft:locale=en-US) topic in the ServiceNow® Platform Security documentation.

-   **[Customer Service Case Types moved from family to store release](https://servicenow-staging.fluidtopics.net/access?context=customer-service-case-types&family=zurich&ft:locale=en-US)**

Starting with the Zurich release, the Customer Service Case Types application \(sn\_csm\_case\_types\) has moved to the ServiceNow Store. Any new enhancements to this application are delivered through the Customer Service Case Types store app.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Case management for CSM features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Case management for CSM features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Starting with the Yokohama release, Customer Service CTI Demo Data is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. ServiceNow Voice with Amazon Connect provides the latest experience for this functionality. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Zurich

</td><td>

-   Starting with the Yokohama release, Customer Service CTI Demo Data is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. ServiceNow Voice with Amazon Connect provides the latest experience for this functionality. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.
-   Starting with the Zurich release, the Customer Service Case Types plugin is available as a store plugin and, as such, the family version of the plugin is being prepared for future deprecation. Upon upgrading, customers will automatically move to the store version of the plugin. It will be hidden from the family plugins and no longer installed on new instances but will continue to be supported as a store plugin. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Case management for CSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Customer Service Management is available with activation of the Customer Service plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://servicenow-staging.fluidtopics.net/access?context=t_ActivateCustomerService&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Customer Service Management is available with activation of the Customer Service plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://servicenow-staging.fluidtopics.net/access?context=t_ActivateCustomerService&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Case management for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Case management for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

ServiceNow workspaces don’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge - Chromium or one of the other supported browsers listed in [Browser support](https://servicenow-staging.fluidtopics.net/access?context=browser-support&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

ServiceNow workspaces don’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge - Chromium or one of the other supported browsers listed in [Browser support](https://servicenow-staging.fluidtopics.net/access?context=browser-support&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Case management for CSM, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Case management for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Case management for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   Create cases for invoice-related services such as invoice disputes or requested corrections with the Case management for Invoice Operations application.
-   Use process mining to mine the configured base system project to investigate the causes of long resolution times.

 See [Case management for Customer Service Management](https://servicenow-staging.fluidtopics.net/access?context=csm-case-management&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Sharing task plan templates ensures that only authorized users can access, edit, or share templates based on their role and location, preventing misuse and maintaining operational integrity.
-   View the most relevant services that are available for customers when creating customer service cases.
-   View and select from the available entitlements that are associated with the customer, product, and contract information to associate multiple entitlements with customer service cases.
-   Filter the service definitions that are displayed to agents based on such criteria as the assigned role or group, or entity criteria.

 See [Case management for Customer Service Management](https://servicenow-staging.fluidtopics.net/access?context=csm-case-management&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)

