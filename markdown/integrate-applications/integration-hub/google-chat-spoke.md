---
title: Google Chat spoke
description: Manage communication within your Google Chat spaces directly from your ServiceNow instance using Google Chat spoke. Create flows in your ServiceNow instance to manage media, members, messages, and spaces in Google Chat.Also reuse this short description in the release notes.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-09-02"
reading_time_minutes: 5
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Google Chat spoke

Manage communication within your Google Chat spaces directly from your ServiceNow instance using Google Chat spoke. Create flows in your ServiceNow instance to manage media, members, messages, and spaces in Google Chat.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Google Chat spoke v1.2.0 is the latest spoke version.

## Supported versions

This spoke was built for Google Chat API v1, but may be compatible with later versions.

## Spoke requirements

-   Google Chat API access
-   Google Cloud console access

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Google Chat spoke provides actions to automate Google Chat tasks when events occurs in your ServiceNow instance. Available actions include:

<table id="table_ggq_q5r_dcc"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th><th>

Required Scopes \(at least one scope is required\)

</th></tr></thead><tbody><tr><td>

Media Management

</td><td>

Download Media

</td><td>

Downloads the uploaded media from Google Chat and attaches to the specified incident record. This action does not download the media uploaded to Google Drive.

</td><td>

-   https://www.googleapis.com/auth/chat.messages.readonly
-   https://www.googleapis.com/auth/chat.messages

</td></tr><tr><td rowspan="6">

Member Management

</td><td>

Add Current Application to Space

</td><td>

Adds the current calling application to the specified space.

</td><td>

-   https://www.googleapis.com/auth/chat.memberships.app
-   https://www.googleapis.com/auth/chat.memberships

</td></tr><tr><td>

Add Member to Space

</td><td>

Adds the specified member to the specified space.

</td><td>

https://www.googleapis.com/auth/chat.memberships

</td></tr><tr><td>

Look up Space Member

</td><td>

Retrieves details of the specified member for the specified space.

</td><td>

-   https://www.googleapis.com/auth/chat.memberships.readonly
-   https://www.googleapis.com/auth/chat.memberships

</td></tr><tr><td>

Look up Space Members Stream

</td><td>

Retrieves members of the specified space to which you have access.

</td><td>

-   https://www.googleapis.com/auth/chat.memberships.readonly
-   https://www.googleapis.com/auth/chat.memberships

</td></tr><tr><td>

Remove Current Application from Space

</td><td>

Removes the current calling application from the specified space.

</td><td>

-   https://www.googleapis.com/auth/chat.memberships.app
-   https://www.googleapis.com/auth/chat.memberships

</td></tr><tr><td>

Remove Member from Space

</td><td>

Removes the specified member from the specified space.

</td><td>

https://www.googleapis.com/auth/chat.memberships

</td></tr><tr><td rowspan="5">

Message Management

</td><td>

Create Message Thread

</td><td>

Creates a message thread in the specified space.

</td><td>

-   https://www.googleapis.com/auth/chat.messages.create
-   https://www.googleapis.com/auth/chat.messages

</td></tr><tr><td>

Delete Message

</td><td>

Deletes the specified message from the specified space. All the threaded replies of the message are also deleted.

</td><td>

https://www.googleapis.com/auth/chat.messages

</td></tr><tr><td>

Look up Message

</td><td>

Retrieves details about the specified message from the specified space.

</td><td>

-   https://www.googleapis.com/auth/chat.messages.readonly
-   https://www.googleapis.com/auth/chat.messages

</td></tr><tr><td>

Look up Messages Stream

</td><td>

Retrieves messages from the specified space in which you are a member.

</td><td>

-   https://www.googleapis.com/auth/chat.messages.readonly
-   https://www.googleapis.com/auth/chat.messages

</td></tr><tr><td>

Send Message to Thread

</td><td>

Creates a message in the specified thread of the specified space.

</td><td>

https://www.googleapis.com/auth/chat.messages

</td></tr><tr><td rowspan="5">

Space Management

</td><td>

Create Space

</td><td>

Creates a named space in Google Chat.

</td><td>

-   https://www.googleapis.com/auth/chat.spaces.create
-   https://www.googleapis.com/auth/chat.spaces

</td></tr><tr><td>

Delete Space

</td><td>

Deletes the specified Google Chat space.

</td><td>

https://www.googleapis.com/auth/chat.delete

</td></tr><tr><td>

Look up Space

</td><td>

Retrieves information about the specified Google Chat space.

</td><td>

-   https://www.googleapis.com/auth/chat.spaces.readonly
-   https://www.googleapis.com/auth/chat.spaces

</td></tr><tr><td>

Look up Spaces Stream

</td><td>

Retrieves a stream of Google Chat spaces in which you are a member.

</td><td>

-   https://www.googleapis.com/auth/chat.spaces.readonly
-   https://www.googleapis.com/auth/chat.spaces

</td></tr><tr><td>

Update Space

</td><td>

Updates the specified Google Chat space.

</td><td>

https://www.googleapis.com/auth/chat.spaces

</td></tr></tbody>
</table>## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information about creating a clone.
-   See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for information about AI agents.

Available AI agents include:

|AI Agent|Description|
|--------|-----------|
|Google Chat member management AI agent|Performs actions for managing members\(adds current application to a space, removes current application from a space, adds member to a space, removes member from a space, look up a space member\) in Google Chat.|
|Google Chat space management AI agent|Performs actions for managing\(looks up a space, deletes a space, creates a space, updates a space\) spaces in Google Chat.|
|Google Chat message management AI agent|Performs actions for managing\(deletes a message, creates a message thread, looks up a message, sends a message to thread\) messages in Google Chat.|

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

