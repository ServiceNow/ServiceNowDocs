---
title: Attachment quarantine policies
description: Manage policies that automatically isolate suspicious attachments for security review and analysis.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/data-privacy-classic/attachment-quarantine-policies.html
release: australia
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: task
last_updated: "2026-07-09"
reading_time_minutes: 1
breadcrumb: [Real time protection, Data privacy, Data Privacy, Platform Privacy]
---

# Attachment quarantine policies

Manage policies that automatically isolate suspicious attachments for security review and analysis.

## Before you begin

Role required: data\_privacy\_admin and admin

## About this task

To create attachment quarantine policies, perform the following procedure:

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Data privacy** &gt; **Real time protection** &gt; **Attachment quarantine policies**.

2.  Select **Create new policy**.

3.  Enter a Policy Name for the policy.

4.  Toggle the **Active** button on if you want the policy to be enforced.

5.  Select **Add table**.

6.  Enter the tables you want the policy to apply to.

7.  Specify which data patterns you want to monitor for sensitive content in attachments.

    **Important:** Attachments matching the patterns you define here will be automatically quarantined. Users will receive an **Attachment Quarantined** message indicating the attachment was quarantined due to sensitive data detection, information on the scan result, and instructions for getting their attachment released.

8.  Select **Save** to set the table definitions as part of the policy.

    **Note:** You can define multiple tables for the policy to apply to.

9.  Select **Confirm** to save the policy.

    The new attachment quarantine policy is added on the main view.


## What to do next

The attachment quarantine policies you create show in the main view. You can edit or delete them by selecting the appropriate option from their Actions menu. You can also select either of the following buttons under each policy:

<table id="table_rpk_b5z_4lb"><thead><tr><th>

Button

</th><th>

Description

</th></tr></thead><tbody><tr><td>

View scan findings

</td><td>

View the findings specific to the quarantine scan policy, including links to flagged attachments and their status.**Note:** To work with the findings themselves, including the release of quarantined attachments, refer to [Attachment scan findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/data-privacy-classic/attachment-findings.md).

</td></tr><tr><td>

View policy details

</td><td>

View the configuration of the attachment quarantine policy. You can also toggle the **Active** button to turn the policy on or off.

</td></tr></tbody>
</table>**Important:** Currently, two known limitations exist for quarantined attachments:

-   Hyperlinks for quarantined attachments may still be clicked by users. In this case, the attachment will not download, and the user will a receive a message that the file contains sensitive data.
-   In the Workspace UI, users may still be able to click quarantined attachments in the Activity Stream of the record.

