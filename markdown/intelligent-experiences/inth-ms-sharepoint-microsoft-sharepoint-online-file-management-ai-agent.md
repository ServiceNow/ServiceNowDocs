---
title: Microsoft SharePoint Online file management AI agent
description: This AI agent manages Microsoft SharePoint Online files.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/inth-ms-sharepoint-microsoft-sharepoint-online-file-management-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 2
breadcrumb: [Microsoft SharePoint Online Spoke AI agents, Integration Hub AI agents, Integration Hub, AI agents library, AI assets, Enable AI experiences]
---

# Microsoft SharePoint Online file management AI agent

This AI agent manages Microsoft SharePoint Online files.

## Workflow

The agent copies, moves, creates, and deletes files, checks files in and out, shares and unshares files, retrieves details, permissions, and download links, and moves files between Microsoft SharePoint and ServiceNow.

1.  Ask the user what they want to do and collect the details the action needs, such as the site, file, and target.
2.  Look up a file's details or permissions, or get a download link.
3.  Create a text file, copy a file within Microsoft SharePoint, or copy a ServiceNow attachment to a Microsoft SharePoint folder.
4.  Move a file or delete it.
5.  Check a file out or check it back in.
6.  Share a file with a user or group, or unshare it.
7.  Attach a Microsoft SharePoint file to a ServiceNow record.
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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Flow Actions**

Attach Sharepoint File To A Record \(Simplified\)

Check-in File

Check-out File

Copy Attachment To Folder \(simplified\)

Copy File

Create A Text File

Delete File

Get File Download Link

Look Up File Details

Look up File Permissions

Move File

Share File With Group

Share File With User

Unshare File With Group

Unshare File With User


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

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>**Parent Topic:**[Microsoft SharePoint Online Spoke AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/inth-ms-sharepoint-ai-agents-overview.md)

**Related topics**  


[Microsoft SharePoint Online Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/sharepoint-online-spoke.md)

[Integration Hub spokes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/spokes-list.md)

