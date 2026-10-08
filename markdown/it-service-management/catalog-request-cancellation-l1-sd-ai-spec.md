---
title: Request cancellation workflow
description: When an incident is escalated to a human agent, the L1 IT Service Desk AI Specialist automatically cancels any catalog request it created for that incident, to prevent unnecessary fulfillment work.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/catalog-request-cancellation-l1-sd-ai-spec.html
release: zurich
topic_type: concept
last_updated: "2026-09-25"
reading_time_minutes: 2
keywords: [cancel, cancellation, request, negative comment, feedback]
breadcrumb: [Use, L1 IT Service Desk AI Specialist, IT Service Management]
---

# Request cancellation workflow

When an incident is escalated to a human agent, the L1 IT Service Desk AI Specialist automatically cancels any catalog request it created for that incident, to prevent unnecessary fulfillment work.

## Automatic cancellation on escalation

Requesters sometimes realize after submission that a catalog request drafted or submitted by the L1 IT Service Desk AI Specialist is not what they actually need. If the incident is escalated to a human agent for any reason, the L1 IT Service Desk AI Specialist automatically cancels any catalog request it created for that incident. This helps prevent unnecessary fulfillment effort and reduce duplicate work.

## How cancellation works

Cancellation is triggered by escalation to a human agent, not directly by the comment itself. Any escalation, for any reason, cancels the L1 IT Service Desk AI Specialist's pending or submitted catalog request. When cancellation happens, the system:

-   Closes any request items the L1 IT Service Desk AI Specialist created for the incident that aren't already closed, setting them to Closed Incomplete
-   Posts a customer-facing note on each cancelled request explaining why it was cancelled

## Monitoring cancellations

The performance dashboard tracks the cancellation rate: the percentage of requests submitted by the L1 IT Service Desk AI Specialist that are later cancelled by the requester. A high cancellation rate may indicate that:

-   The L1 IT Service Desk AI Specialist is matching incidents to the wrong catalog items
-   Catalog item descriptions or variables are unclear to requesters
-   The variable collection process is not capturing the requester's actual needs

When you identify patterns in cancellations, review your L1 IT Service Desk AI Specialist catalog matching configuration and consider updating catalog item details or variable wording to reduce future mismatches.

## Requester experience

A requester's comment can trigger escalation: for example, if they indicate the request is wrong. If that happens, any catalog request the L1 IT Service Desk AI Specialist created for that incident is cancelled and the requester is notified. This gives requesters a simple, natural way to correct a mistake without having to navigate administrative workflows.

## Example: catalog request cancellation

The following example illustrates the state changes for an incident-linked catalog request when a requester adds a negative comment.

When the requester adds a comment such as "It did not resolve my issue" to the incident, the incident state changes from **On Hold** to **In Progress**. If that comment results in the incident being escalated to a human agent, the linked request is cancelled and its state changes to **Closed Incomplete**.

\[Omitted image "l1-catalog\_negative-comment.png"\] Alt text: An incident with a customer comment stating the issue was not resolved, prompting a state change to In Progress.

\[Omitted image "l1-catalog\_closed-incomplete.png"\] Alt text: A catalog request status changed to Closed Incomplete after cancellation.

