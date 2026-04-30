---
title: Architecture, design, and threat modeling
description: This broad control addresses high level design considerations and key elements to implement a secure application. This covers the tenants of availability, confidentiality processing integrity, non-repudiation and privacy. Additionally, elements of a secure software development lifecycle are included.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Hardening settings, Platform Security]
---

# Architecture, design, and threat modeling

This broad control addresses high level design considerations and key elements to implement a secure application. This covers the tenants of availability, confidentiality processing integrity, non-repudiation and privacy. Additionally, elements of a secure software development lifecycle are included.

-   **[Certificate based authentication not enforced \[New in Security Center 1.3\]](sc-certificate-based-authentication-not-enforced.md)**  
The **glide.authenticate.mutual.enabled** property enables certificate based authentication, a type of mutual authentication for inbound REST connections to REST and SOAP APIs in the ServiceNow AI Platform.
-   **[Check impersonation on ACL evaluation in HR App \[New in Security Center 1.3 and updated in 1.5\]](sc-check-impersonation-on-acl-evaluation-in-hr-app-plugin-applicability-human-resources-scoped-app.md)**  
Use the **sn\_hr\_core.impersonateCheck** property to prevent a user from impersonating another user and accessing their HR information.
-   **[Disable unauthenticated published reports \[Updated in Security Center 2.0\]](sc-disable-unauthenticated-published-reports.md)**  
Deactivate this property to prevent the user from publishing or accessing reports. This property disables the published reports feature in reporting.
-   **[Enforce field ACLs for inbound query requests](sc-enforce-field-acls-for-inbound-query-requests.md)**  
Manage how incoming queries are validated on your instance.
-   **[Enforce read ACLs on report views](sc-enforce-read-acls-on-report-views.md)**  
Manage how Read ACLs are enforced on your instance.
-   **[Define allowed ServiceNow internal IP addresses \[Updated in Security Center 1.3 and 1.5\]](sc-ip-addresses-access-allowlist.md)**  
Use the **glide.ip.authenticate.strict** property to specify IP ranges that can make inbound connections on an instance.
-   **[Disable legacy JQuery behavior \[Updated in Securty Center 1.3\]](sc-legacy-jquery-behavior.md)**  
The **glide.jquery.legacy** is used to prevent older prepatched JQuery versions from being used which will introduce unpatched vulnerabilities in the library.
-   **[Disable GlideRecord Scope Fencing Legacy Behavior \[New in Security Center 1.3 and updated in 1.5 and 2.0\]](sc-enable-gliderecord-scope-fencing-legacy-behavior.md)**  
The **glide.record.legacy\_cross\_scope\_access\_policy\_in\_script** property disables scope fencing allowing scoped apps to access global script interfaces. It was created as a patch to GlideRecord's cross scope access.
-   **[Disable legacy AngularJS behavior \[Removed in Security Center 2.2\]](sc-legacy-angularjs-behavior.md)**  
Use the **glide.angular.legacy** property to protect from potential security risks arising from attacks on vulnerabilities discovered in outdated AngularJS library versions.
-   **[Require authorization for data broker rest API \[Updated in Security Center 1.3\]](sc-data-broker-rest-api-authorization.md)**  
Use the **glide.basicauth.required.databrokerrestapiprocessor** property to require basic authorization for all inbound Data Broker Rest API requests.
-   **[Deny by default with empty ACLs \[Updated in Security Center 1.3\]](sc-security-manager-default-deny.md)**  
Use the **glide.sm.default\_mode** property to control the default behavior of security manager when it finds that existing Access Control List \(ACL\) rules are a part of wildcard table ACL rules.

**Parent Topic:**[Hardening settings](security-hardening-settings.md)

