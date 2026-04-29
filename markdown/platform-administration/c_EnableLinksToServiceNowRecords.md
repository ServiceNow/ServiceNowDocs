---
title: Enable links to records
description: Adding the special $\{URI\} parameter to an outbound email body or template creates a link to a specific record.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Links to records, Create an email notification, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable links to records

Adding the special **$\{URI\}** parameter to an outbound email body or template creates a link to a specific record.

When a user clicks the word **LINK**, the instance prompts the user to log in if not already logged in, and then redirects the user to the record specified in the URI.

![](../../../administer/notification/image/EmailURI.png "URI email notification")

The **$\{URI\}** parameter has an extension called the **$\{URI+\}** format to specify additional arguments in the email link, such as sysparm terms, in addition to the automatically created URI. For example \(whitespace added for improved readability\):

```
${URI+&sysparm_scriptlet=current.assigned_to=gs.getUserID()
&sysparm_scriptlet_condition=current.assigned_to.nil()
&sysparm_view=incident_active}
```

This example executes the JavaScript:

```
current.assigned_to=gs.getUserID()
```

The JavasScript is executed when the condition is satisfied:

```
current.assigned_to.nil()
```

Additionally, the script sets the view to incident\_active.

**Parent Topic:**[Links to records in email notifications](../../../administer/notification/concept/c_EnablingLinksToServiceNowRecords.md)

