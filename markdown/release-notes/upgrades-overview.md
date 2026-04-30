---
title: Upgrade to the Zurich release
description: Upgrading and patching your instance requires planning, testing, and validation. To ensure a safe and effective upgrade, read the release notes, create upgrade plans, and test your upgrade on non-production instances before upgrading your production instance.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Zurich release notes]
---

# Upgrade to the Zurich release

Upgrading and patching your instance requires planning, testing, and validation. To ensure a safe and effective upgrade, read the release notes, create upgrade plans, and test your upgrade on non-production instances before upgrading your production instance.

**Important:** These topics contain in-depth explanations about upgrades. For a step-by-step reference of upgrade steps, refer to the [Upgrade planning checklist](../upgrades-planning-checklist.md).

<table id="table_sqt_d3p_d2b"><tbody><tr><td>

![Release notes](../image/phase1-book.png)

</td><td>

-   **[Phase 1 - Read the release notes and plan your upgrade](../task/upgrades-phase-1.md)**

Before you begin the upgrade process, it is essential to read the release notes for your target version so you understand the required upgrade and migration tasks. This information helps you plan a safe and effective upgrade.


</td></tr><tr><td>

![Upgrade checklist](../image/phase2-checklist.png)

</td><td>

-   **[Phase 2 - Prepare for the development instance upgrade](../task/upgrades-phase-2.md)**

For a better understanding of your production upgrade duration, request a full clone of your production instance \(including large tables and attachments\) onto a non-production instance. Confirm your current and target release versions, because you will later use this information when scheduling your upgrade in Now Support.


</td></tr><tr><td>

![Calendar with an upgrade date](../image/phase3-calendar.png)

</td><td>

-   **[Phase 3 - Verify your upgrade configurations and schedule the development instance upgrade in Now Support](../task/upgrades-phase-3.md)**

Check the configuration of the **Check distribution for possible upgrade** scheduled job to view how often and when it runs. Review information about timing your upgrade in coordination with the **Check distribution for possible upgrade** scheduled job. Then, schedule your upgrade in Now Support.


</td></tr><tr><td>

![Upgrade progress screen](../image/phase4-upgrade-progress-checkmark.png)

</td><td>

-   **[Phase 4 - Upgrade and validate the development instance](../task/upgrades-phase-4.md)**

Track the progress of your upgrades with the Upgrade Monitor. For your first non-production instance upgrade \(your development instance\), use the Upgrade Monitor to process the skipped list of records that were not addressed in the upgrade. Then identify your update sets and perform functional testing.


</td></tr><tr><td>

![Upgrade other instances](../image/phase5-recursive-arrow.png)

</td><td>

-   **[Phase 5 - If applicable: Upgrade and validate your other non-production instances, such as your test instance](../task/upgrades-phase-5.md)**

After you've configured and refined your development instance, request to upgrade any other non-production instances you have, such as a test instance. Immediately after the upgrade is complete, apply the post-upgrade changes made to your development instance, including activating optional plugins, installing and upgrading applications, and applying update sets.


</td></tr><tr><td>

![Upgrade checklist](../image/phase2-checklist.png)

</td><td>

-   **[Phase 6 - Prepare to upgrade the production instance](../task/upgrades-phase-6.md)**

After you have configured and refined your test environment to be a good representation of your production environment, prepare to upgrade your production instance.


</td></tr><tr><td>

![Upgrade progress screen](../image/phase4-upgrade-progress-checkmark.png)

</td><td>

-   **[Phase 7 - Upgrade the production instance](../task/upgrades-phase-7.md)**

After you have upgraded your development, non-production, and test instances, upgrade your production instance last. Then validate that the upgrade was complete, apply update sets and fix scripts, and perform post-upgrade user acceptance testing \(UAT\).


</td></tr></tbody>
</table>