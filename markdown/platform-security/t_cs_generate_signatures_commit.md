---
title: Generate signatures when committing to source control
description: Turn on signature generation during commit and commit application files from ServiceNow Studio. Eligible records are signed automatically and pushed to the remote repository with their signatures.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/t\_cs\_generate\_signatures\_commit.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Code Signing, source control, commit, generate signatures, ServiceNow Studio]
breadcrumb: [Signature generation during source control commit, Using Code Signing, Code Signing, Platform Security]
---

# Generate signatures when committing to source control

Turn on signature generation during commit and commit application files from ServiceNow Studio. Eligible records are signed automatically and pushed to the remote repository with their signatures.

## Before you begin

Before you begin:

-   Install the Code Signing Enterprise plugin. For more information, see [Configuring Code Signing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/config-code-signing.md)
-   Complete the Circle of Trust guided setup on the trusted instance, including uploading your signing certificate.
-   Perform this task on a trusted instance. Signatures can't be generated on a protected instance.
-   Link the application to source control in ServiceNow Studio. For more information, see 

Role required: codesigning\_admin \(to turn on the property only\)

## About this task

Turn on signature generation during commit so that a trusted instance signs eligible records as part of the source control commit. The signatures are added to the same update set as their source records and pushed to the remote repository together.

## Procedure

1.  In the navigation filter, enter `sys_properties.list` and press Enter.

2.  Open the **sn\_cse.com.snc.csf.generate\_signature\_commit** property.

    This property turns signature generation during commit on or off. It ships with a value of `false`.

3.  Set the value to `true` and save the property.

4.  Open your application in ServiceNow Studio.

5.  Create or update the records to commit.

6.  Select **Source Control** &gt; **Commit changes**.

    The Commit changes dialog box lists the created or updated files for the application, grouped by update set.

7.  Select the files to commit, and then select **Continue**.

    The instance generates a signature for each eligible selected record.

8.  Review the source records and their signatures on the confirmation screen.

9.  Enter a commit comment.

10. Select **Commit files**.


## Result

The instance pushes the source records and their signatures to the remote repository together. Each committed record has a corresponding signature record in the repository.

If a signature can't be generated for a selected record, for example because of a network issue, the confirmation screen doesn't open. You remain on the file selection screen and an error message identifies the record. Select **Continue** to retry signature generation for the failed record.

**Parent Topic:**[Signature generation during source control commit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown)

**Related topics**  


[bundle-cadev.servicenow-studio-landing]

