---
title: Combined Case management for CSM release notes for upgrades from Xanadu to Yokohama
description: Consolidated page of all release notes for Case management for CSM from Xanadu to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-xanadu-yokohama/yokohama-xanadu-casemanagementforcsm-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Case management for CSM release notes for upgrades from Xanadu to Yokohama

Consolidated page of all release notes for Case management for CSM from Xanadu to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Case management for CSM release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Case management for CSM to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

The customer service manager role \[sn\_customerservice\_manager\] includes the approver user role \[approver\_user\]. The approver user role replaces the approval admin role \[approval\_admin\]. Users with the customer service manager role can approve the approval requests that are assigned to them.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Case management for CSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Playbooks](https://www.servicenow.com/docs/access?context=customer-service-case-playbooks&family=xanadu&ft:locale=en-US)**

Use updated playbook templates in UI Builder that incorporate generative AI feature parity and Agent Experience modernization features such as the modeless dialogs, activity stream, lookup cards, and related items.

-   **[Order Operations Case Management](https://www.servicenow.com/docs/access?context=csm-case-mgmt-order-ops&family=xanadu&ft:locale=en-US)**

Use the Order Operations Case Management application \(com.sn\_order\_case\) to create order cases that reference multiple line items, including orders and order lines. Agents can use these cases to process order-related services such as order changes, inquiries, and disputes.

-   **[Case lines and workflows](https://www.servicenow.com/docs/access?context=csm-case-mgmt-case-lines&family=xanadu&ft:locale=en-US)**

Use the Case lines and workflows application \(com.sn\_case\_line\) to reference multiple line items on a case record, including orders or order lines, invoices or invoices lines, contracts, and sold products.

-   **[Quick start tests for Customer Service Management](https://www.servicenow.com/docs/access?context=quick-start-tests-csm&family=xanadu&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Customer Service Management works as expected. If you customized Customer Service Management, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Case Management for Invoice Operations](https://www.servicenow.com/docs/access?context=csm-invoice-operations&family=yokohama&ft:locale=en-US)**

Use the Case Management for Invoice Operations application \(com.sn\_csm\_invoice\) to create cases for multiple invoices or for specific invoice lines. Agents can use these cases to process invoice-related services such as invoice disputes or requested corrections.

-   **[Process mining](https://www.servicenow.com/docs/access?context=process-mining&family=yokohama&ft:locale=en-US)**

Use the following features to find process improvement opportunities:

    -   Use work notes analysis to learn the operational reasons behind activity transitions. This feature is Now LLM based.
    -   Mine the configured base system project to investigate the causes and get a clear view of the long resolution times and delays.
-   **[Quick start tests for Customer Service Management](https://www.servicenow.com/docs/access?context=quick-start-tests-csm&family=yokohama&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Customer Service Management works as expected. If you customized Customer Service Management, copy the quick start tests and configure them for your customizations.


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Case management for CSM features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Case type selector configuration](https://www.servicenow.com/docs/access?context=csm-case-type-select-modals-product-service&family=xanadu&ft:locale=en-US)**

Configure the Product Service select version of the case type selector to hide the product filter.

-   **[Roles included with the customer service manager role](https://www.servicenow.com/docs/access?context=r_RolesInstalledWithCustomerService&family=xanadu&ft:locale=en-US)**

The customer service manager role \[sn\_customerservice\_manager\] includes the approver user role \[approver\_user\]. For upgrade customers, the approver user role replaces the approval admin role \[approval\_admin\]. Users with the customer service manager role can approve the approval requests that are assigned to them.

-   **[Process Mining](https://www.servicenow.com/docs/access?context=improve-opportunities&family=xanadu&ft:locale=en-US)**

Added different variants of the two enhanced types of base system opportunities that you can use on a project to identify and address common inefficiencies in customer operations:

    -   Rule-based finding definitions: Execute one or more finding rule chains in sequence according to the definitions. The records that match the logic of these specifications are classified as a match for improvement opportunities.
    -   Automated finding definitions: Show improvement opportunities by using the default patterns that are already available for selection.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Process mining](https://www.servicenow.com/docs/access?context=process-config-builder&family=yokohama&ft:locale=en-US)**

Use the process mining enhancements to improve processes as needed:

    -   Removed the viewer role from all records in the Process Mining Content Pack for Customer Service Management \(CSM\).
    -   Set process configurations as read-only templates, deletable only by a process mining administrator. You can enable customers to copy the template or import specific parts into their custom configuration.
-   **[Case lines and workflows](https://www.servicenow.com/docs/access?context=case-line-form&family=yokohama&ft:locale=en-US)**

The Case Line table \(sn\_case\_line\) includes the **Install base** and **Asset** reference fields. These fields display information based on the selected account and product.


</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Case management for CSM features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some Case management for CSM features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Starting with the Xanadu release, CSM Agent Workspace is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. [CSM Configurable Workspace](https://www.servicenow.com/docs/access?context=csm-workspaces-configure&family=xanadu&ft:locale=en-US) provides the latest experience for this functionality.

</td></tr><tr><td>

Yokohama

</td><td>

Starting with the Yokohama release, Customer Service CTI Demo Data is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. ServiceNow Voice with Amazon Connect provides the latest experience for this functionality. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Case management for CSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Customer Service Management is a ServiceNow AI Platform feature that is available with activation of the Customer Service Management plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://www.servicenow.com/docs/access?context=t_ActivateCustomerService&family=xanadu&ft:locale=en-US).

 Additional Customer Service Management features are available with the activation of other plugins. For details, see [Additional plugins for Customer Service Management](https://www.servicenow.com/docs/access?context=r_CustServMgmtAddtlPluginsTable&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Customer Service Management is available with activation of the Customer Service plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://www.servicenow.com/docs/access?context=t_ActivateCustomerService&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Case management for CSM we have noted them here.

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Case management for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

ServiceNow workspaces don’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge - Chromium or one of the other supported browsers listed in [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

ServiceNow workspaces don’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge - Chromium or one of the other supported browsers listed in [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Case management for CSM, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

The following templates were updated to support reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels.

-   [Case playbook: horizontal stages template](https://www.servicenow.com/docs/access?context=csm-playbook-templates&family=xanadu&ft:locale=en-US)
-   [Case playbook: vertical stages template](https://www.servicenow.com/docs/access?context=csm-playbook-templates&family=xanadu&ft:locale=en-US)

</td></tr><tr><td>

Yokohama

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

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

Xanadu

</td><td>

-   Create pages and page variants that contain horizontal or vertical playbooks by using playbook templates.
-   Use playbook record pages in CSM Configurable Workspace to guide users through the stages and activities of a playbook and resolve cases.
-   Identify common inefficiencies in customer operations by using process mining definitions.

 See [Case management for Customer Service Management](https://www.servicenow.com/docs/access?context=csm-case-management&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Create cases for invoice-related services such as invoice disputes or requested corrections with the Case management for Invoice Operations application.
-   Use process mining to mine the configured base system project to investigate the causes of long resolution times.

 See [Case management for Customer Service Management](https://www.servicenow.com/docs/access?context=csm-case-management&family=yokohama&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-xanadu-yokohama/rn-combined-intro.md)

