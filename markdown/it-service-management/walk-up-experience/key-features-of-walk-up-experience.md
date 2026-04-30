---
title: Key features of Walk-up Experience
description: Walk-up Experience enhances user satisfaction and productivity by providing immediate and personalized support for IT-related needs.
locale: en-US
release: xanadu
product: Walk-Up Experience
classification: walk-up-experience
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Explore, Walk-up Experience, IT Service Management]
---

# Key features of Walk-up Experience

Walk-up Experience enhances user satisfaction and productivity by providing immediate and personalized support for IT-related needs.

Every employee or a guest can check in and get support at an established walk-up service center.

-   **Requesters**

    Requesters can access the Walk-up Experience application in several ways.

    -   Online and via mobile device:
        -   Quickly check in online to the nearest available walk-up venue via a prebuilt check-in widget on the Service Portal using your laptop, tablet, or mobile phone.

            **Note:** Geolocation interfaces with the Walk-up Experience application to route you to the nearest walk-up queue. You can change the location, if desired.

            Geolocation uses browsers or mobile device coordinates to determine location. If geolocation is blocked on the browser, Walk-up Experience defaults to Latitude/Longitude criteria in the user profile or mobile device.

        -   View hours of operation, the estimated wait time, and your position in the queue at the check-in location via the **Walk-up Status** widget on the Service Portal. You can also access the online Walk-up Experience check-in from this widget.

            **Note:** The **Walk-up Status** widget must be configured to appear on the Service Portal.

        -   View upcoming walk-up appointments and current queue position by location using the Now® Mobile application **Services** tab on your mobile device. **Tech Lounge visits** appears if there is associated data. If no data exists, the section is hidden.

            **Note:** Requires activation of the ServiceNow Mobile Request Native Application Screens and Applet Launcher plugin \(com.glide.mobile-employee\). See [Mobile plugins and upgrades](https://www.servicenow.com/docs/access?context=plugins-upgrades&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US) for more information. This plugin enables the Service Catalog functionality by default.

        -   Schedule appointments for support and receive appointment reminders, as well as cancel or reschedule appointments from links in the reminder or from the online check-in interface.
        -   Schedule only one appointment for each walk-up location queue at a time.

            **Note:** Even with a scheduled appointment, you can still check into a walk-up location queue online or in person onsite.

        -   Schedule appointments on behalf of others who need IT support, such as executives or direct reports.

            **Note:** Configuration is necessary to make this available to the **Appointment delegation group** of users, such as executive assistants. This is configured in the Walk-up Location Queue \(wu\_location\_queue\) table.

        -   Receive notifications via email or your mobile device when your request is assigned to an IT support fulfiller, when you are close to next in line to be helped, and when your walk-up request has been closed or abandoned, should you decide not to attend the queue.
        -   View your Walk-up Experience appointments in your primary calendar with Microsoft Office 365 Outlook calendar integration. When you make an appointment, modify it, or cancel it, your calendar is sent invites to an appointment and any updates.

            **Note:** This feature is only available when Microsoft Office 365 Outlook is the hosted calendar service.

        -   Add your online Walk-up Experience appointment to a calendar of your choice with iCalendar. Click a link in the portal to download an iCalendar file containing appointment details, including appointment location.
    -   Onsite at the Walk-up Experience location:
        -   Check into a queue at the physical walk-up location by manually entering either your name or email or by scanning an employee badge.

            **Note:** The badge scanning feature requires activation and configuration. Refer to [Badge Reader Integration for Walk-up Experience](badge-scan-walkup-onsite.md).

        -   Observe queue activities on a large monitor that displays both walk-in requesters and those with appointments.
        -   View the monitor displaying how many people are currently in the queue, guest positions in the queue, who is being helped, and estimated wait times.
        -   Hear an audio sound emitted from the on-site walk-up location large monitor when a person moves to the top of the queue for service.
        -   Answer an available single-question survey which captures your user sentiment after a visit.
    -   After-hours support — Get support even when a walk-up queue is closed. An IT support phone number is displayed on the check-in device, along with a link to create an incident in real time.
-   **Agents**

    The IT organization uses the Walk-up Experience application to meet the demand of urgent IT issues and requests.

    -   Walk-up Experience IT technicians manage daily operations at the walk-up queue locations. They resolve IT-related issues, support mobile devices and laptops, and fulfill requests for software and hardware consumables.
    -   The agents can accept and close Walk-up Experience interactions through the Agent Workspace interface. Agent Workspace contains a personal inbox where walk-up interactions, if configured in Advanced Work Assignment, are automatically pushed for assignment.
    -   Agents can manage all aspects of Walk-up Experience fulfillment using Agent Workspace. Based on their capacity, and if records are on-hold, they can work on multiple transactions at the same time and promote interactions to incidents or requests, or access associated stockroom consumables.
    -   Technicians can view and accept scheduled appointments in their Agent Workspace personal inbox. Appointments are routed to the inbox according to agent availability. Alternatively, agents can pick and choose appointments manually.
    -   If necessary, technicians can work with anyone in the queue at any time. Technicians can manually assign themselves to a walk-up interaction, by accepting the interaction from a list of unassigned interactions in Agent Workspace.
    -   Agents can use the Agent Assist feature to expedite incident resolution.
-   **Managers**

    IT managers supervise the walk-up location technicians and oversee daily operations.

    -   Walk-up managers can observe and capture operational and performance data by monitoring the walk-up dashboard.
    -   Walk-up managers can use the application to increase IT customer satisfaction, verify, and confirm that stockroom inventory is available, provide customer service in a timely manner, and report performance data to upper management.
-   **Administrators**

    Configure and maintain walk-up related systems, such as the walk-up location branding and text, queue locations and schedules, appointments, advanced work assignments, and notifications, CSAT surveys, and associated stockrooms.

    Access the pre-built **Walk-up online check-in Experience** widget for use in your Service Portal. Make minor label changes directly in the widget without the need to customize through code.

    Enable Walk-up Experience Microsoft Office 365 calendar integration. When users make an appointment, modify it, or cancel it, the Outlook calendar is sent invites to an appointment and any updates. For more information about this feature, refer to [Integrate Microsoft Office 365 calendar with Walk-up Experience](walkup-ms-office-365-integration.md).

    **Note:** This feature is only available when Microsoft Office 365 Outlook is the hosted calendar service.


