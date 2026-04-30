---
title: Multi File Upload utility
description: Use the Multi File Upload utility to upload more than one file at a time in a Virtual Agent conversation.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Virtual Agent Designer utilities, Virtual Agent Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Multi File Upload utility

Use the Multi File Upload utility to upload more than one file at a time in a Virtual Agent conversation.

## Multi File Upload utility properties

Specify the flow action properties for the node that you want to create.

**Note:** The Multi File Upload utility is supported in Microsoft Teams, Slack, and Virtual Agent API only.

Uploaded files are stored in the Attachments \[sys\_attachment\] table.

<table id="action-utility-properties-sheet-table"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

Name of the Multi File Upload node.

</td></tr><tr><td class="sub-head" colspan="2">

Input mapping

</td></tr><tr><td>

Prompt

</td><td>

Text string prompting the user to upload files.

</td></tr><tr><td>

Allow user to skip

</td><td>

Option to skip uploading files if a user has none.

</td></tr><tr><td>

Max file count

</td><td>

Maximum number of files that can be uploaded.

</td></tr><tr><td>

Max file size

</td><td>

Maximum size of individual files uploaded, measured in megabytes.

</td></tr><tr><td>

Try Again message

</td><td>

Message sent to a user if the file upload fails.

</td></tr><tr><td>

User confirmation message

</td><td>

Message sent to a user confirming that files uploaded.

</td></tr><tr><td>

Allow all file types

</td><td>

Option to allow uploading all file types.

</td></tr><tr><td class="sub-head" colspan="2">

Output mapping

</td></tr><tr><td>

Files

</td><td>

The message sent to the user that lists files uploaded. Select **Enable** to activate this output, and input a custom variable name to store the value under if desired.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced

</td></tr><tr><td class="sub-head" colspan="2">

Hide this node

</td></tr><tr><td>

Conditionally show this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for presenting this node in the conversation. The condition must evaluate to true.

</td></tr></tbody>
</table>## Example Multi File Upload utility

![Multi File Upload utility properties.](../images/flow-designer-multi-file-upload-properties.png)

**Parent Topic:**[Virtual Agent Designer utilities](va-utilities.md)

