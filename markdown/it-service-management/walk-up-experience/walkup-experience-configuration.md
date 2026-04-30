---
title: Configuring Walk-up Experience
description: Customize your Walk-up Experience portal and configure appointments, notifications, walk-up venue locations, associated stockrooms, customer satisfaction surveys, and hours of operation to meet your required needs.
locale: en-US
release: xanadu
product: Walk-Up Experience
classification: walk-up-experience
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Walk-up Experience, IT Service Management]
---

# Configuring Walk-up Experience

Customize your Walk-up Experience portal and configure appointments, notifications, walk-up venue locations, associated stockrooms, customer satisfaction surveys, and hours of operation to meet your required needs.

Walk-up Experience includes associated notifications to alert requesters when the location is closed or when an interaction is assigned to an agent. Pre-built customer satisfaction surveys capture user sentiment about the experience. Also included are several configurable tables for customizing your walk-up portal and service center experience. You can configure and specify the following features for your experience:

-   Configure an online check-in channel for requesters to join a walk-up queue before physically arriving at the walk-up location.
-   Access the pre-built **Walk-up online check-in Experience** widget for use in your Service Portal. Make minor label changes directly in the widget without customizing through the code.
-   Configure the physical walk-up location queue information to manage and administer the walk-up service centers.
-   Establish walk-up locations, set hours of operation, enable online check-in, determine assignment groups, associate stockrooms, as well as design the queue time display and position notification system.
-   Configure reasons for visits to a walk-up queue by location.
-   Add a logo and brand your portal and walk-up location to fit your style.
-   Access location-specific branding elements, such as logo images, for walk-up queues. These configuration options are found in the Walk-up Location Queue \[wu\_location\_queue\] table.

The following applications are included in the **Administration** module of the Walk-up Experience navigation bar:

|Application|Description|
|-----------|-----------|
|Portal Configurations|Create and modify custom Walk-up Experience online and on-site service portals.|
|Notifications|Access and configure alerts that keep requesters and agents informed of events that concern them.|
|Appointment Configurations|Create service configurations for individual walk-up queue locations. You can configure schedules, number of appointments allowed per day, how far in the future requesters can book appointments, and more.|
|Walk-up Locations|Create walk-up location queues with custom schedules, assignment groups, average wait time, and more.|
|Schedules|View, create, or modify walk-up venue schedules, such as 8-5 weekdays, and associate them to the walk-up location queues.|
|Walk-up Stockrooms|Establish walk-up venue stockrooms by location and specify available consumables.|
|Surveys|Access customer satisfaction surveys and enable public access to the surveys, set survey trigger conditions, and view requester responses.|

-   **[Walk-up Experience administration](walkup-experience-administration.md)**  
Walk-up Experience users with the sn\_walkup.walkup\_admin role and administrators can activate and configure the application to meet specific requirements.
-   **[Walk-up Experience portal security and access](walkup-exper-security-portal-acess.md)**  
Security is built into the application to prevent end-user facing devices at the Walk-up Experience on-site portal from offering elevated role privileges to users. The Walk-up Experience on-site portal is accessed by an account containing only the sn\_walkup.walkup\_login role.
-   **[Configure the Walk-up Experience portal](../task/configure-walkup-portal.md)**  
Create engaging walk-up center service portals featuring your logo, portal theme, desired catalog, links to a knowledge base and social community, and more.
-   **[Configure Walk-up Experience service channel](../task/configure-walkup-service-channel.md)**  
Configure the Walk-up Experience service channel to meet the needs of your walk-up agents and how they are assigned to and manage interactions in Agent Workspace.
-   **[Create or modify Walk-up Experience schedules](../task/configure-walkup-location-schedules.md)**  
Once you know the hours of operation for your Walk-up Experience location, you can either access the base-system default schedules or create new schedules to associate with your walk-up location.
-   **[Book Walk-up Experience appointments](walkup-appointment-booking.md)**  
With the Walk-up Experience appointment booking feature, walk-up users can view available appointment windows, make a selection, and book an appointment for a walk-up location using online **Walk-up Check-in** feature. Walk-up agents can also book appointments on behalf of customers.
-   **[Create or modify a Walk-up Experience stockroom](../task/configure-walkup-stockroom.md)**  
Create stockrooms and assign assets and groups specifically for your walk-up location. Walk-up stockrooms contain common assets that visitors to the walk-up location will typically request, such as a computer mouse, monitors, and cables. The walk-up location stockroom should be easily accessible to your walk-up location for fast request fulfillment.
-   **[Create or modify Walk-up Experience locations](../task/configure-walkup-location.md)**  
Create or customize the predefined Walk-up Experience location. Walk-up Experience locations contain all the information about the walk-up support venue. You can define the way each location or support venue works.
-   **[Walk-up Experience kiosk](walk-up-experience-kiosk-administration.md)**  
Walk-up Experience kiosks help your requesters to resolve information technology \(IT\)-related issues and access various IT services and resources in your organization.
-   **[Configure skill-based routing in Walk-up Experience](walkup-skill-based-routing.md)**  
Route work items to assigned groups. Use skill-based routing to ensure that the right work goes to the right agent depending on the walk-up reasons.
-   **[Create or modify Walk-up Experience notifications](../task/configure-walkup-notifications.md)**  
Create and use Walk-up Experience notifications to keep requesters informed of queue events that concern them. The system can notify users by email, SMS text message, or push notification to a mobile device.
-   **[Configure Walk-up Experience customer satisfaction surveys](walkup-survey.md)**  
With Walk-up Experience surveys, requesters can rate their satisfaction with walk-up location interactions and provide feedback to improve the Walk-up Experience application.
-   **[Remove a Walk-up Experience location](../task/remove-walkup-location.md)**  
If you permanently close down a physical Walk-up Experience location, you can also remove the location from the Walk-up Location Queues table.
-   **[Integrate Microsoft Office 365 calendar with Walk-up Experience](walkup-ms-office-365-integration.md)**  
With Microsoft Office 365 calendar integration, Walk-up Experience users can view appointments in their primary calendar. When they make an appointment, modify it, or cancel it, they are sent invites and updates via their Outlook calendar.
-   **[Badge Reader Integration for Walk-up Experience](badge-scan-walkup-onsite.md)**  
Improve Walk-up Experience user satisfaction by using the Badge Reader Integration application at your on-site walk-up queue locations. Walk-up Experience users can scan an employee badge to check in to a queue, rather than entering credentials.
-   **[Enable Self-Service online check-in for Walk-up Experience](../task/enable-online-walkup-checkin.md)**  
Show or hide the Walk-up Experience online **Walk-up Check-in** module under **Self-Service** in the application navigator. You can enable or disable the module using the basic platform menu or module enablement process.
-   **[Configure Walk-up Experience online check-in icon to appear on Service Portal](../task/add-walkup-checkin-icon-to-servport.md)**  
Requesters can check into a walk-up location online via the Service Portal. You can edit the Service Portal Home page to replace the general IT **Get Help** support icon link with the Walk-up Experience online check-in support icon link.

**Parent Topic:**[Walk-up Experience](../reference/walkup-experience-landing-page.md)

