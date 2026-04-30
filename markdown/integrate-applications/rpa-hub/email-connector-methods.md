---
title: Email connector methods
description: The methods in the Email connector retrieve, send, and reply to email messages, and can download attachments. Use the SetConfig method first to set up the connection to your mail server.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Email connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Email connector methods

The methods in the Email connector retrieve, send, and reply to email messages, and can download attachments. Use the SetConfig method first to set up the connection to your mail server.

Use the SetConfig method to configure the mail server properties and access credentials. This method must precede all the other Email connector methods in the automation.

The GetMails method retrieves messages from the mail server and passes them to other methods as an object that contains one or more messages. The ReadMail, ReplyMail, and SaveAllAttachments methods operate on a single message at a time. When these methods receive an object that contains more than one message, the automation must use a For Each or For Loop method to iterate each message in the collection.

-   For information about how to use the For Each method, see [Use the For Each component](../task/use-loops-foreach.md).
-   For information about how to use the For Loop method, see [Use the For Loop component](../task/use-loops-forloop.md).

## SetConfig

Sets up the connection to the mail server so that the automation can work with messages.

**Note:** You must run this method before running any other methods in the Email connector.

For information about how to set the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Required?|Notes|
|---------|-----------|--------------|---------|-------------|---------|-----|
|Username|User name to log in to the mail server|Data In|String|\(none\)|Yes| |
|Password|Password to log in to the mail server|Data In|String|\(none\)|Yes| |
|UseDefaultCredentials|Sends the default credentials of the currently logged-in user to the SMTP server.|Data In|Boolean|False|No| |
|SmtpMailServer|Name of the SMTP server|Data In|String|smtp.gmail.com|No|Access to Gmail by using the Email connector is not currently supported. Make sure to change the default value.|
|ImapMailServer|Name of the IMAP server|Data In|String|imap.gmail.com|No|Access to Gmail by using the Email connector is not currently supported. Make sure to change the default value.|
|SSL|Use the Secure Socket Layer protocol|Data In|Boolean|True|No| |
|SmtpPort|SMTP port number|Data In|Integer|587|No| |
|ImapPort|IMAP port number|Data In|Integer|993|No| |

## GetMails

Returns messages from the mail server for use by other methods. You can set the method to retrieve either read \(seen\) or unread \(unseen\) messages and specify the folder that they're gathered.

For information about how to set the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Required?|Notes|
|---------|-----------|--------------|---------|-------------|---------|-----|
|FolderName|Name of the IMAP folder that the method fetches the collection \(for example, **Inbox**\)|Data in|String|Inbox|Yes|To specify a nested IMAP folder, enter the folder hierarchy by using backslashes \(for example, Project\\Meetings\)|
|Filter|Set to get only unread \(**Unseen**\) or read \(**Seen**\) messages|Data in|FilterMode|Unseen|Yes| |
|Return|Returns the mail collection as an object|Data out|Object|Object|Yes| |

## MarkAsRead

Marks messages from a specified folder as read.

For information about how to set the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Port type|Data type|Default value|Required?|Notes|
|---------|-----------|---------|---------|-------------|---------|-----|
|MailObject|The email object based on which the corresponding message is marked as read|Data in|Object|Object|Yes| |
|FolderName|Name of the IMAP folder that the email object is fetched|Data in|String|Inbox|Yes|To specify a nested IMAP folder, enter the folder hierarchy by using backslashes \(for example, Project\\Meetings\)|

## MarkAsUnread

Marks messages from a specified folder as unread.

For information about how to set the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Port type|Data type|Default value|Required?|Notes|
|---------|-----------|---------|---------|-------------|---------|-----|
|MailObject|The email object based on the corresponding email that is marked as unread.|Data in|Object|Object|Yes| |
|FolderName|Name of the IMAP folder that the email object is fetched.|Data in|String|Inbox|Yes|To specify a nested IMAP folder, enter the folder hierarchy by using backslashes \(for example, Project\\Meetings\)|

## ReadMail

Reads a message and returns its details, including subject, body, sender \(from\), recipients in the CC field, recipients in the BCC field, and the number of attachments.

