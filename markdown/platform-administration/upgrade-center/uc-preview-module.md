---
title: Upgrade Preview module
description: The Upgrade Preview module enables you to have an unprecedented insight to an instance prior to an actual upgrade. You can explore and preview upgrades to different ServiceNow release versions and see how your instance might be impacted with your current configurations. The Upgrade Preview utility helps you to plan, schedule, and prepare for an upgrade.
locale: en-US
release: yokohama
product: Upgrade Center
classification: upgrade-center
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Exploring Upgrade Center, Upgrade Center, Upgrade, Administer the ServiceNow AI Platform]
---

# Upgrade Preview module

The Upgrade Preview module enables you to have an unprecedented insight to an instance prior to an actual upgrade. You can explore and preview upgrades to different ServiceNow release versions and see how your instance might be impacted with your current configurations. The Upgrade Preview utility helps you to plan, schedule, and prepare for an upgrade.

The preview status info and link in the message displayed on top of the Upgrade Preview page states the current status of the ongoing preview process. Because you can get an accurate prediction on the new and existing applications and their skipped records, the preview execution time has increased considerably. Select the link in the message to see the status of the preview process.

![Image showing the status message and link](../image/uc-status-message-link.png)

The Execution Tracker record displays when you select the progress link in the message. Select Show status related list to show the current status of the executed preview process.

![Image showing the preview screen](../image/uc-preview-screen.png)

**Note:** Depending on the eligibility of your instance, the list of available target versions for preview varies. Only versions that are allowed for a particular instance to be upgraded to, show up on the list. If your instance is not eligible to be upgraded to any version, the drop-down menu is empty.

The following cards display with more information.

<table id="table_tht_fp2_clb"><thead><tr><th>

Card names

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Current version

</td><td>

Name of the current version.-   Upgraded on: Date on which the instance got upgraded to the current version
-   End of life: Link to [KB0610454](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0610454) for more information about end of life

</td></tr><tr><td>

Previewing version

</td><td>

Information about the previewing version displays. If you haven't previewed any version, you are expected to select a version for preview and select **Go**. If you have already previewed a version, the following information displays.-   Preview created: Date on which the preview was created
-   View preview details: Link to the Upgrade Preview form

 **Note:** Select **Refresh preview** if you want to regenerate a new preview of the same target version. Although selecting **Refresh preview** regenerates the skipped list, the reverted records won't get skipped. If you have reviewed and retained some records, they get replaced as soon as you select **Refresh preview**.

</td></tr><tr><td>

Scheduled upgrade

</td><td>

Name of the next upgrade that has been scheduled to start. If there is no currently scheduled upgrade, the card shows No upgrade scheduled.**Note:** This card can have different messages depending on the schedule of the upgrade.

 If there is an upgrade scheduled, the following information displays.

 -   Estimated upgrade duration: Estimated duration needed to complete the scheduled upgrade.

**Note:** If this is your first upgrade, there will be no information about estimated upgrade duration.

-   Next scheduled upgrade: Date and time on which the next upgrade has been scheduled to start.

</td></tr><tr><td>

Find out what's new and changed

</td><td>

Links to view the new and changed features in the current upgrade version. The following three links show up when you select **Go** to preview the upgrade version.-   Problem fixes: Fixes that have been made since the last upgrade version
-   Personalized release notes: Release notes summary for the previewed version
-   Known error articles: Errors that have been identified but not yet resolved

 **Note:** These links don't show up if you haven't previewed any upgrades.

</td></tr><tr><td>

Skipped list prediction**Note:** If you are using Upgrade Plan, the card name changes to Skipped list prediction with plans.

</td><td>

Information about the predicted skipped records. See [Preview predicted changes](../reference/uc-previewed-changes.md) for more details.-   Total record changes: Total number of records that are predicted to change when the upgrade occurs. Total record changes also include possible predicted skipped files known as Predicted skipped records.

Review changes: Link to the list of records that have changed and can be reviewed.

-   Predicted skipped records: Total number of records that have been predicted to be skipped.

    -   Total: Total predicted skipped records
    -   To review: Predicted skipped records to be reviewed
    -   Reviewed: Predicted skipped records that have been reviewed
    -   Resolved: Predicted skipped records that have been resolved by implementing the rules

**Note:** This entry shows up on the card only when rules are executed on the skipped records. You will also see a link to create a skipped record rule if either there are no existing rules or the existing rules aren't executed.

**Note:** Skipped record rules and upgrade plans can't be implemented together. See [Execute a skipped record rule automatically](../task/uc-execute-skipped-record-rule.md#) for more information.

-   Predicted skipped records by priority: Pie chart to represent the predicted skipped records by priority.

**Note:** Select the pie chart to see the list of predicted skipped records.

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

Application Upgrade Preview

</td><td>

Accurate prediction on the installs and upgrades for new and existing applications and for their specific skipped records. It states the total number of applications that have been either upgraded or installed.**Note:** The skipped records prediction is reflected on the Predicted skipped records by product card.

![Image showing Application Upgrade Preview card](../image/uc-upgrade-preview-apps.png)

By default, 10 applications preview details show up. Select View all applications preview details link to view the entire list. It states the name of the application and the following information:

-   Action: The action taken on the specific application. It can either be upgraded for the existing applications or installed for the new applications.
-   From version: States the previous version of the upgraded application \(existing application\).

**Note:** This field is empty if the application is a newly installed application.

-   To version: States the current version to which the existing application has been upgraded.

**Note:** This field shows the current version of the newly installed application.


</td></tr><tr><td>

Predicted Schema Changes

</td><td>

Prediction about the kind of changes in the database based on the upgrade on your instance.![Image showing the Predicted Schema Changes list](../image/uc-predicted-schema.png)

By default, 10 predicted schema changes show up. Select View all predicted schema changes link to view the entire list. Changes like new columns, new tables, and new indexes are captured in this section.

</td></tr><tr><td>

Automated Test Framework \(ATF\) results

</td><td>

Percentage of passing ATF tests that ran in the last 30 days.-   Most recent ATF run: Date and time on which the recent ATF tests ran
-   View ATF results: Link to show more information about the recent ATF results

 **Note:** Only the tests which are finished and have passed are considered for the ATF results. If one test runs more than once, only the recent execution is considered in the results.

</td></tr></tbody>
</table>