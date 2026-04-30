---
title: Phone number field type
description: The E.164 phone number standard ensures that all necessary information for a phone number is included and properly formatted to successfully route an international call over a territory's public telephone network.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Field types reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Phone number field type

The E.164 phone number standard ensures that all necessary information for a phone number is included and properly formatted to successfully route an international call over a territory's public telephone network.

When a user enters a phone number, it is received and stored as a string of numbers. An E.164 phone number field automatically formats and validates the numbers so that they are E.164-compliant when displayed as local and international numbers. The E.164 phone number field type does not replace the phone field type.

An E.164 phone number field displays:

-   \[Optional\] A choice list for the phone number territory.
-   \[Always\] An input box for entering phone numbers.
-   \[By Default\] A red underline when a phone number does not match the format for the selected phone territory and cannot be saved.
-   \[Optional\] A green underline when a phone number does not match the format for the selected phone territory but can be saved with **Other / Unknown** as the territory.

![](../image/PhoneE164.png "Phone e164")

