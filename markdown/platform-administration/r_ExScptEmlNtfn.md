---
title: Example scripting for email notifications
description: Examples of scripting for email notifications.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Scripting for email notifications, Create an email notification, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Example scripting for email notifications

Examples of scripting for email notifications.

## Scripting examples for email notifications

A simple text string is the most basic example of the way a mail script works. This script prints out "Incident number - INC00001".

```
template.print("Incident number - "+ current.number);
```

More advanced scripts, like this one, can be found by browsing through the base system email templates.

```
template.print("Summary of Requested items:<br />");  
var now_GR = new GlideRecord("sc_req_item");
now_GR.addQuery("request", current.sysapproval);
now_GR.query();
while(now_GR.next()) {
  template.print(now_GR.number + ":  " + now_GR.quantity + " X " + now_GR.cat_item.getDisplayValue() 
                   + " at " + now_GR.cat_item.price.getDisplayValue() + " each <br />");
}
```

To dynamically change field values within an email, use the following functions within &lt;mail\_script&gt; syntax:

```
...
email.setFrom(current.caller_id.email);
email.setReplyTo("joe.employee@yourcompany.com");
email.setSubject("This is the new subject line");
email.setBody("This is the new body");
...
```

Using the **instance\_name** property ensures that the notification still works when migrated between instances.

```
dothis();
 
function dothis(){
    var now_GR =new GlideRecord('sys_attachment');
    now_GR.addQuery('table_sys_id',current.sys_id);
    now_GR.query();while(now_GR.next()){
        template.print('Attachment: <a href="https://'+ gs.getProperty('instance_name')+'
            .service-now.com/sys_attachment.do?sys_id='+ now_GR.sys_id+'">'+ now_GR.file_name+'</a>');}}
```

You can specify copied and blind copied recipients by using the email object within a mail script.

```
//email.addAddress(type, address, displayname);
    email.addAddress("cc","john.copy@example.com","John Roberts");
    email.addAddress("bcc","john.secret@example.com","John Roberts");
```

The following is an example script to add users from **watch\_list** as copied recipients.

```
if(!current.watch_list.nil()){
   //get watch list addresses and add to cc
   var watcherIds = current.watch_list.split(",");
 
   //get user records
   var user = new GlideRecord("sys_user");
   user.addQuery("sys_id", watcherIds);
   user.addQuery("notification",2); 
   //email
   user.addQuery("email","!=","");
   user.query();
 
   while(user.next()){
      //add to cc list    
      email.addAddress("cc", user.email, user.getDisplayValue());}}
```

**Parent Topic:**[Scripting for email notifications](../concept/c_ScriptingForEmailNotifications.md)

**Related topics**  


[JavaScript in emails](../concept/c_UseJavaScriptInEmails.md)

[Mail script variables](r_MailScriptAPI.md)

[Useful attachment scripts](../../useful-scripts/reference/r_UsefulAttachmentScripts.md)

[TemplatePrinter API](https://www.servicenow.com/docs/access?context=c_TemplatePrinterScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

[GlideEmailOutbound API](https://www.servicenow.com/docs/access?context=c_GlideEmailOutboundScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

