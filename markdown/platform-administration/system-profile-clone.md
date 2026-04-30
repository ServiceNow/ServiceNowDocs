---
title: Clone profiles for clone requests
description: A clone profile enables you to store predefined target and clone options. The clone profile automatically populates your clone request with your selected profile settings.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Request a clone, System clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Clone profiles for clone requests

A clone profile enables you to store predefined target and clone options. The clone profile automatically populates your clone request with your selected profile settings.

## Clone profiles

Navigate to **System Clone** &gt; **Clone Profiles** to view your clone profiles. With a clone profile, you can:

-   Create a profile with specific target instance and option settings, tables to exclude, data to preserve, and cleanup scripts to run
-   Create a clone request directly from the clone profile
-   Apply the clone profile to a clone request

You can create, edit, and delete clone profiles from the **Clone Profile** view. The system profile is a read-only clone profile that you can't delete. It shows a predefined list of table exclusions, data preservers, and cleanup scripts. This list is based on the plugins that your instance contains.

![Clone profile](../image/clone-profile.png)

To set a new clone profile as the default profile used when you request a clone, select the **Make Default** option. Verify that this is the correct clone profile you want to use for the clone scenario you are requesting.

If you create a new data preserver, exclusion, or cleanup script, it is not automatically added to your clone profiles. To add a preserver, exclusion, or cleanup script, open the clone profile, select **Additional actions** &gt; **Configure** &gt; **Form Layout**, and move the new preserver to the selected list.

You are not required to use clone profiles. If you leave the clone profile field empty when scheduling a clone, the system uses the exclude tables, data preservers, and cleanup scripts configured under **System Clone** &gt; **Clone Definition**.

