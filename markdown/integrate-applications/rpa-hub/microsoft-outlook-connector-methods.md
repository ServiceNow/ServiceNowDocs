---
title: Microsoft Outlook connector methods
description: The Microsoft Outlook connector methods automate various actions on the Microsoft Outlook. In an automation flow, the methods are connected with other methods and components. To use the methods, you must first expose them.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 10
breadcrumb: [Microsoft Outlook, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Microsoft Outlook connector methods

The Microsoft Outlook connector methods automate various actions on the Microsoft Outlook. In an automation flow, the methods are connected with other methods and components. To use the methods, you must first expose them.

The Microsoft Outlook connector enables the automation of routine tasks within the Microsoft Outlook application, integrating these functions into broader automated workflows.

You can automate processes such as sending or replying to emails without manual intervention. This connector provides various methods to facilitate the automation of actions within Microsoft Outlook. These methods can be seamlessly combined with other methods or components within an automation framework, enabling more complex and efficient workflow designs.

## AddFolder

Adds a new folder within a specified hierarchy and, optionally, a sub folder to the Outlook account set.

<table id="table_k42_vfb_qtb"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

MainFolder

</td><td>

Name of the folder that the method adds to the Outlook account.This parameter specifies the main folder where the new folder is added.

</td><td>

Data in

</td><td>

String

</td></tr><tr><td>

SubFolderName

</td><td>

Name of the sub folder that the method adds under the main folder.This parameter specifies the name of the new folder to be created.

If you use this parameter, you must use the IsSubFolder parameter.

</td><td>

Data in

</td><td>

String

</td></tr><tr><td>

IsSubFolder

</td><td>

Option to indicate that the folder created in the SubFolderName parameter is a subfolder under the main folder.This parameter indicates whether the SubFolderName must be added as a subfolder within the main folder. Defaults to False, meaning SubFolderName is added directly under the main folder.

</td><td>

Data in

</td><td>

Boolean

</td></tr></tbody>
</table>## Close

Closes the Microsoft Outlook explorer by specifying the profile name.

This method can be used as a cleanup activity after all automation tasks are completed.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|ProfileName|This parameter specifies the Outlook profile name that you want to close.|Data in|String|

## DeleteFolder

Deletes the specified folder and all subfolders under it.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|FolderName|Name of the folder that the method deletes.|Data in|String|

## DeleteMail

Deletes one or more emails. Deletes an email based on its unique entry ID.

**Tip:** Use the GetMails method to provide the emails the DeleteMail method will delete.

<table id="table_nvy_c2j_qtb"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

MailId

</td><td>

Takes the email from which the method deletes the emails.This parameter specifies the unique entry ID of the email that needs to be deleted.

</td><td>

Data in

</td><td>

String

</td></tr></tbody>
</table>## ForwardMail

Forwards an email based on its unique entry ID to a specified email address \(EmailID\).

<table id="table_rvb_4q4_hcc"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

MailId

</td><td>

This parameter specifies the unique entry ID of the email that needs to be forwarded.

</td><td>

Data in

</td><td>

String

</td></tr><tr><td>

EmailID

</td><td>

This parameter specifies the email address to which the email must be forwarded.

</td><td>

Data in

</td><td>

String

</td></tr><tr><td>

CC

</td><td>

This parameter specifies Email address to send a carbon copy \(CC\) of the forwarded email.

</td><td>

Data in

</td><td>

String

</td></tr><tr><td>

BCC

</td><td>

This parameter specifies Email address to send a blind carbon copy \(BCC\) of the forwarded email.

</td><td>

Data in

</td><td>

String

</td></tr><tr><td>

Subject

</td><td>

This parameter specifies the subject line of the forwarded email.

</td><td>

Data in

</td><td>

String

</td></tr><tr><td>

Return

</td><td>

This method returns a boolean value indicating whether the email was successfully forwarded. A return value of true signifies that the operation was successful.

</td><td>

Data out

</td><td>

Boolean

</td></tr></tbody>
</table>## GetAttachmentNames

Retrieves a list of attachment names associated with an email specified by its unique entry ID.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|MailId|This parameter specifies the unique entry ID of the email for which attachment names are to be retrieved.|Data in|String|

## GetExistingAccounts

Retrieves information about configured accounts such as a list of configured accounts and their count.

This is helpful when there are multiple accounts configured in the outlook.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|Accounts|This parameter is passed by reference and is expected to be a List \(Of String\). Upon calling this method, it is populated with the list of configured account names.|Data out|List1|
|Count|This parameter is passed by reference. Upon calling this method, this parameter is populated with the count of configured accounts.|Data out|Int32|

## GetFolderNames

Retrieves and returns a list of folder names from the active outlook account.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|Return|Returns the list of folder names from the active outlook account.|Data out|List1|

## GetMail

Retrieves all details of an email, specified by its unique entry ID \(MailId\).

To specify additional criteria for retrieving all details of an email, on the GetMail method bar, click the method settings icon \(![Method settings icon.](../image/component-settings-icon.png)\), select the required mail items such as CC, BCC, Subject, Body, Sender, To, AttachmentsCount, ReceivedTime, EntryId.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|MailId|This parameter specifies the unique entry ID of the email to retrieve details from.|Data in|String|

## GetMails

Retrieves a list of mail entry IDs from a specified folder within an email system.

The GetMails method retrieves a list of mail entry IDs from a specified folder within an email system.

<table id="table_nc2_zw4_hcc"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

FolderName

</td><td>

This parameter specifies the name of the folder from which to retrieve mail entry IDs.Default value is "Inbox".

</td><td>

Data in

</td><td>

String

</td></tr><tr><td>

Filter

</td><td>

This parameter specifies a filter condition to apply when retrieving mail entry IDs.

</td><td>

Data in

</td><td>

String

</td></tr><tr><td>

NoOfMails

</td><td>

This parameter specifies the maximum number of mail entry IDs to retrieve. Default value is 10.

</td><td>

Data in

</td><td>

Int32

</td></tr><tr><td>

UnreadOnly

</td><td>

This parameter indicates whether to retrieve only unread mails \(True\) or all mails \(False\). Default is True.

</td><td>

Data in

</td><td>

Boolean

</td></tr><tr><td>

AvoidMeetingItems

</td><td>

This parameter specifies whether to exclude meeting items from the retrieved mail entry IDs. Default is True.

</td><td>

Data in

</td><td>

Boolean

</td></tr><tr><td>

FetchingOrder

</td><td>

This parameter specifies the order in which mails are fetched. For example, FIFO, LIFO. Default is FIFO.

</td><td>

Data in

</td><td>

FetchingOrder

</td></tr><tr><td>

Return

</td><td>

This parameter returns a list of emails from the specified folder.

</td><td>

Data out

</td><td>

List1

</td></tr><tr><td>

Count

</td><td>

This parameter specifies total count of mail entry IDs retrieved.

</td><td>

Data out

</td><td>

Int32

</td></tr></tbody>
</table>## GetSenderName

Retrieves the sender's email address associated with an email specified by its unique entry ID.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|MailId|This parameter specifies the unique entry ID of the email for which the sender's email address is to be retrieved.|Data in|String|
|Return|This method returns a string value indicating sender name.|Data out|String|

## MarkAsRead

Marks an email as read based on its unique entry ID.

<table id="table_dmc_rrc_pcc"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

MailId

</td><td>

This parameter specifies the unique entry ID of the email for which the sender's email address is to be retrieved.

</td><td>

Data in

</td><td>

String

</td></tr><tr><td>

Return

</td><td>

This method returns a boolean value indicating whether the email was successfully marked as read.A return value of true signifies that the operation was successful.

</td><td>

Data out

</td><td>

Boolean

</td></tr></tbody>
</table>## MarkAsUnread

Marks an email as unread based on its unique entry ID.

<table id="table_cpr_csc_pcc"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

MailId

</td><td>

This parameter specifies the unique entry ID of the email that needs to be marked as unread.

</td><td>

Data in

</td><td>

String

</td></tr><tr><td>

Return

</td><td>

This method returns a boolean value indicating whether the email was successfully marked as unread. A return value of true signifies that the operation was successful.

</td><td>

Data out

</td><td>

Boolean

</td></tr></tbody>
</table>## MoveMail

Moves an email based on its unique entry ID from one folder to another folder within the email system.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|MailId|This parameter specifies the unique entry ID of the email that must be moved.|Data in|String|
|DestinationFolder|This parameter specifies the name or path of the destination folder where the email must be moved.|Data in|String|

## ReadMsgFile

Reads the contents of a .msg file from the file system.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|Filepath|This parameter specifies the path to the .msg file that must be read.|Data in|String|
|Body|This parameter is passed by reference \(ByRef\) and is populated with the body content of the .msg file after the method call.|Data out|String|

## Reply

Generates and sends a reply to an email specified by its unique entry ID.

<table id="table_e1f_q5c_pcc"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

IsHtmlBody

</td><td>

This parameter indicates whether the body content of the reply email is in HTML format. Default is False.

</td><td>

Data in

</td><td>

Boolean

</td></tr><tr><td>

Return

</td><td>

This method returns a boolean value indicating whether the reply was successfully sent. A return value of true signifies that the operation was successful.

</td><td>

Data out

</td><td>

Boolean

</td></tr></tbody>
</table>## SaveAllAttachments

Saves all attachments from an email specified by its unique entry ID into a specified folder path.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|MailId|This parameter specifies the unique entry ID of the email from which attachments must be saved.|Data in|String|
|FolderPath|This parameter specifies the path of the folder where attachments must be saved.|Data in|String|

## SaveAttachment

Saves specified attachment of a mail with given entry ID into a given file.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|MailId|This parameter specifies the unique entry ID of the email from which attachment must be saved.|Data in|String|
|AttachmentName|This parameter specifies the name of the attachment that must be saved.|Data in|String|
|Filepath|This parameter specifies the path of the file where attachment must be saved.|Data in|String|

## SaveMail

Saves an email specified by its unique entry ID \(MailId\) to a file at a specified file path.

<table id="table_hfc_xvc_pcc"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

MailId

</td><td>

This parameter specifies the unique entry ID of the email to be saved.

</td><td>

Data in

</td><td>

String

</td></tr><tr><td>

Filepath

</td><td>

This parameter specifies the path where the email must be saved as a file

</td><td>

Data in

</td><td>

String

</td></tr><tr><td>

SaveType

</td><td>

This parameter specifies the format in which the email must be saved. Default is MsgSaveType.olMSG, indicating Microsoft Outlook MSG format.

</td><td>

Data in

</td><td>

MsgSaveType

</td></tr></tbody>
</table>## SendMail

Sends an email to recipient. It offers various optional parameters to customize the email, including the ability to add images, set the sender's address, and specify CC and BCC recipients.

<table id="table_l34_2xc_pcc"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

ToEmailId

</td><td>

This parameter specifies email address of the recipient.

</td><td>

Data in

</td><td>

String

</td></tr><tr><td>

Image

</td><td>

This parameter specifies an optional image to include in the email.

</td><td>

Data in

</td><td>

Drawing.Bitmap

</td></tr><tr><td>

From

</td><td>

This parameter specifies the email address of the sender. If not specified, the default sender's address is used.

</td><td>

Data in

</td><td>

String

</td></tr><tr><td>

CC

</td><td>

This parameter specifies Email address to send a carbon copy \(CC\) to.

</td><td>

Data in

</td><td>

String

</td></tr><tr><td>

BCC

</td><td>

This parameter specifies email address to send a blind carbon copy \(BCC\) to.

</td><td>

Data in

</td><td>

String

</td></tr><tr><td>

Subject

</td><td>

This parameter specifies the subject line of the email.

</td><td>

Data in

</td><td>

String

</td></tr><tr><td>

Body

</td><td>

This parameter specifies the body content of the email.

</td><td>

Data in

</td><td>

String

</td></tr><tr><td>

Attachments

</td><td>

This parameter specifies file paths of the attachments to include in the email. Multiple files can be separated by semi colon.

</td><td>

Data in

</td><td>

String

</td></tr><tr><td>

IsHtmlBody

</td><td>

This parameter indicates whether the body of the email is in HTML format. Default is False.

</td><td>

Data in

</td><td>

Boolean

</td></tr><tr><td>

Return

</td><td>

This method returns a boolean value indicating whether the email was successfully sent. A return value of true signifies that the operation was successful.

</td><td>

Data out

</td><td>

Boolean

</td></tr></tbody>
</table>## SentAs

Sends an email on behalf of another email account.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|ToEmailId|This parameter specifies email address of the recipient.|Data in|String|
|SentOnBehalfEmailID|This parameter specifies email address on whose behalf the email will be sent.|Data in|String|
|Subject|This parameter specifies the subject line of the email.|Data in|String|
|Body|This parameter specifies the body content of the email.|Data in|String|
|Attachments|This parameter specifies file paths of the attachments to include in the email.|Data in|String|
|IsHtmlBody|This parameter indicates whether the body of the email is in HTML format. Default is False.|Data in|Boolean|

## SetAccount

Specifies the outlook account on which you want to perform operations for your automation tasks.

The SetAccount method must be used initially, before any other method of this connector, to specify or set the context or email account for subsequent methods to execute upon.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|AccountName|This parameter specifies the Outlook email account ID on which you want to perform operations.|Data in|String|

**Parent Topic:**[Microsoft Outlook](../concept/microsoft-outlook-connector.md)

