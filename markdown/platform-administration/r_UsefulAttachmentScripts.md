---
title: Useful attachment scripts
description: This is a searchable version of the Useful Attachment Scripts.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Scripting for email notifications, Create an email notification, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Useful attachment scripts

This is a searchable version of the Useful Attachment Scripts.

**Warning:** The customization described here was developed for use in specific instances, and is not supported by Now Support. This method is provided as-is and should be tested thoroughly before implementation. Post all questions and comments regarding this customization to our community [forum](http://community.service-now.com/).

## Copy attachments from record to record

Use the following script to copy an attachment from one record to another record:

```
GlideSysAttachment.copy('sourcetable','sys_id','destinationtable','sys_id');
```

**Note:** GlideSysAttachment.copy copies all attachments; it cannot select specific attachments.

## Delete duplicate attachments

Use the following script in a business rule, scheduled job, or background script to delete duplicate attachments located in the Attachments \[sys\_attachment\] table:

```
function fixDuplicateImages(){
  var now_GR = new GlideRecord('sys_attachment');
  now_GR.addQuery('table_name','LIKE','ZZ_YY%');
  now_GR.orderBy('table_sys_id');
  now_GR.orderByDesc('sys_created_on');
  now_GR.query();
  var lastID ='not_a_match';
  var lastFile ='not_a_match';
  while(now_GR.next()){
    var isDuplicate = (lastID == now_GR.table_sys_id)&&(lastFile == now_GR.file_name);
    lastID = now_GR.table_sys_id;
    lastFile = now_GR.file_name;
    gs.print(now_GR.table_sys_id + ' ' + now_GR.table_name + ' ' + now_GR.file_name + ' ' + now_GR.sys_created_on + ' ' + isDuplicate);
    if(isDuplicate)
      now_GR.deleteRecord();
  }
}
```

## Display whether tasks have attachments in list view

Use the following script in a business rule to display whether tasks have attachments when viewed in the record list view. Note that the script needs a custom field on the Has Attachments \[u\_has\_attachments\] table.

```
checkAttachment();
 
function checkAttachment(){
  // if inserting then the task has an attachment
  if(current.operation()=='insert') {
    hasAttachment('true'); // if deleting attachment check for other attachments
    if(current.operation()=='delete') {
      var timeNow3 =new GlideDateTime();
      gs.log('has_attachment br: gliderecord query start date time is: '+ timeNow3.getNumericValue(),'jwtest');
      var attachCount = new GlideAggregate('sys_attachment');
      attachCount.addQuery('table_sys_id',current.sys_id);
      attachCount.addAggregate('COUNT');
      attachCount.query();
      var numAttachments ='0'; 

      // if no other attachments task does not have attachment
      if(attachCount.next()){
        numAttachments = attachCount.getAggregate("COUNT");
        if(numAttachments >0){
          hasAttachment ='true';
        } else {
          hasAttachment('false');
        }
        var timeNow4=new GlideDateTime();
        gs.log('has_attachment br: gliderecord query start date time is: '+ timeNow4.getNumericValue(),'jwtest');
      }
 
function hasAttachment(answer){
  var task = new GlideRecord('task');
  task.addQuery('sys_id',current.table_sys_id);
  task.query();
 
  if(task.next()){
    task.u_has_attachment= answer;
    task.autoSysFields(false);  //Don't set the lastUpdatedTime or the Simultaneous Update Alert will likely get triggered
    task.setWorkflow(false);  //Don't allow other business rules to run, otherwise multiple notifications will likely be sent
    task.update();
  }
}
```

**Note:** Schedule the business rule to run after insert/delete.

## Link to attachments in an email notification

Use the following script in an email notification or template to include links to attachments:

```

printattachments(); 
 
function printattachments(){
  var now_GR =new GlideRecord('sys_attachment');
  now_GR.addQuery('table_sys_id',current.sys_id);
  now_GR.query();
  while(now_GR.next()){
    template.print('Attachment: <a href="http://'+gs.getProperty("instance_name")+'.service-now.com/sys_attachment.do?sys_id='+ now_GR.sys_id+'">'+ now_GR.file_name+'</a>');
  }
}
```

**Note:** Replace "instance\_name" with your instance name.

## Attachment Logging

Whenever a user downloads an attachment, the action writes an attachment.read event record to the event log. If desired, you can process these events with a Script Action or an Email Notification. This can be useful if you want to do something when an attachment is read. For example, you can record when and by whom certain attachments are downloaded. For this functionality, the current variable must point to a sys\_attachment record, and the event record must use the following parameters:

-   parm1: File name
-   parm2: Table name

**Parent Topic:**[Scripting for email notifications](../../server-scripting/concept/c_ScriptingForEmailNotifications.md)

**Related topics**  


[JavaScript in emails](../../server-scripting/concept/c_UseJavaScriptInEmails.md)

[Mail script variables](../../server-scripting/reference/r_MailScriptAPI.md)

[Example scripting for email notifications](../../server-scripting/reference/r_ExScptEmlNtfn.md)

