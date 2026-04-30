---
title: Code Signing
description: Code Signing creates digital signatures for the data which later are checked to confirm the authenticity and integrity of the data. Code Signing is a module licensed as a component of ServiceNow Vault.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Platform Security]
---

# Code Signing

Code Signing creates digital signatures for the data which later are checked to confirm the authenticity and integrity of the data. Code Signing is a module licensed as a component of ServiceNow Vault.

## Code signing and Circle of Trust

The Circle of Trust \(COT\) is a prerequisite for Code Signing that creates secure communication between your trusted and protected instances to ensure that only authorized users can access the Code Signing feature.

Multiple security measures help to prevent malicious actors from disabling or misusing code signing in the case a protected instance is compromised. As part of the defense-in-depth strategy, the COT uses the following components:

-   Controls that restrict even the most powerful administrator accounts are established in the protected instance to help protect Code Signing processes and configuration.
-   Trusted instances are required to work together with protected instances to establish the Circle of Trust relationship. At least one trusted instance is required, but multiple trusted instances may be configured to collaborate with the protected instance.



    ![Circle of trust diagram.](../image/circle-trust-overview.png)

    The Circle of Trust uses jobs, scripts, and business rules along with a key pair to generate signatures to sign update sets to the protected instance. When the job is called, the signature is verified along with the trusted certificate to execute protected instance updates.



    ![Diagram that shows the trusted update sets process.](../image/cot-updatesets-overview-remake.png)

    ![Diagram that shows the different workflows for code signing.](../image/code-signing-flow-remake.png "Code Signing flow")


The Circle of Trust requires an initial trust relationship between trusted and protected instances that prevents any unauthorized user with any authorization level from accessing unapproved activities.

## Get started

<table id="table_mlx_cnb_mzb" class="nav-card"><tbody><tr><td>

[Explore![](../../../reuse/icons/brand-icons/bus-explore.svg)](explore-code-signing.md)

 [Learn the key features and business value of Code Signing.](explore-code-signing.md)

</td><td>

[Configure![](../../../reuse/icons/brand-icons/bus-sdlc.svg)Activate and configure Code Signing.](config-code-signing.md)

</td><td>

[Reference![](../../../reuse/icons/brand-icons/bus-learn.svg)Get details about properties and troubleshooting](../reference/code-signing-reference.md)

</td></tr><tr><td>

 

</td><td>

[Use![](../../../reuse/icons/brand-icons/bus-monitor.svg)Learn how to use Code Signing to help verify the authenticity and integrity of your data.](using-code-signing.md)

</td><td>

 

</td></tr></tbody>
</table>## Troubleshoot and get help

-   [https://www.servicenow.com/community/secops/ct-p/security-operations](https://www.servicenow.com/community/secops/ct-p/security-operations)
-   [Search the Known Error Portal for known error articles](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0597477)
-   [Contact Customer Service and Support](https://support.servicenow.com/now?draw=case)

-   **[Exploring Code Signing](explore-code-signing.md)**  
Code Signing provides cryptographic verification to ensure that only authorized scripts can execute on MID Servers. Code Signing prevents unauthorized or tampered ECC queue records from being processed by MID Servers, maintaining the integrity of integrations between ServiceNow and external systems.
-   **[Configuring Code Signing](config-code-signing.md)**  
Activate and configure Code Signing to verify the authenticity and integrity of your data.
-   **[Using Code Signing](using-code-signing.md)**  
Learn how to sign records, messages, and attachments to help verify the authenticity and integrity of your data.
-   **[Code Signing Health and Status Dashboard](../../code-signing/concept/code-signing-health-and-status-dashboard.md)**  
The Code Signing Health and Status dashboard provides a centralized, user-friendly view of your Code Signing environment's health and configuration. Use it to identify issues, verify configuration accuracy, and support secure, uninterrupted code-signing operations.

**Parent Topic:**[Platform Security](../../general/concept/platsec-sublanding.md)

