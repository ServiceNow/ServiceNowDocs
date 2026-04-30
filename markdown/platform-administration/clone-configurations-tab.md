---
title: Configurations
description: Use the configurations page to add clone instances or create clone profiles.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-09-24"
reading_time_minutes: 1
breadcrumb: [Explore, Instance Clone, Configure core features, Administer]
---

# Configurations

Use the configurations page to add clone instances or create clone profiles.

**Before you begin**

-   You can add external email addresses to receive clone notifications.
-   Some default items can't be removed from the exclusions, preservers, or scripts list.

## Configurations overview

The overview page displays the current number of clone instances and clone profiles in your instance.

## Clone instances

The clone instances page displays all available instances. You can use instances added to this list as a clone source or clone target for your clones. To add your non-production instance to your clone instances list, select **New**.

## Clone profiles

Clone profiles display all available profiles. Clone profiles are customizable templates for clones and can be saved and reused to achieve consistent outcomes with each of your clones. To learn more about Clone Profiles, see [Create a custom clone profile](../task/configure-clone-profile.md).

The profile System Profile is available by default and can't be modified. Custom profiles use the default Exclusions, Preservers, and Scripts from the System Profile. When creating a custom profile, all existing custom exclusions and preservers are automatically added.

You can create as many custom clone profiles as you'd like and edit them as needed. To change the definitions of a clone profile, such as exclusions, preservers or cleanup scripts, select the number under the definition and select the **Edit** button on the page.

