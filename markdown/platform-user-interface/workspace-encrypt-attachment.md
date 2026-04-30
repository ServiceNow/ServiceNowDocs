---
title: Encrypt an attachment in a record
description: Secure sensitive files by encrypting the files as they are attached to Core UI and Workspace records.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Communicating with requesters and agents using Compose, Responding to issues in an open record in Workspace, Use, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Encrypt an attachment in a record

Secure sensitive files by encrypting the files as they are attached to Core UI and Workspace records.

## Before you begin

Role required: agent

## About this task

Encrypted attachments enable you to do the following:

-   Choose which encryption context is to be used for file encryption when you have access to more than one context.
-   View which encryption context is used after the file is attached to a record.

For more information on encryption, see [Encryption](https://www.servicenow.com/docs/access?context=encryption&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## Procedure

1.  Log in as a user with at least one encryption context.

2.  Navigate to a form that needs an attachment added, such as the Incident or Problem form, and click the attachment icon to open the Attachments dialog box.

3.  Select the file to be attached.

    If you have more that one encryption context, you will see an option to select a context to use.

4.  Close the Attachments dialog box to upload the file attachment.

    Attached files are listed across the top of the form. A special icon identifies encrypted files. Pointing to the icon shows the name of the encryption context. Note that you can see only encrypted files for which you have the encryption context.


## Result

Only users with the same context used to encrypt the attachment can see the attachment in the Activity Formatter. Users without the appropriate context won't see the Activity Formatter entry associated with the encrypted attachment.

