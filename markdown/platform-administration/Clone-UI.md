---
title: Clone Admin Console
description: The Clone Admin Console is the user interface where administrators can manage, request, and monitor their instance clones.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/Clone-UI.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
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

Use the search bar to locate a specific clone. Filter options enable you to locate clones based on their status. To view a list of statuses, see [Clone states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/clone-states.md).

The **Request Clone** button in the upper right allows you to initiate a new clone request.

## Instance Overview

The Instance Overview tab provides a high-level view of your clone environment and instance relationships. This page displays last-cloned timestamps for each instance, enabling you to quickly identify stale environments and prioritize update activities.

## Help

The Help tab provides access to Now Assist for Clone and curated clone help articles.

**Now Assist for Clone**

Now Assist for Clone allows you to ask clone questions in natural language and receive answers based on clone documentation and knowledge base articles. This AI-powered agent is available within the Clone Admin Console if you have a Now Assist license.

**Requirements**

-   Now Assist license activated on your instance
-   Australia Patch 5 or later

**Access Now Assist for Clone**

If you have an active Now Assist license, the Now Assist icon appears in the top navigation of the Clone Admin Console. Select the icon to open the Now Assist panel and ask clone-related questions.

**Important:** If you purchase a Now Assist license after initially installing the Clone Admin Console, you must reinstall the Clone application from the store to enable the Clone FAQ Agent skill. This is a one-time step that loads the clone-specific skill into Now Assist.

## Configuration

The Configuration tab consolidates all clone-related settings in a single menu, including:

-   **Overview** — Summary of clone instances and clone profiles
-   **Exclusions** — Tables not copied during a clone
-   **Preservers** — Data protected from being overwritten on the target instance
-   **Cleanup Scripts** — Automated post-clone tasks
-   **Clone Profiles** — Reusable templates for clone settings
-   **Clone Instances** — Registered instances and their URLs
-   **Multi-Instance View** — Consolidated clone activity across linked instances

For more information, see [Configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/clone-configurations-tab.md).

## Request a clone

The clone request page contains guidance and explanations for how the various clone settings affect your clone. You can use the scheduling calendar to help prevent timing conflicts with ServiceNow maintenance windows.

The **Request Clone** button allows you to initiate a new clone request.

To learn more about how to request a clone see [Request a clone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_StartAClone.md).

