---
title: Exploring Antivirus Scanning
description: Use Antivirus Scanning to help protect your instance against virus infections that can be introduced by file attachments to your system records, such as incidents, problems, and stories.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Antivirus Scanning]
---

# Exploring Antivirus Scanning

Use Antivirus Scanning to help protect your instance against virus infections that can be introduced by file attachments to your system records, such as incidents, problems, and stories.

Antivirus Scanning scans file attachments stored in your attachment \[sys\_attachment\] table to help protect users from uploading and downloading infected files. All the document types supported by the Platform are scanned by Antivirus Scanning.

If Antivirus Scanning is enabled, all file attachments in the Attachments table \[sys\_attachment.do\] are scanned by default.

The Antivirus Protection plugin \(com.glide.snap\) is activated and enabled by default on your instance. As an administrator, you can deactivate and reactivate the Antivirus Scanning feature across your instance at the switch of a toggle, set configuration options, and review antivirus activity on the instance.

**Note:**

-   Antivirus Scanning is also available for customers in the Government Community Cloud \(GCC\) and commercial environment.

    GCC Users must set the \(com.glide.snap.fed\_enable\_scan\) property to `true` to start using the feature.

    Commercial users must set **com.glide.snap.enable\_scan** to `true`.

-   HTTP and HTTPS communication protocols are supported.
-   Edge-encrypted files are excluded from this scan.
-   Antivirus definitions are updated everyday.
-   Any file above 100-MB file size isn’t scanned.

## Email scanning

Inbound emails are scanned for viruses by the system [email filters](https://www.servicenow.com/docs/access?context=c_EmailFilters&version=australia&pubname=australia-platform-administration&ft:locale=en-US), not by Antivirus Scanning.

## File Attachment field in a table

The addition of a **File Attachment** field in a table generates zz\_yy tables. These tables are dynamic and virtual. They are automatically generated when the column type **file\_attachment** is added to parent tables.

Consider adding a user photo to the Users table and incorporating it into the form view. When a photo is uploaded to a record, it automatically uploads the attachment to the sys\_attachment table. The sys\_attachment table maps the photo to the zz\_yyUsers table.

By default only attachments attached to zz\_yylive\_profile tables are scanned. To scan other tables that have column type **file\_attachment** create the system property **com.glide.snap.scan.zz\_yytables** and insert the table name.

**Example**

The "zz\_yyincident" and "zz\_yycase" tables are dynamic tables created when the column is added to the parent tables: Incident and Case, then the property value should be **zz\_yyincident,zz\_yycase**.

After this property is set, attachments for the zz\_yyincident and zz\_yycase tables are scanned.

## Scanning scenarios

Review these upload and download scenarios to understand how the system identifies potential security threats from files attached to your records.

-   **Scenario 1 - Upload a file**
    1.  The user unknowingly uploads an infected file to a record.
    2.  The system scans the file and moves it to quarantine.
    3.  The file appears in the Attachments window, where it’s marked as unavailable.
    4.  The user selects the file and this error message appears: `The file Infected_testing.txt did not pass the security scan. Please remove the file from record INC0000059 and try again.`
    5.  The system sends an email notification to the user and the antivirus administrator.
    6.  The user closes the Attachments window and is returned to the record. The infected file is displays in the header as unavailable. Example, `infected_testing123.txtZ [unavailable]`.
-   **Scenario 2 - Download a file**
    1.  The user opens a record to download a file that is attached to it.
    2.  Unaware that the file is infected, the user selects it for download.
    3.  The system scans the file, moves it to quarantine, and displays a message similar to `The file infected_testing123.txt did not pass security scan and cannot be downloaded.`
    4.  The user closes the message and the screen refreshes showing that the file is unavailable.
    5.  The system sends an email notification to the user and the antivirus administrator.
-   **Scenario 3 - Download a ZIP file**
    1.  A user opens a record and downloads a ZIP file that is attached to it.
    2.  The system scans the ZIP files individually.
    3.  One file doesn’t pass the security scan and is marked as unavailable. The remaining files are zipped and downloaded successfully.
    4.  The user opens the ZIP file and sees an “error.txt” file in addition to the successfully downloaded file. This file contains an error message specifying which file didn’t pass scanning and was therefore not included in the ZIP.
    5.  The user opens the record again, and sees that the unavailable file has been moved into the **Potential security risks** section in the Attachments window and can’t be downloaded.

