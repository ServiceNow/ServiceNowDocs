---
title: Configuring Code Signing
description: Activate and configure Code Signing to verify the authenticity and integrity of your data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/config-code-signing.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Code Signing, Platform Security]
---

# Configuring Code Signing

Activate and configure Code Signing to verify the authenticity and integrity of your data.

\[Omitted image "cse-process.png"\] Alt text: Overall process for Code Signing configuration

Code Signing Enterprise requires an initial trust relationship between trusted and protected instances that helps to prevent any unauthorized user with any authorization level from accessing unapproved activities.

Refer to each topic to complete the configuration steps to establish the Circle of Trust with Code Signing Enterprise:

-   **[Assign the Code Signing Administrator Role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/cse-assign-roles.md)**

    Assign the Code Signing Administrator role to a user to access the Code Signing configuration experience.

-   **[Configure Code Signing Enterprise on your trusted instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/cse-turn-on-cse.md)**

    Turn on Code Signing on your trusted instance.

-   **[Upload your Code Signing configuration file to your protected instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/cse-upload-cs-config.md)**

    Upload the configuration file generated on your trusted instance.

-   **[Configure Code Signing Enterprise on your protected instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/cse-ppi-config.md)**

    Turn on and configure Code Signing on your protected instance.

-   **[Turn on certificate validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/cse-turn-on-cert-validation.md)**

    Turn on certificate validation on your instance.

-   **[Turn off Code Signing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/cse-turn-off-cse.md)**

    Disable code signing on your protected instance.

    **Note:** This optional step isn’t part of the initial configuration for Code Signing


