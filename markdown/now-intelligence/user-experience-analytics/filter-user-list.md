---
title: Filter data in User Experience Analytics
description: Drill down into usage data with standard and custom filters.
locale: en-US
release: zurich
product: User Experience Analytics
classification: user-experience-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, User Experience Analytics, Platform Analytics]
---

# Filter data in User Experience Analytics

Drill down into usage data with standard and custom filters.

Users with the analytics\_viewer, portal\_analytics\_viewer, mobile\_analytics\_viewer, core\_ui\_analytics\_viewer, now\_experience\_analytics\_viewer roles can filter pages that they have access to.

Most pages in the User Experience Analytics application have visible default filters and an option to add other standard filters. To add additional user-related fields, see [Add user properties as filters to User Experience Analytics](uxa-add-filters-uxa-pages.md).

## Default filters

On each page of User Experience Analytics, there are several default filters for constraining the information on the page. Most pages have filters for date range, user type, and country.

![Default filters for the individual application view in User Experience Analytics](../image/uxa-indiv-app-filters.png)

**Note:** Mobile applications have additional default filters for operating system and version.

The Cross-application overview also has filters for channel, application, and role.

![Default filters for the All Applications view in User Experience Analytics](../image/uxa-cross-app-filters.png)

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

In addition to the default filters on the pages of the  User Experience Analytics application, you can add filters based on user properties. See [Add user properties as filters to User Experience Analytics](uxa-add-filters-uxa-pages.md) for details.

**Parent Topic:**[Using User Experience Analytics](../content-framework/concept/using-uxa.md)

