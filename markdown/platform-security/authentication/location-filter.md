---
title: Location filter
description: Location filter criteria can be used as filter input for users based on the user location.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/authentication/location-filter.html
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Filter criteria, Adaptive authentication, Authentication, Access Management]
---

# Location filter

Location filter criteria can be used as filter input for users based on the user location.

Location filter is a filter criteria that the admins can use while crafting the authentication policies based on the physical location of the device.

**Note:**

-   Location filter is available with the Zero Trust Access feature. For more information, see [Zero Trust Access \(ZTA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/session-access.md).
-   The instance should be on ADCv2. If the instance isn’t on ADCv2, then user location information won’t be available.

The location filter criteria enable you to perform the following:

-   Act as policy input for policy conditions to verify and meet the requirements for authentication.
-   Provide an ability to create adaptive authentication policies based on the **country**.
-   Allow or not allow instance access to a given geography.
-   Use the geo location-based pre-authentication or post authentication policy to:
    -   Block access from sanctioned countries and from outside a tight privacy-controlled region, at company discretion.
    -   Allow access only to areas within the applicable privacy region, at company discretion.
    -   Configure country-based allow list for authentication.

## Use cases

Following are some of the use cases for using location filter criteria for Adaptive Authentication:

-   Block access to the instance from a country.
-   Allow access to the instance only from a particular country.
-   Enforce step-up authentication or MFA to log in based on country.
-   Reduce or limit roles for the user based on the country.
-   Location filter criteria can be used for MFA, Zero Trust Access \(ZTA\), pre-authentication context, and post-authentication context.

## Location Identification

The location services for identifying the location of the user are provided by a third-party service - MaxMind.

The location of the user is identified through the VPN, from the x-forwarded-for header. If there’s no header populated by the service, then only the VPN IP \(location\) is displayed as the user location.

**Note:** If there are incorrect locations displayed after the location filter configuration, see the [KB article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1436102) to troubleshoot.

