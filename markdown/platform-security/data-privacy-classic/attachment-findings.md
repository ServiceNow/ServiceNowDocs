---
title: Attachment scan findings
description: You can review the findings of your attachment quarantine scans, and work with any quarantined or alerted attachments.
locale: en-US
release: australia
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 2
breadcrumb: [Real time protection, Data privacy, Data Privacy, Platform Privacy]
---

# Attachment scan findings

You can review the findings of your attachment quarantine scans, and work with any quarantined or alerted attachments.

## About this task

Role required: data\_privacy\_admin and admin

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Data privacy** &gt; **Real time protection** &gt; **Attachment findings**.

2.  Review the list of attachment quarantine findings. The following information is shown:

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Policy

</td><td>

The quarantine attachment policy used in the scan.Select the name of the policy to view it.

</td></tr><tr><td>

Attachment source table

</td><td>

The tables the scan applied to.Select the name of the table to view it.

</td></tr><tr><td>

Record ID

</td><td>

The record produced by the scan.Select the ID of the record to view it.

</td></tr><tr><td>

Attachment

</td><td>

The attachment flagged in the scan. Select the link to view it.Select the name of the attachment to view it.

</td></tr><tr><td>

Status**Note:** A background job exists that will perform a one-time rescan of any attachments in Pending or Available status. If this rescan fails, the file cannot be downloaded.

</td><td>

The status of the attachment found in the scan. Status options include:-   **Pending** - Either the file has not yet been scanned for sensitive data or the scan failed because the property `dp.pii.document.download.allowed` is set to `false`. The file is not available to download.
-   **Available** - The file has been scanned and no sensitive data was found. It is available to download.
-   **Available conditionally** - The file failed to scan for sensitive data and the property `dp.pii.document.download.allowed` is set to `true`. It is available for download.

**Note:** The default value of the property is `true`. If the property is not set, the default value applies.

This state allows users to download an attachment even if it has not yet been scanned, as long as the `dp.pii.document.download.allowed` is set to `true`. If this property is `false`, existing attachments in the **Available conditionally** state will not be available for download.

-   **Quarantined** - The file was scanned and sensitive data was discovered. The file is quarantined and not available to download \(until reviewed and approved by an Admin\).
**Note:** Even if a file has been quarantined, a user may still be able to select the file name as if it were available. However, the attachment will not download and they will see a message indicating that it contains sensitive data.

</td></tr><tr><td>

Data pattern

</td><td>

The confidential information patterns discovered in the scan.

</td></tr></tbody>
</table>
## What to do next

You can make quarantined attachments available. To do so, check the boxes of the individual attachments you want to release from quarantine, then select **Mark as available**. If the attachments can be released, a dialog will ask you to confirm. Select **Mark as available** once more to release the attachments to their original locations and allow them to be accessed.

