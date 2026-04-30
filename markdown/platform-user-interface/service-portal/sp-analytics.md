---
title: User Experience Analytics for Service Portal
description: The User Experience Analytics application provides views for monitoring usage analytics of your Service Portal applications. Visualize metrics and interactions to better understand the Service Portal user experience and identify how to improve it.
locale: en-US
release: yokohama
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2025-08-13"
reading_time_minutes: 2
breadcrumb: [Analytics and Reporting Solutions for Service Portal, Analyzing portal performance and usage, Service Portal, Configure UIs and portals, Configure user experiences]
---

# User Experience Analytics for Service Portal

The User Experience Analytics application provides views for monitoring usage analytics of your Service Portal applications. Visualize metrics and interactions to better understand the Service Portal user experience and identify how to improve it.

Video showing how to navigate and use User Experience Analytics 

You can view user analytics tracking for the portal in the User Experience Analytics application. For more information, see [Overview of the User Experience Analytics application](https://www.servicenow.com/docs/access?context=user-exp-analytics-dashboard&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

![User Experience Analytics interface for Service Portal](../image/sp-analytics-dashboard.png)

User Experience Analytics for Service Portal provides views for monitoring the key performance indicators \(KPIs\) of web applications built on Service Portal. You can use these insights to optimize your portal.

For example, User Experience Analytics tracks when a user orders a catalog item or views a knowledge article. You can use this data to infer which items or articles are the most popular among users. For more information on user-triggered events that are tracked automatically, see [Service Portal events](../reference/sp-analytics-events.md).

-   **Note:** User Experience Analytics tracking is enabled for all portals by default. You need to enable tracking for a portal only if you enabled tracking for some portals but not others in a previous version. For more information, see [Track User Experience Analytics in Service Portal](../task/create-sp-analytics-settings.md).

-   **Note:** If you make certain key changes to portals, such as changing the sys\_id, data is not carried over and you see a different dashboard.


## Roles

The portal\_analytics\_admin and portal\_analytics\_viewer roles are installed with the Service Portal Analytics plugin \(com.glide.service-portal.analytics\). For information on other roles associated with User Experience Analytics, see [Roles installed with User Experience Analytics](https://www.servicenow.com/docs/access?context=components-installed-user-exp-analytics&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

## User consent notices

User consent notices must conform to the ServiceNow Data Processing Addendum. Review your ServiceNow template user consent notices before they are presented to users. You can tailor the options for how these notices are presented to users, including the wording. For more information, see [Define texts for Notice and Explicit Opt-in user consent management policies](https://www.servicenow.com/docs/access?context=uxa-define-text-policies&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

-   **[Track User Experience Analytics in Service Portal](../task/create-sp-analytics-settings.md)**  
Track User Experience Analytics for Service Portal to monitor key performance indicators with the User Experience Analytics application.
-   **[Activate the privacy notice for unauthenticated users](../task/activate-privacy-notice.md)**  
If you enabled unauthenticated user tracking in your portal, you may be required by law to notify unauthenticated users that you are tracking their usage for analysis. You can display a legal notice by activating the Privacy Notice announcement.
-   **[Service Portal events](../reference/sp-analytics-events.md)**  
View Service Portal events to get insight into how a portal is being used in your organization.
-   **[User Experience Analytics related properties for Service Portal](../reference/sp-analytics-properties.md)**  
Use system properties to configure User Experience Analytics for Service Portal.

**Parent Topic:**[Analytics and Reporting Solutions for Service Portal](../../../use/dashboards/application-content-packs/service-portal-user-experience-analytics-content-pack.md)

**Related topics**  


[User Experience Analytics](https://www.servicenow.com/docs/access?context=user-exp-analytics-landing&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)

