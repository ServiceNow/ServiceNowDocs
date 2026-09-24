---
title: Display business rules
description: Display business rules are processed when a user requests a record form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/business-rules-classic/c\_ScriptingWithDisplayBusinessRules.html
release: brazil
product: Business rules \(Classic\)
classification: business-rules-classic
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Classic Business rules, Build workflows]
---

# Display business rules

Display business rules are processed when a user requests a record form.

The data is read from the database, display business rules are executed, and the form is presented to the user. The current object is available and represents the record retrieved from the database. Any field changes are temporary since they are not yet submitted to the database. To the client, the form values appear to be the values from the database; there is no indication that the values were modified from a display business rule. This is a similar concept to calculated fields.

The primary objective of display business rules is to use a shared scratchpad object, *g\_scratchpad*, which is also sent to the client as part of the form. This can be useful when you need to build client scripts that require server data that is not typically part of the record being displayed. In most cases, this would require a client script making a call back to the server. If the data can be determined prior to the form being displayed, it is more efficient to provide the data to the client on the initial load. The form scratchpad object is an empty object by default, and used only to store name:value pairs of data.

To populate the form scratchpad with data from a display business rule:

```
// From display business rule
g_scratchpad.someName = "someValue";
g_scratchpad.anotherName = "anotherValue";
 
// If you want the client to have access to record fields not being displayed on the form
g_scratchpad.created_by = current.sys_created_by; 
 
// These are simple examples, in most cases you will probably perform some other 
// queries to test or get data
```

To access the form scratchpad data from a client script:

```
// From client script 
if(g_scratchpad.someName == "someValue") { 
  //do something special 
}
```

**Parent Topic:**[Classic Business rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/business-rules-classic/c_BusinessRules.md)

