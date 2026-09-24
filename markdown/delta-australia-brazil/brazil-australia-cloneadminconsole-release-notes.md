---
title: Combined Clone Admin Console release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Clone Admin Console from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-cloneadminconsole-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Clone Admin Console release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Clone Admin Console from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Clone Admin Console release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Clone Admin Console to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Clone Admin Console.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Instance Overview Page](https://www.servicenow.com/docs/access?context=instance-clone-landing&family=australia&ft:locale=en-US)**

The Instance Overview page now displays last-cloned timestamps for each instance, enabling you to quickly identify stale environments and prioritize update activities.

-   **[Multi-Instance View](https://www.servicenow.com/docs/access?context=instance-clone-landing&family=australia&ft:locale=en-US)**

View clone activity across connected instances from a single console. Opt in from **Configuration** &gt; **Multi-Instance View** to begin monitoring multiple instances simultaneously.

Both the source and target instances must be on Australia Patch 2 or a subsequent release to use **Multi-Instance View**.

-   **[Clone FAQ Agent \(via Now Assist\)](https://www.servicenow.com/docs/access?context=instance-clone-landing&family=australia&ft:locale=en-US)**

Get answers to clone questions directly in the console, powered by curated ServiceNow clone documentation. This AI-assisted capability streamlines the learning experience for new users.

-   **Now Assist license requirement**

Requires a Now Assist license. If Now Assist is installed after the Clone Admin Console, reinstall the console from the Store to enable the skill.

-   **[Help Page](https://www.servicenow.com/docs/access?context=instance-clone-landing&family=australia&ft:locale=en-US)**

The static FAQ section on the Homepage has been replaced with a dedicated Help page. Links to curated clone help articles are now consolidated into the new dedicated Help page for a streamlined user experience and details about the Now Assist AI skill.

-   **[Clone Request Estimated Completion](https://www.servicenow.com/docs/access?context=instance-clone-landing&family=australia&ft:locale=en-US)**

The Clone Request page now displays an estimated completion time beneath the selected Date/Time. A relative time indicator \(for example, "in 2 hours" or "in 2 weeks"\) helps you plan activities accordingly.


 -   **[OAuth 2.0 authentication for clone targets](https://www.servicenow.com/docs/access?context=clone-oauth-authentication&family=australia&ft:locale=en-US)**

Authenticate clone requests to target instances using OAuth 2.0 without requiring local admin credentials.

Both the source and target instances must be on Australia Patch 5 or a subsequent release to use OAuth target authentication.


</td></tr><tr><td>

Brazil

</td><td>

-   **[OAuth 2.0 authentication for clone targets](https://www.servicenow.com/docs/access?context=clone-oauth-authentication&family=brazil&ft:locale=en-US)**

Authenticate clone requests to target instances using OAuth 2.0 without requiring local admin credentials. One-time target instance registration enables automatic token generation and expiration for each clone request, improving security and simplifying cross-instance authentication.

Both the source and target instances must be on Australia Patch 5 or a subsequent release to use OAuth target authentication.

-   **[Multi-Instance View](https://www.servicenow.com/docs/access?context=clone-multi-instance-view&family=brazil&ft:locale=en-US)**

View clone activity across connected instances from a single console. Opt in from **Configuration** &gt; **Multi-Instance View** to begin monitoring multiple instances simultaneously.

Both the source and target instances must be on Australia Patch 2 or a subsequent release to use **Multi-Instance View**.

-   **Instance Overview**

The Instance Overview tab now displays last-cloned timestamps for each instance, enabling you to quickly identify stale environments and prioritize update activities.

-   **Clone FAQ Agent \(via Now Assist\)**

Get answers to clone questions directly in the console, powered by curated ServiceNow clone documentation. This AI-assisted capability streamlines the learning experience for new users. Requires a Now Assist license. If Now Assist is installed after the Clone Admin Console, reinstall the console from the Store to enable the skill.

-   **Help page**

The static FAQ section on the Homepage has been replaced with a dedicated Help page. Links to curated clone help articles are now consolidated into the new dedicated Help page for a streamlined user experience and details about the Now Assist AI skill.

-   **Clone request estimated completion**

The Clone Request page now displays an estimated completion time beneath the selected Date/Time. A relative time indicator \(for example, "in 2 hours" or "in 2 weeks"\) helps you plan activities accordingly.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Clone Admin Console features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Updated authentication model](https://www.servicenow.com/docs/access?context=configure-target-instance&family=australia&ft:locale=en-US)**

Clone Admin Console now uses JWT certificate-based authentication instead of username and password authentication, improving security and simplifying cross-instance authentication.


 -   **[Updated clone menu navigation items](https://www.servicenow.com/docs/access?context=instance-clone-landing&family=australia&ft:locale=en-US)**

All clone-related functions are now available under the Clone Admin Console menu navigation item.

-   **[Submit a new clone even if another clone is scheduled](https://www.servicenow.com/docs/access?context=t_StartAClone&family=australia&ft:locale=en-US)**

Create an additional clone request even if there’s already a future clone for that target. This feature removes the previous limitation where any new clone requests were not allowed until all existing requests were canceled. You can now submit new clone requests if more than five days apart from existing ones.

-   **[Clone summary](https://www.servicenow.com/docs/access?context=t_StartAClone&family=australia&ft:locale=en-US)**

Help prevent clone conflicts with the **Clone summary**, which highlights clones that are scheduled in the next 30 days that involve the same target instance.

-   **[Configuration tab](https://www.servicenow.com/docs/access?context=instance-clone-landing&family=australia&ft:locale=en-US)**

All clone-related settings are now grouped under a single **Configuration** tab for improved organization and discoverability.

-   **[Clone Home Renamed to Clone Activity](https://www.servicenow.com/docs/access?context=instance-clone-landing&family=australia&ft:locale=en-US)**

The **Clone Home** menu item has been renamed to **Clone Activity** to be more descriptive of the page's purpose and improve navigation clarity.

-   **Clone profile script updates**

Fixed an issue where setting a script in the clone\_cleanup\_script table to active=false or active=true did not apply consistently across all clone profiles the script was listed on. Changes now propagate correctly.

Both the source and target instances must be on Australia Patch 5 or a subsequent release to use cleanup script status.


</td></tr><tr><td>

Brazil

</td><td>

-   **Updated clone menu navigation items**

All clone-related functions are now available under the Clone Admin Console menu navigation item.

-   **[Configuration tab](https://www.servicenow.com/docs/access?context=clone-configurations-tab&family=brazil&ft:locale=en-US)**

All clone-related settings are now grouped under a single **Configuration** tab for improved organization and discoverability.

-   **Clone Home renamed to Clone Activity**

The **Clone Home** menu item has been renamed to **Clone Activity** to be more descriptive of the page's purpose and improve navigation clarity.

-   **Submit a new clone even if another clone is scheduled**

Create an additional clone request even if there's already a future clone for that target. This feature removes the previous limitation where any new clone requests were not allowed until all existing requests were canceled. You can now submit new clone requests if more than five days apart from existing ones.

-   **Clone summary**

Help prevent clone conflicts with the **Clone summary**, which highlights clones that are scheduled in the next 30 days that involve the same target instance.

-   **Updated authentication model**

Clone Admin Console now uses JWT certificate-based authentication instead of username and password authentication, improving security and simplifying cross-instance authentication. See [Register instance for cloning](https://www.servicenow.com/docs/access?context=configure-target-instance&family=brazil&ft:locale=en-US).

-   **Clone profile script updates**

Fixed an issue where setting a script in the clone\_cleanup\_script table to active=false or active=true did not apply consistently across all clone profiles the script was listed on. Changes now propagate correctly.

Both the source and target instances must be on Australia Patch 5 or subsequent release to use cleanup script status.

-   **Clone profile duplication**

Fixed an issue where duplicating a clone profile pulled in all existing scripts, preservers, and exclusions from the original profile. Duplicating a profile now correctly creates a new profile containing only the intended scripts, preservers, and exclusions from the source.

-   **Static FAQ content removed**

Static FAQ content has been removed from the landing page and consolidated into the new dedicated Help page for a streamlined user experience.

-   **Clone requests via lists and forms \(legacy\) deprecated**

Clone requests via lists and forms \(legacy\) are no longer supported. The page redirects to the new request page after 30 seconds.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Clone Admin Console features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Clone Admin Console features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Static FAQ Content**

Static FAQ content has been removed from the landing page and consolidated into the new dedicated Help page for a streamlined user experience.

-   **Clone requests via lists and forms \(legacy\)**

Clone requests via lists and forms \(legacy\) are no longer supported. The page redirects to the new request page after 30 seconds.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Clone Admin Console.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Activation information**

Clone Admin Console is a ServiceNow AI Platform feature that is active by default.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Clone Admin Console we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Clone Admin Console we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Clone Admin Console, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Clone Admin Console we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Clone Admin Console we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   Access all clone functions from the Clone Admin Console menu navigation item.
-   Monitor clone activity across multiple connected instances from a single console view.
-   Get answers to clone questions directly in the console with AI-assisted Now Assist capability.
-   Plan clone activities with estimated completion time indicators.

 See [Instance Clone](https://www.servicenow.com/docs/access?context=instance-clone-landing&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

