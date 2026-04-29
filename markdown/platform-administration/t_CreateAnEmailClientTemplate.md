---
title: Create an email client template
description: Create a different template for each table that uses the email client to pre-populate data for recipients and email content.After you create an email client template, you can apply it to an email.You can now create custom email client response templates that support conditions.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Configure, Email client, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create an email client template

Create a different template for each table that uses the email client to pre-populate data for recipients and email content.

## Before you begin

Role required: admin

## About this task

The email client uses its own [email templates](../concept/c_EmailTemplates.md) to define default values for fields. Use the following sections in the Email Client Template form to build a client template:

-   Content: The message body.
-   Recipients: The email addresses of users receiving the email message. The email addresses are displayed in the To, Cc, and Bcc fields of the message.
-   Sender Configuration: The method used to generate the email sender \(From email address\) of the message.

## Procedure

1.  Navigate to **All** &gt; **Email Client** &gt; **Email Client Templates**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_dpp_vtl_xfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique template name.

</td></tr><tr><td>

Table

</td><td>

The table that the template applies to. Enable the email client for the same table.

</td></tr><tr><td>

Conditions

</td><td>

The conditions that determine when this client template is used. Use the condition builder to identify the target record that must match before this template is applied to the email client. **Note:** Conditions are only used for to apply a default template upon initial load. Conditions are not used when loading a custom email template from a workspace sidebar.

</td></tr><tr><td>

Application

</td><td>

The type of scoped application.

</td></tr><tr><td>

Execution Order

</td><td>

A number that indicates the order in which the template conditions are evaluated. The template with the lowest execution order is considered.

</td></tr><tr><td>

Include attachment from email

</td><td>

Option for including attachments from email to the **replyall-received**, **reply-received**, **forward-sent**, **reply-sent**, **replyall-sent**, and **forward-received** response templates.**Note:** This option is applicable only for response email in a configurable workspace.

</td></tr></tbody>
</table>4.  On the **Content** tab, fill in the fields.

<table id="table_f5h_lsl_qq"><thead><tr><th>

Field

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Subject

</td><td>

Enter a description of the email.**Note:** The **Subject** field on the email client allows a larger character count than the default setting for the **Subject** field in the Email \[sys\_email\] table. If the subject text from the client is being truncated, increase the **Max length** value for the **Subject** field in the Email table.

</td></tr><tr><td>

Content Type

</td><td>

Select the format of the message body content: **HTML** or **plain text**.

</td></tr><tr><td>

Body HTML

</td><td>

If you've selected **HTML** for the **Content Type** field, enter the content of the message body using the HTML editor toolbar to format the HTML.

 To reference field values, select variables from the variables list or manually type variable references using the syntax `${table_name.variable_name}`. To reference the user who launches the email client, enter the variable `${current_user}`.

**Note:** Line breaks don't appear for multi-line fields such as $\{description\} and $\{comments\} in the email client template.

 You can call a mail script by using `${mail_script:script name}` in the **Body HTML** field.

</td></tr><tr><td>

Body text

</td><td>

If you selected **plain text** for the **Content Type** field, enter any text or mail script that you want to appear in the message body.

 You can insert a mail script in the **Body text** field by using the following syntax:

```
<mail_script> [code] </mail_script>
```

</td></tr></tbody>
</table>5.  On the **Recipients** tab, fill in the fields.

<table id="table_ybt_fcm_xfb"><thead><tr><th>

Field

</th><th>

Action

</th></tr></thead><tbody><tr><td>

To

</td><td>

Enter a comma-separated list of either field names that contain user email addresses or just email addresses. To reference an email address using a script, create a script include and then call the script include in the **To** field. Your script must start with the `javascript:` prefix. The script must return email addresses in a comma-separated string. Use only one JavaScript expression and do not combine it with field names.

</td></tr><tr><td>

Cc

</td><td>

Enter a comma-separated list of either field names that contain user email addresses or just email addresses. To reference an email address using a script, create a script include and then call the script include in the **Cc** field. Your script must start with the `javascript:` prefix. The script must return email addresses in a comma-separated string. Use only one JavaScript expression and do not combine it with field names.

 This field can’t have the same addresses as the **To** field.

</td></tr><tr><td>

Bcc

</td><td>

Enter a comma-separated list of either field names that contain user email addresses or specific email addresses. To reference an email address using a script, create a script include and then call the script include in the **Bcc** field. Your script must start with the `javascript:` prefix. The script must return email addresses in a comma-separated string. Use only one JavaScript expression and do not combine it with field names.

 This field can’t have the same addresses as the **To** or **Cc** fields.

