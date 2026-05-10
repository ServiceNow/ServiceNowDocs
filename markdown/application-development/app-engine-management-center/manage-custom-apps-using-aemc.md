---
title: Managing custom apps using AEMC
description: Review custom app metrics and manage apps through the development life cycle using the App Engine Management Center \(AEMC\).
locale: en-US
release: australia
product: App Engine Management Center
classification: app-engine-management-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manage app development, Use, App Engine Management Center, Governing app development, Building applications]
---

# Managing custom apps using AEMC

Review custom app metrics and manage apps through the development life cycle using the App Engine Management Center \(AEMC\).

The App Engine adoption metrics section of the AEMC Overview page shows how many apps you have in development and production environments. Access more information by selecting the large number on each Custom apps card.

The Custom apps page in AEMC shows more detailed metrics and a full list of your applications. In each tile in the Custom app lifecycle status section, you can see trending data for the last 90 days. You can show all apps in the Custom apps list or limit the list to only certain types of applications using the filter. Select a trend chart to filter the list to those criteria.

![Custom app page, with high-level metrics and list of all apps](../image/custom-app-page.png)

The Custom app page also lists all the applications individually, with a single record for each application. If the app has been published to production, the **Published Version** column shows the version number. If the **Published Version** column is blank, the app exists in development but has never been published to production.

![List of all custom apps](../image/custom-app-list-purple.png)

View the app's usage data, subscription monitoring details,deployment history, and collaborators, if any, by selecting an application name from the list.

Select **Open in App Engine Studio** to see the contents of the app and access more information. The App Engine Studio application opens in a new browser window.

## App usage

See a high-level view of the usage data for apps on production instances by selecting the **App usage** tab. The data includes the user count, insert count, and update count aggregated for the current month.

-   User count: The number of users who have accessed the application.
-   Insert count: The number of new records on tables in the application.
-   Update count: The number of records in the application that have been updated.

Knowing usage data for your applications has several benefits:

-   Discover whether your app is being used. Are people using the app? Are they creating records? If not, consider updating or deleting the app.
-   Investigate and fix problems with the app. Knowing when or how data was changed can help identify where something went wrong.
-   Determine whether you must load balance the processing power of your instance by seeing when there might be consistently higher traffic in your app.

In the Usage Insights dashboards section, see detailed data such as active users, sessions, and page views by selecting an experience. For more information about how to understand and use this data, see [Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/usage-insights/user-exp-analytics-landing.md).

## Subscription monitoring

Understand the roles used in your custom application and their implications for licensing and subscriptions. The data in this section includes details about each role and the users assigned to each role.

Knowing subscription and licensing data information for each of your applications has several benefits:

-   Discover what roles are active in your custom application.
-   Discover which users are assigned each role and the permission levels they have.
-   See the cost implications of each license type and where it's used in your apps.

System administrators can see which subscription the app is mapped to and have an option to change the subscription. Several factors affect what you see in this section.

-   If the app is mapped to an App Engine subscription, the **Subscription Monitoring** tab is visible.
-   If the app is mapped to a different subscription such as ITSM, the **Subscription Monitoring** tab is not visible.
-   If the app is mapped to App Engine, is switched to another subscription, and then is changed back to App Engine, the **Subscription Monitoring** tab is visible again.

App Engine admins do not have permissions to change subscriptions. However, if an app is in the production environment, and there is a **Subscription Monitoring** tab, the App Engine admin can infer that the app is mapped to an App Engine subscription. If the **Subscription Monitoring** tab is not there, that app isn't mapped to App Engine.

You can select a user's name in the **Assigned Users** section to see a role inheritance map. This map shows how this user inherited the role, whether from a parent role, a group assignment, or another inheritance. This information can help you take action if someone has a role you believe they shouldn't, and you want to change it.

![Role inheritance map, showing how a user got their roles](../image/role-inheritance-map.png "Role inheritance map")

## App deployments

View the list of deployments your app has gone through on the **Deployment history** tab.

Knowing deployment history information has several benefits:

-   If an app is deployed to production and there’s a defect, you can quickly see when the app was deployed and track down the problem.
-   If an app is deployed multiple times, you can quickly track what's changed over multiple deployments.
-   If an app is deployed to production, you can quickly see who approved the app deployment.

## App collaborators

View the collaborators for the app by selecting the **Collaborators** tab. All collaborators are stored on the Development instance.

If you must take quick action in the application to fix an issue or defect, you can quickly see who has permissions to make changes in an app and what those permissions are.

**Parent Topic:**[Managing app development using the App Engine Management Center](../../app-engine-management-center/concept/managing-app-development-using-aemc.md)

