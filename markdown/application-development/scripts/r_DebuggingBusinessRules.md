---
title: Debugging business rules
description: Debugging business rules can be achieved with resources available in the ServiceNow product.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Debugging scripts, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Debugging business rules

Debugging business rules can be achieved with resources available in the ServiceNow product.

## 1. Tools

The first step in the process is to identify tools which will help you figure out what's wrong.

|Debugging tool|Description|
|--------------|-----------|
|System Dictionary|Navigate to **System Definition** &gt; **Dictionary**. The dictionary provides a list of all tables within your instance and can be invaluable when trying to locate information.|
|System Log|Navigate to **System Logs** &gt; **System Log**. You can place alert statements in your business rule which can write information to the log.|
|Debug Business Rule \(Details\)|Navigate to **System Diagnostics** &gt; **Session Debug** &gt; **Debug Business Rule \(Details\)**. This debugging module displays the results business rules. Use this module to see if conditions are being met and values are being set as expected.|
|Alert Messages|There are several system functions that allow you to print messages to the page, the field or the log file. See [Scripting alert, info, and error messages](https://www.servicenow.com/docs/access?context=r_ScriptingAlertInfoAndErrorMsgs&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).|
|Business Rule Examples|Sometimes you can find what you're looking for in scripts others have written, including business rule error messages, or by building an OR query.|
|GlideRecord Information|This is the basic syntax used to query the database for information. See [Querying tables in script](https://www.servicenow.com/docs/access?context=c_UsingGlideRecordToQueryTables&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US). GlideRecord also includes aggregation support.|

## 2. Variables

The next step is to gain some insight into the behavior of your business rule. For every action except an insert, you will more than likely use a query to get your record\(s\).

```
var rec = new GlideRecord('incident');
rec.addQuery('active',true); 
rec.query();
while (rec.next()) {
 gs.print(rec.number + ' exists');
 }
```

To verify whether your query is actually returning records you can use *gs.addInfoMessage* to display information at the top of the screen.

```
var rec = new GlideRecord('incident');
rec.addQuery('active',true); 
rec.query();
gs.addInfoMessage("This is rec.next: " + rec.next());
while (rec.next()) {
 gs.print(rec.number + ' exists');
 }
```

If your query returns no records you see the following:

```
This is rec.next: false
```

Use this technique to verify every variable within your business rule contains expected values.

**Tip:** If necessary, break your script down into individual pieces and verify each piece works separate from the whole and then put them all back together one step at a time.

## 3. Locating information

The last step is to make sure you know where to find the information your rule is looking for.

In the ServiceNow application, one table can extend another table. This means when searching for information, you might need to query the parent table for the extended table's sys\_id to find what you seek.

A good example is the sc\_task table, which extends the task table. The script below queries the extended table \(sc\_task\) for the current sys\_id and then query the parent table \(task\) for records with the matching sys\_id, and then prints out the work notes field.

```
var kids = new GlideRecord('sc_task');
kids.query();
 
gs.addInfoMessage("This is requested item number: " + current.number);
gs.print("This is the requested item number: " + current.number);
 
while (kids.next()) { 
 var parents = new GlideRecord('task');
 parents.addQuery('sys_id', '=', kids.sys_id);
 parents.query();
 
 while(parents.next()) {
  gs.addInfoMessage("This is task number: " + parents.number);
  gs.print("This is task number: " + parents.number);
  gs.addInfoMessage("These are the work notes: " + parents.work_notes);
  gs.print("These are the work notes: " + parents.work_notes);
  }
 
 }
```

**Parent Topic:**[Debugging scripts](../../debugging/concept/script-debug-overview.md)