</td></tr></tbody>
</table>6.  On the **Sender Configuration** tab, select the **From Generation Type** method to determine how the sender \(From address\) in the email client message is generated.

<table id="choicetable_f3x_twt_pfc"><thead><tr><th align="left" id="d36369e499">

Type

</th><th align="left" id="d36369e502">

Description

</th></tr></thead><tbody><tr><td id="d36369e508">

**None**

</td><td>

The From address isn’t generated in the email client message.

</td></tr><tr><td id="d36369e517">

**SMTP Email Account**

</td><td>

Use the From address of the SMTP email account for the instance as the sender.

</td></tr><tr><td id="d36369e526">

**Select From List**

</td><td>

Choose from a list of allowable From addresses defined in the Email Client From Address \[sys\_email\_client\_from\_address\] table.

</td></tr><tr><td id="d36369e535">

**Script**

</td><td>

Run a GlideRecord query on the Email Client From Address \[sys\_email\_client\_from\_address\] table.For example, the following script sets the From address based on the location of the incident caller:

```
(function (fromAddressQuery, targetRecord) {
    // targetRecord is incident for this template
    var location = targetRecord.caller_id.country;

    if (location == 'us')
        fromAddressQuery.addQuery('email_address', 'servicedesk.us@example.com');
    else if (location == 'japan')
        fromAddressQuery.addQuery('email_address', 'servicedesk.jp@example.com');
    else if (location == 'uk')
        fromAddressQuery.addQuery('email_address', 'servicedesk.uk@example.com');

})(fromAddressQuery, targetRecord);
```

</td></tr><tr><td id="d36369e549">

**Text**

</td><td>

Enter the email From address to be used in the client.

</td></tr><tr><td id="d36369e558">

**User Email Addresses**

</td><td>

For integrating users or agents personal corporate mail boxes with ServiceNow to send and receive emails.**Note:** This requires User Mailbox Integration \(com.glide.email.user\_mailbox.integration\) plugin to be installed.

