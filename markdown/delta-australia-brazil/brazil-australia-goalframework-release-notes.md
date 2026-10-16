---
title: Combined Goal Framework release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Goal Framework from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-goalframework-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-10-09"
reading_time_minutes: 5
breadcrumb: [Products combined by family]
---

# Combined Goal Framework release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Goal Framework from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Goal Framework release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Goal Framework to Brazil

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

Between your current release family and Brazil, new features were introduced for Goal Framework.

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

-   **[Maintain-type targets](https://www.servicenow.com/docs/access?context=target-types-gf&family=brazil&ft:locale=en-US)**

Track targets that must hold a value for the whole period instead of growing or shrinking toward it. The **Type** field on a target has three new options: **Maintain above**, **Maintain below**, and **Maintain constant**.

For these types, target progress is the percentage of breakdown periods with actuals where the target was met. For example, if a Maintain above target is met in three of four quarters, its progress is 75%.

Maintain types are available only with quantitative units of measure. The **Target value distribution** field isn't shown for them.

-   **[Tolerance for Maintain constant targets](https://www.servicenow.com/docs/access?context=configure-maintain-constant-tolerance&family=brazil&ft:locale=en-US)**

Set how far a Maintain constant target's actual value can move from the final target and still count as met. By default, an actual value within 5% of the final target, above or below, counts as met. Administrators can change the tolerance with the **sn\_gf.maintain\_constant\_tolerance\_percent** system property.

-   **[Unique numbers and prefixes for goals and targets](https://www.servicenow.com/docs/access?context=change-number-prefix-goals-targets&family=brazil&ft:locale=en-US)**

Match goal and target numbers to your organization's terminology, for example, OBJ and KR if you use objectives and key results. After an administrator changes the prefix in the number configuration, run the **GF - Override Goal and Target Number fields with customized prefixes** scheduled job to update existing records. The job keeps the numeric part of each number, so GOAL0004512 becomes OBJ0004512. It also skips records that already have the new prefix.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Goal Framework features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Changes to Goal and Target forms](https://www.servicenow.com/docs/access?context=goal-form&family=australia&ft:locale=en-US)**

The **Cancelled** option has been added to the **State** field in both the [Goal](https://www.servicenow.com/docs/access?context=goal-form&family=australia&ft:locale=en-US) and [Target](https://www.servicenow.com/docs/access?context=target-form&family=australia&ft:locale=en-US) forms, enabling you to set their status to **Cancelled** when needed.

-   **[Changes to Strategic Priority form](https://www.servicenow.com/docs/access?context=strategic-priority-form&family=australia&ft:locale=en-US)**

The **Status** field has been added to the Strategic Priority form, enabling you to set the status of a strategic priority as **None**, **Green**, **Yellow**, or **Red**.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Target type editable when actuals exist](https://www.servicenow.com/docs/access?context=change-target-type-gf&family=brazil&ft:locale=en-US)**

You can change a target's **Type** after actual values have been recorded. Previously, the **Type** field became read-only once a target had progress. A confirmation message appears before the change is applied, and if you cancel, the **Type** goes back to its original value. Changing the **Type** clears the target's actual value and percent complete. The exceptions are changes between two Maintain types and changes to or from Milestone.

-   **[Type and unit of measure stay in sync](https://www.servicenow.com/docs/access?context=target-types-gf&family=brazil&ft:locale=en-US)**

Choosing a target **Type** sets a matching unit of measure:

    -   **Milestone**: Sets the unit of measure to Yes/No, or keeps a custom qualitative unit if one is already selected.
    -   **Maximize**, **Minimize**, or a Maintain type: Restores the last quantitative unit you used, or sets Count \(\#\) if there isn't one.
The **Type** list always shows all six types. The same pairing also applies to targets created or updated through imports or APIs.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Goal Framework features or functionality were removed.

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

Between your current release family and Brazil, some Goal Framework features or functionality were deprecated.

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
</table>## Activation information

Review information on how to activate Goal Framework.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Activation information**

Install Goal Framework by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


**Important:** Goal Framework is available in the ServiceNow Store. For details, see the Activation information section of these release notes.

</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Install Goal Framework by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store.


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Goal Framework we have noted them here.

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

If any specific browser requirements were introduced or changed for Goal Framework we have noted them here.

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

Review details on accessibility information for Goal Framework, such as specific requirements or compliance levels.

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

If there are specific localization considerations for Goal Framework we have noted them here.

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

If there are specific highlight considerations for Goal Framework we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

Use the enhanced Goal, Target, and Strategic Priority forms to more effectively manage and track your organization’s goals.

 See [Goal Framework](https://www.servicenow.com/docs/access?context=goal-framework&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   Create strategic plans, define organizational goals with quantitative or qualitative targets, and establish real-time checkpoints across daily, weekly, monthly, quarterly, and yearly frequencies to track execution.
-   Associate work and planning items—including demand, projects, and portfolios—with strategic goals and targets to provide end-to-end performance visibility across the organization.
-   Support Enterprise PMO \(EPMO\) and portfolio managers with customizable goal preferences, weighted progress calculations, and centralized governance to drive business outcomes aligned to strategic priorities.

 See [Goal Framework](https://www.servicenow.com/docs/access?context=goal-framework&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

