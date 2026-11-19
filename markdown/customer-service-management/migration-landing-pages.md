---
title: Migrate landing pages
description: CSM Agent Workspace landing pages can't be imported into CSM Configurable Workspace. Rebuild each landing page using the full UI Builder.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/migration-landing-pages.html
release: australia
topic_type: task
last_updated: "2026-10-25"
reading_time_minutes: 2
breadcrumb: [Migrate to CSM Configurable Workspace, Migrating to CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Migrate landing pages

CSM Agent Workspace landing pages can't be imported into CSM Configurable Workspace. Rebuild each landing page using the full UI Builder.

## Before you begin

Role required: admin

-   Map out the layout you want before you open UI Builder. Decide which visualizations, lists, and KPIs belong on the page for each agent group.
-   Design the page so that it makes sense to the logged-in agent, which encourages adoption. Include the key metrics and condensed data that agents want to check regularly.
-   If you have different agent groups, plan page variants. Each variant can be restricted to a specific role or audience.

## About this task

The landing page is the first page agents see when they open the workspace. CSM Configurable Workspace supports a richer landing page with real-time SLA gauges, case throughput metrics, team performance indicators, and layouts tailored to each agent group.

Follow these performance guidelines when you design the page:

-   Retrieve data in the context of an agent or their team, such as My active cases or My team's cases. Don't retrieve all records.
-   Apply date range filters when you retrieve data. For example, show cases created in the last month.
-   Apply query filters on fields that are optimized for search, and index fields that are used frequently in queries on large tables.
-   Include only the visualizations that agents use multiple times a day.
-   Don't add more than 15 visualization components to a single landing page.

## Procedure

1.  Review your existing landing pages.

    1.  Navigate to **All** &gt; **Workspace Experience** &gt; **Administration** &gt; **All Workspaces**.

    2.  Open the CSM Agent Workspace record and go to the **Landing Pages** related list.

    3.  Note the components, agent groups, and reports on each page.

2.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**. On the **Experiences** tab, select **CSM/FSM Configurable Workspace**.

3.  From the **Page** list, select **Landing Page**, and then select the **CSM Landing Page** variant.

4.  Open the additional actions menu next to the variant and select **Duplicate variant**.

    **Note:** Always duplicate the CSM Landing Page variant instead of editing it directly. Editing the base system variant can cause issues during upgrades.

5.  Enter a name for the variant and select **Create**.

6.  Optional: Specify the audience and display conditions for the new page variant.

7.  Add and arrange components from the component library in the left pane.

8.  Select **Save**.


## Result

The new variant appears in the Landing Page section in UI Builder. The **Order** field and the audiences on each page determine which landing page appears for each persona. The landing page with the lowest order number appears first.

## What to do next

For more information about landing page configuration, see [Create a CSM Configurable Workspace landing page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/config-csm-config-ws-landing-page.md).

