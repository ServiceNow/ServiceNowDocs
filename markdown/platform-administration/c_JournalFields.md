---
title: Journal field type
description: There are three types of journal field: journal, journal\_list, and journal\_input.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Journal field type

There are three types of journal field: journal, journal\_list, and journal\_input.

|Journal field types|Description|
|-------------------|-----------|
|journal|Allow and store input, and display the combined inputs below the input box. Journal fields display in the activity stream in the form and in the list view.|
|journal\_input|Allow and store input, but do not display the combined inputs. Journal input fields only display with the record they are associated with, so they do not display in the activity stream on the list view.|
|journal\_list|Do not allow or store input; they merely display the contents of other Journal fields upon which the journal\_list field is dependent. If a journal\_list field is dependent on more than one Journal field, it will chronologically interweave those fields' inputs. The journal\_list field does not display content within the activity stream, but rather in a separate block.|

![Journal field types](../image/JournalFieldTypes.png "Journal fields on a form")

The example image contains the three available journal field types. The first is a journal field, with its inputs displayed below the field. The second is a journal input field, which does not show its previous inputs. The third is Journal list field, which is configured to show the input from the journal input field above it.

## Restricting journal entries sent in a notification

Administrators can control the number of journal entries notifications include with the following system property.

<table id="table_wj5_yw1_dr"><thead><tr><th>

Property

</th><th>

Label

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.email.journal.lines

</td><td>

Number of journal entries \(Additional comments, Work notes, etc.\) included in email notifications \(-1 means all\).

</td><td>

Specifies the number of entries from a journal field \(such as **Additional comments** and **Work notes**\) included in email notifications. A value of -1 includes all journal entries.

 -   Type: integer
-   Default value: 3
-   Location: System Properties &gt; Email

</td></tr></tbody>
</table>## Code for getting the contents of a journal field into an array

To put the contents of a journal field into an array so that you can iterate through each entry, you can use the code in this page.

```
var notes = current.work_notes.getJournalEntry(-1);
//gets all journal entries as a string where each entry is delimited by '\n\n'
var na = notes.split("\n\n");

//stores each entry into an array of strings
 for (var i = 0; i < na.length; i++)                 
  gs.print(na[i]);
```

## Journal field script values

The setValue\(\) method is not supported for journal fields. Instead, assign values in script as in the following example.

```
var now_GR = new GlideRecord('incident');
 
//query priority 1 incidents in the state of either 'new' or 'active'.
gr.addQuery('priority', 1);
var gc = gr.addQuery('state', 1);
gc.addOrCondition('state', 2);
gr.query();
 
while(gr.next())
{
 
//print a list of the incident numbers updated
gs.print(gr.number);
 
//add an entry to the 'work notes' journal field for each incident
gr.work_notes = "This is a high-priority incident. Please prioritize.";
gr.update();
}
```

