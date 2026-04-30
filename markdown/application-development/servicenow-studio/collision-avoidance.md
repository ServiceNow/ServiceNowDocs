---
title: Legacy - Collision avoidance
description: Avoid modifying an application file across different update sets to ensure seamless experience during the commit process.
locale: en-US
release: zurich
product: ServiceNow Studio
classification: servicenow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Legacy - Source Control integration, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Collision avoidance

Avoid modifying an application file across different update sets to ensure seamless experience during the commit process.

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

When the logged in user opens an application file that was modified in an update set different from the user’s current update set for the corresponding application:

-   Collision is detected in the application file and a warning message is displayed.
-   Logged in user to prompted to choose an update set.
-   Read-only protection policy is applied to the application file.

![Collision avoidance message](../image/collision-avoidance.png)

User can make changes to the application file only after selecting the required update set.

**Note:** This feature is applicable to only those applications that are linked to GIT.

Enable or disable the collision avoidance feature using the **glide.ui.vcs.collision\_avoidance** property in the System Property \[sys\_properties\] table. By default, the feature is enabled. See [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) for more information.

When the feature is enabled, users can't work in the default update set of the application. If a user is assigned the default update set, a unique update set is created when the user logs in to the application for the first time after the collision avoidance feature is enabled. This new update set is specific to the user in current application.

Name of the update set specific to the logged in user is, User ID or user name based on the value specified for the **glide.ui.vcs.updateset\_identifier** property in the System Property \[sys\_properties\] table. See [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) for more information. By default, the update set name is set to user name of the logged in user. However, users can rename the update set.

**Parent Topic:**[Legacy - Source Control integration](../concept/c_SourceControlIntegration.md)

