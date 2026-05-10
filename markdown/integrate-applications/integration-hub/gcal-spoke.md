---
title: Google Calendar Spoke
description: Use ServiceNow to create and update events and attendees in Google Calendar.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Google Calendar Spoke

Use ServiceNow to create and update events and attendees in Google Calendar.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Google Calendar spoke v2.6.1 is the latest version.

## Supported versions

API version v1.

## Spoke actions

The Google Calendar spoke provides actions to perform Google Calendar tasks when events occur in ServiceNow. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Attendee Management|Add Attendees To Event|Updates an event by adding to the list of attendees. Values you specify replace the existing values. Fields that you don’t specify in the request do not change.|
|Remove Attendees From Event|Updates an event by removing specified attendees. Values you specify replace the existing values. Fields that you don’t specify in the request do not change.|
|Event Management|Create Event|Creates an event on the specified calendar.|
|Update Event|Edit event information. Values you specify replace the existing values. Fields that you don’t specify in the request do not change.|
|Look up Event By ID|Retrieves details of the specified event.|
|Delete Event|Removes a specified event from a calendar.|
|Look up Events Stream|Retrieves events on a specified calendar based on start time, end time, or search terms.|
|Look up Events by Calendar ID|Retrieves events on the specified calendar.|
|Look up Free or Busy Schedules|Retrieves the free or busy information for the specified set of calendars.|
|Move Event|Moves the specified event to another calendar.|
|Access Control List Management|Create Access Control List|Creates an access control rule.|
|Delete Access Control List|Deletes the specified access control rule.|
|Look up Access Control List by Calendar ID|Retrieves details of the required access control rule.|
|Look up Access Control List Stream|Retrieves the rules in the access control list for the calendar.|
|Update Access Control List|Updates details of the required access control rule.|
|Calendar List Management|Add Calendar to Calendar List|Inserts an existing calendar into the user's calendar list.|
|Delete Calendar from Calendar List|Removes a calendar from the user's calendar list.|
|Look up Calendar from Calendar List by ID|Retrieves calendar from the user's calendar list.|
|Look up Calendars from Calendar List Stream|Retrieves calendars on the user's calendar list.|
|Update Calendar from Calendar List|Updates an existing calendar on the user's calendar list.|

## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-use-case-ai-agents.md) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/find-ai-agents.md) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-ai-agent.md) for more information about creating a clone.
-   See [Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-ai-agents.md) for information about AI agents.

Available AI agents include:

|AI agents|Description|
|---------|-----------|
|Google Calendar event manager AI agent|Manages event manager tasks \(that is, look up an event by an event ID, look up an events stream, look up busy slots by a calendar ID, move an event, create an event, look up events by a calendar ID, delete an event, update an event\) in Google Calendar.|
|Google Calendar list manager AI agent|Manages calendar list tasks \(that is, delete a calendar from a calendar list, look up a calendar from a calendar list by an ID, look up calendars from a calendar list stream\) in Google Calendar.|
|Google Calendar access control list manager AI agent|Manages access control list tasks \(that is, update an access control list, delete an access control list, look up an access control list stream, look up an access control list by a calendar ID\) in Google Calendar.|
|Google Calendar metadata manager AI agent|Retrieves time zones metadata \(that is, look up time zones metadata\) from Google Calendar.|

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/find-ai-agents.md).

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Spoke module

The Google Calendar spoke adds a Google Calendars module to your ServiceNow instance. The Google Calendars module displays the details of the calendar lists.

## Google Calendar Online account requirements

The Google Calendar spoke requires a custom app that you create in [Google G Suite](https://gsuite.google.com/).

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Google Calendar spoke](../task/setup-gcal.md#).

## MID Server requirements

These actions use REST calls that can run either on an instance or, optionally, through a MID Server. Use the connection record associated with the Google Calendar alias to configure where actions run and, if needed, specify MID Server selection attributes. For more information, see [MID server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-landing.md).

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

