---
title: Upgrade Preview module
description: The Upgrade Preview module enables you to have an unprecedented insight to an instance prior to an actual upgrade. You can explore and preview upgrades to different ServiceNow release versions and see how your instance might be impacted with your current configurations. The Upgrade Preview utility helps you to plan, schedule, and prepare for an upgrade.
locale: en-US
release: xanadu
product: Upgrade Center
classification: upgrade-center
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Exploring Upgrade Center, Upgrade Center, Upgrade, Administer the ServiceNow AI Platform]
---

# Upgrade Preview module

The Upgrade Preview module enables you to have an unprecedented insight to an instance prior to an actual upgrade. You can explore and preview upgrades to different ServiceNow release versions and see how your instance might be impacted with your current configurations. The Upgrade Preview utility helps you to plan, schedule, and prepare for an upgrade.

![Image showing the preview screen](../image/uc-preview-screen.png)

**Note:** Depending on the eligibility of your instance, the list of available target versions for preview varies. Only versions that are allowed for a particular instance to be upgraded to, show up on the list. If your instance is not eligible to be upgraded to any version, the drop-down menu is empty.

The following cards show up with more information.

<table id="table_tht_fp2_clb"><thead><tr><th>

Card names

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Current version

</td><td>

Name of the current version.-   Upgraded on: Date on which the instance got upgraded to the current version
-   End of life: Link to KB0610454 for more information about end of life

</td></tr><tr><td>

Previewing version

</td><td>

Information about the previewing version shows up. If you haven't previewed any version, you are expected to select a version for preview and click **Go**. If you have already previewed a version, the following information shows up.-   Preview created: Date on which the preview was created
-   View preview details: Link to the Upgrade Preview form

 **Note:** Click **Refresh preview** if you want to regenerate a new preview of the same target version. Although clicking **Refresh preview** regenerates the skipped list, the reverted records won't get skipped. If you have reviewed and retained some records, they get replaced as soon as you click **Refresh preview**.

</td></tr><tr><td>

Scheduled upgrade

</td><td>

Name of the next upgrade that has been scheduled to start. If there is no currently scheduled upgrade, the card shows No upgrade scheduled.**Note:** This card can have different messages depending on the schedule of the upgrade.

 If there is an upgrade scheduled, the following information shows up.

 -   Estimated upgrade duration: Estimated duration needed to complete the scheduled upgrade

**Note:** If this is your first upgrade, there will be no information about estimated upgrade duration.

-   Next scheduled upgrade: Date and time on which the next upgrade has been scheduled to start.

</td></tr><tr><td>

Find out what's new and changed

</td><td>

Links to view the new and changed features in the current upgrade version. The following three links show up when you click **Go** to preview the upgrade version.-   Problem fixes: Fixes that have been made since the last upgrade version
-   Personalized release notes: Release notes summary for the previewed version
-   Known error articles: Errors that have been identified but not yet resolved

 **Note:** These links don't show up if you haven't previewed any upgrades.

</td></tr><tr><td>

Skipped list prediction**Note:** If you are using Upgrade Plan, the card name changes to Skipped list prediction with plans.

</td><td>

Information about the predicted skipped records. See [Preview predicted changes](../reference/uc-previewed-changes.md) for more details.-   Total record changes: Total number of records that are predicted to change when the upgrade occurs. Total record changes also include possible predicted skipped files known as Predicted skipped records.

Review changes: Link to the list of records that have changed and can be reviewed

-   Predicted skipped records: Total number of records that have been predicted to be skipped.

    -   Total: Total predicted skipped records
    -   To review: Predicted skipped records to be reviewed
    -   Reviewed: Predicted skipped records that have been reviewed
    -   Resolved: Predicted skipped records that have been resolved by implementing the rules

**Note:** This entry shows up on the card only when rules are executed on the skipped records. You will also see a link to create a skipped record rule if either there are no existing rules or the existing rules aren't executed.

**Note:** Skipped record rules and upgrade plans can't be implemented together. See [Execute a skipped record rule automatically](../task/uc-execute-skipped-record-rule.md#) for more information.

-   Predicted skipped records by priority: Pie chart to represent the predicted skipped records by priority.

**Note:** Click the pie chart to see the list of predicted skipped records.

ServiceNow prioritizes the skipped records based on the importance of the file types. The prioritization is done as follows:

    -   Priority 1 \(highest priority\): UI pages, UI macros, and more
    -   Priority 2: Business Rules, Security ACLs, and more
    -   Priority 3: Reports and more
    -   Priority 4: Form Sections, Choice Sets, and more
    -   Priority 5 \(lowest priority\): everything else

</td></tr><tr><td>

Predicted skipped records by product

</td><td>

Records that have been predicted to be skipped and are sorted as per their product families.![](../image/uc-skipped_records_product.png)

 **Note:** The products sorted under the Other category don't have any specific product family.

</td></tr><tr><td>

Automated Test Framework \(ATF\) results

</td><td>

Percentage of passing ATF tests that ran in the last 30 days.-   Most recent ATF run: Date and time on which the recent ATF tests ran
-   View ATF results: Link to show more information about the recent ATF results

 **Note:** Only the tests which are finished and have passed are considered for the ATF results. If one test runs more than once, only the recent execution is considered in the results.

</td></tr></tbody>
</table>