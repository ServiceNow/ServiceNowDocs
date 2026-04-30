---
title: Google Meet Spoke
description: Set up a flow and complete various actions on Google Meet after integrating your ServiceNow instance with the Google Meet account. For example, you can set up a meeting space or end an active conference as part of the flow.Also reuse this short description in the release notes.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-09-02"
reading_time_minutes: 6
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Google Meet Spoke

Set up a flow and complete various actions on Google Meet after integrating your ServiceNow instance with the Google Meet account. For example, you can set up a meeting space or end an active conference as part of the flow.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Google Meet spoke v1.2.1 is the latest spoke version.

## Supported versions

This spoke was built for Google Meet API v2, but may be compatible with later versions.

## Spoke requirements

-   Google Meet API access
-   Google Meet Cloud console access

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Google Meet provides actions to automate Google Meet tasks when events occurs in your ServiceNow instance. Available actions include:

<table id="table_fqn_r14_ydc"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th><th>

Required Scopes \(at least one scope is required\)

</th></tr></thead><tbody><tr><td rowspan="2">

Conference Management

</td><td>

Look up Conference

</td><td>

Retrieve a details of conference record associated with a specific Google Meet space.

</td><td>

-   https://www.googleapis.com/auth/meetings.space.readonly
-   https://www.googleapis.com/auth/meetings.space.created

</td></tr><tr><td>

Look up Conferences Stream

</td><td>

Retrieves a list of conference records, which can be filtered optionally and limited by a specified page size.

</td><td>

-   https://www.googleapis.com/auth/meetings.space.readonly
-   https://www.googleapis.com/auth/meetings.space.created

</td></tr><tr><td rowspan="4">

Space Management

</td><td>

Create Meeting Space \(Conversational -ready\)

</td><td>

Creates a Google Meet space and shares the link for participants to join and collaborate.

</td><td>

-   https://www.googleapis.com/auth/meetings.space.readonly
-   https://www.googleapis.com/auth/meetings.space.created

</td></tr><tr><td>

End Active Conference

</td><td>

Ends the active Google Meet session, disconnecting all participants and concluding the meeting.

</td><td>

-   https://www.googleapis.com/auth/meetings.space.readonly
-   https://www.googleapis.com/auth/meetings.space.created

</td></tr><tr><td>

Look up Meeting Space

</td><td>

Retrieves conference record details, including the configuration and current conference status for a specific Google Meet space.

</td><td>

-   https://www.googleapis.com/auth/meetings.space.readonly
-   https://www.googleapis.com/auth/meetings.space.created

</td></tr><tr><td>

Update Meeting Space \(Conversational -ready\)

</td><td>

Updates the settings of an existing Google Meet space.

</td><td>

https://www.googleapis.com/auth/meetings.space.created

</td></tr><tr><td rowspan="4">

Participant Management

</td><td>

Look up Participant

</td><td>

Retrieves details of a participant in a Google Meet conference.

</td><td>

-   https://www.googleapis.com/auth/meetings.space.readonly
-   https://www.googleapis.com/auth/meetings.space.created

</td></tr><tr><td>

Look up Participant Session

</td><td>

Retrieves the details of a specific session, including session start and end times, in a Google Meet conference.

</td><td>

-   https://www.googleapis.com/auth/meetings.space.readonly
-   https://www.googleapis.com/auth/meetings.space.created

</td></tr><tr><td>

Look up Participants Stream

</td><td>

Retrieves a paginated list of participants in a specified Google Meet conference, with optional filtering.

</td><td>

-   https://www.googleapis.com/auth/meetings.space.readonly
-   https://www.googleapis.com/auth/meetings.space.created

</td></tr><tr><td>

Look up Participant Sessions Stream

</td><td>

Retrieves a paginated stream of sessions for a specific participant in a Google Meet conference.

</td><td>

-   https://www.googleapis.com/auth/meetings.space.readonly
-   https://www.googleapis.com/auth/meetings.space.created

</td></tr><tr><td rowspan="6">

Artifacts Management

</td><td>

Look up Recording

</td><td>

Retrieves the details of a Google Meet recording, including its state, timestamps, and Google Drive location.

</td><td>

-   https://www.googleapis.com/auth/meetings.space.readonly
-   https://www.googleapis.com/auth/meetings.space.created

</td></tr><tr><td>

Look up Recordings Stream

</td><td>

Retrieves a paginated list of recordings for a specific Google Meet conference, including recording status, timestamps, and Google Drive location.

</td><td>

-   https://www.googleapis.com/auth/meetings.space.readonly
-   https://www.googleapis.com/auth/meetings.space.created

</td></tr><tr><td>

Look up Transcript

</td><td>

Retrieves the details of a Google Meet transcript, including its state, timestamps, and document location in Google Docs.

</td><td>

-   https://www.googleapis.com/auth/meetings.space.readonly
-   https://www.googleapis.com/auth/meetings.space.created

</td></tr><tr><td>

Look up Transcript Entry

</td><td>

Retrieves a specific transcript entry from a Google Meet conference, including its content, speaker details, and timestamp.

</td><td>

-   https://www.googleapis.com/auth/meetings.space.readonly
-   https://www.googleapis.com/auth/meetings.space.created

</td></tr><tr><td>

Look up Transcripts Stream

</td><td>

Retrieves a paginated list of transcripts for a specific Google Meet conference, including transcript status, timestamps, and the document location in Google Docs.

</td><td>

-   https://www.googleapis.com/auth/meetings.space.readonly
-   https://www.googleapis.com/auth/meetings.space.created

</td></tr><tr><td>

Look up Transcript Entries Stream

</td><td>

Retrieves a list of transcript entries for a specific Google Meet conference, including details like participant, transcript text, language, and timestamps.

</td><td>

-   https://www.googleapis.com/auth/meetings.space.readonly
-   https://www.googleapis.com/auth/meetings.space.created

</td></tr></tbody>
</table>## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information about creating a clone.
-   See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for information about AI agents.

Available AI agents include:

|AI Agent|Description|
|--------|-----------|
|Google Meet artifacts management AI agent|Automates tasks such as retrieving recordings, transcripts, and other meeting-related data, making it easier to organize and utilize meeting resources effectively.|
|Google Meet participant management AI agent|Automates tasks such as looking up participant details, retrieving participant session streams, and accessing session-specific information.|
|Google Meet conference management AI agent|Automates tasks such as look up conference details, retrieve live conference streams, and manage meeting spaces and participants.|
|Google Meet space management AI agent|Automates tasks such as creating and updating meeting spaces, ending active conferences, and retrieving information about existing meeting spaces.|

## Available conversational actions

Install Now Assist for Conversational Spokes and start using the conversational ability of Integration Hub spokes. For more information, see [Now Assist in Conversational Spokes](../../integrationhub/concept/conv-spokes-na.md).

|Action|Usage|
|------|-----|
|Create Meeting Space|In the Ask Now Assist to... field, enter the phrase that asks Now Assist to perform the action and press **Enter**. For example, `Create a meeting space`.|
|Update Meeting Space|In the Ask Now Assist to... field, enter the phrase that asks Now Assist to perform the action and press **Enter**. For example, `Update a meeting space`.|

![Use conversational action on Now Assist.](../image/gmeet-spk-nowassist.png)

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the Google Meet spoke](../task/set-up-the-google-meet-spoke.md#).

