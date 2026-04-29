---
title: Setup OAuth connectivity between ServiceNow and Zoom
description: Register Zoom with ServiceNow instance for OAuth authorization to get create virtual meetings and get recordings after a virtual meeting.
locale: en-US
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Connect Workplace Reservation Management with Zoom, Configure Workplace Reservation Management portal, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Setup OAuth connectivity between ServiceNow and Zoom

Register Zoom with ServiceNow instance for OAuth authorization to get create virtual meetings and get recordings after a virtual meeting.

## Before you begin

Ensure the following:

-   Setup Zoom to enable virtual meeting.

    Refer to the Create a connected app in Zoom topic in [Set up the](https://www.servicenow.com/docs/access?context=setup-zoom&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

    **Note:** While setting up zoom, ensure the following:

    -   Copy the url specified in **Redirect URL for OAuth** to **Add allow list** as well.
    -   Select the following scopes:
        -   In **Meeting**, select the following:
            -   **View and manage sub account’s users meetings \(meeting: master\)**
            -   **View and manage all user meetings \(meeting:write:admin\)**
        -   In **Recording**, select **View all users recordings \(recording:read:admin\)**
-   Set the application scope to Zoom spoke.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Select **Zoom**.

3.  On the form, update the following fields.

    |Filed|Description|
    |-----|-----------|
    |Client ID|Client ID created during the app creation. Copy from the **Application credentials** in Zoom.|
    |Client Secret|Client secret created during application registration.|
    |Default Grant Type|Grant type used to establish the token. Select **Authorization code**.|
    |Redirect URL|OAuth callback endpoint. The URL is automatically filled as `https://<instance-name>.service-now.com/oauth_redirect.do`.|

4.  Right-click the form header, and click **Save**.

    A system-generated OAuth entity profile is created and displayed in the OAuth Entity Profiles related list. For example, `Zoom default_profile`.

5.  Save the changes.


## Result

The OAuth registration is added for Zoom.

**Parent Topic:**[Connect Workplace Reservation Management with Zoom](connect-rsv-mtm-with-zoom.md)

**Previous topic:**[Connect Workplace Reservation Management with Zoom](connect-rsv-mtm-with-zoom.md)

**Next topic:**[Create connection and credential for Zoom](create-connection-and-credentials-for-zoom.md)

