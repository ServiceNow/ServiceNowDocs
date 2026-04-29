---
title: Error handling and logging
description: The error handling and logging category addresses the quality and verbosity of logged information exposed to stakeholders.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Hardening settings, Platform Security]
---

# Error handling and logging

The error handling and logging category addresses the quality and verbosity of logged information exposed to stakeholders.

This includes ensuring logs and error messages do not collect sensitive information, correctly protect data according to classification and have an appropriate lifetime. Additionally, this category relates to appropriate error handling and not revealing sensitive errors to end users, such as verbose stack traces for unhandled exceptions with security implications.

-   **[Disable logger for low privilege users in script sandbox](sc-glide-security-logger-no-loggining-for-sandbox.md)**  
Manage Glide System's ability to log scripts being executed in the sandbox environment.
-   **[Disable secure cookie debugging](sc-disable-secure-cookie-debugging.md)**  
Manage the log messages related to cookies in your instance.
-   **[Disable SQL error messages](sc-disabling-sql-error-messages.md)**  
Use the **glide.db.loguser** property to disable SQL error messages from rendering in a browser.
-   **[Enable Identity and Access Audit Tool](sc-enable-identity-and-access-audit-tool.md)**  
Use Identity and Access Audit to track changes to user accounts, groups, and roles.
-   **[Enable MID audit log](sc-enable-mid-audit-log-plugin-applicability-mid-server.md)**  
The MID Server command audit log records details such as the command name, command hash, name of credential used, and execution status.
-   **[Enable protected tables plugin](sc-enable-protected-tables-plugin.md)**  
Use the **com.glide.security.protected\_table.enabled** property to prevent higher privilege users from tampering with log tables.
-   **[Log all outbound http request fields \[Removed in Security Center v1.3.2\]](sc-log-all-outbound-http-request-fields.md)**  
Configure the **glide.outbound\_http.security.log.allow.all.fields** property to false to prevent sensitive Outbound HTTP fields from being logged in plain text.
-   **[Log html sanitization \[Removed in Security Center 2.0\]](sc-log-html-sanitization.md)**  
Configure **glide.html\_sanitize.discarded\_log.enable** property to determine if HTML sanitization events will be logged in your instance.
-   **[Log Impersonation History](sc-log-impersonation-history.md)**  
Enable impersonation history logging using a system property.
-   **[Log session audit events](sc-log-session-audit-events.md)**  
Use a system property to enable creations of session audit events
-   **[Log user impersonation](sc-log-user-impersonation.md)**  
Configure **glide.sys.log\_impersonation** to control if user-impersonating events are logged in your instance.
-   **[Prevent verbose HTTP request logging](sc-prevent-verbose-http-request-logging.md)**  
Help prevent access to sensitive information by reducing verbose HTTP request logging.
-   **[Track Impersonation Events](sc-track-impersonation-events.md)**  
Enable impersonation event tracking using a system property.
-   **[Turn off verbose SQL error messages for import processor](sc-turn-off-verbose-sql-error-messages-for-import-processor.md)**  
Configure this property to control whether verbose SQL error messages are displayed.

**Parent Topic:**[Hardening settings](security-hardening-settings.md)

