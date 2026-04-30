---
title: Set up privacy consent for Vaccination Status
description: Set up privacy consent for users who are providing their vaccination data to your organization.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Vaccination Status, Safe Workplace, Health and Safety, Employee Service Management]
---

# Set up privacy consent for Vaccination Status

Set up privacy consent for users who are providing their vaccination data to your organization.

## Before you begin

Role required: sn\_imt\_core.admin and sn\_imt\_checkin.checkin\_admin

## About this task

Use Emergency Outreach to send a privacy consent form to users. Users must agree to the privacy consent before they can submit their vaccination status.

## Procedure

1.  Customize the privacy consent template.

    1.  Navigate to **Employee Health and Safety Status** &gt; **Privacy Consent Templates** and click **Vaccine Administration**.

    2.  Fill in the placeholder text with the name of your organization and contact information.

        **Note:** If you customize the privacy consent template with HTML, such as including tables or links, the HTML renders properly in the email that is sent to users. The HTML does not render in the privacy consent form when a user is submitting their response.

    3.  Click **Update**.

2.  Assign the sn\_imt\_core.privacy\_consent\_user role to all users who will be reporting their vaccination status.

    This role enables users to complete the privacy consent.

3.  Add all usersfrom the User \[sys\_user\] table who will be reporting their vaccination status to a Safe Workplace audience.

    1.  Navigate to **Emergency Outreach** &gt; **Safe Workplace Audience** and click **Vaccine Privacy Consent Audience**.

    2.  Add users to the audience.

        For detailed instructions about adding users to an audience, see [Add a Safe Workplace audience](../../employee-readiness-core/task/add-safe-workplace-audience.md).

    3.  Click **Update**.

4.  Configure an outreach to send the privacy consent to users.

    1.  Navigate to **Emergency Outreach** &gt; **View Outreaches** and click the **Vaccine Privacy Consent Placeholder** outreach.

        This outreach is preconfigured to use the Vaccine Privacy Consent Audience and the Vaccine Administration privacy consent template.

    2.  Make any modifications to the outreach if needed, such as scheduling a time to send.

        For detailed instructions about configuring an outreach, see [Send notifications for an emergency](../../business-continuity/task/send-eo-notification-outreach.md).

    3.  Enable the outreach to provide location-specific privacy consents by selecting the **Use Country** option on the **Content configuration** tab.

        When enabled, the privacy statement text in Location Privacy Configuration takes precedence over text in the privacy consent templates. This text is used for the outreach, system notification email, and push notification. If you need to update the text that users receive, you must change the location's privacy statement.

        For more information on updating a location's privacy statement, see [Generate location-based privacy configurations](../../employee-readiness-core/task/generate-location-common-privacy-configuration.md).

    4.  Click **Update**.


**Parent Topic:**[Vaccination Status](../concept/vaccination-status.md)

