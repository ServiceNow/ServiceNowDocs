---
title: Best Practices
description: Learn details about the Best Practices in the Security Posture Console.
locale: en-US
release: australia
product: Security Center
classification: security-center
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 17
breadcrumb: [Security Best Practices, Security posture console, Security Center, Platform Security]
---

# Best Practices

Learn details about the Best Practices in the Security Posture Console.

<table id="table_bmy_gzy_fgc"><thead><tr><th>

Best Practice

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activate the ServiceNow Access Control plugin

</td><td>

Use the ServiceNow Access Control plugin to control which employees can access your instance, and when. Enforcing a default deny posture for all users except those users you specify. This can include ServiceNow employees. Using this plugin helps prevent unwanted access to your instance.

 **Note:** After ServiceNow Access Control is activated, personnel must explicitly request access from you on an ad-hoc and temporary basis.

 For details on this plugin, see [ServiceNow access control](../../security/concept/c_SNCAccessControl.md).

</td></tr><tr><td>

Appoint and add a security contact in your instance

</td><td>

Select an information security contact within your organization who receives security-related information from the Security Team. This contact is in addition to your admin, who also receives these updates.

 This information could be security issues, security alerts, or details about important software updates.

 For details on adding a security contact, see [KB0621516](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0621516).

</td></tr><tr><td>

Change the default login credentials

</td><td>

Change the passwords on your instance's built-in user accounts, such as admin, ITIL, and employee. These accounts are provisioned with default passwords, unique to your instance, but should be changed as soon as possible.

 For details on how to change the passwords for user accounts on your instance, see [Configure password for a user](../../../integrate/authentication/task/reset-your-password.md).

</td></tr><tr><td>

Configure web browsers to use only TLS 1.2 or higher when connecting to your instance

</td><td>

Verify that browsers that connect to your instance are using the more secure Transport Layer Security \(TLS\) 1.2. This change can be made on the browser or enforced by your web proxy or other gateway.

 Consult the documentation for your browser, web proxy, or gateway for steps on how to configure those products to use only TLS 1.2.

</td></tr><tr><td>

Configure your email systems to accept mail from your instance by using SPF

</td><td>

If your organization uses Sender Policy Framework \(SPF\) to control inbound email with anti-spam technology, you must configure it to accept email originating from your instance. Configure SPF to query the SPF records dynamically.

 If SPF isn’t an option, another approach is to add the mail server IP addresses to your allow list. This configuration must be monitored as the addresses could be subject to change.

 For steps and additional details on these solutions, see [KB0535456](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0535456)

</td></tr><tr><td>

Consider limiting file attachments, uploads, and downloads

</td><td>

Restrict attachment uploads by role, file extension, MIME type, or size to help prevent potentially malicious files being stored and delivered from your instance. You can also control which file types can be downloaded, including by MIME type, and prevent image access by unauthenticated users.

 These attachment restrictions are controlled by system properties on your instance. For details on their configuration, see [Configure attachment system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_DisablingTheDragAndDropFeature.md).

</td></tr><tr><td>

Disable browser SQL messages

</td><td>

Prevent SQL error messages from being presented in the web browser. Though useful to users and developers, these messages can be used by attackers to learn information about your system or to help guide their attempts to access your data. These messages can be turned off using a system property.

 For details on this system property, see [Disable SQL error messages](sc-disabling-sql-error-messages.md).

</td></tr><tr><td>

Disable password-less authentication

</td><td>

Help ensure strong authentication by disabling password-less authentication when possible. Without disabling password-less authentication, potential attackers could gain access to your instance by correctly guessing a user name \(such as firstname.lastname or a role title\).

 You can disable password-less authentication on your instance using a system property. For details on this property see [Disable password-less authentication](sc-disable-password-less-authentication.md).

</td></tr><tr><td>

Enable table auditing for important or sensitive data

</td><td>

Track changes to your data using table auditing. Auditing tracks the creation, update, and deletion of all records in the table where it’s enabled, enabling admins to track changes to important or sensitive data. Admins can also choose to select specific fields in a table for auditing to see more targeted results or to reduce performance impact.

 For details on auditing on instances, see [Auditing](../../time/concept/c_AuditedTables.md).

 For specific instructions on enabling auditing on a table, see [Configuring auditing for a table](../../security/task/t_EnableAuditingForATable.md).

</td></tr><tr><td>

Encrypt data at rest within the instance

</td><td>

