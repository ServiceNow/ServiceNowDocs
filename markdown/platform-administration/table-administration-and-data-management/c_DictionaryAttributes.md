---
title: Altering tables and fields using dictionary attributes
description: Dictionary attributes alter the behavior of the table or field that the dictionary record describes. Administrators can add or modify dictionary attributes.
locale: en-US
release: zurich
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 26
breadcrumb: [Managing tables and indexes, Table admin, Tables and data, Configure core features, Administer]
---

# Altering tables and fields using dictionary attributes

Dictionary attributes alter the behavior of the table or field that the dictionary record describes. Administrators can add or modify dictionary attributes.

## Adding an attribute

To add or remove an attribute to a table or field, open a dictionary record, select the **Advanced** link, and modify the **Attributes** field. Alternatively, in a dictionary record, select **New** in the Attributes related list. For details on modifying dictionary entries, see [Modify dictionary entries](../../data-dictionary-tables/task/t_ModifyADictionaryEntryFromAForm.md).

Attributes are comma-separated. If attributes exist on a dictionary record, add a comma with no spaces before adding an attribute.

For an attribute that accepts true/false values:

-   To specify a value of true, you can either enter `attribute` or `attribute=true`.
-   To specify a value of false, you can either ensure that the attribute does not appear or enter `attribute=false`. To maintain the values during upgrades, do not remove an attribute that is on a table by default.

## Maintaining attribute values for upgrades

If you remove an attribute that is part of the base system, it is automatically restored during an upgrade. To prevent upgrades from changing the behavior of your system, leave the attribute on the table or field, but set its value as desired.

For example, if a field has the attribute `knowledge_search=true` by default, do not remove the attribute to set it to false; rather set it to `knowledge_search=false`.

## Available dictionary attributes

<table id="table_gfb_bz2_3cc"><thead><tr><th>

Name

</th><th>

Value

</th><th>

Target Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

allow\_null

</td><td>

true/false

</td><td>

field\_name field

</td><td>

If present or true, enables you to enter `None` as the field

</td></tr><tr><td>

allow\_public

</td><td>

true/false

</td><td>

table\_name field

</td><td>

If true, the table name field displays tables from all scopes instead of only the current scope.

</td></tr><tr><td>

allow\_references

</td><td>

true/false

</td><td>

field\_name field

</td><td>

If true, a tree is displayed to select from that includes reference fields so you can dot-walk.

</td></tr><tr><td>

allowHugeAlter

</td><td>

true/false

</td><td>

any table

</td><td>

If true, enables you to add a column to a table with more than 100 million rows.

</td></tr><tr><td>

approval\_user

</td><td>

name of field containing the users for the approval type this field represents

</td><td>

integer field

</td><td>

Specifies the table fields that are used to perform lookups using a matcher. You specify approvals as table fields that have an attribute of **approval\_user=&lt;field\_name&gt;**, where &lt;field\_name&gt; indicates the field in the table that contains the users for this approval type. -   Fields with this attribute contain an integer value that indicates the sequence for the approvals.
-   All approval fields with the same sequence number indicate that multiple approvals are required before continuing.
-   Approvals are requested in the order of the sequence numbers. For example, all approvals with sequence number 100 must be approved before approvals with sequence number 200 are requested.

</td></tr><tr><td>

attachment\_index

</td><td>

true/false

</td><td>

any table

</td><td>

If true, attachments on the table are indexed for search purposes. To learn more, see [Index attachments on a table](../../form-administration/task/t_DisablingAttachmentsOnATable.md).

</td></tr><tr><td>

barcode

</td><td>

true/false

</td><td>

string field

</td><td>

Enables a string field to access a camera on a mobile device to scan and process a bar code.

</td></tr><tr><td>

base\_table

</td><td>

name of base table type

</td><td>

table\_name field

</td><td>

Specifies the table\_name field that enables you to select any table that is derived from the table specified by this attribute. By default, the base table itself is also included in the list \(but see **skip\_root** to turn off this behavior\).

</td></tr><tr><td>

calendar\_elements

</td><td>

list of field names, separated by semicolons \(";"\)

</td><td>

any calendar event table

</td><td>

Specifies the list of fields used when constructing the description of a calendar event. If not specified, the display name plus short description are used. The **calendar\_elements** attribute does not support derived \(dot-walked\) fields.

</td></tr><tr><td>

collection\_interval

</td><td>

interval specified as "HH:MM:SS" \(like "01:02:30" for one hour, two minutes, and 30 seconds\)

</td><td>

collection field

</td><td>

Specifies the interval of metrics collection.

</td></tr><tr><td>

close\_states

</td><td>

inactive state integer values

</td><td>

task state field

</td><td>

