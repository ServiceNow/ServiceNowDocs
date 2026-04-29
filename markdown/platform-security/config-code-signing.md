---
title: Configuring Code Signing
description: Activate and configure Code Signing to verify the authenticity and integrity of your data.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Code Signing, Platform Security]
---

# Configuring Code Signing

Activate and configure Code Signing to verify the authenticity and integrity of your data.

![Overall process for Code Signing configuration](../image/cse-process.png)

Code Signing Enterprise requires an initial trust relationship between trusted and protected instances that helps to prevent any unauthorized user with any authorization level from accessing unapproved activities.

Refer to each topic to complete the configuration steps to establish the Circle of Trust with Code Signing Enterprise:

-   **[Assign the Code Signing Administrator Role](../task/cse-assign-roles.md)**

    Assign the Code Signing Administrator role to a user to access the Code Signing configuration experience.

-   **[Configure Code Signing Enterprise on your trusted instance](../task/cse-turn-on-cse.md)**

    Turn on Code Signing on your trusted instance.

-   **[Upload your Code Signing configuration file to your protected instance](../task/cse-upload-cs-config.md)**

    Upload the configuration file generated on your trusted instance.

-   **[Configure Code Signing Enterprise on your protected instance](../task/cse-ppi-config.md)**

    Turn on and configure Code Signing on your protected instance.

-   **[Turn on certificate validation](../task/cse-turn-on-cert-validation.md)**

    Turn on certificate validation on your instance.

-   **[Turn off Code Signing](../task/cse-turn-off-cse.md)**

    Disable code signing on your protected instance.

    **Note:** This optional step isn’t part of the initial configuration for Code Signing


-   **[Assign the Code Signing Administrator Role](../task/cse-assign-roles.md)**  
Assign the Code Signing Administrator role to a user to access the Code Signing configuration experience.
-   **[Configure Code Signing Enterprise on your trusted instance](../task/cse-turn-on-cse.md)**  
Turn on and configure Code Signing on your trusted instance.
-   **[Upload your Code Signing configuration file to your protected instance](../task/cse-upload-cs-config.md)**  
Upload the configuration file generated on your trusted instance.
-   **[Configure Code Signing Enterprise on your protected instance](../task/cse-ppi-config.md)**  
Turn on and configure Code Signing on your protected instance.
-   **[Turn on certificate validation](../task/cse-turn-on-cert-validation.md)**  
Protect your instance with certificate based validation.
-   **[Quorum Controlled Certificate Revocation](certificate-revocation.md)**  
The quorum-controlled certificate revocation for Code Signing certificates provides a secure mechanism for a Code Signing admin to revoke Code Signing certificates. The revocation process involves submitting a request that requires approval from multiple stakeholders. This workflow helps to prevent accidental or unauthorized revocations.
-   **[Turn off Code Signing](../task/cse-turn-off-cse.md)**  
Disable code signing on your protected instance.
-   **[Load required key pairs and certificates for Code Signing](../task/circle-trust-setup.md)**  
Establish the relationship in a designated trusted instance using Code Signing. This first step loads two cryptographic keys into the trusted environment to establish a trusted source for updates to the production instance.
-   **[Prepare Circle of Trust certificates](../task/create-updateset-nonprod.md)**  
Create an update set in the trusted environment to export the trusted certificate to the production environment.
-   **[Import and install certificates for Circle of Trust](../task/retrieve-updateset-prod.md)**  
Retrieve the update set in production to establish the trust relationship between the two instances. The certificates that have been created to represent trust in the trusted instance must be accepted into the protected instance.
-   **[Turn on Code Signing](../task/enable-codesiging.md)**  
Turn on Code Signing in your trusted non-production instance to identify the trusted instances linking to your production instance.
-   **[Create Code Signing key pairs and certificates](../reference/create-key-pairs-and-certs.md)**  
Create two key pairs to signed certificates to establish trust between your protected and trusted instances.
-   **[Specify custom rules in ECC firewall](../task/custom-yaml-conf.md)**  
Configure the External Communication Channel \(ECC\) firewall in your MID Server by specifying the custom rules to selectively allow or reject the incoming message and override the Code Signing configuration.
-   **[Change your Root of Trust configuration](change-rot-overview.md)**  
Trust and use your own certificates instead of relying on ServiceNow build certificates \(default\) by changing to use your Root of Trust \(ROT\). ServiceNow components like script includes, business rules, etc., are signed at build time using a ServiceNow build time key \(verification certificate is the ServiceNow build certificate\).

**Parent Topic:**[Code Signing](code-signing-landing.md)

