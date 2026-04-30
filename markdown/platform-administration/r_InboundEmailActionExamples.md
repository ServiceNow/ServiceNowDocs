---
title: Inbound email action examples
description: Various examples of inbound email actions are available to help you build your own inbound email actions. These examples show how to set up inbound email actions to handle email replies, create \(log\) a problem record, request a change, and update an incident.This example shows you how to set up inbound email actions to handle replies that users send back to the instance.This example shows you how to set up inbound email actions to a create a problem record.This example shows you how to set up inbound email actions to create a change request record.The default inbound action for the Incident table automatically sets the following field values when it receives an incoming email.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [References for Inbound email, Inbound email, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Inbound email action examples

Various examples of inbound email actions are available to help you build your own inbound email actions. These examples show how to set up inbound email actions to handle email replies, create \(log\) a problem record, request a change, and update an incident.

**Parent Topic:**[References for Inbound email](../concept/references-inbound-email.md)

## Inbound email action example: handling email replies

This example shows you how to set up inbound email actions to handle replies that users send back to the instance.

### Before you begin

Role required: admin

### About this task

The inbound email action parses the email and responds using a script. By default, an email received by the instance creates a new incident, and the body of the email is added to the **Additional Comments** text box. More refined Inbound Email Actions can create incident tickets with more data, thus saving the incident management team valuable time.

Normally, when a user responds to an email sent by the instance, the inbound email action matches the watermark to an existing incident, and updates the incident rather than creating a new record. However, if the watermark is missing, this inbound email action attempts to match a reply to the original incident.

This inbound email action is replicated in Workflow Studio as the sample flow **Inbound Email Flow Example: handling email replies**. To view the sample flow, navigate to **Flow Designer** &gt; **Designer**.

### Procedure

1.  Navigate to **System Policy** &gt; **Inbound Actions** and click **New**.

2.  Populate the form as follows:

    |Field|Value|
    |-----|-----|
    |Name|Update Incident|
    |Type|Reply|
    |Target table|Incident \[incident\]|

3.  In **Script**, enter this code.

    ```
    gs.include('validators');
     
    //Note: current.caller_id and current.opened_by are already set to the first UserID that matches the From: email address
     
    if (current.getTableName() == "incident") {
      current.comments = "reply from: " + email.origemail + "\n\n" + email.body_text;
     
      if (email.body.assign != undefined)
        current.assigned_to = email.body.assign;
     
      if (email.body.priority != undefined && isNumeric(email.body.priority))
        current.priority = email.body.priority;
     
      if (email.body.category != undefined)
        current.category = email.body.category;
     
      if (email.body.short_description != undefined)
        current.short_description = email.body.short_description;
     
      current.update();
    }
    ```


## Inbound email action example: logging a problem

This example shows you how to set up inbound email actions to a create a problem record.

### Before you begin

Role required: admin

### About this task

Inbound email actions allow users to log or update incidents on an instance via email. The inbound email action parses the email and responds using a script.

This inbound email action is replicated in Workflow Studio as the sample flow **Inbound Email Flow Example: logging a problem**. To view the sample flow, navigate to **Flow Designer** &gt; **Designer**.

### Procedure

1.  Navigate to **System Policy** &gt; **Inbound Actions** and click **New**.

2.  Populate the form as follows:

<table id="simpletable_iry_cjf_hq"><thead><tr><th>

Field

</th><th>

Entry

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Log Problem

</td></tr><tr><td>

Type

</td><td>

New

</td></tr><tr><td>

Active

</td><td>

True

</td></tr><tr><td>

Target Table

</td><td>

Problem \[problem\]

</td></tr><tr><td>

Condition

</td><td>

```
email.subject.indexOf("Problem: ") == 0
```

</td></tr><tr><td>

Script

</td><td>

```
current.description = email.body_text;
  current.short_description = email.subject.toString().substring(9);
 
  current.assignment_group.setDisplayValue("Development");
 
  if (email.body.assign != undefined)
    current.assigned_to = email.body.assign;
 
  current.insert();
```

</td></tr></tbody>
</table>
## Inbound email action example: requesting a change

This example shows you how to set up inbound email actions to create a change request record.

### Before you begin

Role required: admin

### About this task

Inbound Email Actions allow users to log or update incidents on an instance via email. The inbound email action parses the email and responds using a script.

### Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Inbound Actions** and click **New**.

2.  Populate the form as follows:

<table id="simpletable_iry_cjf_hq"><thead><tr><th>

Field

</th><th>

Entry

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Request Change

</td></tr><tr><td>

Type

</td><td>

New

</td></tr><tr><td>

Active

</td><td>

True

</td></tr><tr><td>

Target Table

</td><td>

Change Request \[change\_request\]

</td></tr><tr><td>

Condition

</td><td>

```
email.subject.indexOf("Change Request: ") == 0
```

</td></tr><tr><td>

Script

</td><td>

```
current.comments = email.body_text;
  current.short_description = email.subject;
 
  current.notify = 2;
 
  if (email.body_text.assign != undefined)
    current.assigned_to = email.body_text.assign;
 
  if (email.body_text.priority != undefined)
    current.priority = email.body_text.priority;
 
  if (email.body_text.category != undefined)
    current.category = email.body_text.category;
 
  current.insert();
```

</td></tr></tbody>
</table>
## Values automatically set from incoming email

The default inbound action for the Incident table automatically sets the following field values when it receives an incoming email.

|Field value set|Value used from incoming email|
|---------------|------------------------------|
|`current.caller_id`|User ID of the first user whose email address matches the `email.from` variable.|
|`current.opened_by`|User ID of the first user whose email address matches the `email.from` variable.|

If multiple users have the same email address, the instance first searches for an active user with the email address. Use unique email addresses for each user record whenever possible. If not, having only one active user with the shared email address guarantees that the instance always matches incoming email from this address to the active user.

