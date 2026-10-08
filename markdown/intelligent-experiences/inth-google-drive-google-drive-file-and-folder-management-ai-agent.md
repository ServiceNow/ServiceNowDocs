---
title: Google Drive file and folder management AI agent
description: This AI agent manages Google Drive files and folders. It looks up files, folders, and revisions, creates folders, copies and deletes items, updates metadata, and copies files between Google Drive and ServiceNow attachments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/inth-google-drive-google-drive-file-and-folder-management-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 2
breadcrumb: [Google Drive Spoke AI agents, Integration Hub AI agents, Integration Hub, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Google Drive file and folder management AI agent

This AI agent manages Google Drive files and folders. It looks up files, folders, and revisions, creates folders, copies and deletes items, updates metadata, and copies files between Google Drive and ServiceNow attachments.

## Workflow

The agent helps the user manage Google Drive content and move files to and from ServiceNow.

1.  Ask the user what they want to do and collect the details the action needs, such as the file or folder.
2.  Look up files, folders, a specific file, or items by name.
3.  Look up a file's revisions, copy a revision as an attachment, or delete a revision.
4.  Create a folder or copy a file.
5.  Update a file or folder's metadata.
6.  Copy a ServiceNow attachment to Drive or update it there, or copy a Drive or Docs file to an attachment.
7.  Confirm the user's intent and delete a file or folder.
8.  Report the outcome to the user, including details of any error.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow third party to access this AI agent

</td><td>

When enabled, third-party AI agents can use this agent. This value is off \(false\) by default. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the External discoverable field.

</td></tr><tr><td>

Allow AI specialists to access this AI agent

</td><td>

When enabled, AI specialists can use this agent. This value is off \(false\) by default. When set to true, more configuration options for tools become available so that an AI specialist can map inputs and response templates to tool outputs. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the Specialist enabled field.

</td></tr><tr><td>

Manage long-term memory

</td><td>

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Flow Actions**

Copy Attachment to Drive

Copy Doc File to Attachment

Copy Drive File to Attachment

Copy File

Copy File Revision as Attachment

Create Folder

Delete File Revision

Delete File or Folder

Look up File

Look up File Revisions Stream

Look up Files Stream

Look up Files or Folders by Name

Look up Folders Stream

Update Attachment to Drive

Update File or Folder Metadata


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

snc\_internal

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

snc\_internal

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>**Parent Topic:**[Google Drive Spoke AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/inth-google-drive-ai-agents-overview.md)

**Related topics**  


[Google Drive Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/googledrive-spoke.md)

[Integration Hub spokes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/spokes-list.md)

