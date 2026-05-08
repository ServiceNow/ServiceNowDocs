---
title: Create an inbound email action
description: Create inbound email actions to define the actions that the system takes when an email is received.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Inbound email, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create an inbound email action

Create inbound email actions to define the actions that the system takes when an email is received.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Email** &gt; **Inbound Actions**.

2.  Select **New**.

3.  Fill in the fields as described in the table.

    **Note:** You might need to configure the form to see all fields.

<table id="table_kyc_qhz_lp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

When to run

</td></tr><tr><td>

Name

</td><td>

Enter a descriptive name for this email action.

</td></tr><tr><td>

Target table

</td><td>

Select the table where the action adds or updates records.

</td></tr><tr><td>

Action type

</td><td>

Select the type of action the instance takes. Select **Record Action** to modify a record in the instance, or select **Reply Email** to have the instance send an email back to the source of the inbound email.

</td></tr><tr><td>

Active

</td><td>

Select the check box to activate the inbound email action. Clear the check box to disable the action.

</td></tr><tr><td>

Stop processing

</td><td>

Select this check box to help prevent the system from running additional inbound email actions after this action runs.

</td></tr><tr><td>

Redact sensitive data

</td><td>

Select this to mask sensitive data such as personal details, SSN, credit card details.**Note:** Available only when Sensitive Data Redaction for Inbound Emails plugin is activated.

</td></tr><tr><td>

Type

</td><td>

Select the message type required to run the action. The action runs only if the inbound email is of the selected type. Available types are:-   New: An email that is not recognized as a reply or forward.
-   Reply: An email with a watermark with an In-Reply-To email header, or whose subject line begins with a recognized reply prefix.
-   Forward: An email whose subject line begins with a recognized forward prefix, even if the email also contains a watermark or In-Reply-To header.
 **Note:** By default, inbound emails of the Forward type always generate new incidents regardless of the presence of a watermark. If this behavior doesn’t match your business logic, you can change the recognized reply and forward prefixes to treat forwards like replies.

</td></tr><tr><td>

Required roles

</td><td>

Specify required roles that the sender must have to trigger the inbound action.

</td></tr><tr><td>

Order

</td><td>

Enter a number that specifies when this inbound action runs relative to other inbound actions that use the same target table. The instance processes the action with the lowest order number first.

</td></tr><tr><td>

From

</td><td>

Select the user required to run the action. If a user is selected, the action runs only when the email sender matches the user name. Leave this field empty to perform the action for all users.**Note:** If the selected user is later archived or deleted, the restriction is removed and anyone can trigger the inbound email action.

</td></tr><tr><td>

Condition

</td><td>

Specify the condition that must evaluate to true to trigger the inbound action. Build a condition with the choice lists or enter a statement that determines when the inbound email action runs. For example:```
email.subject. startsWith ( "chg:" )
```

</td></tr><tr><td class="sub-head" colspan="2">

Actions

</td></tr><tr><td>

Field actions

</td><td>

This field appears if the **Action type** is **Record Action**. Specify how information in the email is inserted into the record. For example, select **\[Created by\]** **\[From email\]** **\[Sender\]**, so that when the request is inserted, you can see who it is for.

</td></tr><tr><td>

Reply email

</td><td>

This field appears if the **Action type** is **Reply Email**. compose the email message to send to the source that triggered the inbound email action.

</td></tr><tr><td>

Script

</td><td>

Enter the script that the action runs. Typically, this script uses the validators script include and email variables. A template is provided:

 ```

(function runAction(/*GlideRecord*/ current, /*GlideRecord*/ event, /*EmailWrapper*/ email, /*ScopedEmailLogger*/ logger) {

	// Implement email action here

})(current, event, email, logger);
```

 The following objects are available:

-   **current**: access the record referred to by the inbound email. For example, `current.assigned_to` accesses the person assigned to the task.
-   **event**: access one of the parameters of the originating event. For example, `event.parm1` accesses the first parameter of the event or `event.parm2` for the second parameter. See Events for more information.
-   **email**: access the inbound current email record. For example, `email.subject` accesses the content in the subject line of the email. See [Accessing email object variables](../reference/r_AccessingEmailObjsWithVars.md) for more information.
-   **logger**: add a message to the log file with the source set to `email.<Sys ID of incoming email>`. For example: `logger.log ("Some information")`


</td></tr><tr><td class="sub-head" colspan="2">

Description

</td></tr><tr><td>

Description

</td><td>

Enter a detailed explanation of what this inbound email action does.

</td></tr><tr><td class="sub-head" colspan="2">

Other fields

</td></tr><tr><td>

Order

</td><td>

Enter a number to define the order in which this email action should be processed. Actions with lower numbers are processed first. The Ordered Email Processing plugin does not activate this field.

</td></tr></tbody>
</table>
**Parent Topic:**[Use Inbound email actions](../concept/use-inbound-email-action.md)

