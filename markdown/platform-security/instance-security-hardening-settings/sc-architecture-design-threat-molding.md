---
title: Architecture, design, and threat modeling
description: This broad control addresses high level design considerations and key elements to implement a secure application. This covers the tenants of availability, confidentiality processing integrity, non-repudiation and privacy. Additionally, elements of a secure software development lifecycle are included.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Hardening settings, Platform Security]
---

# Architecture, design, and threat modeling

This broad control addresses high level design considerations and key elements to implement a secure application. This covers the tenants of availability, confidentiality processing integrity, non-repudiation and privacy. Additionally, elements of a secure software development lifecycle are included.

-   **[Check impersonation on ACL evaluation in HR App \[New in Security Center 1.3 and updated in 1.5\]](sc-check-impersonation-on-acl-evaluation-in-hr-app-plugin-applicability-human-resources-scoped-app.md)**  
Use the **sn\_hr\_core.impersonateCheck** property to prevent a user from impersonating another user and accessing their HR information.
-   **[Reduce the Scope of the IP Allow List for an Instance](sc-ip-addresses-access-allowlist.md)**  
Use the **glide.ip.authenticate.strict** property to specify IP ranges that can make inbound connections on an instance.
-   **[Disable legacy JQuery behavior](sc-legacy-jquery-behavior.md)**  
The **glide.jquery.legacy** is used to prevent older prepatched JQuery versions from being used which will introduce unpatched vulnerabilities in the library.
-   **[Disable GlideRecord Scope Fencing Legacy Behavior](sc-enable-gliderecord-scope-fencing-legacy-behavior.md)**  
The **glide.record.legacy\_cross\_scope\_access\_policy\_in\_script** property disables scope fencing allowing scoped apps to access global script interfaces. It was created as a patch to GlideRecord's cross scope access.
-   **[Disable legacy AngularJS behavior \[Removed in Security Center 2.2\]](sc-legacy-angularjs-behavior.md)**  
Use the **glide.angular.legacy** property to protect from potential security risks arising from attacks on vulnerabilities discovered in outdated AngularJS library versions.
-   **[Disable local login for users with Single Sign-On \(SSO\) enabled](sc-disable-local-login-for-users-with-single-sign-on-sso-enabled.md)**  
Update user records to disable local login for users with Single Sign-On \(SSO\) enabled.
-   **[Disable unauthenticated published reports](sc-disable-unauthenticated-published-reports.md)**  
Deactivate this property to prevent the user from publishing or accessing reports. This property disables the published reports feature in reporting.
-   **[Disable public access to favorites](sc-public-access-to-favorites.md)**  
Use the **glide.ui.magellan.favorites.allow\_public** to specify whether unauthenticated users are allowed to see **Favorites** in the navigator.
-   **[Enforce field ACLs for inbound query requests](sc-enforce-field-acls-for-inbound-query-requests.md)**  
Manage how incoming queries are validated on your instance.
-   **[Enforce read ACLs on report views](sc-enforce-read-acls-on-report-views.md)**  
Manage how Read ACLs are enforced on your instance.
-   **[Enable Anti-CSRF Token for Userperf](sc-enable-anti-csrf-token-for-userperf.md)**  
Use a system property to ensure CSRF \(Cross-Site Request Forgery\) protection is enforced when setting user preferences.
-   **[Enforce Query ACLs for Knowledge Quick Links](sc-enforce-query-acls-for-knowledge-quick-links.md)**  
Enforce query ACLs for Knowledge Quick Links using a system property.
-   **[Enforce Query ACLs for SubLists, List Counts and Widget Data Tables](sc-enforce-query-acls-for-sublists-list-counts-and-widget-data-tables.md)**  
Enforce query ACLs on sublist, list count, and widget data table queries using system properties.
-   **[Enforce valid query string choice \[New in Security Center 7.0\]](sc-enforce-valid-query-string-choice.md)**  
Use a system property to ensure that any choice field value, when passed via a URL query string, is a valid active choice when a record is created.
-   **[Ensure An Instance is Allowed to Connect to Only Trusted IP Addresses](sc-ensure-an-instance-is-allowed-to-connect-to-only-trusted-ip-addresses.md)**  
Use a system property to define a list of IP ranges that are appended to the outbound IP allow list.
-   **[Ensure only Trusted IP Addresses are Allowed to Connect to An Instance](../../security/reference/performance-monitoring-ip-restriction.md)**  
Use a system property to define a list of IP ranges that are appended to the outbound IP allow list.
-   **[For Self-Hosted Instance, Ensure only Trusted IP Addresses are Allowed to Connect to An Instance](sc-for-self-hosted-instance-ensure-only-trusted-ip-addresses-are-allowed-to-connect-to-an-instance.md)**  
Use system properties to control which inbound IP addresses can connect to self-hosted instances.
-   **[Require authorization for data broker rest API \[Updated in Security Center 1.3\]](sc-data-broker-rest-api-authorization.md)**  
Use the **glide.basicauth.required.databrokerrestapiprocessor** property to require basic authorization for all inbound Data Broker Rest API requests.
-   **[Restricted Binding functionality in case Bearer Authorization \[New in Security Center 7.0\]](sc-restricted-binding-functionality-in-case-bearer-authorization.md)**  
Use a system property and restricted binding to ensure that an access token generated using that entity can’t be used for UI calls.
-   **[Deny by default with empty ACLs \[Updated in Security Center 1.3\]](sc-security-manager-default-deny.md)**  
Use the **glide.sm.default\_mode** property to control the default behavior of security manager when it finds that existing Access Control List \(ACL\) rules are a part of wildcard table ACL rules.
-   **[Set Automatic Token Cleanup for Token Credentials](sc-set-automatic-token-cleanup-for-token-credentials.md)**  
Use the **com.snc.platform.security.token.auth.cleanup** property to ensure that expired API keys and HMAC secrets are deleted, thereby limiting the potential for token reuse.

**Parent Topic:**[Hardening settings](security-hardening-settings.md)