Used by the TaskStateUtil API to identify the list of inactive state values delimited by semicolons \(;\)

</td></tr><tr><td>

critical

</td><td>

true/false

</td><td>

any field in the apm\_application table

</td><td>

Defines fields that have critical information about an application, which enables tracking the entry of critical information.

</td></tr><tr><td>

current\_location

</td><td>

true/false

</td><td>

string field

</td><td>

Enables a string field to access the GPS location of a mobile device.

</td></tr><tr><td>

disable\_execute\_now

</td><td>

true/false

</td><td>

any table derived from sys\_auto

</td><td>

If present or true, disables the usual **Execute Now** button. The ServiceNow AI Platform applications that use schedules, such as Discovery, use this attribute to substitute their own more appropriate action.

</td></tr><tr><td>

default\_rows

</td><td>

integer value

</td><td>

multitext fields

</td><td>

Sets the default number of rows in a multitext field.

</td></tr><tr><td>

default\_close\_state

</td><td>

state integer value

</td><td>

task state field

</td><td>

Used by the TaskStateUtil API to identify the default close state value for a task table.

</td></tr><tr><td>

default\_work\_state

</td><td>

state integer value

</td><td>

task state field

</td><td>

Used by the TaskStateUtil API to identify the default working state value for a task table.

</td></tr><tr><td>

detail\_row

</td><td>

name of field to display in detail row

</td><td>

any table

</td><td>

