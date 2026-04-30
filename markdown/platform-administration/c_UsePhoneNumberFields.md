---
title: Phone number field type
description: The E.164 phone number standard ensures that all necessary information for a phone number is included and properly formatted to successfully route an international call over a territory's public telephone network.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Field types, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
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

-   **[Territories assigned](c_TerritoriesAssigned.md)**  
Territories are assigned to locations, and are not assigned directly to users.
-   **[Dependent fields](c_SpecifyDependentFields.md)**  
In the dictionary, you can specify a dependent field in the **User** or **Location** field, which displays the appropriate territory in the selector choice list when a user enters a phone number.
-   **[E.164 phone number field configuration](../reference/r_ConfigureE.164PhoneNumberFields.md#)**  
Administrators can use the phone number system properties and dictionary attributes to do certain things.
-   **[Configure a territory phone display rule](../task/t_ConfigATerritoryPhoneDisplRule.md#)**  
The string of numbers that make up a phone number is automatically validated and formatted for a specific territory by applying a series of regular expressions.

**Parent Topic:**[Field types](../../reference-pages/reference/r_FieldTypes.md)

