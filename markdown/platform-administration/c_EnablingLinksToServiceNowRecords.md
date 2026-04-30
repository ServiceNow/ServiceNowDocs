---
title: Links to records in email notifications
description: Adding the $\{URI\} parameter to an outbound email body or template creates a link to a specific record.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create an email notification, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer]
---

# Links to records in email notifications

Adding the **$\{URI\}** parameter to an outbound email body or template creates a link to a specific record.

When a user clicks the word LINK, the instance prompts the user to log in if not already logged in, and then redirects the user to the record specified in the URI.

![](../image/EmailURI.png "Link displayed by ${URI} parameter")

The $\{URI\} parameter has an extension called the $\{URI+\} format to specify additional arguments in the email link, such as sysparm terms, in addition to the automatically created URI. For example \(whitespace added for improved readability\):

```
${URI+&sysparm_scriptlet=current.assigned_to=gs.getUserID()
&sysparm_scriptlet_condition=current.assigned_to.nil()
&sysparm_view=incident_active}
```

This example executes the JavaScript:

```
current.assigned_to=gs.getUserID()
```

when the condition of

```
current.assigned_to.nil()
```

is satisfied. Additionally, the script sets the view to `incident_active`.

## Linking to a record in Workspace

The `${URI}` and `${URI_REF}` variables don't apply to records in Workspace. To link to a record in Workspace, create a mail script and reference it in your notification. For more information on using mail scripts, see [JavaScript in emails](../../../script/server-scripting/concept/c_UseJavaScriptInEmails.md).

The mail script that you create should print a URL to the notification. The URL must have the following format:

```
https://<instance_name>/now/workspace/<workspace_name>/record/<table_name>/<sys_id>
```

The following example script shows the logic that a mail script must include to create a link to a record in Workspace.

```
// Dynamically construct an Agent Workspace URL and insert a link in the notification
  var agentURL = '<a href="' + gs.getProperty('glide.servlet.uri') + '/now/workspace/agent/record/'+ current.getTableName() + '/' + current.sys_id + '">' + current.number + '</a>';
  template.print(agentURL + "<br />");
```

-   **[Enable links to records](../../../script/server-scripting/concept/c_EnableLinksToServiceNowRecords.md)**  
Adding the special **$\{URI\}** parameter to an outbound email body or template creates a link to a specific record.
-   **[Change the link text](../../../script/server-scripting/concept/c_ChangeTheLinkText.md)**  
To show the display value of the record as the link text instead of the word LINK, use the $\{URI\_REF\} parameter instead of the $\{URI\} parameter.
-   **[Link to related records](c_LinkToRelatedRecords.md)**  
A notification can link to a related record by specifying a reference field in front of the**$\{URI\}** or **$\{URI\_REF\}** parameters.
-   **[Content page links in email notifications](c_LinkingToContentPages.md)**  
Links to CMS pages can be put in notifications to make it easy for the reader to access the pages.

**Parent Topic:**[Create an email notification](../task/t_CreateANotification.md)

