---
title: Explore Password complexity requirements
description: Passwords in your ServiceNow instance must meet complexity requirements.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Password complexity requirements, Local authentication, Authentication, Access Management]
---

# Explore Password complexity requirements

Passwords in your ServiceNow® instance must meet complexity requirements.

The Passwords complexity requirements policy setting determines whether passwords must meet a series of strong-password guidelines.

Password complexity requirements are enforced when a password is changed or created.

Password complexity requirements adhere and work based on the following:

-   If the **glide.apply.password\_policy.on\_login** property is enabled, the password policy check is enforced against the user during login. During login, the user must adhere to the password policy and change the password for the instance.
-   The password policy requirements are based on the Basic Multilingual Plane \(BMP\) that contains characters for all modern languages. ServiceNow instances are shipped with BMPs of around 10,000 characters.
-   Passwords within the permissible BMPs can be set for your instance. Passwords that do not adhere within these BMPs are not allowed.

If needed, you can require that passwords are changed regularly, at least every 90 days.

## Requirements and banned characters

To enable a secure network environment, it is necessary for users to use strong passwords that include combination of letters, numbers, and symbols. These combinations help to prevent unauthorized users who usually use manual or automated methods to guess weak passwords.

The password to your instance must meet the following requirements:

-   Minimum 8 characters.
-   Maximum 100 characters.
-   Contains lower case and upper case characters
-   Contains special characters.
-   Contains digits.

You can ban a list of common bad passwords, such as the following:

-   Predictable and repeating sequences such as "123456", "qwerty", "!@\#$%^", "aaaaa", and so on.
-   Employee name or user names.
-   Relevant brand or product names.
-   Locations, such as company headquarters, city, country, and so on.
-   Company-specific internal terms or abbreviations.
-   Emojis.

**Note:** User, brand, or company-specific characters that cannot be used in the password can be configured in the Password Policy or Exclude Password page.

