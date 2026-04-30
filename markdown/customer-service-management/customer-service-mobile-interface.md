---
title: Mobile experience for Customer Service Management
description: Manage customer service cases from a mobile device with the Customer Service Management mobile application. Stay connected and access information in real time to complete tasks quickly.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Manage schedules and sites, Using Customer Service Management, Customer Service Management]
---

# Mobile experience for Customer Service Management

Manage customer service cases from a mobile device with the Customer Service Management mobile application. Stay connected and access information in real time to complete tasks quickly.

Customer service agents and managers can use the Customer Service Management mobile application to review case details quickly and complete case tasks. Agents and customer service managers can perform routine actions and approvals effectively any time and anywhere.

Activate the Customer Service Mobile plugin \(com.sn\_csm\_mobile\) to use the available features. To use the change request feature, the Customer Service with Service Management \(com.sn\_cs\_sm\) plugin is required.

**Note:** The Customer Service Management mobile application supports product cases.

For more information, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

![Customer service mobile launcher screen that displays the agent's cases needing attention and cases that are new, active, and active critical.](../image/csm-mobile-agent.png "Customer Service mobile application applet launcher for agent")

With the customer service agent role \(sn\_customerservice\_agent\), you can:

-   Get a quick overview of your case load, including new cases, critical cases, and those that need attention.
-   Accept and reassign cases.
-   Add comments or work notes to cases.
-   Review case details, activity stream, and related information such as SLAs, case tasks, and child cases.
-   Edit case information such as priority.
-   Propose major cases.
-   Receive push notifications for assigned or updated cases.
-   Search for cases using keywords

With the system administrator role, you can configure the Customer Service Management mobile application in the following ways:

-   Configure pages to display the desired data.
-   Configure the functions associated with swipe actions and top menu actions.
-   Configure and create push notifications.

![Customer Service mobile launcher screen that displays the manager's cases that are new, active, and active critical, and also approvals needed for escalations and change requests.](../image/csm-mobile-manager.png "Customer Service mobile application applet launcher for manager")

With the customer service manager role \(sn\_customerservice\_manager\) you can:

-   Search for cases using keywords
-   Review and approve change requests
-   Approve escalations

## Activate the Customer Service Mobile plugin

The Customer Service Management mobile application runs on the ServiceNow® mobile platform.

To use the Customer Service Management mobile application, activate the Customer Service Mobile plugin \(com.sn\_csm\_mobile\). This plugin activates the following plugins:

-   Mobile Agent Native Client plugin \(com.glide.sg.agent\_native\_client\)
-   Customer Service \(com.sn\_customerservice\)
-   Customer Service Case Action Status \(com.sn.csm\_action\_status\)

To provide support for major cases, you can activate the optional Major Issue Management plugin \(com.sn\_majorissue\_mgt\).

Once the Customer Service Management mobile application is activated and configured, agents can download the ServiceNow Agent mobile app on their mobile devices and access ServiceNow instances.

**Note:** You can activate the Customer Service Mobile plugin \(com.sn\_csm\_mobile\) from the Customer Service Management guided setup.

For more information, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

-   **[Customer Service mobile application overview](../reference/customer-service-mobile-overview.md)**  
Customer service agents and managers can use the applet launcher and applets in the Customer Service mobile application to view notifications and manage customer service cases.
-   **[Get started with the Customer Service mobile application](../task/install-customer-service-mobile-app.md)**  
Use the ServiceNow Agent mobile app to access the Customer Service mobile application. Then log in to an instance as an agent or manager and work on your customer service cases.

**Parent Topic:**[Customer Service Management](c_CustomerServiceManagement.md)

**Related topics**  


[Getting started with ServiceNow Agent](https://www.servicenow.com/docs/access?context=mobile-experience&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)