Encrypt your data to maintain its confidentiality and integrity. Data on your instance can be within the database. You can also elect to subscribe to functionality to encrypt the data volume transparently on the backend. The physical disks on which the instance runs can also be encrypted in their entirety to guard data in case of their loss or theft.

 You can use different methods of encryption simultaneously for data stored in your instance, depending on your use case and the risks you wish to mitigate. For example, you can choose to transparently encrypt your data at rest using database encryption on most tables, cloud encryption on the entire data volume. You could also use full disk hardware encryption, which also requires a dedicated environment to protect against drive or server theft.

 Review the encryption options available with in [Key Management Framework](../../encryption/concept/encryption.md).

</td></tr><tr><td>

Enforce the use of strong passphrases

</td><td>

Use password policies to enforce the length, complexity, expiration, uniqueness, lockout, and more for native and local accounts on your instance. Use these policies to maximize security, encourage the adoption of long passphrases and help to eliminate the use of simple passwords.

 You can retain your existing policies for any external authentication services you have integrated, such as LDAP or SAML.

 For details on password policy configuration, see [Configure your password policy](../../../integrate/authentication/task/set-your-password-policy.md).

</td></tr><tr><td>

Ensure automatic account creation

</td><td>

Use this feature to create user accounts by email dynamically. Activate this feature only if necessary for your business needs, only after you have defined a list of trusted domains from which accounts can be created. You can also control how passwords are assigned to new accounts created this way.

 For details on automatic user creation, see [Enable automatic user creation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_EnablingAutomaticUserCreation.md).

</td></tr><tr><td>

Ensure Secure Access to knowledge bases

</td><td>

Manage access to knowledge bases and articles to help ensure secure and efficient information sharing. You can determine whether certain users or categories of users can access knowledge bases and knowledge articles by controlling contribute and read access.

 The specific configuration depends on your business needs. Learn about your options for configuring knowledge access at [Managing access to knowledge bases and knowledge articles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/user-access-knowledge.md).

</td></tr><tr><td>

Ensure that the High Security plugin is installed and activated

</td><td>

Use the High Security plugin \(HSP\) to enhance security management and applying appropriate settings. High Security Settings provides a central location for security settings, creates a distinct security administrator role, a default deny property, and other important security features.

 HSP is installed and enabled by default on all new instances. You can request HSP activation for older instances, including instances that have had upgrades from an older version. Enabling HSP should be done only after careful testing in a non-production environment, as activation changes some fundamental properties and behaviors.

 For more details on the High Security plugin, see [Enable High Security Plugin](sc-high-security-plugin.md).

</td></tr><tr><td>

Familiarize yourself with NOW security resources

</td><td>

Security information constantly evolves, so it's crucial to stay updated with security resources to keep your information security strong.

 Use the following resources to stay informed about security resources:

 -   [CORE Directory: ServiceNow CORE Compliance Portal](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0959484)
-   [Securing the ServiceNow AI Platform: How ServiceNow protects customer data](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/resource-center/ebook/ebk-how-servicenow-delivers-safe-and-secure-cloud-services.pdf)
-   [Secure your instance](../../general/concept/platsec-landing.md)

</td></tr><tr><td>

Harden your Instance

</td><td>

Use the Security Center Hardening tool to reduce risk by limiting weaknesses that could be exploited, and implement recommended settings to secure your instance further.

 Learn more about Security Center at [Security Center](../concept/sec-center-v2.md).

 Review the available hardening settings at [Hardening settings](security-hardening-settings.md).

</td></tr><tr><td>

Install patches as soon as possible

</td><td>

Install patches and platform updates as soon as possible help ensure the highest levels of security for both your instance and those of other customers. Keeping current with updates also enables you to maintain continuous support by conforming to the EOL policy. Use Upgrade Center to help manage the process.

 Security fixes are routinely released for the Now Platform via the patches and hot fixes that accompany product feature updates. Upgrading when new patches and hot fixes are available helps reduce the risk of potential vulnerabilities.

 Information about Now Platform releases, patches, and hot fixes can be found in the Release Notes section of the product documentation. For more information, see [Phase 1 -](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/upgrades-phase-1.md).

</td></tr><tr><td>

Integrate with MFA

</td><td>

Integrate third-party multi-factor authentication \(MFA\) with your existing SAML IdP to provide additional login security. MFA provides a high level of security because authentication requires multiple authentication factors. Something the user knows \(the password\) as well as something they own \(a one-time code, mobile phone, or biometric attributes, such as a fingerprint\).

 Learn more about MFA integration at [Multi-factor authentication](../../../integrate/authentication/concept/mfa-landing.md).

</td></tr><tr><td>

Limit accepted email sender domains

</td><td>

Control which domains and users your instance can communicate with via email by using system address filters. These filters can be customized to your requirements.

 Learn how to configure trusted domains at [Designate email domains as untrusted or trusted](../../security/task/designate-untrusted-trusted-email-domains.md).

</td></tr><tr><td>

Monitor important logs to help identify any suspicious or malicious activity

