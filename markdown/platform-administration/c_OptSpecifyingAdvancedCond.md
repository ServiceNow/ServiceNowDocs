---
title: Advanced conditions for email notifications
description: Use an advanced condition to send a notification based on the current email record, changing field values, or system properties.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create an email notification, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Advanced conditions for email notifications

Use an advanced condition to send a notification based on the current email record, changing field values, or system properties.

To send a notification using an advanced condition, you can:

-   Call a function that returns a value, or
-   Set the global variable `answer` using a script

For example, in the following code, you call a function to prevent the system from sending an email notification if the sender of a self-service request is a member of the XYZ group:

```
(function() {
  var groupMember = gs.getUser();
  return !groupMember.isMemberOf('XYZ');
})();
```

Alternatively, you can script the same advanced condition by using the `answer` variable:

```

var groupMember = gs.getUser();
  if(groupMember.isMemberOf('XYZ')){
    answer = false;
  } else {
    answer = true;
  };
```

Note that the script must set the `answer` variable to **true** to send the notification. If you script no conditionals, the value of `answer` is equal to the last value that you set for the variable.

You can add a script-based condition in the **Advanced condition** field by configuring the Email Notification form and adding the field. You can access the field in the **Advanced** view without configuring the form.

The advanced condition script uses the following business rule global variables:

-   current: contains the current record from the table to which the notification is linked.
-   event: contains the event that triggered the notification.

**Note:** The **Advanced condition** field is evaluated in addition to other conditions you set on the notification. Both the **Condition** and **Advanced condition** must evaluate to true in order to send the notification.

**Parent Topic:**[Create an email notification](../task/t_CreateANotification.md)

**Related topics**  


[Create an email notification](../task/t_CreateANotification.md)

