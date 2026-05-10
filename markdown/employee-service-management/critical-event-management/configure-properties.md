---
title: Configure Critical Event Management application properties
description: Configure the application properties for Critical Event Management \(CEM\) to access the map feature on the dashboard and to. set the maximum contacts for Email and SMS according to organizational needs.
locale: en-US
release: australia
product: Critical Event Management
classification: critical-event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring, Critical Event Management, Health and Safety, Employee Service Management]
---

# Configure Critical Event Management application properties

Configure the application properties for Critical Event Management \(CEM\) to access the map feature on the dashboard and to. set the maximum contacts for Email and SMS according to organizational needs.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Critical Event Management** &gt; **Properties**.

2.  Set the number of active critical event cards to be displayed on the dashboard.

3.  Set the value for the number of contacts to send Email.

    The value can be customized according to need. The maximum contacts the Email can be sent to is 4000.

4.  Set the value for the number of contacts to send SMS.

    The value can be customized as needed. The maximum contacts the SMS can be sent to is 10,000.

5.  In the Google Map Component Properties section, select the **Enable Geo Map feature** check box.

    **Note:** This configuration is available only when the Geo map application is installed.

6.  Add either a client id or an API key:

    -   To add a client id, obtain a client id from Google and enter it in the **Client ID from google to access Geo map** field.
    -   To add an API key, obtain an API key from Google and enter it in the **Api key from Google to access Geo map** field.
    For more information, see [Set up Google Maps API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/set-up-google-maps-api.md).

7.  Select **Save**.


