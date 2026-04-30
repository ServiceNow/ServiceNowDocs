---
title: Platform Analytics dashboard overview
description: Platform Analytics dashboards have a shared layout of data, utilities, and controls.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Dashboards in Platform Analytics, Platform Analytics experience, Platform Analytics]
---

# Platform Analytics dashboard overview

Platform Analytics dashboards have a shared layout of data, utilities, and controls.

## Dashboard components

When the dashboard is being viewed, rather than edited, it has the following components.

![Section of a dashboard with each of its components numbered. The explanation of each number is in the list that follows.](../../par-for-workspace/image/inline-db-components.png)

1.  Dashboard title
2.  Refresh information

    Indicates how long ago the dashboard was refreshed. Admins can configure refresh intervals. For more information, see [Configure Platform Analytics dashboard settings](../task/configure-ac-db-settings.md#).

3.  Certification badge.

    Certification indicates that the dashboard is company-approved and recommended for use.

4.  Refresh button

    Select to refresh all of the visualizations on the dashboard.

5.  Details button

    Select to show ownership and sharing information about the dashboard. To learn more, see [Configure Platform Analytics dashboard details](../task/config-db-in-ac.md).

6.  Insights button

    Shows configured insights cards. For more information, see [Proactive analytics insights on dashboards](../../par-for-workspace/concept/proactive-analytics.md).

7.  Edit button

    Enables users who own or who have been given edit rights to edit the content on the dashboard.

8.  More actions button

    Opens menu to create a dashboard, duplicate, share, and print the dashboard, clear the filters, as well as bookmark, and delete the dashboard.

9.  Top stage

    Elements in this section are visible no matter which tab has focus. Filters in this section apply to visualizations on all of the tabs.

10. Tabs

    Tabs help you to manage information on your dashboard and keep related information in the same place.


## Dashboard elements

Dashboards contain a combination of visual elements to show data.

![Untitled dashboard with the Add new element menu expanded to show elements you can add to the dashboard](../../par-for-workspace/image/inline-db-elements.png)

-   **[Data visualization](https://developer.servicenow.com/dev.do#!/reference/now-experience/xanadu/shared-components/sn-par-visualization-base/usage)**

    Data visualizations enable you to present a visual representation of current instance data or temporary data that you’ve imported. Data visualizations include visualizations that you create in the dashboard designer and data visualizations from the library.

    **Important:** You cannot place reports or Performance Analytics widgets on a Platform Analytics dashboard. You must create data visualizations instead.

-   **[Filter](https://developer.servicenow.com/dev.do#!/reference/now-experience/xanadu/now-components/sn-component-filter/usage)**

    Filters enable users to filter the visualizations on a dashboard based on specified criteria. You can put filters either on the individual tabs or above the tabs so that the filter applies to elements every tab. Filters include both data filters and domain filters. You can create filters in the dashboard designer or select them from the library.

-   **[Heading](https://developer.servicenow.com/dev.do#!/reference/now-experience/xanadu/now-components/now-heading/usage)**

    Headings provide a place for text at the top of a dashboard or section of a dashboard. Formatting for headings is limited to six heading levels.

-   **[Image](https://developer.servicenow.com/dev.do#!/reference/now-experience/xanadu/now-components/now-image/uib-config)**

    Image elements hold static or animated images on the dashboard.

-   **[List - Simple](https://developer.servicenow.com/dev.do#!/reference/now-experience/xanadu/shared-components/now-record-list-connected-snapshot/usage)**

    Simple lists show table data that you can customize for the dashboard audience.

-   **Rich text**

    Rich text elements hold text that you can format either as text or as html, including font selection, text size, highlighting, and hyperlinks.


## Default element dimensions

Each element has a default height and width when you place it on the stage to configure. Select and drag an element's handlebar to resize it.

-   **Filter**

    six columns by three rows

-   **List, Multipivot, and Indicator Scorecard visualizations**

    48 columns by 18 rows

-   **All other components**

    11 columns by 11 rows


