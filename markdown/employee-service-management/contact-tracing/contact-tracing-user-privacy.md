---
title: User privacy consent for Contact Tracing
description: The Contact Tracing application enables you to send notification to users seeking their consent for contact tracing. You can use user data for contact tracing based on the privacy configuration set for a location and the user response to the privacy consent.
locale: en-US
release: australia
product: Contact Tracing
classification: contact-tracing
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Maintaining user data privacy in Contact Tracing, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# User privacy consent for Contact Tracing

The Contact Tracing application enables you to send notification to users seeking their consent for contact tracing. You can use user data for contact tracing based on the privacy configuration set for a location and the user response to the privacy consent.

You can determine whether privacy consents are needed for specific locations. If a location does not need privacy consent, the user data belonging to that location can be automatically considered for contact tracing.

If a location requires privacy consents and a user has not consented to use the data, that user will be flagged, which has the following impact in contact tracing:

-   You can create a case for those users but cannot run a diagnostic request for them.
-   You cannot create a diagnostic request to identify potentially impacted users for those users.
-   If a diagnostic request was created for the user before the user declined to give consent, you cannot run the diagnostic request.
-   In a diagnostic request for another affected user, non-consenting users are excluded in the impacted users list. However, they can be added to the impacted users manually.

Privacy consent requirements ensure that your users complete a privacy consent before entering the workplace to facilitate the use of their data for contact tracing.

-   Users who agree to the use of their data for contact tracing, the status of their privacy consent requirement updates to Clear. Meeting the privacy consent requirement makes those users eligible to enter the workplace.
-   Users who disagree to the use of their data for contact tracing, the status of their privacy consent requirement updates to Not Clear. Meeting the privacy consent requirement makes those users eligible to enter the workplace.

**Important:** Any data collected for contact tracing before a user withdraws consent remains in the system. The data will be deleted from the system depending on your data retention settings.

## Setting up privacy consents for Contact Tracing

As an admin, you must configure the following settings to use privacy consents with Contact Tracing:

1.  [Modify or add a privacy consent template for Contact Tracing](../task/define-privacy-consent-template.md)
2.  [Generate location-based privacy configurations for Contact Tracing](../task/generate-location-privacy-configuration.md)
3.  [Create a custom Emergency Outreach notification channel](../task/create-additional-channel-notif.md)
4.  [Configure an email notification for a privacy consent request](../task/configure-privacy-email.md)
5.  [Configure an Emergency Outreach notification for Contact Tracing privacy consents](../task/configure-outreach-notif-privacy.md)

**Parent Topic:**[Maintaining user data privacy in Contact Tracing](contact-tracing-user-privacy-options.md)

