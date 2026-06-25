---
title: Configure Soft PIN
description: Users are required to configure Soft PIN before it can be used for authentication with ServiceNow AI Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/configure-soft-pin.html
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Soft PIN authentication, Configure authentication factors for AI voice agents, Authentication factors, Authentication, Access Management]
---

# Configure Soft PIN

Users are required to configure Soft PIN before it can be used for authentication with ServiceNow AI Platform.

## Before you begin

Role required: none

Perform the following:

-   Administrator must enable Soft PIN on the instance before you can enroll.
-   Install Now Assist for Platform `sn_genai_platform` for activating AI voice agents and set `glide.auth_factors.softpin.enrollment.enabled` property to `true`. To know more, see [Availability in Soft PIN authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/softpin-authentication.md).
-   The user record must exist in the `sys_user` table.

## Procedure

1.  Navigate to the Soft PIN enrollment page using any of the following:

    -   **Service Portal**: Go to your **User Profile** and select **Enroll Soft PIN**.

        \[Omitted image "softpin-3.png"\] Alt text: Soft PIN on the Service Portal

    -   **Platform UI**: Go to your **User Profile** and select **Enroll Soft PIN** under Related Links.

        \[Omitted image "softpin-1.png"\] Alt text: Soft PIN on the Platform UI

    -   **Navigation menu**: Select **All** &gt; **Authentication Factors** &gt; **Soft PIN** &gt; **Enroll**.

        \[Omitted image "softpin-2.png"\] Alt text: Soft PIN on the Navigation menu

2.  Specify a six-digit PIN that satisfies the enrollment rules:

    Rules for Soft PIN:

    -   The PIN must be exactly six digits in length
    -   No single digit must be repeated more than twice consecutively
    -   Don’t use ascending or descending numeric sequences longer than two digits
    -   Can’t reuse any of your previous five PINs
    \[Omitted image "configure-soft-pin.png"\] Alt text: Soft PIN Enrollment

3.  Select **Submit**.


## Result

You can use the submitted Soft PIN to authenticate various ServiceNow system or service. For example, AI voice service.

**Note:** Users are eligible for Soft PIN enrollment only if their user ID is present in **sys\_user** table. If its missing, an enrollment failure message is displayed.

-   **Update your Soft PIN**

    To change your PIN, return to the enrollment page from any of the entry points before and enter a new PIN. The new PIN must satisfy the same rules and can't match any of your previous five PINs. Submitting a new PIN replaces the existing one immediately.


**Related topics**  


[Soft PIN authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/softpin-authentication.md)

[Authentication factors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/authentication-factors.md)

