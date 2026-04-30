---
title: Installed application details
description: Gain complete insight into application performance, device utilization, and patterns to identify performance issues, optimize device usage, and improve user experience.
locale: en-US
release: xanadu
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Applications, Application and Device Health, Monitor, Digital End-User Experience, IT Service Management]
---

# Installed application details

Gain complete insight into application performance, device utilization, and patterns to identify performance issues, optimize device usage, and improve user experience.

## Installed application overview

Monitor the application performance in real time to view active alerts, incidents, current users, and time to resolve incidents.

For more details on the health cards, see [Installed application Performance page](../reference/installed-app-health-form.md).

## Installed application metrics

The Application metrics section promotes the smooth functioning of applications by monitoring their real-time health and promptly resolving any potential issues to maintain a seamless user experience. Additionally, it assesses the system's performance in terms of efficiently carrying out its intended tasks and delivering prompt and reliable responses to user requests.

Refine your search based on the **Locations**, or **App version** filter.

**Note:** Access application performance data spanning the past 2 hours, 24 hours, or 30 days by choosing your preferred timeframe from the provided drop-down list.

View the number of crashes of an application over time, reflecting its resilience, sustainability, and reliability.

**Note:** The number of crashes pertains to applications that emit a window app crash event \(event id = 1000\) on crashing such as Microsoft OneDrive, Microsoft Teams, Microsoft Excel, Microsoft OneNote, Microsoft PowerPoint, Microsoft Outlook, and Microsoft Word.

For more information on the cards, see [Installed application — Number of crashes section](../reference/installed-app-crash-rate-form.md).

Find out how well your system performs its intended function and how quickly and reliably it responds to user requests.

For more information on the performance cards, see [Installed application — CPU, memory and I/O performance section](../reference/installed-app-performance-form.md).

## Users

End users can use different devices to connect to an application. Get an overview of the active and impacted users for the following:

-   Last logged in device and location
-   Total duration of time the user spends interacting with the application on the current day
-   Last access time of the application

This information can assist in troubleshooting and support, optimizing performance, and enhancing security.

Refine your search based on the **Users**, **Status**, or **App version** filter.

**Note:** The user list displays all system users with Agent Client Collector \(ACC\) installed on their devices. If a user hasn't used the application in the last three days, the value of the **App last accessed** field is denoted as **-**. By default, sorting is applied on the **App last accessed** field and data is sorted for the latest 1000 records. The **App last accessed** field is not applicable to the Mac-installed applications. Therefore, the **App version** drop-down list displays application versions only for Windows.

Selecting the user name takes you to the details page of that user. For detailed information on a user and associated applications, see [Device details](dex-workspace-user-details.md).

For more information on each field, see [Installed application — Users section](../reference/installed-app-users-form.md).

