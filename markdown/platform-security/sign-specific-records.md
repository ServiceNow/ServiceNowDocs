---
title: Sign specific records or attachments
description: Create a security job to sign specific records or attachments rather than all records or attachments on a table.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Code Signing, Code Signing, Platform Security]
---

# Sign specific records or attachments

Create a security job to sign specific records or attachments rather than all records or attachments on a table.

Beginning in the Vancouver release, security administrators can use security jobs to sign specific records on a table rather than all records on a table. Sign specific records to avoid accidentally signing any unreviewed code.

These jobs include an attached log file, which is generated at the end of the signing job. This log file contains information about signed records and the signature configuration used.

## Signing process

![Signing process diagram](../image/codesign-process-flow.png)

This diagram shows an example of how you can use the signing process. In this example, a script, labeled `Script B` exists only on the protected instance, and must be imported to a trusted instance to be signed. `Script A` exists on both instances already, doesn’t need to be signed. It has either already been reviewed and signed, or hasn't been reviewed yet and shouldn't be signed.

1.  Import the record to your trusted environment.
2.  In the trusted instance, create a signing job to sign the record. This process is detailed in [Create a job to sign specific records or attachments on a trusted instance](../task/sign-files-nonprod.md).
3.  Import the signed signing job to your protected instance using an update set.
4.  In the protected instance, run the imported signing job.

-   **[Create a job to sign specific records or attachments on a trusted instance](../task/sign-files-nonprod.md)**  
Sign a specific record, or group of records you define on a trusted instance.

**Parent Topic:**[Using Code Signing](using-code-signing.md)

