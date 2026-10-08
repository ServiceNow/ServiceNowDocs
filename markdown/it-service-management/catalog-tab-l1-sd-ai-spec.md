---
title: Catalog tab
description: See which catalog items the L1 IT Service Desk AI Specialist drafts requests from, how many of those requests get submitted, and where drafts are abandoned, cancelled, or reassigned to a human agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/catalog-tab-l1-sd-ai-spec.html
release: australia
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 3
keywords: [L1 Service Desk AI Specialist, performance analytics, catalog, catalog requests, catalog items]
breadcrumb: [View the performance, Use, L1 IT Service Desk AI Specialist, IT Service Management]
---

# Catalog tab

See which catalog items the L1 IT Service Desk AI Specialist drafts requests from, how many of those requests get submitted, and where drafts are abandoned, cancelled, or reassigned to a human agent.

## Track how the AI specialist uses catalog items

Track which catalog items the AI specialist matched in autonomous mode, how many requests it drafted and submitted, and where employees abandoned the drafts. Use this information to identify which items the AI specialist completes without a human in the loop and which ones it doesn't.

Every card, chart, and table on the tab responds to the date range and AI specialist that you select on the dashboard. If no data matches your selection, a section shows a message that no data is available.

## Catalog coverage

See how much incident volume the AI specialist covered through catalog items, and how many unique items it used.

-   Incidents with drafted catalog requests: Closed incidents in the selected period where the AI specialist drafted at least one catalog request, compared to all incidents closed in that period. An incident is counted one time, even if it has more than one draft, and whether or not the drafts were submitted. The card also shows a target value.
-   Catalog items used: Number of different catalog items the AI specialist drafted requests from in the selected period. Each item is counted one time, no matter how many times it was used.

## Catalog requests summary

See how many catalog requests the AI specialist drafted, and how many of those were submitted.

-   Requests drafted: Catalog requests that the AI specialist drafted. A draft holds the matched catalog item and the values that the AI specialist filled in. If all mandatory variables are filled, the AI specialist submits the draft. If any are missing, the draft waits for the employee to complete and submit it.
-   Requests submitted: Drafts that were submitted and became request records. The chart splits them by who submitted them: By AI specialist, when the AI specialist submitted the draft without the employee having to act, and By Requester, when the employee reviewed, completed, and submitted the draft.

## Catalog request completion outcomes

See where the AI specialist auto-filled and submitted requests, where it could not finish collecting variables, where employees backed out, and where the incident was reassigned.

-   Zero touch drafts: Drafted requests where the AI specialist filled every mandatory variable and submitted the request automatically, so no exchange with the employee was needed.
-   Drafts with incomplete variables: Drafts sent to the employee for completion because the AI specialist could not source one or more mandatory variables.
-   Abandoned in drafts: Requests that the AI specialist drafted but the employee never submitted, so no request record was created.
-   Cancelled after submit: Submitted requests that were later cancelled or set to Closed Incomplete. For more information about when requests are cancelled, see [Request cancellation workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/catalog-request-cancellation-l1-sd-ai-spec.md).
-   Reassigned to SDA: Incidents reassigned to a human service desk agent \(SDA\) because the employee didn't respond or the AI specialist failed repeatedly to submit the request.

## Catalog item list

Track all catalog items available to the AI specialist and how often it drafted a catalog request after retrieving each item. The table is paginated. Selecting a catalog item link opens that item's record in a new browser tab.

For each catalog item, the table shows the following columns:

-   Catalog item: Name of the catalog item.
-   Class: Class of the catalog item.
-   Drafted: Number of requests that the AI specialist drafted from the item.
-   Submitted: Number of those drafts that were submitted.
-   AI specialist submitted: Number of submitted requests that the AI specialist submitted.
-   Requester submitted: Number of submitted requests that the employee submitted.
-   Abandonment rate: Percentage of drafts for the item that the employee never submitted.
-   Cancellation rate: Percentage of submitted requests for the item that were later cancelled or set to Closed Incomplete.

