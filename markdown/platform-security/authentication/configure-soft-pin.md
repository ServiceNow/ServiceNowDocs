---
title: Configure Soft PIN
description: Users are required to configure Soft PIN before it can be used for authentication with ServiceNow AI Platform.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-11-14"
reading_time_minutes: 1
breadcrumb: [SoftPIN authentication, Configure authentication factors, Authentication factors, Authentication, Access Management]
---

# Configure Soft PIN

Users are required to configure Soft PIN before it can be used for authentication with ServiceNow AI Platform.

## Before you begin

Role required: none

**Note:** Soft PIN enrollment is available to all users and is used exclusively for AI Voice Agent authentication.

## Procedure

1.  Navigate to the Soft PIN enrollment page using any of the following:

    -   **Service Portal**: Go to your **User Profile** and select **Enroll Soft PIN**.

        ![Soft PIN on the Service Portal](../images/softpin-3.png "Soft PIN on Service Portal")

    -   **Platform UI**: Go to your **User Profile** and select **Enroll Soft PIN** under Related Links.

        ![Soft PIN on the Platform UI](../images/softpin-1.png "Soft PIN on Platform UI")

    -   **Navigation menu**: Select **All** &gt; **Authentication Factors** &gt; **Soft PIN** &gt; **Enroll**.

        ![Soft PIN on the Navigation menu](../images/softpin-2.png "Soft PIN on Navigation menu")

2.  Create a PIN that meets these requirements:

    Rules for Soft PIN:

    -   The PIN must be exactly six digits in length
    -   No single digit must be repeated more than twice consecutively
    -   Don’t use ascending or descending numeric sequences longer than two digits
    -   Can’t reuse any of your previous five PINs
    ![Soft PIN Enrollment](../images/configure-soft-pin.png "Soft PIN Enrollment")

3.  Select **Submit**.


## Result

You can use the submitted Soft PIN to authenticate various ServiceNow system or service. For example, AI voice service.

**Note:** Users are eligible for Soft PIN enrollment only if their user ID is present in **sys\_user** table. If its missing, an enrollment failure message is displayed.

