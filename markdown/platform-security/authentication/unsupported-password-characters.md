---
title: Unsupported password characters
description: There are password characters that are not supported. Users cannot use these characters, based on ServiceNow password complexity requirements.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Password complexity requirements, Local Authentication, Authentication, Access Management]
---

# Unsupported password characters

There are password characters that are not supported. Users cannot use these characters, based on ServiceNow password complexity requirements.

To enable a secure network environment, it is necessary for users to use strong passwords that include combination of letters, numbers, and symbols. These combinations help to prevent unauthorized users who usually use manual or automated methods to guess weak passwords.

-   The password policy requirements are based on the Basic Multilingual Plane \(BMP\) that contains characters for all modern languages. ServiceNow instance is shipped with BMPs of around 10000 characters.
-   Password characters within this permissible BMPs can be set for your instance, the password characters that do not adhere within this BMPs are not allowed.

**Note:** User or company-specific characters that cannot be used in the password can be configured in the exclude password list.

For more information about the password policy properties, see [password policy properties](../reference/password-policy-properties.md).

