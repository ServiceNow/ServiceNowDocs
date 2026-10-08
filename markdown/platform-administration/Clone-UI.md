---
title: Clone Admin Console
description: The Clone Admin Console is the user interface where administrators can manage, request, and monitor their instance clones.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/Clone-UI.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Explore, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Clone Admin Console

The Clone Admin Console is the user interface where administrators can manage, request, and monitor their instance clones.

## Clone Activity

The Clone Activity tab is the default view when you open the Clone Admin Console. This tab displays a table of clone requests sorted by most recent, showing:

-   **CHG** — Change request number
-   **Source Instance** — The instance being cloned from
-   **Target Instance** — The instance being cloned to
-   **State** — Clone status \(WIP, Complete, Error, Canceled, etc.\)
-   **Scheduled Date/Time** — When the clone is scheduled to run
-   **Started** — When the clone began
-   **Completed** — When the clone finished
-   **Duration** — How long the clone took
-   **Profile Name** — The clone profile used

Use the search bar to locate a specific clone. Filter options enable you to locate clones based on their status. To view a list of statuses, see [Clone states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/clone-states.md).

The **Request Clone** button in the upper right allows you to initiate a new clone request.

## Instance Overview

The Instance Overview tab lists all your instances and the date each instance was last cloned. Unlike Clone Activity, which lists every clone request, Instance Overview shows each instance only once, with the last clone date in a column. Use this page to quickly identify stale environments and prioritize refreshes.

## Help

The Help tab provides access to Now Assist for Clone, links to clone-related knowledge base articles, and the installed version of the Clone Admin Console app. Now Assist for Clone is available starting with the Australia Patch 2 release. For more information, see [Clone help resources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/clone-help-resources.md).

## Configuration

The Configuration tab consolidates all clone-related settings in a single menu, including:

-   **Overview** — Summary of clone instances and clone profiles
-   **Exclusions** — Tables not copied during a clone
-   **Preservers** — Data protected from being overwritten on the target instance
-   **Cleanup Scripts** — Automated post-clone tasks
-   **Clone Profiles** — Reusable templates for clone settings
-   **Clone Instances** — Registered instances and their URLs
-   **Multi-Instance View** — Consolidated clone activity across linked instances

For more information, see [Configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/clone-configurations-tab.md).

## Request a clone

The clone request page contains guidance and explanations for how the various clone settings affect your clone. You can use the scheduling calendar to help prevent timing conflicts with ServiceNow maintenance windows.

The **Request Clone** button allows you to initiate a new clone request.

To learn more about how to request a clone see [Request a clone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_StartAClone.md).