</td><td>

The system logs module provides a variety of logs that you can use to troubleshoot and debug transactions and events that take place within the instance.

-   **Event logs**

Event logs reveal much about system activity, including login events \(successful or otherwise\), and privilege escalation.

-   **System logs**

System logs contain extensive information about general activity, including configuration changes, system errors, workflows, and inbound / outbound data connections.


**Note:** The Event and System logs can also be used to provide an audit trail of any activity by personnel.

-   **Transaction logs**

Transaction logs record all web browser-related activity for an instance and can provide details of every request made. Transaction logs can be useful for identifying unusual or malicious activity.

-   **Table auditing and record history**

Enable auditing for database tables. Record history is perpetual and enables you to track and view details of any changes made to the data since its creation. By default, only the incident, problem, and change tables are tracked. For other tables, auditing must be enabled manually.

-   **Import logs**

You can view detailed information related to data import activity into your instance by checking the import logs. These logs include information about source and status, time, and so on

-   **Outbound web services logs**

These show REST and SOAP request activity and can help you to track the volume and destination of connections to external services.


 Learn more about system logs in [System logs](../../system-logs/concept/system-logs.md).

</td></tr><tr><td>

Monitor login failure rates and create alerts

</td><td>

Monitor for unusual activity such as high numbers of failed logins, especially within short time frames. You can create alerts to send emails when a threshold you define is exceeded.

 Learn how to configure these thresholds at [Indicator thresholds](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/pa-threshold.md).

</td></tr><tr><td>

Monitor security events

</td><td>

Review the **My security metrics dashboard** to see the available security metrics for your instance, and set thresholds to generate email notifications for notable activity. Examples of notable activity can include:

 -   **Privilege escalation**

Unexpected modifications made to privileged roles, such as Admin, ITIL\_Admin, or any other roles with higher privileges could indicate suspicious actions.

-   **Failed logins**

Unusual numbers or patterns of failed logins can reveal potential brute force attempts or password spray attacks.

-   **Admins and high privilege users added**

New admin account creation should be checked for validity to help to prevent attempts at unauthorized privileged access.


</td></tr><tr><td>

Monitor your instance’s Hardening Compliance level

</td><td>

Ensure that your instances are in compliance with the latest security hardening metrics using the Hardening tool in Security Center. Access this tool in a non-production instance assess impact to your environment. Ideally, the score should be as close to 100% as possible with a minimum score of 83%, without affecting product functionality.

 Learn more about Security Center's hardening settings tool at [Hardening settings](security-hardening-settings.md).

</td></tr><tr><td>

Refer your developers to the Secure Coding Guide

</td><td>

Help to ensure that your instance is secure and resistant to unauthorized access as possible using secure coding practices. The ServiceNow Secure Coding guide for Instance developers provides an overview of application security-related GlideScriptable classes and methods offered by ServiceNow. This guide is designed to assist and educate developers while creating and modifying the code on the target Instance. Review the guide at [ServiceNow Secure Coding guide for Instance developers](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0623354).

</td></tr><tr><td>

Remove the ‘Remember Me’ check box

</td><td>

