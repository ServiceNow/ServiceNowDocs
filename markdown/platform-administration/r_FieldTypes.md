---
title: Field types reference
description: These field types are available to administrators when creating fields or changing the type of existing fields.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 13
breadcrumb: [Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Field types reference

These field types are available to administrators when creating fields or changing the type of existing fields.

<table id="table_nkv_4m4_y4"><thead><tr><th>

Field type

</th><th>

Platform name

</th><th>

Supported in configurable workspace

</th><th>

Description

</th></tr></thead><tbody><tr><td>

approval\_rules

</td><td>

Approval Rules

</td><td>

No

</td><td>

 

</td></tr><tr><td>

audio

</td><td>

Audio

</td><td>

No

</td><td>

Audio field for uploading and embedding `.mp3` or `.ogg` audio files.

</td></tr><tr><td>

auto\_increment

</td><td>

Auto Increment

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

auto\_number

</td><td>

Auto Number

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

boolean

</td><td>

True/False

</td><td>

Yes

</td><td>

True/False field that holds a true or false value, typically displayed as a check box.

</td></tr><tr><td>

bootstrap\_color

</td><td>

Bootstrap Color

</td><td>

No

</td><td>

 

</td></tr><tr><td>

breakdown\_element

</td><td>

Breakdown Element

</td><td>

No

</td><td>

 

</td></tr><tr><td>

calendar\_date\_time

</td><td>

Calendar Date and Time

</td><td>

No

</td><td>

 

</td></tr><tr><td>

catalogue\_preview

</td><td>

Catalog Preview

</td><td>

No

</td><td>

 

</td></tr><tr><td>

char

</td><td>

Char

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

choice

</td><td>

Choice

</td><td>

Yes

</td><td>

Choice field that restricts values to a list of options, which is ideal for fields with a limited set of valid entries. For example, a priority field or a category field.

</td></tr><tr><td>

collection

</td><td>

Collection

</td><td>

No

</td><td>

Collection field type that applies any changes made to the assigned field also to the entire tableFor example, changes such as attributes or the **Read only** check box that are applied to a table entry with this field type are applied to the table rather than a specific field. This entry is automatically created when a table is created. There shouldn't be more than one entry for a table of this type.

</td></tr><tr><td>

color

</td><td>

Color

</td><td>

No

</td><td id="entry_ColorField">

String field that accepts CSS color declarations,including hex or RGB notation, and displays a preview. For more information on CSS color declarations, go to the Mozilla developer web docs. See the "&lt;color&gt;" article. [https://developer.mozilla.org/en-US/docs/Web/CSS/color\_value](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value).

</td></tr><tr><td>

color\_display

</td><td>

Color Display

</td><td>

No

</td><td>

 

</td></tr><tr><td>

composite\_field

</td><td>

Composite Field

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

composite\_name

</td><td>

Composite Name

</td><td>

No

</td><td>

 

</td></tr><tr><td>

compressed

</td><td>

Compressed

</td><td>

No

</td><td>

Compressed field that stores large binary data in a compressed format, reducing database storage requirements.It's used for files like images or documents, automatically compressing and decompressing data to optimize performance. This field type helps maintain efficient storage and database performance, especially when handling large volumes of data.

</td></tr><tr><td>

condition\_string

</td><td>

Condition String

</td><td>

Yes

</td><td>

Text field that accepts a plain JavaScript condition statement that is validated automatically for correctness before an update.

</td></tr><tr><td>

conditions

</td><td>

Conditions

</td><td>

Yes

</td><td id="Conditions">

Field that adds the condition builder to a form. You must specify a dependent field that references the table name.

</td></tr><tr><td>

counter

</td><td>

Counter

</td><td>

No

</td><td>

 

</td></tr><tr><td>

css

</td><td>

CSS

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

currency

</td><td>

Currency

</td><td>

Yes

</td><td id="entry_CurrencyField">

Decimal field with four digits after the decimal point.When displayed on a form, a **Currency** field also includes an additional list of choices for selecting the currency type. If there isn't a default value for the field, then empty **Currency** fields use the reference currency. Adding a value causes the field to use the session currency of the active user. See [Change default currency decimal places](../../currency/task/change-currency-fraction-digits.md) for how to use two fraction digits.

**Note:** After you assign this field type to a field, you can’t change it to the **FX Currency** field type.

</td></tr><tr><td>

currency2

</td><td>

FX Currency

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

data\_array

</td><td>

Data Array

</td><td>

No

</td><td>

 

</td></tr><tr><td>

data\_object

</td><td>

Data Object

</td><td>

No

</td><td>

 

</td></tr><tr><td>

data\_structure

</td><td>

Data Structure

</td><td>

No

</td><td id="entry_DataStructure">

Data structure field where you can select one of the following data structures and enter values to organize particular information in the record:-   String
-   Boolean
-   Integer
-   Decimal
-   Object
-   Array

</td></tr><tr><td>

date

</td><td>

Other date

</td><td>

Yes

</td><td>

Field used to store date and time values without requiring a time zone. Unlike glide\_date\_time, which is converted to UTC in the database, this field retains the date and time exactly as entered, without any conversion.

</td></tr><tr><td>

datetime

</td><td>

Date/Time

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

day\_of\_week

</td><td>

Day of Week

</td><td>

No

</td><td>

 

</td></tr><tr><td>

days\_of\_weeks

</td><td>

Days of Week

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

decimal

</td><td>

Decimal

</td><td>

Yes

</td><td id="entry_DecimalField">

Number field with up to two digits after the decimal points. For example, 12.34.

</td></tr><tr><td>

document\_id

</td><td>

Document ID

</td><td>

Yes

</td><td id="DocumentID">

Document ID field that references a record on a table.

</td></tr><tr><td>

documentation\_field

</td><td>

Documentation Field

</td><td>

Yes

</td><td>

Documentation field used by admins to add the label during table or field creation.

</td></tr><tr><td>

domain\_id

</td><td>

Domain ID

</td><td>

Yes

</td><td>

Domain ID field that contains a reference to the domain.

</td></tr><tr><td>

domain\_path

</td><td>

Domain Path

</td><td>

Yes

</td><td>

String field that contains a domain path, which is a series of three-character codes separated by a slash delimiter that uniquely identifies a domain. For more information on domain paths, see [Domain Separation- Advanced Concepts and Configurations \[KB0716268\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0716268) article in the Now Support Knowledge Base.

</td></tr><tr><td>

due\_date

</td><td>

Due Date

</td><td>

Yes

</td><td>

Date field that stores a date and time.

</td></tr><tr><td>

email

</td><td>

Email

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

email\_script

</td><td>

Email Script

</td><td>

Yes

</td><td>

Field used to create dynamic email templates. It provides the ability to use field name notation `(${fieldname})` to represent the dynamic value of variable. This field is a combination of text area and variable picker.

</td></tr><tr><td>

expression

</td><td>

Expression

</td><td>

No

</td><td>

 

</td></tr><tr><td>

external\_names

</td><td>

External Names

</td><td>

No

</td><td>

 

</td></tr><tr><td>

field\_list

</td><td>

Field List

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

field\_name

</td><td>

Field Name

</td><td>

Yes

</td><td id="entry_FieldName">

Reference field for a field name in the table that is selected in a **Table Name** field type. Make this field dependent on the **Table Name** field.

</td></tr><tr><td>

file\_attachment

</td><td>

File Attachment

</td><td>

Yes

</td><td>

File attachment field that can hold one file. All file types are supported.

</td></tr><tr><td>

float

</td><td>

Floating Point Number

</td><td>

Yes

</td><td>

Floating Point Number fields use a default scale of 7, and the maximum length can't be set below 7 to ensure values can be stored and displayed correctly.

</td></tr><tr><td>

formula

</td><td>

Formula

</td><td>

No

</td><td>

 

</td></tr><tr><td>

geo\_point

</td><td>

Geo Point

</td><td>

No

</td><td>

Geo point field for holding longitude and latitude coordinates.

</td></tr><tr><td>

glide\_action\_list

</td><td>

Action List

</td><td>

No

</td><td>

 

</td></tr><tr><td>

glide\_date

</td><td>

Date

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

glide\_date\_time

</td><td>

Date/Time

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

glide\_duration

</td><td>

Duration

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

glide\_list

</td><td>

List

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

glide\_precise\_time

</td><td>

Precise Time

</td><td>

No

</td><td>

 

</td></tr><tr><td>

glide\_time

</td><td>

Time

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

glide\_utc\_time

</td><td>

UTC Time

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

glide\_var

</td><td>

Var

</td><td>

No

</td><td>

 

</td></tr><tr><td>

glyphicon

</td><td>

Glyph Icon

</td><td>

No

</td><td>

 

</td></tr><tr><td>

graphql\_schema

</td><td>

GraphQL Schema

</td><td>

No

</td><td>

 

</td></tr><tr><td>

GUID

</td><td>

Sys ID \(GUID\)

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

html

</td><td>

HTML

</td><td>

Yes

</td><td id="HTML">

String field with a built-in HTML editor. It supports formatted text with rich text editor and is useful for descriptions that need enhanced readability.

</td></tr><tr><td>

html\_script

</td><td>

HTML script

</td><td>

Yes

</td><td>

HTML script field that provides the ability to add variables in the form of field name notation `(${fieldname})` via a variable picker within the HTML editor. This field is used to create rich text content that also has dynamic values.

</td></tr><tr><td>

html\_template

</td><td>

HTML template

</td><td>

No

</td><td>

 

</td></tr><tr><td>

icon

</td><td>

Icon

</td><td>

No

</td><td>

String field that provides the user access to an icon picker in a form. By default, the favorites icon set is used.

</td></tr><tr><td>

image

</td><td>

Image

</td><td>

No

</td><td>

Image field used for uploading and embedding images.

</td></tr><tr><td>

index\_name

</td><td>

Index Name

</td><td>

No

</td><td>

 

</td></tr><tr><td>

insert\_timestamp

</td><td>

Insert Timestamp

</td><td>

No

</td><td>

 

</td></tr><tr><td>

int

</td><td>

Int

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

integer

</td><td>

Integer

</td><td>

Yes

</td><td id="entry_IntegerField">

Number field with zero decimal points.**Note:** To search for an integer, input `=` followed by the integer in the search bar. For example, if you want to search for an Order of 100, input `=100`.

</td></tr><tr><td>

integer\_date

</td><td>

Integer date

</td><td>

Yes

</td><td>

The int field type is used to store alphanumeric values similar to string field type.

</td></tr><tr><td>

integer\_time

</td><td>

Integer time

</td><td>

Yes

</td><td>

Field used to store time values, similar to glide\_time, but with a few key differences:-   The glide\_time field stores the time as a fully formatted string \(e.g., 1970-01-01 16:04:32\), whereas the integer\_time field stores it as a 6-digit string in a 24-hour format \(e.g., 160432\).
-   glide\_time supports time zones, meaning the displayed value changes based on the user's time zone settings. In contrast, integer\_time does not support time zone adjustments and always displays the same time regardless of the user's location.

</td></tr><tr><td>

internal\_type

</td><td>

Internal Type

</td><td>

No

</td><td>

 

</td></tr><tr><td>

ip\_addr

</td><td>

IP Address \(Validated IPV4, IPV6\)

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

ip\_address

</td><td>

IP address

</td><td>

Yes

</td><td>

Variable character field that stores IPv4 and IPv6 addresses. See [IP address field type](r-IPAddressFieldType.md) for more information.

</td></tr><tr><td>

journal

</td><td>

Journal

</td><td>

No

</td><td>

Journal field that accepts text entries and displays previous entries with a user name and timestamp.

</td></tr><tr><td>

journal\_input

</td><td>

Journal Input

</td><td>

Yes

</td><td id="JournalField">

Journal input field that accepts text entries but doesn't display previous entries.

</td></tr><tr><td>

journal\_list

</td><td>

Journal List

</td><td>

No

</td><td>

Journal list field that displays the contents of journal fields. You must specify the journal fields as the dependent fields. If a journal list field depends on more than one journal field, the entries are displayed chronologically.

</td></tr><tr><td>

json

</td><td>

JSON

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

json\_translations

</td><td>

JSON Translations

</td><td>

No

</td><td>

 

</td></tr><tr><td>

language

</td><td>

Language

</td><td>

No

</td><td>

 

</td></tr><tr><td>

long

</td><td>

Long

</td><td>

Yes

</td><td>

Long field that stores large whole numbers, which can be useful for high-value data. This field handles values that exceed standard integer limits, which is essential in high-volume contexts like serial numbers or counting operations. This field ensures that numeric data is stored accurately without overflow.

</td></tr><tr><td>

longint

</td><td>

Longint

</td><td>

Yes

</td><td>

Longint field that stores large whole numbers, which can be useful for high-value data. This field handles values that exceed standard integer limits, which is essential in high-volume contexts like serial numbers or counting operations. This field ensures that numeric data is stored accurately without overflow.

</td></tr><tr><td>

mask\_code

</td><td>

Mask code

</td><td>

No

</td><td>

 

</td></tr><tr><td>

metric\_absolute

</td><td>

Metric Absolute

</td><td>

No

</td><td>

 

</td></tr><tr><td>

metric\_counter

</td><td>

Metric Counter

</td><td>

No

</td><td>

 

</td></tr><tr><td>

metric\_derive

</td><td>

Metric Derive

</td><td>

No

</td><td>

 

</td></tr><tr><td>

metric\_gauge

</td><td>

Metric Gauge

</td><td>

No

</td><td>

 

</td></tr><tr><td>

mid\_config

</td><td>

Mid Config

</td><td>

No

</td><td>

 

</td></tr><tr><td>

month\_of\_year

</td><td>

Month of Year

</td><td>

No

</td><td>

 

</td></tr><tr><td>

multi\_small

</td><td>

Multi Small

</td><td>

Yes

</td><td>

Text area field that stores shorter texts like short descriptions and notes.

</td></tr><tr><td>

multi\_two\_lines

</td><td>

Two Line Text Area

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

name\_values

</td><td>

Name-Value Pairs

</td><td>

No

</td><td id="NameValue">

Name-value pairs field that maps text values. Each mapping is one-to-one, but a single **Name-Value Pairs** field can contain multiple mappings. Each mapping must use a unique name, and the name can’t be empty.For example, you can use a **Name-Value Pairs** field to hold header information for a web service request. In this example, the name of each mapping is the header such as `Content-Type` and the value is the header value, such as `Application/json`. For information on scripting **Name-Value Pairs** fields, see [Name-value pairs field type](../../field-administration/reference/name-value-pair-scripting.md).

</td></tr><tr><td>

nds\_icon

</td><td>

NDS Icon

</td><td>

No

</td><td>

 

</td></tr><tr><td>

nl\_task\_int1

</td><td>

NL Task Int1

</td><td>

No

</td><td>

 

</td></tr><tr><td>

order\_index

</td><td>

Order Index

</td><td>

Yes

</td><td>

Order index field that defines the display order of records in lists or hierarchies. By assigning a numeric value to each record, it enables admins to control the visual sequence, which is helpful for logically organizing tasks, categories, or items. This field type helps improve user experience by making the interface intuitive and orderly.

</td></tr><tr><td>

password

</td><td>

Password \(1 Way Encrypted\)

</td><td>

Yes

</td><td id="Password1Way">

Text field that stores passwords with one-way encryption. One-way encryption stores the password as a secure hash value that can't be decrypted.

</td></tr><tr><td>

password2

</td><td>

Password \(2 Way Encrypted\)

</td><td>

Yes

</td><td id="Password2">

Text field that stores passwords with two-way encryption. Two-way encryption stores the password as a secure encrypted value that can be decrypted programmatically within the instance. You can use Password 2 encryption with form variables. To encrypt text fields on forms, see [Password2 encryption with KMF](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/platform-encryption/password-2way-encrypted-fields.md). The length for password2 field values must be at least 255 characters.

</td></tr><tr><td>

percent\_complete

</td><td>

Percent Complete

</td><td>

Yes

</td><td>

Decimal field that renders a percent complete bar in lists. You can convert any existing **Decimal** field to a **Percent Complete** field.

</td></tr><tr><td>

ph\_number

</td><td>

Phone Number

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

phone\_number

</td><td>

Phone Number \(Unused\)

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

phone\_number\_e164

</td><td>

Phone number \(E164\)

</td><td>

Yes

</td><td id="PhoneNumber">

String field that provides E164-compliant formatting and validation for telephone numbers.

</td></tr><tr><td>

price

</td><td>

Price

</td><td>

Yes

</td><td id="entry_PriceField">

Currency field that enables control over conversions and display. See [Price fields](../../currency/concept/price-fields.md) for more information.

</td></tr><tr><td>

properties

</td><td>

Properties

</td><td>

No

</td><td>

 

</td></tr><tr><td>

radio

</td><td>

Radio

</td><td>

Yes

</td><td>

Radio field that displays mutually exclusive options as radio buttons, letting users select only one choice. It’s suitable for simple, definitive decisions, like priority level or yes/no responses. This field type helps improve usability by presenting clear options for single-selection inputs. As of the Zurich release, radio buttons can be displayed both horizontally and vertically in the form view.

</td></tr><tr><td>

records

</td><td>

Records

</td><td>

No

</td><td>

 

</td></tr><tr><td>

reference

</td><td>

Reference

</td><td>

Yes

</td><td id="ReferenceField">

Query field that displays records from another table, which is crucial for relational data structures.

</td></tr><tr><td>

reference\_name

</td><td>

Reference Name

</td><td>

No

</td><td>

 

</td></tr><tr><td>

related\_tags

</td><td>

Related Tags

</td><td>

Yes

</td><td>

Field used to categorize and organize records by assigning tags. In the record page, The tags are editable using the option on the form and the same tags get reflected on the related\_tags field type in a read only mode.

</td></tr><tr><td>

reminder\_field\_name

</td><td>

Reminder Field Name

</td><td>

No

</td><td>

 

</td></tr><tr><td>

repeat\_count

</td><td>

Repeat Count

</td><td>

No

</td><td>

 

</td></tr><tr><td>

repeat\_type

</td><td>

Repeat Type

</td><td>

No

</td><td>

 

</td></tr><tr><td>

replication\_payload

</td><td>

Replication Payload

</td><td>

No

</td><td>

 

</td></tr><tr><td>

schedule\_date\_time

</td><td>

Schedule Date/Time

</td><td>

No

</td><td>

 

</td></tr><tr><td>

schedule\_interval\_count

</td><td>

Schedule Interval Count

</td><td>

No

</td><td>

 

</td></tr><tr><td>

script

</td><td>

Script

</td><td>

Yes

</td><td>

Text field that accepts JavaScript code input and provides controls, such as syntax checking and formatting. It also provides a list of fields and server APIs. You must specify a dependent field that references the table name for the list of fields.

</td></tr><tr><td>

script\_client

</td><td>

Script Client

</td><td>

No

</td><td>

 

</td></tr><tr><td>

script\_plain

</td><td>

Script \(Plain\)

</td><td>

Yes

</td><td>

Text field that accepts JavaScript code input and provides controls, such as syntax checking and formatting.

</td></tr><tr><td>

script\_server

</td><td>

Script Server

</td><td>

No

</td><td>

 

</td></tr><tr><td>

short\_field\_name

</td><td>

Short Field Name

</td><td>

No

</td><td>

 

</td></tr><tr><td>

short\_table\_name

</td><td>

Short Table Name

</td><td>

Yes

</td><td>

Text field that stores a compact version of a table name, often used for efficiency in system configurations, URLs, or logs. It helps map the full table names to shorter identifiers, mainly for internal system use rather than direct user interaction.

</td></tr><tr><td>

simple\_name\_values

</td><td>

Name-Value Pairs

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

slushbucket

</td><td>

Slushbucket

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

snapshot\_template\_value

</td><td>

Snapshot Template Value

</td><td>

No

</td><td>

 

</td></tr><tr><td>

source\_id

</td><td>

Source ID

</td><td>

No

</td><td>

 

</td></tr><tr><td>

source\_name

</td><td>

Source Name

</td><td>

No

</td><td>

 

</td></tr><tr><td>

source\_table

</td><td>

Source Table

</td><td>

No

</td><td>

 

</td></tr><tr><td>

string

</td><td>

String

</td><td>

Yes

</td><td id="StringField">

String field that holds a string of characters. Strings of up to 255 characters appear in a single-line text box. Anything 256 characters or over appears as a multi-line text box.**Note:** The database may translate the value that you provide in the **Max length** field to the closest matching database field type. For example, a max string length of 80 maps to the nearest database field type of VARCHAR\(100\).

For Oracle instances, users aren't able to increase the max length of a string field to a value greater than 4000 through the application UI. Changes greater than 4000 require the CLOB data type in Oracle. If you require a field to be larger than 4000 characters, log an incident to request the change.

</td></tr><tr><td>

string\_boolean

</td><td>

String Boolean

</td><td>

No

</td><td>

 

</td></tr><tr><td>

string\_full\_utf8

</td><td>

String \(Full UTF-8\)

</td><td>

Yes

</td><td id="entry_StringUTF8Field">

String field that contains UTF-8 character encoding. This field type is restricted to the same maximum length that can be defined within the application UI as the String data type. Emojis are supported in the String \(Full UTF-8\) field type.

</td></tr><tr><td>

structure

</td><td>

Structure

</td><td>

No

</td><td>

 

</td></tr><tr><td>

sys\_class\_name

</td><td>

System Class Name

</td><td>

Yes

</td><td>

System field that holds the table name.

</td></tr><tr><td>

sys\_class\_path

</td><td>

System Class Path

</td><td>

No

</td><td>

 

</td></tr><tr><td>

sysevent\_name

</td><td>

System Event Name

</td><td>

No

</td><td>

 

</td></tr><tr><td>

sysrule\_field\_name

</td><td>

System Rule Field Name

</td><td>

No

</td><td>

 

</td></tr><tr><td>

table\_name

</td><td>

Table Name

</td><td>

Yes

</td><td id="entry_TableName">

String field that lets you select a table. If you use the **Field Name** field type, add this field type and make the **Field Name** field dependent on the **Table Name** field.If you're in a scoped application, you can view only the tables of that scope.

</td></tr><tr><td>

template\_value

</td><td>

Template Value

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

time

</td><td>

Time

</td><td>

No

</td><td id="entry_TimeField">

Time field that stores a time in the database as a **Date/Time** field, but only the time part of this field is used.**Note:** This field stores the date as 1970-01-01, which doesn't fall within the dates for Daylight Savings Time \(DST\). As a result, the time isn't adjusted automatically for DST. If a custom feature uses time as a start time, the feature must adjust for DST, if necessary.

</td></tr><tr><td>

timer

</td><td>

Timer

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

translated

</td><td>

Translated

</td><td>

No

</td><td>

 

</td></tr><tr><td>

translated\_field

</td><td>

Translated Field

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

translated\_html

</td><td>

Translated HTML

</td><td>

Yes

</td><td id="TranslatedHTML">

HTML text field that displays translations based on the user's language.

</td></tr><tr><td>

translated\_text

</td><td>

Translated Text

</td><td>

Yes

</td><td id="entry_TranslatedTextField">

Text field that displays translations based on the user's language.

</td></tr><tr><td>

tree\_code

</td><td>

Tree Code

</td><td>

No

</td><td>

 

</td></tr><tr><td>

tree\_path

</td><td>

Tree Path

</td><td>

No

</td><td>

 

</td></tr><tr><td>

url

</td><td>

URL

</td><td>

Yes

</td><td id="entry_URLField">

String field that is a selectable URL field when locked. When configuring, there’s an option to allow/disallow links with or without HTTPS.**Note:** In the mobile UI, this field appears as a multi-line text field. The field saves as a single line with the line breaks removed.

</td></tr><tr><td>

user\_image

</td><td>

Image

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

user\_input

</td><td>

User Input

</td><td>

Yes

</td><td>

User input field that captures input provided by users, typically in the context of workflows, surveys, or other interactive processes. This field enables users to enter text, select options, or provide other types of input that can then be processed or stored for further use.The data collected through **User Input** fields is often used to guide decision-making in workflows or to gather information for reporting and analysis. It's a flexible field type that can be customized to fit various use cases where user interaction is required.

</td></tr><tr><td>

user\_roles

</td><td>

User Roles

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

variable\_conditions

</td><td>

Variable Conditions

</td><td>

No

</td><td>

 

</td></tr><tr><td>

variable\_template\_value

</td><td>

Variable Template Value

</td><td>

No

</td><td>

 

</td></tr><tr><td>

variables

</td><td>

Variables

</td><td>

No

</td><td>

 

</td></tr><tr><td>

version

</td><td>

Version

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

video

</td><td>

Video

</td><td>

No

</td><td>

Video field for uploading and embedding video.

</td></tr><tr><td>

week\_of\_month

</td><td>

Week of Month

</td><td>

No

</td><td>

 

</td></tr><tr><td>

wide\_text

</td><td>

Wide Text

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

wiki\_text

</td><td>

Wiki

</td><td>

Yes

</td><td>

String field with a built-in wiki text editor that accepts a simplified version of standard wiki text formatting.

</td></tr><tr><td>

wms\_job

</td><td>

WMS Job

</td><td>

No

</td><td>

 

</td></tr><tr><td>

workflow

</td><td>

Workflow

</td><td>

Yes

</td><td>

List field that displays a stage in a workflow.

</td></tr><tr><td>

workflow\_conditions

</td><td>

Workflow Conditions

</td><td>

No

</td><td>

 

</td></tr><tr><td>

xml

</td><td>

XML

</td><td>

Yes

</td><td>

 

</td></tr></tbody>
</table>