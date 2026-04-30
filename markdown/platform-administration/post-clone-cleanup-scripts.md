---
title: Post-clone cleanup scripts
description: Cleanup scripts automatically run on the target instance after the cloning process finishes.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [System clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Post-clone cleanup scripts

Cleanup scripts automatically run on the target instance after the cloning process finishes.

Use cleanup scripts to modify or remove bad data. Cleanup scripts run after data preservers and the clone are complete.

You can add new post-cloning scripts on the source instance to perform any action that can normally be accomplished through script includes or business rules. To add a script, navigate to **System Clone** &gt; **Clone Definition** &gt; **Cleanup Scripts** and click **New**.

**Note:** Cleanup scripts will always run on clones created using a Clone profile, this is necessary as they're available OOB and ensure a healthy state post clone. After the clone completes, all cleanup scripts are combined together as a scheduled job named **Execute Clone Cleanup Script: Execute Cleanup Scripts Sequentially** and run till completion in the global scope. The cleanup scripts are ordered based on the order field. Cleanup scripts must be defined on the **Source** instance.

You can make post-clone scripts active or inactive to control whether these scripts run or do not run. You can also set an order number on each script, which enables you to set the order that the active scripts run, with lower numbers having a higher priority.

![Cleanup script active order](../image/clone-cleanup-active-order.png)

**Note:** All cleanup scripts run in the global scope irrespective of the scope in which you have configured the cleanup script. An example of how to run a scoped script is to

-   Create a script include in the desired scope with the cleanup logic in it.
-   Have a Restricted Caller Access configuration in place to allow access to your scoped script, be sure you are in the scope of the script include used to create the RCA.

    |Field|Description|
    |-----|-----------|
    |Source Scope|Global|
    |Source Type|Scope|
    |Status|Allowed|
    |Target Scope|The scope of the script include.|
    |Target Type|Script Include|
    |Target|The script.|
    |Operation|Execute API|

-   Call the script include from the clone cleanup script.

The following post-clone cleanup scripts perform various actions on the target instance.

|Script|Description|
|------|-----------|
|Bad MID Server credentials after clone|Runs a script include called BadMIDCredentialAfterClone on a cloned instance to detect [bad MID Server user credentials](https://www.servicenow.com/docs/access?context=mid-post-clone-issue-resolution&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US). This script include creates scheduled jobs that log MID Servers in the **Down** state to the MID Server Issue \[ecc\_agent\_issue\] table after an instance clone.|
|Clear scheduled job node association|Resets any scheduled jobs that were active on the source instance to the **Ready** state. This script also clears the value of the **System ID** and **Claimed by** fields on all scheduled jobs.|
|Configure Email Accounts|Migrates email accounts that existed on the source instance to the target instance if they are not enabled there. This script also migrates the email properties to the target instance.|
|Disable emails|Disables email on the target instance. A default data preserver maintains other email settings from the target instance.|
|Install deactivated plugin|Enables the Domain Separation plugin for instances that use this feature.|
|Regenerate all text indexes|Rebuilds text indexes on the target instance after a clone. Text indexes are not cloned from the source to the target instance.|
|Schedule drop backup tables|Schedules the deletion of the data that is contained in the target instance database prior to the clone. This original data is preserved for 24 hours following a clone to enable you to roll back an instance to the pre-clone state. If the target instance is downgraded as part of the clone, backup data is not available.|

