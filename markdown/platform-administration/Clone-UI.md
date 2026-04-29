---
title: Clone Admin Console
description: The Clone Admin Console is the user interface where administrators can manage, request, and monitor their instance clones.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Clone Admin Console

The Clone Admin Console is the user interface where administrators can manage, request, and monitor their instance clones.

## Clone Home

The home page displays the current clones in your instance. Use the search bar to locate your clone.

Filter options enable you to locate a clone based on its status. To view a list of statuses, see [Clone states](../reference/clone-states.md).

**Note:** Beginning with the Australia release, users attempting to access the legacy Instance Clone page, **clone\_instance.do**, are redirected instead to the [Clone Admin Console](Clone-UI.md#). To view clone history for clones prior to the Australia release, view the legacy Clone History \[clone\_instance\] table.

For more information about using Clone Admin Console instead of the legacy Instance Clone, see [KB1425858: Clone Admin Console: Quick Start Guide &amp; Instructions](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1425858).

![clone home dashboard.](../image/cac-dashboard.png)

## Configurations

The configurations tab displays an overview and information about clone instances and clone profiles. See [Configurations](clone-configurations-tab.md) for more information.

## Definitions

The definitions tab displays an overview for exclusions, preservers, and cleanup scripts. See [Definitions](clone-exclusions-preservers-cleanupscripts.md) for more information.

## Request clone

The clone request page contains guidance and explanations for how the various clone settings affect your clone. You can use the scheduling calendar to help to prevent timing conflicts with ServiceNow maintenance windows. To learn more about how to request a clone see [Request a clone](../task/t_StartAClone.md#).

