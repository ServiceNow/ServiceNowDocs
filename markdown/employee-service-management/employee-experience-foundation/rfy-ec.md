---
title: Recommended for you
description: Recommended for you displays catalog items and knowledge articles, enabling you to view information that is most relevant to you.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Setup Employee Center browse experience features, Configure, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Recommended for you

Recommended for you displays catalog items and knowledge articles, enabling you to view information that is most relevant to you.

## Content recommendations

This widget highlights the most relevant catalog items and knowledge articles for the employee:

-   The **Recommended for you** widget can use an ML algorithm-based on Employee Profile or HR Profile to show popular content accessed by users having similar profile.
-   Recommended items are populated either based on ML or popularity of items based on your license entitlements. Underlying table for calculating similar user is determined by Employee Profile or HR profile.

    **Note:** When you install Employee Profile, the recommendations are populated based on the Employee Profile table.

-   The visual representation of items has a detailed card view with title, description, image, and a simple list view of only titles.
-   Employees can view related articles and catalog items on the portal home page and on ServiceNow mobile page​.
-   By default, the top five recommendations are visible on the widget. The widget provides users with a preview of a knowledge article with the title, description, and other useful information. Similarly, the catalog items show the description and the price of the product, if any.

## Prerequisites

Learn about the version, license, and other requirements to use **Recommended for you**.

-   The widget is available for Employee Center versions 23.0.7 and later.

    **Note:** ML-based recommendations are available only for EC Pro customers or PI entitlement such as HRSD Pro, ITSM Pro, LSD, WSD.

-   Enable Employee Profile first to activate recommendations based on the Employee Profile table. Employee Profile is used to formulate recommendations that have similar profile users. For more information, see [Manage the employee profile AI and ML model](../task/train-employee-profile-model.md)

To make the widget visible on the Employee Center home page:

1.  Verify that an active taxonomy is associated to the Employee Center portal record​.
2.  Verify that you run **Set primary topics for Employee taxonomy** manually after installing the application.
3.  Verify you have articles or catalog item with non-empty **Taxonomy Topic** field​.

For more information, see [Configure the Recommended for you](../task/config-rfy.md)

## How Recommended for you works

Administrators, developers, and advanced users can configure the widget options​. **Recommended for you** highlights the most viewed knowledge article and most requested catalog items across all employees for a time period defined in the [Modify the Recommended for you widget display](../task/config-recommended-for-you.md) by the portal administrator.

-   Knowledge articles recommendations are based on the view count of article.
-   Catalog item recommendations are based on the number of times it is requested for.
-   The recommendations associated to the portal taxonomy are displayed on the home page.

**Note:** The sys property \(enable\_topic\_content\_lang\_fallback\) disables the language fallback for KB articles, feature content in topics, and the Recommended for you widget. When the value is false, content isn't evaluated from the fallback language and only user preference language content is displayed.

**Related topics**  


[View the Recommended for you content](rfy-employee.md)

