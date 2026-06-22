---
title: Combined Domain Separation release notes for upgrades from Washington DC to Australia
description: Consolidated page of all release notes for Domain Separation from Washington DC to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-washingtondc-australia/australia-washingtondc-domainseparation-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Domain Separation release notes for upgrades from Washington DC to Australia

Consolidated page of all release notes for Domain Separation from Washington DC to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Domain Separation release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Domain Separation to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Domain Separation.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Post-Production Domain Separation Activation Utility](https://www.servicenow.com/docs/access?context=post-prod-domain-sep-utility&family=yokohama&ft:locale=en-US)**

Begin using domain separation on a live environment with the guided Post-Production Domain Separation Activation Utility.


</td></tr><tr><td>

Zurich

</td><td>

-   **[\[Placeholder link text to key delete-by-domain\]](https://www.servicenow.com/docs/access?context=delete-by-domain&family=zurich&ft:locale=en-US)**

Domain Admins may now delete by domain to efficiently manage domains and reduce storage overhead. The tool also includes data recovery and retention, enabling rollbacks and retention policy setting.

-   **[\[Placeholder link text to key domain-job-manger\]](https://www.servicenow.com/docs/access?context=domain-job-manger&family=zurich&ft:locale=en-US)**

Changes to the domain table are now queued sequentially and batched into a single background job. This helps simplify domain table updates. Users are notified when a job needs to be delayed as well when a job needs to start.


</td></tr><tr><td>

Australia

</td><td>

-   **[AI Agent for Domain Visibility Management](https://www.servicenow.com/docs/access?context=domain-sep-aia&family=australia&ft:locale=en-US)**

Use the new AI agent to manage domain visibility through natural language conversations. Domain administrators can ask the agent to query visibility by user, validate that visibility is not redundant or oversized, and take direct actions to add or remove visibility settings. The agent supports end-to-end workflows so administrators can complete multistage visibility management tasks without leaving the conversational interface. Install the Domain Separation AI Agent plugin to enable this capability.

-   **[Global Domain Upgraded Process Overrides Report](https://www.servicenow.com/docs/access?context=t_view-upgraded-overriden-domains&family=australia&ft:locale=en-US)**

System and domain administrators can now track and review process overrides that are affected by global process upgrades. A new admin dashboard provides a comprehensive list of impacted overrides with filtering and sorting by date and process type. Use the scriptable API to build custom integrations or automations on top of the override tracking data.

-   **[Domain Visibility Performance Improvements for Large MSPs](https://www.servicenow.com/docs/access?context=t_ViewDomainRelationships&family=australia&ft:locale=en-US)**

Domain visibility queries now complete in under one second on average — a 70% reduction from the previous 3.2 second average for large instances. A new query optimization replaces multiple OR conditions with a single IN clause on the domain ID for instances that exceed the configured domain collection size threshold. All 785 Domain Separation customers benefit from faster queries, with the greatest impact for the 20 customers operating 10,000 or more domains.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Domain Separation features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr><tr><td>

Australia

</td><td>

-   **Dot-Walk Scoping Bypass Compliance \(DIRS0000335\)**

Domain Separation has been updated to comply with the platform-wide dot-walk scoping bypass directive \(DIRS0000335\). Customers who have customizations involving dot-walk queries on domain-separated tables should review their configurations after upgrading.

-   **Java 21 Runtime Support**

Domain Separation has been validated and updated to run on the Java 21 runtime introduced in the Australia release. Deprecated Java APIs have been removed from the Domain Separation codebase. No action is required for customers — this update is included automatically with the Australia upgrade.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Domain Separation features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Domain Separation features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Domain Separation.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

Domain Separation is a ServiceNow AI Platform feature that is available with activation of the com.glide.domain.activation\_utility. For details, see [Domain separation plugin](https://www.servicenow.com/docs/access?context=domain-sep-plugin&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Domain Separation is a ServiceNow AI Platform feature that is available with activation of the com.glide.domain.activation\_utility. For details, see [Domain separation plugin](https://www.servicenow.com/docs/access?context=domain-sep-plugin&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

Domain Separation is a ServiceNow AI Platform feature available with activation of the `com.glide.domain.activation_utility` plugin. For details, see [Domain separation plugin](https://www.servicenow.com/docs/access?context=domain-sep-plugin&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Domain Separation we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Domain Separation we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Domain Separation, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Domain Separation we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Domain Separation we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

Enable domain separation in live environments by using the Post-Production Domain Separation Activation Utility.

 See [Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Changes to the domain table are queued sequentially and batched into a single background job. This helps simplify domain table updates.
-   Domain Admins can delete by domain to efficiently manage domains and reduce storage overhead.

 See [Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Use the new AI agent to manage domain visibility through natural language. Query, validate, add, and remove visibility settings without navigating complex admin interfaces.

-   System and domain administrators can now review a dedicated dashboard of process overrides that were affected by global process upgrades. Filter and sort overrides by date and process type to prioritize review and take action.
-   Domain visibility queries now complete in under one second for large instances — a 70% improvement for MSPs managing thousands of domains and users.

 See for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-washingtondc-australia/rn-combined-intro.md)

