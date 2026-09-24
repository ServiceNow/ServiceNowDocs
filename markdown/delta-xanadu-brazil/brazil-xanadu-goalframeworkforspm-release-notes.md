---
title: Combined Goal Framework for SPM release notes for upgrades from Xanadu to Brazil
description: Consolidated page of all release notes for Goal Framework for SPM from Xanadu to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-brazil/brazil-xanadu-goalframeworkforspm-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Goal Framework for SPM release notes for upgrades from Xanadu to Brazil

Consolidated page of all release notes for Goal Framework for SPM from Xanadu to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Goal Framework for SPM release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Goal Framework for SPM to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

After upgrading to Goal Framework for SPM v2.3.0, run the **Migrate BreakdownInterval To Checkinfrequency** scheduled job. This scheduled job migrates the existing values in the **Review frequency** and **Breakdown interval** fields to the **Check-in frequency** field in the target records. For more information on how these values are migrated for targets with different values, see [Target breakdowns migration](https://www.servicenow.com/docs/access?context=target-breakdowns-migration&family=xanadu&ft:locale=en-US).

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

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Goal Framework for SPM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Enhanced target breakdowns](https://www.servicenow.com/docs/access?context=target-breakdowns-gf&family=xanadu&ft:locale=en-US)**

Create Daily, Weekly, or Monthly target breakdowns according to how often you want to update and track the progress of the target. The target breakdowns are created based on the value selected in the **Check-in frequency** field. For example, if you select **Monthly** in the **Check-in frequency** field for a target spanning a year, then 12 monthly target breakdowns are created.


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

-   **[Define targets at multiple organizational levels](https://www.servicenow.com/docs/access?context=goal-framework&family=australia&ft:locale=en-US)**

Define targets across multiple organizational levels with the **Assigned entity type** and **Assigned entity** fields in the target form. This enables targets created at higher levels \(for example, Company\) to be directly assigned to lower levels \(for example, Business Unit, Department\), eliminating redundant subgoal creation, and streamlining overall goal management.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Automatic status calculation for targets](https://www.servicenow.com/docs/access?context=automatic-status-calculation-targets&family=brazil&ft:locale=en-US)**

Automatically determine target status based on actual achievement percentages. When you enter actual values for a target period, the system compares the achievement percentage against predefined thresholds and automatically assigns a status \(Green, Yellow, or Red\). This eliminates manual status selection, reducing data entry errors and improving organizational governance.

Status is calculated and updated when you enter actual values using the formula: \(\(Actual Value - Start Value\) / \(Planned Target - Start Value\)\) x 100. Target owners can override automatically calculated status values at any time. If you update the actual value after a manual override, the system recalculates the status automatically.

-   **[Configure automatic status calculation thresholds](https://www.servicenow.com/docs/access?context=configure-automatic-status-calculation&family=brazil&ft:locale=en-US)**

Enable administrators to customize automatic status calculation thresholds and enable or disable the feature based on organizational requirements. By default, automatic status calculation is enabled with system-defined thresholds of Green \(≥90%\), Yellow \(75-89%\), and Red \(&lt;75%\).

Administrators can adjust threshold percentages using the system property **sn\_gfa.target.auto\_status.thresholds**. To disable automatic status calculation and revert to manual status selection, set the system property to `false`.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Goal Framework for SPM features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Changes to Target form](https://www.servicenow.com/docs/access?context=target-form&family=xanadu&ft:locale=en-US)**

On the Target form, the **Breakdown interval** and **Cumulative target** fields have been removed, and the **Review frequency** field has been renamed to **Check-in frequency**.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Goal system properties](https://www.servicenow.com/docs/access?context=components-installed-with-goal-framework&family=zurich&ft:locale=en-US)**

Users with the sn\_gf\_goal\_admin role assigned can update goal-specific system properties:

    -   **sn\_gfa.weeklyCheckInDayToMapMonth** - Defines the end day of the week used for mapping weekly target breakdowns to a month. The default value is Friday.
    -   **glide.ui.sn\_gf\_goal\_target\_activity.field** - Enables activity stream for fields of the targets.
    -   **sn\_gfa.target\_breakdown\_decimals** - Sets the number of decimal places displayed for target values when generating target breakdowns. The default value is 2.

</td></tr><tr><td>

Australia

</td><td>

-   **[Changes to Target form](https://www.servicenow.com/docs/access?context=target-form&family=australia&ft:locale=en-US)**

The **Assigned entity type** and **Assigned entity** fields have been added to the Target form to support defining targets at multiple organizational levels.


</td></tr><tr><td>

Brazil

</td><td>

-   **Default check-in frequency**

New quantitative targets now default to **Quarterly** check-in frequency to create target breakdowns when you save the target. You can change the check-in frequency before creating the target.

-   **Improved status labeling**

The **None** status option is now labeled **No status** for goals, strategic priorities, target progress, and target breakdowns, providing clearer communication about goal status states.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Goal Framework for SPM features or functionality were removed.

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

Between your current release family and Brazil, some Goal Framework for SPM features or functionality were deprecated.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Now LLM Service**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr></tbody>
</table>## Activation information

Review information on how to activate Goal Framework for SPM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Install Goal Framework for SPM by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

Install Goal Framework for SPM by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install Goal Framework for SPM by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Install Goal Framework for SPM by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store.


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Goal Framework for SPM we have noted them here.

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

If any specific browser requirements were introduced or changed for Goal Framework for SPM we have noted them here.

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

Review details on accessibility information for Goal Framework for SPM, such as specific requirements or compliance levels.

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

If there are specific localization considerations for Goal Framework for SPM we have noted them here.

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

If there are specific highlight considerations for Goal Framework for SPM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Use the enhanced target breakdown feature to update actuals and track the progress of your targets in daily, weekly, monthly, quarterly, or yearly intervals.

 See [Goal Framework for SPM](https://www.servicenow.com/docs/access?context=goal-framework&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

Use the sn\_gf\_goal\_admin role to update the goal-specific system properties.

 See [Goal Framework for SPM](https://www.servicenow.com/docs/access?context=goal-framework&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

Define targets across multiple organizational levels with the **Assigned entity** field in the target form.

 See [Goal Framework for SPM](https://www.servicenow.com/docs/access?context=goal-framework&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   Align work items to goals and targets, and automate actual value updates by configuring target sources, ensuring real-time progress tracking without manual updates.
-   Set target breakdowns at daily, weekly, monthly, quarterly, or yearly intervals. Distribute the final target value cumulatively or non-cumulatively across the defined time duration.

 See [Goal Framework and Goal Framework for SPM](https://www.servicenow.com/docs/access?context=goal-framework&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-xanadu-brazil/rn-combined-intro.md)

