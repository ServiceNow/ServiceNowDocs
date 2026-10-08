---
title: Google Cloud Storage object management AI agent
description: This AI agent manages objects in Google Cloud Storage buckets. It uploads, downloads, copies, rewrites, updates, and deletes objects, changes storage classes, and lists or retrieves object details.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/inth-google-cloud-google-cloud-storage-object-management-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 2
breadcrumb: [Google Cloud Storage Spoke AI agents, Integration Hub AI agents, Integration Hub, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Google Cloud Storage object management AI agent

This AI agent manages objects in Google Cloud Storage buckets. It uploads, downloads, copies, rewrites, updates, and deletes objects, changes storage classes, and lists or retrieves object details.

## Workflow

The agent helps the user manage the objects stored in Google Cloud Storage buckets.

1.  Ask the user what they want to do and collect the details the action needs, such as the bucket and object names.
2.  List the objects in a bucket or get the details of a specific object.
3.  Upload an object to a bucket or download an object to ServiceNow.
4.  Copy or rewrite an object to a new location or with new properties.
5.  Update an object's metadata or storage class.
6.  Delete an object from a bucket.
7.  Report the outcome to the user, including details of any error.

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

Copy Object

Delete An Object

Download Object To ServiceNow

Get Object Details

List All Objects

ReWrite An Object

Update Object Details In A Bucket

Update Object Storage Class

Upload An Object


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
</table>**Parent Topic:**[Google Cloud Storage Spoke AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/inth-google-cloud-ai-agents-overview.md)

**Related topics**  


[Google Cloud Storage Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/gcloudstorage-spoke.md)

[Integration Hub spokes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/spokes-list.md)

