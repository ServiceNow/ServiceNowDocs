---
title: Scripted templates
description: You can apply an active template to a record using JavaScript.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/r\_ScriptedTemplates.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Form templates, Administer, Form administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Scripted templates

You can apply an active template to a record using JavaScript.

## Apply a template to current

To apply a template, use the applyTemplate method.

```
current.applyTemplate("<templatename>");
```

## Apply a template to a GlideRecord

To apply the template to a record other than current, change current to a GlideRecord variable. When using a GlideRecord variable, you may need to initialize it after declaring the variable.

```
var rec1 = new GlideRecord("incident");
rec1.initialize();
rec1.applyTemplate("my_incident_template");
```

## Apply a template from a UI action

The following script demonstrates a possible customization to the **Create Change** UI action on the Problem form. After you add this script to the UI action, a user can select the UI action to create a change record with information from both the problem record and the change template.

```
var change = new GlideRecord("change_request");
change.initialize();
change.short_description = current.short_description;
change.description = current.u_details;
change.cmdb_ci = current.u_service;
change.priority = current.priority;
change.requested_by = current.caller_id;
change.assignment_group.setDisplayValue('Change & Release');
change.u_status = 'New';
change.parent = current.number;
if(0 == change.applyTemplate("standard_rfc")) {
    current.rfc = change.insert();
    current.comments = 'Change ' + change.number + ' created.';
}

var mySysID = current.update();

gs.addInfoMessage("Change " + change.number + " created");
action.setRedirectURL(change);
action.setReturnURL(current);
```

## Script a template with child templates

When using applyTemplate with a template that has one or more child templates, the system creates the parent record before applying the child templates. This behavior ensures that any references or dot-walked fields from the child record to the parent have a valid target.

For example, if a template for the Change Request table has a child template for the Change Task table, applying the Change Request template inserts a Change Request record into the database. It assigns this record as the Change request for the Change Task record, then applies the child template to the Change Task record.

## Apply a template using a sys\_id instead of a name

To apply a template using a sys\_id, use the following method.

```
GlideTemplate.get(template.sys_id).apply(GlideRecord)
```

**Parent Topic:**[Using form templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_Templates.md)

**Related topics**  


[Create a template using the Template form]()

[Create templates for related task records]()

[Create a template by saving a form]()

[Schedule record creation from a template]()

[Create a module for a template]()

[Template bar]()

[Toggle the template bar]()

