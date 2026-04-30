---
title: Configuring Code Signing
description: Activate and configure Code Signing to verify the authenticity and integrity of your data.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Code Signing, Platform Security]
---

# Configuring Code Signing

Activate and configure Code Signing to verify the authenticity and integrity of your data.

![Overall process for Code Signing configuration](../image/cse-process.png)

Code Signing Enterprise requires an initial trust relationship between trusted and production instances that helps to prevent any unauthorized user with any authorization level from accessing unapproved activities.

Refer to each topic to complete the configuration steps to establish the Circle of Trust with Code Signing Enterprise:

-   **[Assign the Code Signing Administrator Role](../task/cse-assign-roles.md)**

    Assign the Code Signing Administrator role to a user to access the Code Signing configuration experience.

-   **[Configure Code Signing Enterprise on your trusted non-production instance](../task/cse-turn-on-cse.md)**

    Turn on Code Signing on your Trusted non-production instance \(TNPI\).

-   **[Upload your Code Signing configuration file to your protected production instance](../task/cse-upload-cs-config.md)**

    Upload the configuration file generated on your trusted non-production instance.

-   **[Configure Code Signing Enterprise on your protected production instance](../task/cse-ppi-config.md)**

    Turn on and configure Code Signing on your Protected production instance \(PPI\).

-   **[Turn on certificate validation](../task/cse-turn-on-cert-validation.md)**

    Turn on certificate validation on your instance.

-   **[Turn off Code Signing](../task/cse-turn-off-cse.md)**

    Disable code signing on your protected production instance \(PPI\).

    **Note:** This optional step isn’t part of the initial configuration for Code Signing


-   **[Assign the Code Signing Administrator Role](../task/cse-assign-roles.md)**  
Assign the Code Signing Administrator role to a user to access the Code Signing configuration experience.
-   **[Configure Code Signing Enterprise on your trusted non-production instance](../task/cse-turn-on-cse.md)**  
Turn on and configure Code Signing on your Trusted non-production instance \(TNPI\).
-   **[Upload your Code Signing configuration file to your protected production instance](../task/cse-upload-cs-config.md)**  
Upload the configuration file generated on your trusted non-production instance.
-   **[Configure Code Signing Enterprise on your protected production instance](../task/cse-ppi-config.md)**  
Turn on and configure Code Signing on your Protected production instance \(PPI\).
-   **[Turn on certificate validation](../task/cse-turn-on-cert-validation.md)**  
Protect your instance with certificate based validation.
-   **[Turn off Code Signing](../task/cse-turn-off-cse.md)**  
Disable code signing on your protected production instance \(PPI\).
-   **[Create Code Signing key pairs and certificates](../reference/create-key-pairs-and-certs.md)**  
Create two key pairs to signed certificates to establish trust between your production and trusted instances.
-   **[Specify custom rules in ECC firewall](../task/custom-yaml-conf.md)**  
Configure the External Communication Channel \(ECC\) firewall in your MID Server by specifying the custom rules to selectively allow or reject the incoming message and override the Code Signing configuration.
-   **[Change your Root of Trust configuration](change-rot-overview.md)**  
Trust and use your own certificates instead of relying on ServiceNow build certificates \(default\) by changing to use your Root of Trust \(ROT\). ServiceNow components like script includes, business rules, etc., are signed at build time using a ServiceNow build time key \(verification certificate is the ServiceNow build certificate\).

**Parent Topic:**[Code Signing](code-signing-landing.md)