Help prevent unwanted access to your instance by deactivating the **Remember Me** feature. When active, this feature stores a cookie is on the user's computer, which automatically authenticates the user on subsequent visits. This can present security issues if users access your instance from an insecure endpoint, such as a shared computer.

 Learn more about this feature, and how to deactivate it in [Remember me](../../login/concept/c_ChSetRemMeChkbxCookie.md#).

</td></tr><tr><td>

Restrict access to your instance from unknown IP addresses

</td><td>

Help prevent unauthorized access to your instance by restricting access from IP addresses unrelated to your organization. Anyone trying to access the instance from an unauthorized IP address are denied. If using this approach, consider allowing only your gateway or web proxy external addresses, as well as addresses from which your users access the instance from, including remote users. You can restrict both outbound and inbound access by IP address.

 Learn how to restrict access to your instance by IP address in [Restrict access to specific IP ranges plugin](sc-restrict-access-to-specific-ip-ranges-plugin.md).

</td></tr><tr><td>

Review ServiceNow's guidance on password spray attacks

</td><td>

Protect your instance against password spray attacks. These attacks attempt to gain access by testing a commonly used password against multiple accounts in succession.

 Learn more about spray attacks, and how to protect your instances from them in [Password Spray Attack Mitigating Strategies](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0726312).

</td></tr><tr><td>

Review the Shared Security Model

</td><td>

Understand your shared role as a customer in maintaining the security of your instances by reviewing the Shared Responsibility Model. The Shared Responsibility Model defines the partnership between and the customer, both with specific responsibilities.

 Learn more at [ServiceNow Shared Responsibility Model](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/resource-center/white-paper/wp-shared-responsibility-model.pdf).

</td></tr><tr><td>

Transfer log data from the instance for archival and reference

</td><td>

Archive your log data to retain it beyond the default 21-day log rotation period. This archival can be achieved using web services requests, the data export feature, the MID Server, or the Log Export Service from the Vault package.

 Use the following resources to learn more about these methods:

 -   [Web services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/r_AvailableWebServices.md)
-   [Exploring Log Export Service \(LES\)](../../log-export-service/concept/les-landing-page.md)

</td></tr><tr><td>

Use encryption modules with RBAC to further enhance data access control

</td><td>

Learn how to use the Key Management Framework \(KMF\) to protect the data on your instance using Role-Based Access Control \(RBAC\). KMF uses cryptographic modules, which enable you to define what data on your instance is encrypted, and what method of encryption to use. Using multiple modules, you can encrypt different areas of your instance with different specifications.

 Learn how KMF and its components are used to encrypt your data at [Exploring the Key Management Framework](../../encryption/concept/explore-kmf.md).

 Learn about cryptographic modules in [Cryptographic module overview](../../key-management-framework/concept/crypto-module-overview.md).

</td></tr><tr><td>

Use of certificate-based authentication with integration providers

</td><td>

Configure traffic to your integration providers using REST/SOAP connections to use certificate-based authentication. Secure Socket Layer \(SSL\) certificate authentication encrypts data in transit, helping to prevent it from being read as it is sent.

 Learn more about this configuration in [Configure mutual authentication](../../security/concept/c_MutualAuthentication.md).

</td></tr><tr><td>

Use SAML authentication

</td><td>

Integrate third-party multi-factor authentication \(MFA\) with your existing SAML IdP to provide additional login security. MFA provides a high level of security because authentication requires multiple authentication factors. Something the user knows \(the password\) as well as something they own \(a one-time code produced by an MFA token or mobile phone, or biometric attributes, such as a fingerprint\).

 ServiceNow supports direct MFA integration with local accounts, LDAP, SSO with SAML, OIDC, or Digest.

 Adaptive Authentication is a prerequisite for SSO with MFA.

 MFA can be enabled for specified users and specified roles, and configured for ease of use. For example you can exempt recognized devices for a number of hours.

 You can view metrics for MFA use in the Security Center.

 Learn more about SAML authentication using these resources:

 -   [SAML 2.0 concepts](../../../integrate/single-sign-on/concept/c_SAMLConcepts.md)
-   [SAML 2.0 configuration using Multi-Provider SSO](../../../integrate/single-sign-on/task/t_CreateASAML2Upd1SSOConfigMultiSSO.md)

</td></tr><tr><td>

Use the email filters feature set to deal with suspect inbound messages

</td><td>

Create email filters to filter out messages marked as suspicious by ServiceNow Antivirus Protection. In addition to virus protection, Antivirus Protection analyzes email for malware and SPAM, scoring and the results adding this information to the message in x-headers. You can use these headers as criteria for the Email Filters Plugin to act on if desired.

 Learn more about ServiceNow's antivirus feature at [Antivirus Scanning](../../security/concept/antivirus-protection.md).

 Learn how to configure email filters on your instance at [Email filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_EmailFilters.md).

</td></tr><tr><td>

Use the Syslog Probe to send logs to your SIEM

</td><td>

Use the ServiceNow syslog probe to send log messages from your instance to a Security Information and Event Manager \(SIEM\). An SIEM is third-party software or service that can be used for activity monitoring and identifying security events.

 Learn more about ServiceNow syslog probe configuration at [Syslog probe](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_SyslogProbe.md).

</td></tr><tr><td>

Use your own mature email security environment

</td><td>

Consider using your own \(or third-party\) infrastructure to send and receive instance-related email and benefit from more precise perimeter email control.

 By using your own SMTP, POP3, or IMAP servers, you can control how mail is filtered and received before being sent to your instance.

**Note:** Configuration of your own email infrastructure is considered an advanced email configuration, and can optionally use a third-party email infrastructure via OAuth 2.0 email authentication. See your own email vendor documentation and instructions for details.

</td></tr><tr><td>

Validate access using Access Analyzer

</td><td>

Use the ServiceNow Access Analyzer tool to help you compare and analyze permissions for selected users, roles, or groups. You can use this information to troubleshoot access issues, identify who has access to your sensitive data, and determine the correct level of access for users on your instance.

 Learn more about the benefits of Access Analyzer at [Exploring Access Analyzer](../../../integrate/identity/concept/explore-access-analyzer.md).

</td></tr></tbody>
</table>**Parent Topic:**[Security Best Practices](../concept/security-best-practices-manager.md)

