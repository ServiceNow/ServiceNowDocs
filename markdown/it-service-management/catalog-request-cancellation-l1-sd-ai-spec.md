---
title: Request cancellation workflow
description: When a requester replies that a catalog request is wrong or did not help, and the incident is reassigned, the L1 IT Service Desk AI Specialist closes each open requested item it created for that incident, to prevent unnecessary fulfillment work.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/catalog-request-cancellation-l1-sd-ai-spec.html
release: australia
topic_type: concept
last_updated: "2026-09-25"
reading_time_minutes: 2
keywords: [cancel, cancellation, request, negative comment, feedback]
breadcrumb: [Use, L1 IT Service Desk AI Specialist, IT Service Management]
---

# Request cancellation workflow

When a requester replies that a catalog request is wrong or did not help, and the incident is reassigned, the L1 IT Service Desk AI Specialist closes each open requested item it created for that incident, to prevent unnecessary fulfillment work.

## Automatic cancellation on a negative reply

Requesters sometimes realize after submission that a catalog request drafted or submitted by the L1 IT Service Desk AI Specialist is not what they actually need. If the requester replies that the request is wrong or did not help, and the incident is reassigned to a human agent, the L1 IT Service Desk AI Specialist closes each open requested item it created for that incident. Other reassignments do not cancel the request. This helps prevent unnecessary fulfillment effort and reduce duplicate work.

## How cancellation works

Cancellation happens in one case only: the requester replies negatively \(for example, "this didn't fix it"\) and the reply leads to the incident being reassigned. Other reassignments, such as low confidence, routing criteria, reply limit reached, a stuck run, or a cross-group reassignment, leave the request open. Requests that the requester submitted from a draft are not cancelled, because the requester created them. A language model decides whether a reply is negative. When cancellation happens, the L1 IT Service Desk AI Specialist does the following:

-   Closes any requested items the L1 IT Service Desk AI Specialist created for the incident that aren't already closed, setting them to Closed Incomplete. The parent request is not closed.
-   Adds a comment explaining why it was cancelled to each cancelled requested item and to the incident

## Monitoring cancellations

The performance dashboard tracks the cancellation rate: the percentage of requests submitted by the L1 IT Service Desk AI Specialist that are later cancelled by the requester. A high cancellation rate may indicate that:

-   The L1 IT Service Desk AI Specialist is matching incidents to the wrong catalog items
-   Catalog item descriptions or variables are unclear to requesters
-   The variable collection process is not capturing the requester's actual needs

When you identify patterns in cancellations, review your L1 IT Service Desk AI Specialist catalog matching configuration and consider updating catalog item details or variable wording to reduce future mismatches.

## Requester experience

A negative reply from the requester, for example indicating the request is wrong, can lead to the incident being reassigned. If that happens, any open requested item the L1 IT Service Desk AI Specialist created for that incident is closed as Closed Incomplete and the requester is notified. This gives requesters a simple, natural way to correct a mistake without having to navigate administrative workflows.

## Example: catalog request cancellation

The following example illustrates the state changes for an incident-linked catalog request when a requester adds a negative comment.

When the requester adds a comment such as "It did not resolve my issue" to the incident, the incident state changes from **On Hold** to **In Progress**. If that comment results in the incident being reassigned to a human agent, each open requested item the L1 IT Service Desk AI Specialist created for the incident is closed and its state changes to **Closed Incomplete**. The parent request is not closed.

\[Omitted image "l1-catalog\_negative-comment.png"\] Alt text: An incident with a customer comment stating the issue was not resolved, prompting a state change to In Progress.

\[Omitted image "l1-catalog\_closed-incomplete.png"\] Alt text: A catalog request status changed to Closed Incomplete after cancellation.

