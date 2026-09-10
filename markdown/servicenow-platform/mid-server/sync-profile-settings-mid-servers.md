---
title: Sync profile settings to MID Servers
description: Push the profile settings to the MID Server instances assigned to the profile.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/mid-server/sync-profile-settings-mid-servers.html
release: australia
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2026-07-27"
reading_time_minutes: 1
keywords: [sync MID Server profile, MID Server profile settings, sync profile]
breadcrumb: [Configure MID Servers using profiles, MID Server profiles, Configuring MID Servers, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Sync profile settings to MID Servers

Push the profile settings to the MID Server instances assigned to the profile.

## Before you begin

Role required: agent\_admin

The host machine must have at least 2 GB of system memory in addition to the configured JVM maximum.

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Profiles and Deployments** &gt; **MID Server Profiles**.

    Alternatively, in the navigation filter, enter `mid_server_profile.list`.

2.  Select the profile record to sync.

3.  In the **Related Links** section, select **Sync to MID Servers**.

    The **Sync Profile Settings to MID Servers** dialog opens. \[Omitted image "sync-profile-to-mid-servers-dialog.png"\] Alt text: Sync Profile Settings to MID Servers dialog showing sync strategy options

4.  In the **Select a sync strategy** list, select a sync strategy.

5.  To include wrapper-override settings in the sync, select the **Sync wrapper-override settings to MID Server \(Restart is needed to apply changes\)** check box.

    To restart the MID Server automatically after the sync, select the **Do you want to Auto restart MID Server after sync?** check box that appears.

6.  Select **Sync Profile**.

    The profile settings are synced to the assigned MID Server instances.

7.  Verify the sync by comparing the settings stored on the MID Server instances with the settings on the profile.

    1.  In the **Related Links** section, select **Compare with MID Servers**.

        The **Compare MID Servers With Profile** dialog opens. \[Omitted image "compare-mid-server-with-profile-dialog.png"\] Alt text: Compare MID Servers With Profile dialog showing attached MID Server details and validation results

    2.  Review the attached MID Server details and validation results in the **Details of MID Servers with Mismatch** section.


