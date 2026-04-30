---
title: Clone Admin Console
description: The Clone Admin Console provides a streamlined experience and enhanced visibility for cloning data between instances. You’ll find your existing clone profiles, exclusions, preservers, and scripts within the new console. It has added guidance on the clone request page, an on-demand backup option, and provides more visibility into clone progress.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-03-25"
reading_time_minutes: 6
breadcrumb: [System clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Clone Admin Console

The Clone Admin Console provides a streamlined experience and enhanced visibility for cloning data between instances. You’ll find your existing clone profiles, exclusions, preservers, and scripts within the new console. It has added guidance on the clone request page, an on-demand backup option, and provides more visibility into clone progress.

Clone Admin Console overview video 

## Cloning

Clone copies data and metadata from one ServiceNow instance \(source instance\) to another ServiceNow instance \(target instance\). Cloning is typically used to copy the data and metadata from a production instance to a non-production instance to test changes. Cloning data comes from the most recent, daily backup. To learn more about clone, see [System clone](c_SystemClone.md).

## Notes regarding the Clone Admin Console

1.  Legacy clones and new clones are stored separately. Clones requested via the Clone Admin Console are stored on a new table and displayed within the new console.  Legacy clones aren’t shown in the console. Clones initiated via the legacy Request Clone page are stored on the legacy Clone History table.
2.  Since requests submitted from the clone admin console are stored in a separate table, request numbers in this new table may coincide with request numbers in the legacy table \(clone history\).
3.  Your existing clone settings and configurations remain the same. You can find your existing clone instances, clone profiles, exclusions, preservers, cleanup scripts within both the new Clone Admin Console, and within their original lists and forms.
4.  Access and clone-related permissions: The Clone Admin Console requires the clone admin or the admin role on the source and the admin role on the target instance to place a clone request.
5.  The new experience uses the same clone engine as the legacy clone.  Known \(backend\) clone behavior is the same between the legacy and the new user interface. 

## Overview of the Clone Admin Console

The following sections reflect the different parts of the Clone Admin Console.

## Home

The home page displays all current clones in your instance. You can search for your clones by using the **search bar** and entering in the number for your clone.

**Note:** The dashboard shows any clones requested through the app. You can't view clones requested through the Now Platform in the dashboard.

Filter options are available to identify the clones you want to view with the filter drop-down button. You can apply the following conditions to be displayed on your dashboard:

-   Canceled
-   Completed
-   Error
-   Requested
-   Rollback failure
-   Rollback requested
-   Rolled back
-   Rolling back
-   Running

You can choose to view your clones in either a grid or list view by selecting the appropriate button option.

## Configurations

The **Overview** tab displays the current number of **Clone instances** and **Clone profiles** in your instance.

On the **Clone instances** tab, you can view all currently available clone instances. Once you add an instance to this list, you can use it as a clone source or clone target for your clones. To add your non-production instance to your clone instances list, select **New**.

The **Clone profiles** tab displays all of your available **Clone profiles**. You can think of clone profiles as templates for clone, which you can customize, save and reuse to achieve consistent outcomes with each of your clones. To learn more about Clone Profiles see [Clone profiles for clone requests](../reference/system-profile-clone.md).

**Note:** The profile **System Profile** is available out-of-the-box and can't be modified.

Custom profiles you create use the default Exclusions, Preservers, and Scripts from the System Profile as a basis.

**Note:** When you’re creating a custom profile, all existing custom exclusions and preservers are automatically added to it.

You can create as many custom clone profiles as you'd like and edit them as needed. To change the definitions of a clone profile, such as exclusions, preservers or cleanup scripts, select the number under the definition and select the **Edit** button on the page.

**Note:** Certain out-of-the-box system items can't be removed from the exclusions, preservers, or scripts list.

## Definitions

The **Definitions** page displays an overview for the following clone definitions.

-   **Exclusions**
-   **Preservers**
-   **Cleanup Scripts**

The **Exclusions** tab lists the tables that aren’t copied during a system clone. By default, the system excludes tables for logging, auditing, notifications, workflow contexts, and license usage. You can add **Exclusions** by selecting New and adding the table you want to exclude.

The **Preservers** tab displays a list of all of your available data preservers. **Preservers** protect data on the target instance from being overwritten. Preserving data in a table only preserves the specified table and parent tables.

**Note:** Child tables must be individually preserved.

To create a preserver see [Create new clone preserver](../task/create-new-clone-preserver.md).

Importance of saving your in-flight dev work. During a clone, in-progress development work is over-written \(for example work-in-progress update sets, scoped apps which only exist on the target instance but not on the source instance\). If you have in-progress update sets, you must export them prior to the clone and reimport them after the clone is finished. If you have custom applications which are not yet deployed to production, you must install the respective plugins or apps after the clone is completed. To learn more about clone and app development best practices, see Whitepaper [here](https://learning.servicenow.com/nowcreate/en?id=nc_asset&asset_id=ce3c254697cc82d06eedb30e6253af3b&nc_source=copy_asset_link).

Tip for dealing with large quantities of in-progress updates sets:

1.  On your target instance, which has the work in progress \(WIP\) update sets, filter to obtain a list view with all your WIP update sets.
2.  In a separate window/tab, create a new update set.
3.  Batch all incomplete update sets from step 1 - i.e. set the parent field on your list of WIP update sets to the new batch update set
    -   How to mass-update: You can mass-update the list by holding down the shift key + holding a left click of your mouse while you’re selecting the whole column with your mouse.
    -   Double click on any one of the fields in the selected column – type the desired value and update all of them to that value.\)
4.  Set the parent update set to "Completed" and name it "CLNREQ\_DATE" \(naming suggestion to make it easier to identify\).
5.  Export the parent update set.
6.  Back on your source instance, retrieve the update set \(Important: Don’t commit!\) The parent update set is now added to the retrieved update sets on your source instance.
7.  Verify you wait 24 h until your updates set is captured by the daily backup \(alternatively, you can select an on-demand backup on the clone admin console.\)
8.  Perform the clone as usual from your source instance &gt; target instance.
9.  Because your parent update set has been retrieved in the backup, your target instance will have your parent update set along with your dev work which is in flight after the clone.
10. Back on your target instance, you can set the parent update set back to work in progress, and unparent it.
11. On the source instance: Retrieved parent update set can now be cleaned up \(i.e. deleted\).

The **Cleanup scripts** tab displays a list of all of your available scripts. You can write cleanup scripts to automate post-clone steps. To create a cleanup script see [Create cleanup scripts](../task/create-cleanup-script.md).

## Request clone

The app features a clone request page, with guidance and explanations for how the various clone settings affect your clone. The new request page also features a new scheduling calendar to help to prevent timing conflicts with ServiceNow maintenance windows.

To learn more about how to request a clone see [Request a clone in the Clone Admin Console](../task/clone-ui-request-clone.md).

