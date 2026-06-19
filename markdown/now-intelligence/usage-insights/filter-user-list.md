---
title: Filter data in User Experience Analytics
description: Drill down into usage data with standard and custom filters.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/usage-insights/filter-user-list.html
release: zurich
product: Usage Insights
classification: usage-insights
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Usage Insights, Platform Analytics]
---

# Filter data in User Experience Analytics

Drill down into usage data with standard and custom filters.

Users with the analytics\_viewer, portal\_analytics\_viewer, mobile\_analytics\_viewer, core\_ui\_analytics\_viewer, now\_experience\_analytics\_viewer roles can filter pages that they have access to.

Most pages in the Usage Insights application have visible default filters and an option to add other standard filters. To add additional user-related fields, see [Add user properties as filters to Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/usage-insights/uxa-add-filters-uxa-pages.md).

## Default filters

On each page of Usage Insights, there are several default filters for constraining the information on the page. Most pages have filters for date range, user type, and country.

\[Omitted image "uxa-indiv-app-filters.png"\] Alt text: Default filters for the individual application view in User Experience Analytics

**Note:** Mobile applications have additional default filters for operating system and version.

The Cross-application overview also has filters for channel, application, and role.

\[Omitted image "uxa-cross-app-filters.png"\] Alt text: Default filters for the All Applications view in User Experience Analytics

## Additional filters

Select Add filter to choose from available filters configured for the application.

**Note:** Additional filters are joined to the selected default filters with the AND condition, meaning that both filter conditions must be true for the filter to apply. For example, select **User type**=`Returning` and **Additional filter**=`Password needs reset`. If no returning users need to reset their passwords, all of the visualizations on the page will be empty because both conditions must apply.

The available additional filters are:

-   Password needs reset
-   Role
-   Enable multifactor authentication
-   Active
-   Department
-   VIP

In addition to the default filters on the pages of the  Usage Insights application, you can add filters based on user properties. See [Add user properties as filters to Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/usage-insights/uxa-add-filters-uxa-pages.md) for details.

**Parent Topic:**[Using Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/usage-insights/using-uxa.md)

