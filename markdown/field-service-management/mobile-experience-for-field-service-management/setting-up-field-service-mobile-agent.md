---
title: Setting up Field Service Mobile Agent
description: Setting up the Field Service mobile application involves configuring the Mobile Agent application, customizing UI actions, and other functionalities to enable task management from your phone or other mobile device.
locale: en-US
release: australia
product: Mobile Experience for Field Service Management
classification: mobile-experience-for-field-service-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Field Service Management]
---

# Setting up Field Service Mobile Agent

Setting up the Field Service mobile application involves configuring the Mobile Agent application, customizing UI actions, and other functionalities to enable task management from your phone or other mobile device.

The Field Service Management application includes the Field Service Mobile plugin \(com.sn\_fsm\_mobile\) by default. This plugin enables the Field Service mobile application's functionality within your Field Service Management application.

**Note:** The mobile plugin must be installed.

You can configure the following functionalities within this mobile application to ensure an optimized mobile experience for your Mobile Agent application instance, empowering agents and dispatchers to work efficiently from any location:

-   Customize system and mobile properties to tailor the mobile experience according to your organization's requirements. This includes configuring settings such as display options, permissions, and access controls.
-   Enable the outsourced service provider to manage tasks on mobile devices. This functionality allows contractors to access and manage their assigned tasks, ensuring seamless collaboration and efficient task execution.
-   Utilize the task briefing feature using the virtual agent capability. This enables agents to receive briefings and instructions for their tasks directly through the mobile application, ensuring they have all the necessary information to complete their assignments effectively.
-   Implement indoor way finding functionality within the mobile application. This enables agents to navigate complex indoor environments more easily, improving their efficiency and reducing response times.

If you have the wm\_manager, sn\_fsm\_tp.fsm\_territory\_resource\_manager role, and Field Service Manager Mobile is activated, when you sign into the Mobile Agent you see Field Service Manager Mobile.

## Configuration overview

The steps for setting up Field Service Mobile Agent are:

1.  [Configure the Now Mobile Agent application](../task/configure-field-service-mobile.md)

    Configure the Mobile Agent application and customize it for field service agents and dispatchers.

2.  [Field Service Contractor for mobile feature of the Now Mobile Agent application](field-service-contractor-portal-mobile.md)

    The Field Service Contractor for mobile feature of the ServiceNow Agent application enables contractors to manage work order tasks.

3.  [Configuring Field Service Virtual Agent Conversations](fsm-va-conversation.md)

    ServiceNow® Virtual Agent for Field Service Management enables field service agents to get quick answers to their work-related queries by interacting with a virtual agent through the Now Agent mobile application.

4.  [Configuring Site Mapping for Field Service Management](configuring-sitemap-fsm.md)

    Site Mapping for Field Service Management helps agents navigate job sites when their tasks are in large indoor facilities.

5.  [Activate Sidebar for the Field Service Mobile Agent application](../task/activate-sidebar-mobile.md)

    You can activate the Sidebar for Field Service Management plugin \(com.sn\_fsm\_sidebar\) for Field Service Management if you have the admin role. Activating this plugin enables the Sidebar feature on the Mobile Agent application.

6.  [Configuring push notifications for task assignment](push-notifications-tasks-slas.md)

    Configure notifications to ensure agents and dispatchers receive timely updates and alerts on their mobile devices. This feature keeps them informed about important tasks and changes in real-time.

7.  [Activate Field Service Manager Mobile](../task/activate-manager-mobile.md)

    Activate Field Service Manager Mobile so users with the wm\_manager, sn\_fsm\_tp.fsm\_territory\_resource\_manager can access the app.

8.  [Change Field Service Manager Mobile to use assignment groups or territories](../task/change-manager-territory.md)

    Change the Field Service Manager Mobile app to use territories instead of the default assignment groups.


