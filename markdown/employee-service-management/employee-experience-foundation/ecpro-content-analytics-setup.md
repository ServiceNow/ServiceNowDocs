---
title: Create a Content Analytics tracking profile
description: Use Tracking Profiles to configure your ServiceNow content analytics dashboards.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Content Analytics, Setup continuous improvement, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Create a Content Analytics tracking profile

Use Tracking Profiles to configure your ServiceNow content analytics dashboards.

## Before you begin

Role required: sn\_cda.analytics\_admin

Tracking profiles define:

-   What website you want to collect data from.
-   From what time zone a day starts and ends for data tracking.
-   From what time zone the time data collection should start.
-   What countries you want to exclude in your analytics data collection and where you want to capture data from.

## Procedure

1.  Navigate to **All** &gt; **Content Analytics** &gt; **Setup**.

2.  Click **New**.

3.  Click **ServiceNow**.

4.  Fill in the form.

<table id="table_atc_q2x_sfb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A description of the tracking profile.

</td></tr><tr><td>

Active

</td><td>

Indicates that the profile is active and available to use.**Note:** If you attempt to deactivate a tracking profile that is in use, a warning message appears to confirm your actions.

</td></tr><tr><td>

Default

</td><td>

Indicates that the profile is the default profile. Portals use the default tracking profile when configured for tracking without setting a specific tracker.**Note:** The base system Employee Center \(EC\) uses the default tracking profile.

</td></tr><tr><td>

Owner

</td><td>

The user that is responsible for the profile.

</td></tr><tr><td>

Collection time zone

</td><td>

Defines when a day starts for data collection based on the time zone you select. A day starts at 12:00 AM and ends at 11:59:59 PM by default.For example, if you select System \(America/Los\_Angeles\), that means a day starts at 12:00 AM PST.

</td></tr><tr><td>

Import run time

</td><td>

For the ServiceNow profiles, the time and the time zone data moves from the content analytics tables to the shared analytics tables. See [Collected data](../concept/ecpro-content-automation-analytics.md#section-collected-data).

</td></tr><tr><td>

Import run time zone

</td><td>

The time zone for the Import run time. For example, if you set the Import run time as 00: 00: 00 and System \(America/Los\_Angeles\) as the Import run time zone, your data moves from the content analytics tables to the shared analytics tables at midnight, PST.

</td></tr><tr><td>

Restricted Countries

</td><td>

The countries of the users you do not want to track. **Note:** Restricted countries are based on the user profile \(sys\_user\) and not the country the user is in at the time.

Click **Insert a new row...** and select a country.

If a country you want restricted does not appear, add it to the list by navigating to **Organization** &gt; **Locations**.

</td></tr></tbody>
</table>5.  Click **Submit**.


## Result

The new tracking profile appears in the Tracking profiles list and the system creates a scheduled job to collect data. You can modify or manually execute the script associated with the scheduled job by doing these steps:

1.  Click the link in the Trigger column.

    **Note:** If the Trigger column doesn't appear in the Tracking profiles list, click the **Update Personalized List** icon and add the Trigger column to the selected list.

    The Profile trigger form opens, where you can modify the import run time \(how often the script runs\) or set a condition.

2.  To manually execute the script, click **Execute Now**.

