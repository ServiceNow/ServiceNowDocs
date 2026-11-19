---
title: Clone Admin Console
description: The Clone Admin Console is the user interface where administrators can manage, request, and monitor their instance clones.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/Clone-UI.html
release: zurich
topic_type: concept
last_updated: "2025-09-12"
reading_time_minutes: 2
breadcrumb: [Explore, Instance Clone, Configure core features, Administer]
---

# Clone Admin Console

The Clone Admin Console is the user interface where administrators can manage, request, and monitor their instance clones.

## Clone Home

The home page displays the current clones in your instance. Use the search bar to locate your clone.

Filter options enable you to locate a clone based on its status. To view a list of statuses, see [Clone states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/clone-states.md).

**Note:** The clone home page displays clones requested through the Clone Admin Console. You can't view clones requested through the legacy request page `(clone_instance.do)` in the dashboard. To view legacy clones in either a grid or list view, navigate to **All** &gt; **Instance Clone** &gt; **Live Clones** &gt; **Clone History**.

\[Omitted image "cac-dashboard.png"\] Alt text: clone home dashboard.

## Configurations

The configurations tab displays an overview and information about clone instances and clone profiles. See [Configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/clone-configurations-tab.md) for more information.

## Definitions

The definitions tab displays an overview for exclusions, preservers, and cleanup scripts. See [Definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/clone-exclusions-preservers-cleanupscripts.md) for more information.

## Request clone

The clone request page contains guidance and explanations for how the various clone settings affect your clone. You can use the scheduling calendar to help to prevent timing conflicts with ServiceNow maintenance windows. To learn more about how to request a clone see [Request a clone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/t_StartAClone.md).

## Deprecated Clone Options

The clone option check box **Preserve users and related tables** was removed from the [Clone options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/clone-options.md) in the Utah release. In some cases, past customizations to the clone request page or related to clone, may cause this field to remain on your form.

**Important:** Selecting this deprecated field doesn't effect the user, role, or related tables during your clone.

**Note:** Beginning with the Australia release, users attempting to access the legacy Instance Clone page, **clone\_instance.do**, are redirected instead to the [Clone Admin Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/Clone-UI.md). To view clone history for clones prior to the Australia release, view the legacy Clone History \[clone\_instance\] table.

For more information about using Clone Admin Console instead of the legacy Instance Clone, see [KB1425858: Clone Admin Console: Quick Start Guide &amp; Instructions](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1425858).

