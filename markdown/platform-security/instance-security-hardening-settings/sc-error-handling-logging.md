---
title: Error handling and logging
description: The error handling and logging category addresses the quality and verbosity of logged information exposed to stakeholders.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Hardening settings, Platform Security]
---

# Error handling and logging

The error handling and logging category addresses the quality and verbosity of logged information exposed to stakeholders.

This includes ensuring logs and error messages do not collect sensitive information, correctly protect data according to classification and have an appropriate lifetime. Additionally, this category relates to appropriate error handling and not revealing sensitive errors to end users, such as verbose stack traces for unhandled exceptions with security implications.

-   **[Disable logger for low privilege users in script sandbox \[Updated in Security Center 1.3\]](sc-glide-security-logger-no-loggining-for-sandbox.md)**  
Manage Glide System's ability to log scripts being executed in the sandbox environment.
-   **[Disable secure cookie debugging](sc-disable-secure-cookie-debugging.md)**  
Manage the log messages related to cookies in your instance.
-   **[Disable SQL Error Messages \[Updated in Security Center 1.3 and 1.5\]](sc-disabling-sql-error-messages.md)**  
Use the **glide.db.loguser** property to disable SQL error messages from rendering in a browser.
-   **[Enable MID audit log \[New in Security Center 1.3 and updated in 1.5\]](sc-enable-mid-audit-log-plugin-applicability-mid-server.md)**  
The MID Server command audit log records details such as the command name, command hash, name of credential used, and execution status.
-   **[Enable protected tables plugin \[New in Security Center 1.3\]](sc-enable-protected-tables-plugin.md)**  
Use the **com.glide.security.protected\_table.enabled** property to prevent higher privilege users from tampering with log tables.
-   **[Log all outbound http request fields \[Removed in Security Center v1.3.2\]](sc-log-all-outbound-http-request-fields.md)**  
Configure the **glide.outbound\_http.security.log.allow.all.fields** property to false to prevent sensitive Outbound HTTP fields from being logged in plain text.
-   **[Log html sanitization \[Removed in Security Center 2.0\]](sc-log-html-sanitization.md)**  
Configure **glide.html\_sanitize.discarded\_log.enable** property to determine if HTML sanitization events will be logged in your instance.
-   **[Log session audit events \[New in Security Center 1.3 and updated in 1.5\]](sc-log-session-audit-events.md)**  
Set the **glide.authenticate.session\_access.log\_audit\_event** property to **true**, so that session audit events will be created in the **sys\_session\_access\_audit** table.
-   **[Log user impersonation \[Updated in Security Center 1.3 and 2.0\]](sc-log-user-impersonation.md)**  
Configure **glide.sys.log\_impersonation** to control if user-impersonating events are logged in your instance.
-   **[Prevent verbose HTTP request logging](sc-prevent-verbose-http-request-logging.md)**  
Help prevent access to sensitive information by reducing verbose HTTP request logging.
-   **[Turn off verbose SQL error messages for import processor \[Updated in Security Center 1.3\]](sc-turn-off-verbose-sql-error-messages-for-import-processor.md)**  
Configure this property to control whether verbose SQL error messages are displayed.

**Parent Topic:**[Hardening settings](security-hardening-settings.md)

