---
title: Combined Goal Framework for SPM release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Goal Framework for SPM from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-goalframeworkforspm-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-10-09"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Goal Framework for SPM release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Goal Framework for SPM from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Goal Framework for SPM release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Goal Framework for SPM to Brazil

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

Between your current release family and Brazil, new features were introduced for Goal Framework for SPM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Status rollup for goals and targets](https://www.servicenow.com/docs/access?context=defining-goals-using-goal-framework&family=australia&ft:locale=en-US)**
    -   Status — **Green**, **Yellow**, **Red**, or **None** — rolls up automatically from target breakdowns to the target for targets set to cumulative distribution.
    -   Status — **Green**, **Yellow**, **Red**, or **None** — rolls up automatically from targets and subgoals to the goal.

 -   **[Define targets at multiple organizational levels](https://www.servicenow.com/docs/access?context=goal-framework&family=australia&ft:locale=en-US)**

Define targets across multiple organizational levels with the **Assigned entity type** and **Assigned entity** fields in the target form. This enables targets created at higher levels \(for example, Company\) to be directly assigned to lower levels \(for example, Business Unit, Department\), eliminating redundant subgoal creation, and streamlining overall goal management.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Maintain-type targets](https://www.servicenow.com/docs/access?context=target-types-overview&family=brazil&ft:locale=en-US)**

Track targets that need to hold steady at a value over time, such as keeping server uptime above 98% for a year. In addition to **Maximize** and **Minimize**, the **Type** field on a target includes three options:

    -   **Maintain above**: The actual value must stay at or above the final target.
    -   **Maintain below**: The actual value must stay at or below the final target.
    -   **Maintain constant**: The actual value must stay within a tolerance range of the final target.
When you select a Maintain type, the **Target distribution** field is hidden on the target form.

-   **[Progress calculation for Maintain-type targets](https://www.servicenow.com/docs/access?context=target-types-overview&family=brazil&ft:locale=en-US)**

Measure progress on Maintain-type targets by how consistently the metric meets the target across check-in periods. The system automatically calculates status for each target breakdown period that has an actual value:

    -   **Maintain above**: Green when the actual is at or above the final target, and Red when it's below.
    -   **Maintain below**: Met when the actual is at or below the final target.
    -   **Maintain constant**: Met when the actual falls within the tolerance range, bounds included.
Target-level progress equals the number of periods that meet the target divided by the total periods up to the latest actual value, multiplied by 100. For example, a **Maintain above** target with a final target of 75 and quarterly actuals of 78, 72, 80, and 76 shows 75% progress. Three of 4 periods meet the target.

-   **[Target breakdowns for Maintain-type targets](https://www.servicenow.com/docs/access?context=target-breakdowns&family=brazil&ft:locale=en-US)**

Start every check-in period from the same value. When you save a Maintain-type target, each target breakdown gets a planned target equal to the final target value. You can edit the planned target of any breakdown. If the final target value is empty, breakdowns are created with a planned target of 0.


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

Australia

</td><td>

-   **[Changes to Target form](https://www.servicenow.com/docs/access?context=target-form&family=australia&ft:locale=en-US)**

The **Assigned entity type** and **Assigned entity** fields have been added to the Target form to support defining targets at multiple organizational levels.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Target breakdown regeneration](https://www.servicenow.com/docs/access?context=target-breakdowns&family=brazil&ft:locale=en-US)**

Target breakdowns adjust to changes in a target's dates or final target value, and recorded actuals are kept:

    -   Moving the start date later removes the breakdowns before the new start date. The remaining breakdowns keep their planned targets and actuals.
    -   Moving the start date earlier adds breakdowns for the new periods, with the same planned target.
    -   Shortening or extending the end date removes or adds the matching breakdowns.
    -   Changing the final target value updates the planned target of every breakdown and recalculates status and progress.
-   **[Type field editable after actuals are recorded](https://www.servicenow.com/docs/access?context=change-target-type-spw&family=brazil&ft:locale=en-US)**

Change the **Type** of a target after actual values are recorded, without deleting and recreating the target. When you change the type from Maximize to Minimize, or from Maximize to a Maintain type:

    -   The total actuals to date stay the same and are placed in the latest target breakdown period.
    -   Planned values are recalculated for the new type.
    -   Progress and attainment are recalculated using the new type's logic.
A warning appears before you save the change. The change is recorded in the audit history.

-   **[Number field in the target list view](https://www.servicenow.com/docs/access?context=target-form-egm&family=brazil&ft:locale=en-US)**

The **Number** field appears as a link in the actual value automation list view. That list view opens when you view targets in Core UI.


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

Australia

</td><td>

-   **Activation information**

Install Goal Framework for SPM by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


**Important:** [Goal Framework for SPM](https://www.servicenow.com/docs/access?context=goal-framework&family=australia&ft:locale=en-US) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

