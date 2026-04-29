---
title: Setting field values from the email body
description: Values in an inbound email can set field values in a task record.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Inbound email, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Setting field values from the email body

Values in an inbound email can set field values in a task record.

Any name:value pair in an inbound email body gets parsed into a variable/value pair in the inbound email script. The name:value pair must be on its own line. Note that most email clients limit the number of characters allowed per line and may truncate excessively long name:value pairs.

**Tip:** To prevent unexpected parsing, ensure that all the names in the name:value pairs are unique.

See [Redirecting Emails](r_RedirEmailDifferentAssignGrp.md) for an example of using **setDisplayValue\(\)** in an inbound email action.

**Note:** The action always generates a lowercase variable name. Also, this functionality does not work on reference fields.

For example, if an email body contains this line:

```
Foo:bar
```

The inbound email script creates the variable *email.body.foo* with the value of **bar**. You can use these variables to create conditions such as:

```
if(email.body.foo!=undefined){
   current.[field]=email.body.foo;}
```

In this example, the script sets the value of *\[field\]* to the value **bar**.

**Note:** Spaces are rendered as underscores when a name:value pair gets parsed into a variable/value pair. For example, if an email body contains a line with spaces like `my variable:data`, then the inbound email script creates the variable *email.body.my\_variable*. The value of the variable is **data**.

**Parent Topic:**[Configure inbound email actions](../concept/configure-inbound-email.md)

