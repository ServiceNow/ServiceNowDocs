---
title: Detected AI service details
description: Break down a detected AI service's usage by device, user, department, event, and source.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/sh-ai-service-details.html
release: zurich
topic_type: concept
last_updated: "2026-08-24"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Investigate a detected AI service, Detecting shadow AI, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Detected AI service details

Break down a detected AI service's usage by device, user, department, event, and source.

## Key benefits

-   Identify which devices, people, or departments are driving a service's usage.
-   Determine whether a device is managed by your organization by checking whether it resolves to a known configuration item.
-   Distinguish a single heavy user from broad department-wide adoption.
-   Compare the file types sent to a service, not just how often it was used.

After reviewing the details, take action by the following the steps in [Triage a detected AI service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/sh-ai-respond-to-service.md).

## Required roles

The AI steward \[sn\_ai\_governance.ai\_steward\] role is required to view the **Details** tab on an AI service record.

## Accessing AI service details

View AI service details by navigating to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Inventory** &gt; **Shadow AI**, selecting an AI service, and then opening the **Details** tab.

## Details

Review a detected AI service's current status and more in the **Details** card.

-   Check the service's current review status in the **Status** field. See [Shadow AI status values](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/sh-ai-status-values.md).
-   Determine whether a block policy applies to the service, and how broadly in the **Policy status** field.
-   View what kind of work the service is built for and what data is likely flowing to it by checking the **AI category** field.
-   Determine which method or methods reported the service by viewing the **Detection methods** field. These determine which signals appear on the record. See [How Shadow AI detects unsanctioned AI use](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/sh-ai-how-detection-works.md).
-   See the date this service was initially discovered in the **First detected** field. Compare this against **Last activity** to tell a long-running pattern apart from something that appeared recently.
-   See the most recent date usage was detected in the **Last activity** field. A recent date on a service you already reviewed means the pattern is continuing.
-   View the total data sent to the service in the selected date range in the **Payload size** field. High volume relative to the event count suggests users are sending substantial content, such as documents or data extracts, rather than short prompts.
-   View the company who publishes the service in the **Provider** field. Recognize when a service traces back to a provider your organization already has an agreement with, which can change your response from an outright block to a redirect.
-   See exactly which underlying model was called by checking the **Model** field.

## Devices

Determine which machines reached the service, and the count of events sent in the **Devices** tab.

-   Select a device that resolves to a known configuration item to open it in a read-only side panel.
-   Distinguish a managed corporate machine from one your organization doesn't manage, since the same usage pattern carries more risk on a device outside your other controls.
-   Compare event counts across devices to see whether use is concentrated on one machine or spread across many.

## Users

Determine which people used the service, and how heavily in the **Users** tab.

-   See a complete list of users who accessed the service.
-   Determine relative usage by comparing event counts between users.
-   Select a user to open a side panel and see the user profile and other detected service they've used.

Activity that can't be matched to a known person, such as from a personal device or a shared machine, appears under a single **Unknown user** entry instead of being dropped. Fields like email, role, and department are left empty. This indicates a coverage gap rather than a usage pattern.

## Departments

Determine whether use is contained to one team or spread across the organization in the **Departments** tab.

-   Check whether a pattern is confined to one department.
-   Check a pattern spread across several departments, which is indicates users are solving a problem approved tools don't cover.
-   Compare user counts across departments to see where adoption is concentrated.

## Events

Determine when use of a service started, and whether it's growing in the **Events** tab.

-   Compare the start of usage against a known date, such as a project kickoff or a new hire's start date, to see whether it has an explanation.
-   Check whether event counts are increasing over time to judge whether a pattern is still growing.
-   Confirm a service is still active by checking whether events continue to appear in the selected date range.

**Note:** For a service detected by Armis, each device contributes at most one event per day, regardless of how many times that device used the service that day. Event counts for a service detected by ACC reflect each request.

## Sources

Determine how people are reaching a service in the **Sources** tab.

-   Check for an agent calling the service unattended, which represents a different risk than a person typing into a browser tab, even at the same event count.
-   Compare source types to see whether use is from a sanctioned channel, like a browser, or through a channel that's harder to monitor, like a command line tool.

## Attachments

Determine what kind of data exposure a service represents in the **Attachments** tab.

-   Check for spreadsheets or documents, which suggest whole files leaving your organization rather than typed questions.
-   Check for a spike in one file type, which is worth following into the prompts that carried them.
-   Compare attachment counts against event counts to see whether a service is used mostly for questions or mostly for file transfer.

**Parent Topic:**[Investigating a detected AI service in Shadow AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/sh-ai-investigating-detected-services.md)