</td></tr></tbody>
</table>    Use this method only if you want a different From address than the one defined in your SMTP email account.

    **Note:**

    The From email address doesn’t appear in the email client unless you configure an email client to display the From address. For more information on managing the behavior of an email client, see [Email client configurations](../concept/email-client-configuration.md).

    If the domain for the From address isn’t the domain of the SMTP email account server, the owner of the From domain address must configure the SPF record for the domain. The owner changes the domain settings to enable the instance to send an email as if from that domain. For more information on using SPF records, see ServiceNow [KB0535456](https://support.servicenow.com/kb_view.do?sysparm_article=KB0535456).

7.  Select **Submit**.

    The template is added to the Email Client Templates \[sys\_email\_client\_template\] table.


**Parent Topic:**[Configure email client](../concept/configuring-email-client.md)

**Related topics**  


[Script includes](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=australia&pubname=australia-api-reference&ft:locale=en-US)

## Apply an email client template

After you create an email client template, you can apply it to an email.

### Before you begin

Role required: admin

### About this task

The following steps are implemented only after creating an email client template

### Procedure

1.  Click the ellipsis \(...\) icon at the top of the template to apply the template to an email.

2.  Select **Email**.

3.  Fill in the fields to compose an email.

    See [Create an email client template](t_CreateAnEmailClientTemplate.md#) for field details.

    **Note:** The body of the email is filled up with the details from the incident record. If you modify one or more fields in the incident record and are not saved, the unsaved changes still reflect in the email body.

    **Note:** 2000 characters is the total limit for all the changes in the incident record. If some of your changes are not reflected and get truncated in the email body, this is because the total changes is more than 2000 character limit.


## Create an email client response template

You can now create custom email client response templates that support conditions.

### Before you begin

Role required: admin

### About this task

Email client template is applied automatically in the email client based on the specified table, conditions, and execution order.

### Procedure

1.  Navigate to **All** &gt; **Email Client** &gt; **Email Client Templates**.

    The following options for **Response Template - Received** and **Response Template - Sent** show up.

2.  Click one of the available options to create a template for that selected option.

3.  Fill in the fields at the top of the Email Client Template form.

<table id="table_dpp_vtl_xfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Auto-filled template name based on the selected template option.**Note:** This is a read-only field.

</td></tr><tr><td>

Table

</td><td>

Auto-filled table name.**Note:** This is a read-only field because for response templates, the table name is always sys\_email.

</td></tr><tr><td>

Conditions

</td><td>

The conditions that determine when this client response template is used. Use the condition builder to identify the target record that must match before this template is applied.**Note:** If the conditions are not true, the email client gets the default template.

Select the target table name under conditions that the template applies to. Enable the response template for the same table.

 ![Image showing the target table](../image/target-table.png)

</td></tr><tr><td>

Application

</td><td>

The type of scoped application.

</td></tr><tr><td>

Execution Order

</td><td>

A number that indicates the order in which template conditions are evaluated.

</td></tr></tbody>
</table>4.  Fill in the fields in the **Content** tab.

<table id="table_f5h_lsl_qq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Subject

</td><td>

Enter a description of the email.**Note:** The **Subject** field on the email client allows a larger character count than the default setting for the **Subject** field on the Email \[sys\_email\] table. If the subject text from the client is being truncated, increase the **Max length** value for the **Subject** field on the Email table.

</td></tr><tr><td>

Content Type

</td><td>

Select the format of the message body content: HTML or plain text.

</td></tr><tr><td>

Body HTML

</td><td>

If you selected HTML for the **Content type**, enter the content of the message body using the HTML editor toolbar to format the HTML.

 To reference field values, select variables from the variables list or manually type variable references using the syntax `${table_name.variable_name}`. To reference the user who launches the email client, enter the variable `${current_user}`.

**Note:** Line breaks don't appear for multi-line fields such as $\{description\} and $\{comments\} in the email client template.

 You can call a mail script by using `${mail_script:script name}` in the **Body HTML** field.

</td></tr><tr><td>

Body text

</td><td>

If you selected plain text for the **Content type**, enter any text or mail script that you want to appear in the message body.

 You can insert a mail script in the **Body text** field by using the following syntax:

```
<mail_script> [code] </mail_script>
```

</td></tr></tbody>
</table>5.  Fill in the fields in the **Recipients** tab.

<table id="table_ybt_fcm_xfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

To

</td><td>

Enter a comma-separated list of either field names that contain user email addresses or just email addresses. To reference an email address using a script, create a script include and then call the script include in the **To** field. Your script must start with the `javascript:` prefix. The script must return email addresses in a comma-separated string. Use only one JavaScript expression and do not combine it with field names.

</td></tr><tr><td>

Cc

</td><td>

Enter a comma-separated list of either field names that contain user email addresses or just email addresses. To reference an email address using a script, create a script include and then call the script include in the **Cc** field. Your script must start with the `javascript:` prefix. The script must return email addresses in a comma-separated string. Use only one JavaScript expression and do not combine it with field names.

 This field can’t have the same addresses as the **To** field.

</td></tr><tr><td>

Bcc

</td><td>

Enter a comma-separated list of either field names that contain user email addresses or specific email addresses. To reference an email address using a script, create a script include and then call the script include in the **Bcc** field. Your script must start with the `javascript:` prefix. The script must return email addresses in a comma-separated string. Use only one JavaScript expression and do not combine it with field names.

 This field cannot have the same addresses as the **To** or **Cc** fields.

</td></tr></tbody>
</table>6.  In the **Sender Configuration** tab, select the **From Generation Type** to determine how the sender \(From address\) in the email client message is generated.

    Use this field only if you want a different From address than the one defined in your SMTP email account.

    -   None: The From address is not generated in the email client message.
    -   SMTP Email Account: Use the From address of the SMTP email account for the instance as the sender.
    -   Select From List: Choose from a list of allowable From addresses defined in the Email Client From Address \[sys\_email\_client\_from\_address\] table.
    -   Script: Run a GlideRecord query on the Email Client From Address \[sys\_email\_client\_from\_address\] table.

        For example, the following script sets the From address based on the location of the incident caller:

        ```
        (function (fromAddressQuery, targetRecord) {
            // targetRecord is incident for this template
            var location = targetRecord.caller_id.country;
        
            if (location == 'us')
                fromAddressQuery.addQuery('email_address', 'servicedesk.us@example.com');
            else if (location == 'japan')
                fromAddressQuery.addQuery('email_address', 'servicedesk.jp@example.com');
            else if (location == 'uk')
                fromAddressQuery.addQuery('email_address', 'servicedesk.uk@example.com');
        
        })(fromAddressQuery, targetRecord);
        ```

    -   Text: Enter the email From address to be used in the client.
    **Note:** The From email address does not appear in the email client unless you configure email client to display the From address. For more information on managing the behavior of email client, see [Email client configurations](../concept/email-client-configuration.md).

    If the domain for the From address is not the domain of the SMTP email account server, the owner of the From domain must configure the SPF record for the domain. The owner changes the domain settings to allow the instance to send email as if from that domain. For details on using SPF records, see ServiceNow [KB0535456](https://support.servicenow.com/kb_view.do?sysparm_article=KB0535456).

7.  Click **Submit**.


