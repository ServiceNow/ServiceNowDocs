---
title: Configure MID Servers using profiles
description: Use MID Server profiles to configure settings and assign MID Server instances directly from your ServiceNow instance, without accessing host servers or editing configuration files manually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/mid-server/configure-mid-server-profile.html
release: zurich
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2026-07-27"
reading_time_minutes: 1
keywords: [MID Server profiles, configure MID Server, assign MID Server profile]
breadcrumb: [MID Server profiles, Configuring MID Servers, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Configure MID Servers using profiles

Use MID Server profiles to configure settings and assign MID Server instances directly from your ServiceNow instance, without accessing host servers or editing configuration files manually.

## Before you begin

Role required: agent\_admin

You can configure the MID Servers using a profile in two ways:

-   Using the **MID Servers** tab:

    1.  On the MID Server profile record, select the **MID Servers** tab, and then select **Edit**.

        The **Edit Members** screen lists the available MID Server instances in the **Collection** list and the currently assigned instances in the **MID Servers List**.

        \[Omitted image "attach-midservers-to-profile.png"\] Alt text: Edit Members screen showing available MID Server instances and the MID Servers List.

    2.  In the **Collection** list, select the MID Server instances to assign.

        **Tip:** To select more than one instance, hold Ctrl \(Windows\) or Command \(Mac\) and select each name.

    3.  Select the add \(&gt;\) icon to move the selected instances to the MID Servers List.
    4.  Select **Save**.
-   From the MID Server record:

    1.  Open the MID Server record you want to assign to a profile.
    2.  In the **Profile ID** field, select the lookup icon.

        The **MID Server Profiles** dialog opens and displays the available profiles.

    3.  Select the profile to assign to the MID Server.
    4.  Save the MID Server record.

        The MID Server is assigned to the selected profile. Because the profile settings are not yet applied to the MID Server, the following message appears: **Profile is not synced to newly added MID\(s\). Use the Sync to MID Servers UI action in Profile.**


## What to do next

Apply the profile settings to the MID Server instances. See [Sync profile settings to MID Servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/sync-profile-settings-mid-servers.md).

