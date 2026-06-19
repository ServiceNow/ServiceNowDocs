---
title: Configurations
description: Use the configurations page to configure clone instances or create clone profiles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-platform-administration/clone-configurations-tab.html
release: australia
product: AI Platform Administration
classification: ai-platform-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Explore, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Configurations

Use the configurations page to configure clone instances or create clone profiles.

**Before you begin**

-   You can add external email addresses to receive clone notifications.
-   Some default items can't be removed from the exclusions, preservers, or scripts list.

## Configurations overview

The Clone Admin Console provides a unified interface to configure, request, and monitor instance clones across your environments. The overview page displays the current number of clone instances and clone profiles in your instance.

The Configurations tab includes the following key areas:

-   **Overview**: Summary of clone instances and clone profiles
-   **Exclusions**: Manage tables that are not copied during a clone
-   **Preservers**: Protect data on the target instance from being overwritten
-   **Cleanup scripts**: Automate post-clone tasks and adjustments
-   **Clone profiles**: Store predefined clone options for reuse
-   **Clone instances**: View registered instances and their URLs
-   **Multi-Instance View**: Consolidated information across all instances

## Exclusions

Exclusions are tables that are not copied during a clone. Excluding a table results in an empty but usable table on the target instance after the clone. You can view and manage all exclusions from the [Exclusions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/t_ExcludeATableFromCloning.md) page.

## Preservers

Preservers protect data on the target instance from being overwritten. Unpublished custom applications and their data must be manually preserved. You can view and manage all preservers from the [Preservers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/create-new-clone-preserver.md) page.

## Cleanup scripts

Cleanup scripts automatically run on the target instance after the cloning process finishes. Use [cleanup scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/create-cleanup-script.md) to adjust settings, modify data, or automate other post-clone tasks.

## Clone instances

The clone instances page displays all available instances and their URLs which can be used within instance clone. You can use instances added to this list as a clone source or clone target for your clones. To add your non-production instance to your clone instances list, select **New**.

## Multi-Instance View

Multi-Instance View unlocks consolidated information showing clone activity across all instances, last clone timestamps, and enhanced management features. This provides a unified perspective of your cloning operations across your environment.

## Clone profiles

Clone profiles enable you to store predefined clone options, including preservers, exclusions and cleanup scripts. These can then be applied to your clone request depending on your desired outcome. The clone profiles page displays all available profiles. Clone profiles are customizable templates for clones and can be saved and reused to achieve consistent outcomes with each of your clones. To learn more about Clone Profiles, see [Create a custom clone profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/configure-clone-profile.md).

The profile, System Profile is available by default and can't be modified. Custom profiles use the default Exclusions, Preservers, and Scripts from the System Profile. When creating a custom profile, all existing custom exclusions and preservers are automatically added.

You can create as many custom clone profiles as you'd like and edit them as needed. To change the definitions of a clone profile, such as exclusions, preservers or cleanup scripts, select the number under the definition and select the **Edit** button on the page.

