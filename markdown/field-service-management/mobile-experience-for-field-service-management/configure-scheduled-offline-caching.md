---
title: Configure scheduled offline caching
description: Configure system components to automatically download the cache in the background. If you are making changes to these properties, then you must create them first.
locale: en-US
release: xanadu
product: Mobile Experience for Field Service Management
classification: mobile-experience-for-field-service-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure the Now Mobile Agent application, Setting up Field Service Now Mobile Agent application, Configuring Field Service Management, Field Service Management]
---

# Configure scheduled offline caching

Configure system components to automatically download the cache in the background. If you are making changes to these properties, then you must create them first.

## Before you begin

Role required: wm\_admin

## Procedure

1.  Configure properties to schedule the offline cache download.

    1.  In the application navigator, enter `sys_properties.list`.

    2.  Set the values for the system properties.

<table id="table_srs_h1q_gmb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.sg.offline.scheduled\_download.enabled

</td><td>

Enable scheduled downloading for all Agent app users​. -   Type: true/false
-   Default value: false


</td></tr><tr><td>

glide.sg.offline.scheduled\_download.cachesync\_offset

</td><td>

Number of minutes before a user's shift to begin payload generation. The property value is in minutes.​**Note:** Do not set the value of this property to less than the interval that the Mobile Offline Scheduling job is running. Doing so would prevent offline payloads from being generated.

</td></tr><tr><td>

glide.sg.offline\_payload.refresh\_frequency

</td><td>

The number of minutes before a cached record is flagged for refresh.-   Type: Integer
-   Default value: 240 minutes


</td></tr><tr><td>

glide.sg.offline.expiration

</td><td>

The duration when the cache expires on the client. Every time the payload is refreshed, this time gets extended. -   Type: Integer
-   Default value: 172,800,000 milliseconds

**Note:** 172,800,000 milliseconds is 48 hours. After 48 hours, the system deletes the data due to a security protocol.

</td></tr></tbody>
</table>        **Note:** To set additional properties for scheduling offline cache download, see [Configure offline mode behavior](https://www.servicenow.com/docs/access?context=sg-configure-offline-mode&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US).

    3.  Select **Update**.

2.  Configure the scheduled job to schedule the offline cache download.

    1.  Navigate to **System Definition** &gt; **Scheduled Jobs**.

    2.  Select the **Populate Agents Daily Schedule Table** scheduled job and configure the job schedule.

        1.  Activate the job by selecting the **Active** check box.
        2.  In the **Time** field, enter the time to execute the job.
        3.  Set the **Run** field to **Daily**.
    3.  Select **Update**.


**Related topics**  


[Scheduled offline caching](https://www.servicenow.com/docs/access?context=scheduled-offline-caching&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US)

