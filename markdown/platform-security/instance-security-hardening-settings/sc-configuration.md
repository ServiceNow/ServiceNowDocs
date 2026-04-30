---
title: Configuration
description: The Configuration category ensures applications have a secure build environment and hardened third party library components. Specifically, ensuring a build and deploy pipeline is repeatable and includes automated testing and prevents known security issues from being deployed. This includes keeping dependencies up to date and free from known vulnerabilities.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Hardening settings, Platform Security]
---

# Configuration

The Configuration category ensures applications have a secure build environment and hardened third party library components. Specifically, ensuring a build and deploy pipeline is repeatable and includes automated testing and prevents known security issues from being deployed. This includes keeping dependencies up to date and free from known vulnerabilities.

-   **[Auto set content type options \[Removed in Security Center 1.3.3\]](sc-auto-set-content-type-options.md)**  
Configure the Auto set content type options property on your instance to prevent MIME confusion attacks.
-   **[Cache-Control HTTP Header Value \[Updated in Security Center 1.3 and removed in 1.5\]](sc-cache-control-http-header-value.md)**  
Use the **glide.http.cache\_control** property to set the default cache-control value in the HTTP response headers that the ServiceNow AI Platform sends when requesting static content data for a page. Examples of static content include images, CSS, and JavaScript rendered from within, for a page.
-   **[sc-disable-chat-server-debugging.md](sc-disable-chat-server-debugging.md)**  

-   **[Disable locked form elements debugging](sc-disable-locked-form-elements-debugging.md)**  
Here's the description for **glide.security.explain.write.locks**.
-   **[Disable MultiSSO Debugging \[Updated in Security Center 1.3 and 1.5\]](sc-disable-multisso-debugging.md)**  
The **glide.authenticate.multisso.debug** property controls debug logging for Multi-SSO.
-   **[Disallow target cloning \[New in Security Center 1.3\]](sc-disallow-target-cloning.md)**  
Configure the **glide.db.clone.allow\_clone\_target** property to prevent your instance from being used as a clone target.
-   **[Enable HTTP response headers configuration](sc-enable-http-response-headers-configuration.md)**  
Reduce the risk of cookie/session-related hijacking of web apps using a system property.
-   **[Disable soap fault stack trace display](sc-disable-soap-fault-stack-trace-display.md)**  
Manage how stack traces are displayed in your instance.
-   **[Restrict performance monitoring access \[Updated in Security Center 1.3\]](sc-performance-monitoring-acl.md)**  
Use the **glide.security.diag\_txns\_acl** property to control stats.do, threads.do, thread\_pool\_stats, and replication.do access from an unauthenticated connection.
-   **[Enable updated version of MultiSSO plugin \[Updated in Security Center 1.3 and 1.5\]](sc-updated-version-of-multi-sso-plugin-is-enabled.md)**  
Verify that you're using v2 of the MultiSSO plugin and that it's set to true to reduce security vulnerabilities.
-   **[Enforce secure referrer policy \[New in Security Center 1.3\]](sc-enforce-secure-referrer-policy.md)**  
Use the **com.glide.security.referrerpolicy** property to ensure that the Referrer-Policy HTTP header sends the appropriate level of data to each ServiceNow® page to prevent data leaks.
-   **[Implement the x-frame-options: SAMEORIGIN security header \[Updated in Security Center 1.3\]](sc-x-frame-options-sameorigin.md)**  
Use the **glide.set\_x\_frame\_options** property to set the X-Frame-Options response header to SAMEORIGIN for all UI pages.
-   **[Require write access to access service catalog add item page \[New in Security Center 1.3\]](sc-require-write-access-to-access-service-catalog-add-item-page.md)**  
Use the **glide.sc.request.add\_item\_write\_access** property to prevent unauthorized operations from being performed on catalog items.
-   **[Set Xframe options to prevent embedding third-party websites \[Updated in Security Center 1.3\]](sc-xframe-options.md)**  
Configure this property to prevent the content of a web-application from being embedded in a third-party site.

**Parent Topic:**[Hardening settings](security-hardening-settings.md)