Displays the value of the specified field as a [Lists](https://www.servicenow.com/docs/access?context=c_UseLists&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) for each record in the list view. UI15 is required to use this attribute.**Note:** If different **detail\_row** attributes are defined for a parent table and a child table, the system uses the child table attribute.

</td></tr><tr><td>

display\_image

</td><td>

true/false

</td><td>

table with fields of the user\_image type

</td><td>

If present or true, displays records of the user\_image type in an image form. If the record is in the \[sys\_user\] table, and the image is not available, the user initials are displayed.

</td></tr><tr><td>

document\_viewer\_audit

</td><td>

view, download, or all

</td><td>

any table

</td><td>

When the Document Viewer is enabled, this attribute keeps a record of the user actions that are performed on attachments. The values are as follows:-   **view**: Enables an audit when users view an attachment
-   **download**: Supplies audit information for only downloaded attachments
-   **all**: Shows audit information when attachments are viewed and downloaded

</td></tr><tr><td>

email\_client

</td><td>

true/false

</td><td>

any table

</td><td>

If present or true, causes an icon \(an envelope\) to appear in the more options menu in the form header. If you click it, a pop-up email client appears.

</td></tr><tr><td>

exclude\_auto\_recovery

</td><td>

true/false

</td><td>

any table

</td><td>

Disables automatic recovery of draft records for this table and its extensions.

</td></tr><tr><td>

exclude\_from\_rollback

</td><td>

true/false

</td><td>

any table

</td><td>

Excludes this table \(and any of its descendant tables\) from being recorded for rollback. For example, use this attribute to preserve records that are created from an automated test. For tables excluded by default, see [Tables excluded from rollback after running an automated test](https://www.servicenow.com/docs/access?context=atf-excluded-from-rollback&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

</td></tr><tr><td>

extensions\_only

</td><td>

true/false

</td><td>

any table

</td><td>

Specifies that the table should only have records in tables that extend it. For example, the Task table has this attribute because you would create incident, problem, change records, and not task records.

</td></tr><tr><td>

field\_list\_selector

</td><td>

true/false

</td><td>

any glide\_list

</td><td>

Enables the user to select a field from the dependent table \(or current if the dependent is not specified\). Some workflow activities use this attribute.

</td></tr><tr><td>

field\_decorations

</td><td>

UI Macro name list, separated by semicolons \(";"\)

</td><td>

most fields \(except list and multiline text fields\)

</td><td>

Similar to **ref\_contributions**, causes the named UI macro to be invoked when the field is rendered on a form.

</td></tr><tr><td>

format

</td><td>

format name

</td><td>

any numeric field

</td><td>

Specifies a named format to use instead of the standard numeric formatting. Options are as follows: -   **glide\_duration**: Formats a time specified in milliseconds as **ddd hh:mm:ss**.
-   **none**: Disables automatic number formatting \(for example, changes 2,500–2500\).

**Note:** This attribute applies only to display values and not user input values.

</td></tr><tr><td>

glide.db.oracle.ps.query

</td><td>

true/false

</td><td>

any table

</td><td>

If present and false, prevents the use of Oracle prepared queries on the table.

</td></tr><tr><td>

global\_visibility

</td><td>

true/false

</td><td>

any table with a sys\_domain column

</td><td>

If present or true, makes this table visible globally even if there are domain restrictions \(that is, the sys\_domain field has a value\).

</td></tr><tr><td>

hasLabels

</td><td>

true/false

</td><td>

any table

</td><td>

If present or true, marks this table as being the target of a label at some point. You can manually set this attribute, but it is normally set automatically whenever a label is generated. When true, the label engine runs on any change to the table, and updates the labels as needed.

</td></tr><tr><td>

hasListeners

</td><td>

true/false

</td><td>

any table

</td><td>

If present or true, marks this table as available for listeners to get events \(insert, update, delete\).

</td></tr><tr><td>

hasWorkflow

</td><td>

true/false

</td><td>

any table

</td><td>

Instructs the workflow engine to listen for changes to the table and fires events to a workflow when a record associated with a particular workflow has changed.

</td></tr><tr><td>

html\_sanitize

</td><td>

true/false

</td><td>

any HTML or translated HTML field

</td><td>

If present or true, enables HTML sanitization for the selected HTML or Translated HTML field. By default, performs HTML Sanitization on all HTML and Translated HTML fields. Set this attribute to false to disable sanitization.

</td></tr><tr><td>

html\_sanitize\_config

</td><td>

name of custom sanitizer configuration file

</td><td>

any HTML or translated HTML field

</td><td>

If present, performs sanitization using the specified configuration file instead of the default platform sanitizer. For example, the Embedded Help \[sys\_embedded\_help\_content\] table uses a specified file \(EmbeddedHelpSanitizerConfig\) for the help **Content** field.

</td></tr><tr><td>

i18n\_session\_language\_sortable

</td><td>

true/false

</td><td>

any string field

</td><td>

If true, enables sorting the column by the user's session language. If false, sorting by the user's session language is disabled and the column is sorted according to the English alphabet.

</td></tr><tr><td>

icons

</td><td>

name of JavaScript class

</td><td>

any workflow field

</td><td>

Specifies a JavaScript class that produces workflow icons.

</td></tr><tr><td>

ignore\_filter\_on\_new

</td><td>

true/false

</td><td>

any field

</td><td>

If true, prevents the fields on a form from populating with values from a filtered list.

</td></tr><tr><td>

image

</td><td>

relative path of image file

</td><td>

any table

</td><td>

Specifies an image file to use when a module or BSM map uses this table. This specification overrides the icons that would otherwise be used for the table.

</td></tr><tr><td>

include\_container\_types

</td><td>

true/false

</td><td>

any internal\_type field

</td><td>

Causes the field to render with container \(split\) types as well other types.

</td></tr><tr><td>

ip\_data\_control

</td><td>

-   none
-   canonical
-   expanded
-   canonicalize\_when\_possible \(default value\)

</td><td>

field type on any table

</td><td>

Checks whether the data should be normalized through the **ip\_data\_control** attribute. -   If the attribute is none, no conversion happens and data is inserted as-is.
-   If the attribute is canonical, values are inserted in their smaller canonical form.
-   If the attribute is expanded, values are inserted in the larger expanded form to facilitate comparisons.
-   If the attribute is canonicalize\_when\_possible, values are inserted in canonical form when it is a valid IP or as-is when it is not.

</td></tr><tr><td>

isOrder

</td><td>

true/false

</td><td>

any field

</td><td>

Sets the field as the default field that is used for the sort order in lists. Overridden by the **ORDERBY** URL parameter, or the user's sort preferences.

</td></tr><tr><td>

iterativeDelete

</td><td>

true/false

</td><td>

any table

</td><td>

If present or true, forces all row deletes to execute iteratively. Otherwise, you can perform some deletes using a more efficient bulk method.

</td></tr><tr><td>

json\_view

</td><td>

true/false

</td><td>

any table

</td><td>

if a JSON object is associated with the field, places an icon next to a field that, when you click it, displays the data interchange information.

</td></tr><tr><td>

knowledge\_custom

</td><td>

name of JavaScript function

</td><td>

any field

</td><td>

Specifies a JavaScript function to implement a custom knowledge search \(see **knowledge\_search**\).

</td></tr><tr><td>

knowledge\_search

</td><td>

true/false

</td><td>

string fields

</td><td>

If present or true, causes a knowledge search icon \(a small book\) to appear next to the field. Clicking this icon launches a pop-up window for searching the knowledge base, unless a custom knowledge search function has been specified. To learn more, see **knowledge\_custom**.

</td></tr><tr><td>

largeTable

</td><td>

true/false

</td><td>

any table

</td><td>

If present or true, marks this table as "large" to preventing table locking with specific MySQL database operations \(adding/removing a column/index, compacting a table\). Without this attribute \(or the **smallTable** attribute\), the **glide.db.large.threshold** property, or the default value of **5,000**, determines whether a table is large.

</td></tr><tr><td>

listen

</td><td>

true/false

</td><td>

any field

</td><td>

If present or true, calls a JavaScript function named &lt;tableName&gt;\_&lt;fieldName&gt;Listen, or globalListen if that function does not exist. It calls the function with arguments \(tableName, fieldName, oldValue, newValue\).

</td></tr><tr><td>

live\_feed

</td><td>

true/false

</td><td>

any field

</td><td>

If present or true, creates a toggle option on the activity formatter header for incidents, tasks, and problems. The toggle provides a choice between the **Live Feed** for that record \(also known as a document feed\) or the activity formatter fields already in use. To learn more, see [Activity formatter](../../form-administration/concept/c_ActivityFormatter.md#) for more details.

</td></tr><tr><td>

long\_label

</td><td>

true/false

</td><td>

any reference field

</td><td>

Long or short labels refer to the label that appears for reference fields on a form. For example, if the reference field contains the caller’s email address, the long label would be Caller Email, while the short label would be Email.

-   Usually the placement of the reference field on the form makes it clear what the field represents.
-   It uses the global property \(**glide.short.labels**\) to specify the type of labels that appear for all reference fields on any form.
-   You can override the global property for any reference field by setting the **short\_label=true** or **long\_label=true** attribute in the dictionary for the reference field.

</td></tr><tr><td>

maintain\_order

</td><td>

true/false

</td><td>

any glide\_list

</td><td>

If present or true, the up/down arrow order buttons appear to the right of the list of selected items.**Note:** You need to use the **Add multiple** button to see the order buttons.

</td></tr><tr><td>

mode\_toggler

</td><td>

true/false

</td><td>

any composite\_name field

</td><td>

If present or true, causes a name mode toggle icon \(a small right-pointing triangle\) to appear to the right of the label. Clicking this icon causes the field's rendering to change from a text field that accepts &lt;tablename&gt;.&lt;fieldname&gt; to a pair of reference choice boxes \(one for the table, the other for the field\). The latter is the default.

</td></tr><tr><td>

model\_class

</td><td>

binary Java class name

</td><td>

any field of type glide\_var

</td><td>

Specifies a model variable within the Java code. The model must have a class that implements the IVariablesModel interface.

</td></tr><tr><td>

model\_field

</td><td>

see description

</td><td>

any field of type glide\_var

</td><td>

Identifies a reference field in the record that has the model defined for it. For example, a workflow activity is associated with an activity definition. The activity definition has a related list of questions that make up the model for that activity definition. By using the activity\_definition as the model\_field for the activity, it builds the workflow activity model by reading the questions that are defined for the referenced activity definition.

</td></tr><tr><td>

nibble\_size

</td><td>

positive integer

</td><td>

any table affected by the table cleaner.

</td><td>

Specifies the maximum number of records that the table cleaner can delete in a single operation. The default value for this attribute is **250**.

</td></tr><tr><td>

nibble\_sleep

</td><td>

true/false

</td><td>

any table affected by the table cleaner.

</td><td>

If false, causes the table cleaner to perform cleanup operations without a pause between each operation.

</td></tr><tr><td>

no\_add\_me

</td><td>

true/false

</td><td>

any table

</td><td>

If present or true, hides the display of the Add Me icon that appears next to certain fields, such as the **Watch List** field.

</td></tr><tr><td>

no\_attachment

</td><td>

true/false

</td><td>

any table

</td><td>

If present or true, prevents the attachment icon \(a paperclip\) from appearing on the form header.

</td></tr><tr><td>

no\_attachments

</td><td>

true/false

</td><td>

any table

</td><td>

If present or true, attachments are not checked for and deleted when a record from this table is deleted. Meant for high-activity tables that never have attachments.

</td></tr><tr><td>

no\_audit

</td><td>

true/false

</td><td>

any table

</td><td>

If present, this field is not audited, even if the table is being audited. The true or false value is ignored.

</td></tr><tr><td>

no\_audit\_delete

</td><td>

true/false

</td><td>

any table

</td><td>

If present or true, a sys\_audit\_delete record is never created when you delete a record from this table. Meant for high-activity tables that never need sys\_audit\_delete information.

</td></tr><tr><td>

no\_auto\_map

</td><td>

true/false

</td><td>

any table

</td><td>

If true, this field is not mapped during an import set. Primarily used for LDAP imports.

</td></tr><tr><td>

no\_email

</td><td>

true/false

</td><td>

any glide\_list field referencing sys\_user

</td><td>

If present or true, the email box is removed from the glide\_list field like the **Watch list** field.

</td></tr><tr><td>

no\_multiple

</td><td>

true/false

</td><td>

any glide\_list field

</td><td>

Hides the select multiple icons.

</td></tr><tr><td>

no\_optimize

</td><td>

true/false

</td><td>

any table affected by the table cleaner.

</td><td>

If present or true, prevents the MySQL table compaction operation from running on the specified table. The table compaction operation typically runs after the table cleaner deletes at least 50 percent of the data in the specified table.

</td></tr><tr><td>

no\_separation

</td><td>

true/false

</td><td>

any table

</td><td>

If present or true, marks this table as not participating in domain separation. To learn more, see [Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

</td></tr><tr><td>

no\_text\_index

</td><td>

true/false

</td><td>

any field on a text indexed table, or any child table of a text indexed table

</td><td>

If a table is text indexed, the **no\_text\_index** field attribute prevents this field or child table from being included in the text index.

</td></tr><tr><td>

no\_truncate

</td><td>

true/false

</td><td>

any string field

</td><td>

In a list view, shows the entire text value of the multitext value in a list, without truncating it. Without this attribute, the string is truncated based on the UI property **Number of characters displayed in list cells** which is **40** by default.

</td></tr><tr><td>

no\_update

</td><td>

true/false

</td><td>

table

</td><td>

True for tables in which records are inserted or deleted but not updated. Prevents the system from creating sys\_mod\_count, sys\_updated\_by, sys\_updated\_on fields in the table when created. Does not stop updates of the table. This attribute setting is used to save space on high volume system tables, such as syslog and sys\_audit.

</td></tr><tr><td>

no\_view

</td><td>

true/false

</td><td>

any glide\_list field

</td><td>

Hides the view-selected item icon.

</td></tr><tr><td>

omit\_sys\_original

</td><td>

true/false

</td><td>

price and currency type fields

</td><td>

When true, avoids retrieving the original value of a field during calculations. Omitting the sys\_original value from being referenced during calculations can reduce performance issues when dealing with currencies or prices.

</td></tr><tr><td>

onlineAlter

</td><td>

true/false

</td><td>

any table

</td><td>

Tables with the **onlineAlter** attribute perform MySQL database operations using online schema changes. -   Online schema changes provide a lock-free table upgrade when adding, modifying, or removing columns and when adding or dropping indexes. Without online schema changes, these changes to the database lock write access during execution.
-   Online schema changes use additional system resources. Oracle databases do not lock tables by default and do not use online schema changes.

</td></tr><tr><td>

order

</td><td>

numeric value

</td><td>

model variable fields

</td><td>

Used internally only \(for model variables\).

</td></tr><tr><td>

pop-up\_processor

</td><td>

binary Java class name

</td><td>

any field or table

</td><td>

Specifies a custom pop-up processor for processing the field \(or all fields in a table\).

</td></tr><tr><td>

readable

</td><td>

true/false

</td><td>

any conditions field

</td><td>

When true, causes rendering of the conditions field in any list view as a human-readable condition \(instead of the encoded query that is stored in the database\).

</td></tr><tr><td>

ref\_ac\_columns

</td><td>

list of field names separated by semi-colons

</td><td>

any reference field with an auto completer \(see ref\_auto\_completer\)

</td><td>

Specifies the columns whose display values should appear in an auto completion list, in addition to the name. To learn more, see the cmdb\_ci field \(**Configuration Item**\) on the Incident form for a working example.

</td></tr><tr><td>

ref\_ac\_columns\_search

</td><td>

true/false

</td><td>

any reference field with an auto completer \(see ref\_auto\_completer\)

</td><td>

Causes auto-complete to work with all fields that are specified in the **ref\_ac\_columns** attribute. This attribute overrides the default behavior, which searches only the display value column. To learn more, see [Configure auto-complete to match text from any reference field](../../field-administration/concept/c_AutoCompleteForReferenceFields.md#).

</td></tr><tr><td>

ref\_ac\_display\_value

</td><td>

true/false

</td><td>

any reference field with an auto completer \(see ref\_auto\_completer\)

</td><td>

Causes the reference field to hide the display value column so that the auto-complete function only matches the text from the columns that are listed in the **ref\_ac\_columns** attribute. This feature requires the use of the AJAXTableCompleter class and the **ref\_ac\_columns**, **ref\_ac\_columns\_search**, and **ref\_ac\_display\_value** attributes. To learn more, see [Remove the display value column](../../field-administration/concept/c_AutoCompleteForReferenceFields.md#).

**Note:** The ref\_ac\_display\_value function does not work with Catalog Item variables.

</td></tr><tr><td>

ref\_ac\_order\_by

</td><td>

field name

</td><td>

any reference field with an auto completer \(see ref\_auto\_completer\)

</td><td>

Specifies the column that is used to order the auto completion list.

</td></tr><tr><td>

ref\_auto\_completer

</td><td>

JavaScript class name

</td><td>

any reference field \(can be applied to a table to affect all reference fields on the table.\)

</td><td>

Specifies the name of a JavaScript class \(client side\) that creates the list auto completion choices. Valid class values include: -   AJAXReferenceCompleter: Matching auto-complete choices appear as a list. Only the [Display values](../../field-administration/concept/c_DisplayValues.md) column of the reference table appears. If there is no other auto-completion class specified, reference fields automatically use this class.
-   AJAXTableCompleter: Matching auto-complete choices appear as rows in a table. The display value column of the reference table appears, with any columns listed in the **ref\_ac\_columns** attribute.
-   AJAXReferenceChoice: Displays matching auto-complete choices as a list. Only the display value column of the reference table, and up to 25 matching choices, appear. If there are more than 25 auto-complete choices, the choices for the AJAXTableCompleter class appear for the reference field instead.

 For more information, see [Auto-complete for reference fields](../../field-administration/concept/c_AutoCompleteForReferenceFields.md#).

</td></tr><tr><td>

ref\_contributions

</td><td>

UI Macro name list, separated by semicolons \(";"\)

</td><td>

any reference field

</td><td>

When the field renders on a form, it invokes the named UI macro.

</td></tr><tr><td>

ref\_decoration\_disabled

</td><td>

true/false

</td><td>

any reference field

</td><td>

When set to `true`, disables the display of the reference icon on a selected field.

</td></tr><tr><td>

ref\_list\_label

</td><td>

label text

</td><td>

any table

</td><td>

Specifies the title to use in a list banner.

</td></tr><tr><td>

ref\_qual\_elements

</td><td>

field name list, separated by semicolons \(";"\)

</td><td>

any reference field with a reference\_qual field

</td><td>

Specifies a list of fields to send back to the server to get an updated reference.

</td></tr><tr><td>

ref\_sequence

</td><td>

list of fields in referenced table, separated by top hats \("^"\)

</td><td>

any reference field

</td><td>

Specifies the fields in the referenced table that are used to order the list. This attribute works like an ORDER BY clause in SQL, with each element in ascending order.

</td></tr><tr><td>

reference\_types

</td><td>

list of valid reference types that are clickable separated by semicolons \(";"\)

</td><td>

field\_name field

</td><td>

Limits the reference fields that appear in the tree to the specified types.

</td></tr><tr><td>

remoteDependent

</td><td>

name of database and table \(like "model.matcher"\)

</td><td>

any script field

</td><td>

Defines the remote \(such as in another database\) table that the script depends on.

</td></tr><tr><td>

repeat\_type\_field

</td><td>

field name

</td><td>

a repeat count field for schedule rotation

</td><td>

Specifies the field that contains the repeat type \(daily, weekly, monthly, or yearly\).

</td></tr><tr><td>

ro\_collapsible

</td><td>

true/false

</td><td>

any multiline field

</td><td>

If present or true, causes an icon \(either a "+" or a "-"\) to appear next to the field label, allowing the field itself to be expanded or collapsed.

</td></tr><tr><td>

saver\_exempt

</td><td>

-   exempt\_always= field will be skipped from writing to xml for all install contexts.
-   exempt\_never= field will not be skipped from writing to xml \(Default\).
-   exempt\_vcs\_only= field will be skipped from writing to xml only in source control context.

</td><td>

Fields of metadata records

</td><td>

When present, determines if the field is written to the xml representation of the record. An absence of the attribute is equivalent to exempt\_never. When exempt\_always, the field is skipped from writing to xml when exporting \(publish, commit to source control, update set\). When exempt\_vcs\_only, the field is skipped from writing to xml only in the source control context.

</td></tr><tr><td>

scale

</td><td>

integer

</td><td>

decimal field

</td><td>

Sets the number of decimal places to use on a Decimal field type. The default is 2. This attribute is applied to the max length attribute setting for the field. The decimal places for a field are a combination of the max length attribute setting and the scale attribute. For example, if you want four decimal places for the field, you need a max length attribute setting of 4, plus the default of 15 or 19. You would set the scale attribute to 4 to indicate the number of decimal places. Six decimal places require a max length setting of 21, a scale attribute setting of 6, and so on.

 **Note:** Increase the max length attribute to a value greater than 15 to increase this attribute.

</td></tr><tr><td>

script

</td><td>

a function that returns the contents of the field

</td><td>

any slushbucket field

</td><td>

Enables you to write a script to define what is loaded into the slush bucket field.

</td></tr><tr><td>

short\_label

</td><td>

true/false

</td><td>

any reference field

</td><td>

Long or short labels refer to the label that appears for reference fields on a form. For example, if the reference field contains the caller’s email address, the long label would be Caller Email, while the short label would be Email.

-   Usually the placement of the reference field on the form makes it clear what the field represents.
-   The global property \(**glide.short.labels**\) specifies the type of labels that appear for all reference fields on any form.
-   You can override the global property for any reference field by setting the **short\_label=true** or **long\_label=true** attribute for the reference field in the dictionary

</td></tr><tr><td>

show\_all\_tables

</td><td>

true/false

</td><td>

document ID fields

</td><td>

Enables users to select documents from system tables. For example, sys\_script or sys\_user. By default, users cannot select records from system tables.

</td></tr><tr><td>

show\_condition\_count

</td><td>

true/false

</td><td>

condition fields

</td><td>

Enables or disables the condition count widget to preview how many records are a set of conditions. To learn more, see [Add the condition count to a condition field](../../field-administration/task/t_AddingTheConditionCountWidget.md).

</td></tr><tr><td>

skip\_root

</td><td>

true/false

</td><td>

table\_name field

</td><td>

If present or true, removes the base table from the list. To learn more, see base\_table.

</td></tr><tr><td>

sla\_basis

</td><td>

list of table names separated by semicolons \(";"\)

</td><td>

any field of date type \(glide\_date\_time, glide\_date, due\_date, date, or datetime\)

</td><td>

Defines the tables for which this field determines the start \(open\) time of an SLA.

</td></tr><tr><td>

sla\_closure

</td><td>

list of table names separated by semicolons \(";"\)

</td><td>

any field of date type \(glide\_date\_time, glide\_date, due\_date, date, or datetime\)

</td><td>

Defines the tables for which this field determines the ending \(close\) time of an SLA.

</td></tr><tr><td>

slushbucket\_ref\_no\_expand

</td><td>

true/false

</td><td>

any reference field

</td><td>

If present or true, prevents users from expanding the field from a form or list slush bucket.

</td></tr><tr><td>

smallTable

</td><td>

true/false

</td><td>

any table

</td><td>

If present or true, marks this table as Small \(that is, not large\) for querying purposes. Without this attribute \(or the **largeTable** attribute\), the **glide.db.large.threshold** property, or a default value of **5,000** determines whether the table is large.

</td></tr><tr><td>

start\_locked

</td><td>

true/false

</td><td>

any glide\_list field

</td><td>

Determines whether the field is locked or unlocked by default. Set the value to false to unlock the field by default.

</td></tr><tr><td>

staticDependent

</td><td>

name of table

</td><td>

any script field

</td><td>

Specifies the table that the script depends on.

</td></tr><tr><td>

strip\_html\_in\_pdf

</td><td>

true/false

</td><td>

any field

</td><td>

Attempts to remove HTML tags from a field when that field is exported to a PDF. This attribute is most useful on HTML fields.

</td></tr><tr><td>

synch\_attachments

</td><td>

true/false

</td><td>

any table

</td><td>

Similar to **update\_synch** but writes the file attachments of the record to update sets. To learn more, see [Index attachments on a table](../../form-administration/task/t_DisablingAttachmentsOnATable.md).

</td></tr><tr><td>

table

</td><td>

name of table

</td><td>

field\_name field

</td><td>

Displays the specified table fields.

</td></tr><tr><td>

tableChoicesScript

</td><td>

name of script include

</td><td>

table\_name field

</td><td>

Specifies the name of a script include whose process\(\) method returns an array of table names from which to select.

</td></tr><tr><td>

target\_field

</td><td>

percent\_complete\_target decimal field name

</td><td>

any percent complete fieldany decimal field

</td><td>

Works in combination with the target\_threshold\_colors attribute to define thresholds for percent complete fields. See the description for target\_threshold colors.Example:

 ```
target_field=percent_complete_target,target_threshold_colors=0:tomato;50:khaki;90:lightgreen
```

 Specify an additional target\_field attribute to compare the actual completion percentage of a task with a target percentage in a different decimal field that specifies where the task should be at this point. Use the column name of the decimal field.

 Example:

 ```
target_field=percent_complete_target,target_threshold_colors=0:tomato;50:khaki;90:lightgreen,target_field=u_expected_completion
```

 If you do not specify an additional target\_field, a target value of 100 is used, allowing you to use the color thresholds with a single field value. See [Target threshold colors attribute](../../field-administration/concept/c_TargetThresholdColorsAttribute.md#).

</td></tr><tr><td>

target\_form

</td><td>

name of form

</td><td>

any table

</td><td>

Specifies the alternative form to be used when this table is referenced through a pop-up window on a reference field.

</td></tr><tr><td>

target\_threshold\_colors

</td><td>

threshold limit:color

</td><td>

any percent complete field with the target\_field attribute

</td><td>

Works in combination with the target\_field attribute to define thresholds for percent complete fields. See the description for target\_field.

</td></tr><tr><td>

text\_index\_filter\_junk

</td><td>

true/false

</td><td>

any table

</td><td>

Sets the value to false to [Enable or disable the Zing junk filter](../../search-administration/task/t_DisableTheJunkFilter.md) for the table. -   By default, Zing does not index or search for two-digit numbers and single character words \(unless they are Chinese or Japanese characters\).
-   Regenerate the index after disabling the junk filter. This attribute results in a larger table index.
-   For optimal performance, do not apply it unless it is required.

</td></tr><tr><td>

text\_search\_only

</td><td>

true/false

</td><td>

table\_name field

</td><td>

Limits the tables listed to those tables that are searchable by text.

</td></tr><tr><td>

text\_index\_translations

</td><td>

true/false

</td><td>

any table

</td><td>

If present or true, forces indexes to be recalculated when translated strings are added. You must have a sys-admin role to modify this attribute. This one is automatically set for indexed fields that are translated, and to fields that have a translation and are being indexed. The **glide.i18n.force\_index system** property, which defaults to true, overrides this attribute.

</td></tr><tr><td>

time\_zone\_field

</td><td>

name of field containing the time zone

</td><td>

any schedule date/time field

</td><td>

Specifies the field in the parent record that contains the reference time zone for this field.

</td></tr><tr><td>

timeDimension

</td><td>

true/false

</td><td>

any field of date type \(glide\_date\_time, glide\_date, due\_date, date, or datetime\) in a table subclassed from the task table

</td><td>

If present or true, enables the production of time dimension data for use by OLAP \(to produce reports based on quarters, weeks, or other time periods\). **Note:** OLAP functionality has been deprecated.

</td></tr><tr><td>

tree\_picker

</td><td>

true/false

</td><td>

reference field to a hierarchical table

</td><td>

Displays the hierarchy of reference values in a tree display \(such as locations\). **Note:** The tree display hierarchy does not appear in reference fields when you are using mobile applications.

</td></tr><tr><td>

ts\_weight

</td><td>

integer value

</td><td>

any field

</td><td>

Controls the relative importance of a match in the field for a text search. To learn more, see [Set the relative weight of a field](../../search-administration/task/t_ControlMatchRelevanceByField.md).

</td></tr><tr><td>

types

</td><td>

list of valid element types separated by semicolons \(";"\)

</td><td>

field\_name field

</td><td>

Limits the display of fields to the specified types.

</td></tr><tr><td>

update\_exempt

</td><td>

true/false

</td><td>

any field from a table that has update\_synch set to true

</td><td>

If present or true, you can change this field without skipping updates to the rest of the record. During software upgrades, the value of this field is preserved, while the rest of the record receives upgrades. By default, the Active field on a tracked table is treated as update\_exempt even if the attribute is not present.

</td></tr><tr><td>

update\_synch

</td><td>

true/false

</td><td>

any table

</td><td>

Indicates that changes in the table are tracked in update sets. Administrators cannot modify this attribute. To migrate data, use an [Importing from another ServiceNow instance](https://www.servicenow.com/docs/access?context=c_ImportingFromAnotherSNInstance&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

</td></tr><tr><td>

use\_document\_viewer

</td><td>

true/false

</td><td>

any table

</td><td>

If present or true, enables users to open supported attachments in a document viewer within the platform, rather than downloading the files directly to their own file system.

</td></tr><tr><td>

use\_workflow

</td><td>

true/false

</td><td>

any table that has delivery plans or uses workflow

</td><td>

If present or true, causes a workflow to be used instead of delivery plans.

</td></tr><tr><td>

user\_preference

</td><td>

true/false

</td><td>

any field

</td><td>

If present or true, causes any user preferences to be used instead of the normal default value.

</td></tr><tr><td>

vertical\_layout

</td><td>

true/false

</td><td>

radio buttons

</td><td>

If true, displays the radio buttons vertically.

</td></tr></tbody>
</table>-   **[Modify the Glide durations format](../../data-dictionary-tables/concept/c_ModifyTheGlideDurationsFormat.md)**  
To convert fields that are displayed in milliseconds \(such as 'Resolution Time' on the Incident table\) to a duration format \(Months/Days/Hours/Seconds\), populate the attribute field on the dictionary with: `format=glide_duration`.

**Parent Topic:**[Managing tables and indexes](../../table-administration/concept/using-table-administration.md)