For information about how to set the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Required?|
|---------|-----------|--------------|---------|-------------|---------|
|MailObject|MailObject that gives the details of the last message received|Data in|Object|Object|Yes|
|Subject|Subject of the message|Data out|String|None|No|
|Body|Body of the message|Data out|String|None|No|
|Sender|Sender of the message|Data out|String|None|No|
|CC|Recipients marked in CC|Data out|String|None|No|
|BCC|Recipients marked in BCC|Data out|String|None|No|
|AttachmentsCount|Number of attachments in the message|Data out|Integer|None|No|

## ReplyMail

Automatically replies to a message. Use the parameters to set the body of the message and other details. You can include attachments.

For information about how to set the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

<table id="table_hm3_kmz_mtb"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data port type

</th><th>

Data type

</th><th>

Default value

</th><th>

Required?

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

MailObject

</td><td>

Message object containing the message details

</td><td>

Data in

</td><td>

Object

</td><td>

Object

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

ReplyToAll

</td><td>

Replies to all recipients in the To and CC fields of the message

</td><td>

Data in

</td><td>

Boolean

</td><td>

False

</td><td>

No

</td><td>

 

</td></tr><tr><td>

BCC

</td><td>

Replies to all recipients in the BCC field of the message

</td><td>

Data in

</td><td>

String

</td><td>

None

</td><td>

No

</td><td>

 

</td></tr><tr><td>

Body

</td><td>

Body of the reply message

</td><td>

Data in

</td><td>

String

</td><td>

None

</td><td>

No

</td><td>

 

</td></tr><tr><td>

IsHtmlBody

</td><td>

Option to indicate whether the reply body is in HTML format

</td><td>

Data in

</td><td>

Boolean

</td><td>

False

</td><td>

No

</td><td>

 

</td></tr><tr><td>

Attachments

</td><td>

Attachments to the reply message

</td><td>

Data in

</td><td>

String

</td><td>

None

</td><td>

No

</td><td>

To attach a file:1.  Paste the path to the file in the field.
2.  Remove the quotes enclosing the path.

 To include multiple attachments, separate the paths by commas.

</td></tr></tbody>
</table>## SaveAllAttachments

Saves all attachments from a message to the local drive.

For information about how to set the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Required?|
|---------|-----------|--------------|---------|-------------|---------|
|MailObject|Message that the method downloads the attachments from|Data In|Object|Object|Yes|
|FolderPath|Path of the directory to which the attachments are downloaded|Data In|String|None|Yes|

## SendMail

Sends a message. Use the parameters to set the body of the message and other details. You can include attachments.

**Note:** Use the SetConfig method to set the From address.

For information about how to set the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

<table id="table_qvr_frz_mtb"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data port type

</th><th>

Data type

</th><th>

Default value

</th><th>

Required?

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

ToAddress

</td><td>

Address to which to send the message

</td><td>

Data in

</td><td>

String

</td><td>

None

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

CC

</td><td>

Addresses to include in the CC field

</td><td>

Data in

</td><td>

String

</td><td>

None

</td><td>

No

</td><td>

 

</td></tr><tr><td>

BCC

</td><td>

Addresses to include in the BCC field

</td><td>

Data in

</td><td>

String

</td><td>

None

</td><td>

No

</td><td>

 

</td></tr><tr><td>

Subject

</td><td>

Message subject

</td><td>

Data in

</td><td>

String

</td><td>

None

</td><td>

No

</td><td>

 

</td></tr><tr><td>

Body

</td><td>

Message body

</td><td>

Data in

</td><td>

String

</td><td>

None

</td><td>

No

</td><td>

 

</td></tr><tr><td>

IsHtmlBody

</td><td>

Option to indicate whether the reply body is in HTML format

</td><td>

Data in

</td><td>

String

</td><td>

False

</td><td>

No

</td><td>

 

</td></tr><tr><td>

Attachments

</td><td>

Message attachments

</td><td>

Data in

</td><td>

String

</td><td>

None

</td><td>

No

</td><td>

To attach a file:1.  Paste the path to the file in the field.
2.  Remove the quotes enclosing the path.

 To include multiple attachments, separate the paths by commas.

</td></tr></tbody>
</table>**Parent Topic:**[Email connector](../concept/email-connectors.md)

