---
title: Avoid log tampering
description: Configure system log table protection rules to limit the scope of modification and deletion of application log records. The rules enable you to determine the logging of changes or attempts to changes in these tables.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [System logs, Logs, Platform Security]
---

# Avoid log tampering

Configure system log table protection rules to limit the scope of modification and deletion of application log records. The rules enable you to determine the logging of changes or attempts to changes in these tables.

If you are a security\_admin, activate the Protected Tables plugin \(com.glide.protected\_tables\) that allows the platform to restrict update, insert and delete operations on the following system log tables:

-   syslog
-   syslog\_transaction
-   sys\_outbound\_http\_log
-   sysevent
-   sys\_audit
-   sys\_push\_notification
-   syslog\_app\_scope
-   protected\_table\_configuration \(config not modifiable\)

**Note:** The com.glide.protected\_tables plugin gives protection only to the system log tables mentioned above. Any attempt to update, insert or delete a record logs a message in the protected\_table\_log table.

See [Installing and configuring the log protection plugin](../task/accept-log-protection.md) for more details.

You can specify one of the following log protection levels for each of the system log table.

-   Block and log the attempt: Blocks any modification and logs the attempt
-   Only block the attempt: Blocks any modification and doesn't log the attempt
-   Only log the attempt: Doesn't block the modification but logs the attempt
-   Don't block and don't log the attempt: Doesn't block the modification and doesn't log the attempt

Platform uses the log protection levels specified for each of the system log tables to block and/or log any attempts to modify a record after being initially created.

**Note:** If you are a security\_admin, you have the ability to override the default log protection levels in each of the system log tables to adapt to the customizations on your instance.

If there have been any attempts to modify the system log tables, they are logged into the protected\_table\_log table.

**Note:** If the protection level is not specified for a table, any attempts of modification are not logged into the protected\_table\_log table.

In order to disable the plugin operations on tables in the Admin Panel, set the com.glide.security.protected\_table.enabled property to false. See [Create log protection property](../task/log-protection-property.md) for more information.

