---
title: Configuring Vaccine Administration Management
description: Complete all configuration tasks to ensure that Vaccine Administration Management is set up correctly for your organization.
locale: en-US
release: australia
product: Vaccine Administration Management
classification: vaccine-administration-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Vaccine Administration Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configuring Vaccine Administration Management

Complete all configuration tasks to ensure that Vaccine Administration Management is set up correctly for your organization.

-   [Install Vaccine Administration Management](../task/hcls-install-vaccine-management.md#)
-   [Create vaccine models](../task/add-vaccine-inventory.md)
-   [Create vaccine consumable assets](../task/create-vaccine-consumable-assets.md)
-   [Create vaccination programs](../task/hcls-create-vaccination-program.md)
-   [Configure the eligibility criteria for a vaccination program](../task/configure-eligibility-for-appointment-booking.md)
-   [Configure advanced appointment scheduling for a center](../task/configure-location-level-weekly-schedule-config.md)
-   [Guidance for configuring advanced appointment scheduling for a vaccination center](../reference/recommendation-on-vaccination-appointment-configuration.md)
-   [Configure inventory-based scheduling for a center](../task/configure-scheduling-by-inventory.md)
-   [Configure vaccine appointment scheduling](../task/vaccine-appt-booking.md)
-   [Multi-vaccine appointment bookings configuration](multi-vaccine-appointment-bookings-configuration.md)
-   [Book appointments for subsequent doses after a previous dose is complete](../task/schedule-second-appointment-after-completion-of-first.md)
-   [Privacy policy settings for Vaccine Administration Management](privacy-policy-VAM.md)
-   [Customize vaccination notification emails](vaccine-emails.md)
-   [Mass book vaccine appointments](../task/hcls-vaccine-mass-booking.md)
-   [Cancel appointments in a given date range](../task/cancel-appointment-over-date-range.md)
-   [Vaccine Administration Management system properties](vam-system-properties.md)
-   [Configure the Patient Portal for Vaccine Administration Management](hcls-vam-configure-patient-portal.md)
-   [Turn off automatic email notifications for mass booking](../task/turn-off-automatic-email-notifications-for-mass-booking.md)
-   [Configure an appointment reminder and pre-appointment questionnaire](../task/configure-vaccine-user-questionnaire.md)
-   [Virtual Agent conversations for Vaccine Administration Management](va-vaccine-admin-mgmt.md)
-   [Retry booking for skipped appointment records](../task/Retry-process-booking.md)
-   [Encrypt search fields to appear in search assist](../task/Configure-fields-for-search-assist.md)
-   [Manage high number of concurrent bookings](managing-high-number-of-concurrent-booking.md)
-   [Manage processing for a high number of concurrent vaccine events](managing-high-number-of-concurrent-vaccine-events.md)
-   [Configure the questionnaire text for the user and clinician portals](../task/configure-vam-portal-questionnaire-text.md)
-   [Configure VAM property to enable scoped caching](../task/hcls-vam-enable-scoped-cache.md)
-   [Encryption options in Vaccine Administration Management](../task/vam-encryption-support.md)

-   **[Install Vaccine Administration Management](../task/hcls-install-vaccine-management.md#)**  
Vaccine Administration Management \(VAM\) is available on the ServiceNow Store.
-   **[Create vaccine models](../task/add-vaccine-inventory.md)**  
Create a vaccine model to track and manage different vaccines under Vaccine Administration Management.
-   **[Create vaccine consumable assets](../task/create-vaccine-consumable-assets.md)**  
Create a vaccine consumable asset and associate it with a vaccine model.
-   **[Create vaccination programs](../task/hcls-create-vaccination-program.md)**  
Create vaccination programs to track and manage vaccinations.
-   **[Configure the eligibility criteria for a vaccination program](../task/configure-eligibility-for-appointment-booking.md)**  
Configure the eligibility criteria that users must meet to be eligible for a vaccination program.
-   **[Configure advanced appointment scheduling for a center](../task/configure-location-level-weekly-schedule-config.md)**  
Configure advanced appointment scheduling for a center. Advanced appointment scheduling enables you to configure different vaccination schedules, weekly, daily, and more, and the capacity to meet the changing needs of different location centers and programs.
-   **[Configure inventory-based scheduling for a center](../task/configure-scheduling-by-inventory.md)**  
Configure scheduling based on available inventory for a center.
-   **[Configure vaccine appointment scheduling](../task/vaccine-appt-booking.md)**  
Appointments are automatically scheduled when users request a vaccination through the portal or when using mass booking. Define a schedule for the automatic appointment creation to follow, like creating appointments on specific days of the week or during specific time frames.
-   **[Multi-vaccine appointment bookings configuration](multi-vaccine-appointment-bookings-configuration.md)**  
Administer multi-vaccine appointment bookings based on auto-selection and manual selection of the vaccine method. You can select your preferred vaccine method based on the eligibility criteria, order of method selection, and inventory availability.
-   **[Book appointments for subsequent doses after a previous dose is complete](../task/schedule-second-appointment-after-completion-of-first.md)**  
Define whether to enable booking for all doses of the vaccine, for both mass booking and self-service, or to enable booking for the first dose, with subsequent appointments booked after the first dose is administered.
-   **[Privacy policy settings for Vaccine Administration Management](privacy-policy-VAM.md)**  
Users are required to provide their privacy consent at the time of registration on the Vaccine Administration Management portal.
-   **[Customize vaccination notification emails](vaccine-emails.md)**  
Customize the vaccination notification emails that are sent to users about vaccination appointments. Using the customizations, you can keep users informed about activities, such as updates to vaccination booking appointments.
-   **[Mass book vaccine appointments](../task/hcls-vaccine-mass-booking.md)**  
Schedule appointments for multiple users at the same time instead of having users individually request appointments in the self-service portal.
-   **[Cancel appointments in a given date range](../task/cancel-appointment-over-date-range.md)**  
Cancel multiple appointment bookings at a location in a given date range.
-   **[Configure the Patient Portal for Vaccine Administration Management](hcls-vam-configure-patient-portal.md)**  
Complete all configuration tasks to confirm that the Vaccine Administration Management \(VAM\) Patient Portal is set up correctly for the user.
-   **[Turn off automatic email notifications for mass booking](../task/turn-off-automatic-email-notifications-for-mass-booking.md)**  
Turn off automatic email notifications by first turning off the default notification for the appointment configuration, then turn off the corresponding business rule. By default, email notifications are automatically sent to users when the appointments are scheduled as part of mass booking.
-   **[Configure an appointment reminder and pre-appointment questionnaire](../task/configure-vaccine-user-questionnaire.md)**  
By default, appointment reminders aren’t sent to the user. To enable appointment reminders, you must configure the appointment reminder in the appointment configuration record. You can also configure the pre-appointment questionnaire for users.
-   **[Retry booking for skipped appointment records](../task/Retry-process-booking.md)**  
Book vaccination requests for skipped appointment records for users whose appointments were unsuccessful or skipped due to missing data.
-   **[Encrypt search fields to appear in search assist](../task/Configure-fields-for-search-assist.md)**  
Encrypt search fields to search from a field other than the first name, last name, and phone fields. By encrypting search fields, you can configure them to appear in search assist.
-   **[Manage high number of concurrent bookings](managing-high-number-of-concurrent-booking.md)**  
Manage multiple parallel queues to help process mass booking appointments run in a parallel mode. You can distribute the mass booking event processors to different nodes rather than keeping the load on a single node.
-   **[Manage processing for a high number of concurrent vaccine events](managing-high-number-of-concurrent-vaccine-events.md)**  
Manage multiple parallel queues to help process vaccine events run in a parallel mode. You can distribute the vaccine queue events process to different nodes rather than keeping the load on a single node.
-   **[Configure the questionnaire text for the user and clinician portals](../task/configure-vam-portal-questionnaire-text.md)**  
Configure the questionnaire text that is displayed in the user and clinician portals for Vaccine Administration Management.
-   **[Configure VAM property to enable scoped caching](../task/hcls-vam-enable-scoped-cache.md)**  
Use a scoped cache instead of a global cache in Vaccine Administration Management to improve application performance.

**Parent Topic:**[Vaccine Administration Management](hcls-vam.md)

