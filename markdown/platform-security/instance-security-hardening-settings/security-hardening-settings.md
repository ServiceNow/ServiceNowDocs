---
title: Hardening settings
description: The ServiceNow Security Center \(SSC\) hardening settings content contains detailed descriptions and compliance values for the security-related system properties and plugins in the ServiceNow AI Platform. You can set these properties using the hardening settings app in the Security Center.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Platform Security]
---

# Hardening settings

The ServiceNow Security Center \(SSC\) hardening settings content contains detailed descriptions and compliance values for the security-related system properties and plugins in the ServiceNow AI Platform. You can set these properties using the hardening settings app in the Security Center.

## Overview and purpose

The Security Center calculates a daily compliance score, expressed as a percentage that is based on how compliant your current instance security settings are with the compliance values in Security Center hardening settings.

You can manage the specific security configuration settings that may affect the score for your instance directly from the Security Center.

The hardening settings configurations are explained with several attributes described in the table.

<table id="table_mtb_wsf_swb"><thead><tr><th>

Configuration attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Overview

</td><td>

Provides a high level overview of the recommendation.

</td></tr><tr><td>

Configuration name

</td><td>

The property or plugin name.

</td></tr><tr><td>

Configuration type

</td><td>

Describes where the property can be configured outside of the Security Center, such as in system properties \(**sys\_properties\_list.do**\).

</td></tr><tr><td>

Data type

</td><td>

Describes the type of value required for the configuration. Examples are true/false boolean, installation, plugin, string, etc.

</td></tr><tr><td>

Recommended value

</td><td>

The value that is recommended by the Security Center to enhance security compliance in your instance.

</td></tr><tr><td>

Default value

</td><td>

The value that the configuration is set to in the base system.

</td></tr><tr><td>

Category

</td><td>

The name and link to the category for the hardening setting.

</td></tr><tr><td rowspan="3">

Security risk

</td><td>

**Severity score**: The score indicates the potential security risk to your instance as per the likelihood of the vulnerability to be exploited. The security vulnerability is considered and scored individually using the CVSS \(Common Vulnerability Scoring System\) score on a scale ranging from **0.0** to **10.0**. See [https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator](https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator) for additional information.

</td></tr><tr><td>

**Severity rating per CVSS score**: -   Critical: 9.0-10.0
-   High: 7.0-8.9
-   Medium: 4.0-6.9
-   Low: .01-3.9
-   None: 0.0

</td></tr><tr><td>

**Security risk details**: Describes the importance of the setting configuration and the risk of not utilizing the recommended configuration.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

Related settings or configurations that are required before or in conjunction with the hardening configuration.

</td></tr><tr><td>

Functional impact

</td><td>

The impact this hardening setting has on the operation of your instance.

</td></tr><tr><td>

References

</td><td>

Links to configuration documentation or other helpful information.

</td></tr></tbody>
</table>**Note:** Some of the configurations can only be completed by Customer Service and Support and will be indicated as such.

To learn more about ensuring your instances meet hardening requirements, see [Security hardening](../concept/sc-hardening.md).

## Other resources

For user reference, the ServiceNow AI Platform maintains extensive configuration capabilities information in the product documentation. You access most of the security content using the links found in [Secure your instance](../../general/concept/platsec-landing.md). Also, see the following:

-   Available system properties
-   General security settings properties
-   [High Security Settings](../../security/concept/c_HighSecuritySettings.md)

-   **[Hardening settings baseline versions](../concept/hardening-settings-baseline.md)**  
Explore how baseline versions for hardening settings align with family and store releases.
-   **[Access control](sc-access-control.md)**  
The access control category audits the process of protecting resources from unauthorized access through granting and denying requests based on a permission model. This includes ensuring an entity accessing a resource holds valid credentials to do so, creating and protecting a well-defined set of roles or permissions and ensuring role or permission controls are protected from replay and tampering.
-   **[API and web service](sc-api-web-service.md)**  
The API and Web Service category ensures that applications have appropriate authentication, authorization and session management, validate all input that traverses a trust boundary and include security controls for all API types.
-   **[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)**  
This broad control addresses high level design considerations and key elements to implement a secure application. This covers the tenants of availability, confidentiality processing integrity, non-repudiation and privacy. Additionally, elements of a secure software development lifecycle are included.
-   **[Authentication](sc-authentication.md)**  
The authentication category covers the main elements of modern authentication to confirm an entity and its claims are authentic and correct, resistant to impersonation and prevent interception of passwords.
-   **[Business Logic](sc-business-logic.md)**  
This category looks at the logic and flow unique to each application with general secure principles. Specifically ensure that the intended sequence of business logic flow cannot by bypassed, that limits exist to detect and prevent automated attacks, and that protections against spoofing, tampering, information disclosure and elevation of privilege attacks exist.
-   **[Communications](sc-communications.md)**  
This control ensures proper encryption using strong algorithms and ciphers. This includes ensuring the recommended version of TLS is used for client connectivity, use of strong cipher suites, use of trusted and signed certificates, ensuring connections are encrypted between components and logging of connection failures.
-   **[Configuration](sc-configuration.md)**  
The Configuration category ensures applications have a secure build environment and hardened third party library components. Specifically, ensuring a build and deploy pipeline is repeatable and includes automated testing and prevents known security issues from being deployed. This includes keeping dependencies up to date and free from known vulnerabilities.
-   **[Data protection](sc-data-protection.md)**  
The data protection category addresses the elements of confidentiality, integrity and availability \(CIA\) of data.
-   **[Error handling and logging](sc-error-handling-logging.md)**  
The error handling and logging category addresses the quality and verbosity of logged information exposed to stakeholders.
-   **[File and resources](sc-file-resources.md)**  
The file and resources category ensures applications handle untrusted file data securely and store untrusted data from untrusted sources with limited permissions in an appropriate location.
-   **[Malicious code](sc-malicious-code.md)**  
The Malicious Code category ensures that best efforts are made to confirm that your code is free of vulnerabilities and unwanted functionality.
-   **[Session management](sc-session-management.md)**  
This category looks at the security of the application state for a user. Sessions should be unique to each individual, unable to be guessed or shared, and invalidated after periods of inactivity or when not required. This includes factors such as cookie attributes for cookie-based sessions, session token generation, and storage and requirements for federated re-authentication.
-   **[Stored cryptography](sc-stored-cryptography.md)**  
This category focuses on the encryption of stored data. It encompasses several key aspects, such as employing established algorithms and cryptographic modules, ensuring the proper generation of pseudo-random values, implementing encryption based on data classification, and securely storing and isolating key material.
-   **[Validation, sanitization, and encoding](validation-sanitization-encoding.md)**  
Validation, sanitization, and encoding addresses input validation to prevent against vulnerabilities like Cross-Site Scripting \(XSS\), SQL injection and other attacks.

**Parent Topic:**[Platform Security](../../general/concept/platsec-sublanding.md)

