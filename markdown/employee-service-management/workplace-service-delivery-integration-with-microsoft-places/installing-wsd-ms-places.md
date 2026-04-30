---
title: Register the WSD for Microsoft places application
description: Register the WSD for Microsoft places application in the Microsoft Azure portal.
locale: en-US
release: zurich
product: Workplace Service Delivery Integration with Microsoft Places
classification: workplace-service-delivery-integration-with-microsoft-places
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure WSD for Microsoft places, WSD for Microsoft places, Workplace Service Delivery, Employee Service Management]
---

# Register the WSD for Microsoft places application

Register the WSD for Microsoft places application in the Microsoft Azure portal.

## Before you begin

Role required: admin

## Procedure

1.  Log in to Microsoft Azure portal.

2.  Click **App registrations**.

3.  Click **+ New registration**.

4.  Enter the **Display name**.

    **Application \(client\) ID**, **Directory \(tenant\) ID**, **Object ID**, and **Application ID URL** are auto-generated.

5.  Go to **API permissions**.

6.  Under **Configured permissions**, add the following permissions and provide **Grand admin consent for ServiceNow**.

    -   Calendars\_ReadWrite
    -   email
    -   offline\_access
    -   openid
    -   profile
    -   User\_Read
7.  Go to **Expose an API**.

8.  You can add clients like selecting **+Add a client application**.

9.  Go to **Authentication**.

10. Add the **Web Redirect URLs**.


## What to do next

Follow up with downloading the manifest files.

