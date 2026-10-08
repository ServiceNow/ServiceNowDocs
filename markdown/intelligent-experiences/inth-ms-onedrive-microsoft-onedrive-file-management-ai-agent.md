---
title: Microsoft OneDrive file management AI agent
description: This AI agent manages Microsoft OneDrive files.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/inth-ms-onedrive-microsoft-onedrive-file-management-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 2
breadcrumb: [Microsoft OneDrive Spoke AI agents, Integration Hub AI agents, Integration Hub, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Microsoft OneDrive file management AI agent

This AI agent manages Microsoft OneDrive files.

## Workflow

The agent looks up items, copies files and folders, uploads and replaces files, handles large uploads, checks files in and out, manages versions, and copies files between Microsoft OneDrive and ServiceNow attachments.

1.  Ask the user what they want to do and collect the details the action needs, such as the file or folder.
2.  Look up items, or look up a file or folder by ID or path.
3.  Copy a file or folder within Microsoft OneDrive.
4.  Copy a ServiceNow attachment to Microsoft OneDrive, or copy a Microsoft OneDrive file or file version to an attachment.
5.  Upload and replace a file, or upload a large file using an upload session.
6.  Check the status of an upload session or delete it.
7.  Check a file out or check it back in.
8.  Restore a file version or delete one.
9.  Report the outcome to the user, including details of any error.

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

Check In File

Check Out File

Check Upload Session Status

Copy Attachment to OneDrive

Copy Attachment to OneDrive Using Path

Copy File or Folder Item

Copy OneDrive File Version to Attachment

Copy OneDrive File to Attachment Using File Path

Create Upload Session

Delete Upload Session

Delete Version of a File

Look up File or Folder Item Info by ID

Look up File or Folder Item Info by Path

Look up Items

Restore File Version

Upload Large File

Upload and Replace File


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
</table>**Parent Topic:**[Microsoft OneDrive Spoke AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/inth-ms-onedrive-ai-agents-overview.md)

**Related topics**  


[Microsoft OneDrive Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/onedrive-spoke.md)

[Integration Hub spokes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/spokes-list.md)

