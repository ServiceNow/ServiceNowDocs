---
title: Retry Handler Framework
description: Framework that retries a failed HTTP request when the API rate limits are exceeded and the 429 Too Many Requests status code is returned. The retry-after time HTTP header is used to retry the request again after that specified retry-after time. Also reuse this short description in the release notes.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Integration Hub solutions, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Retry Handler Framework

Framework that retries a failed HTTP request when the API rate limits are exceeded and the 429 Too Many Requests status code is returned. The retry-after time HTTP header is used to retry the request again after that specified retry-after time.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Spoke requirements

**Note:** The Retry Handler Framework app is available only as a part of [Microsoft Exchange Online Spoke](ms-exch-online-spoke.md) or [Journey Accelerator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/journey-accelerator/journey-accelerator.md) app.

-   Install Journey Accelerator app
-   Microsoft Exchange Online spoke

## Spoke flows

The Retry Handler Framework provides sample flows to demonstrate automating the Journey Accelerator tasks. To customize a sample flow, copy it to a new application scope. Available sample flows include:

<table id="table_lrp_h43_wqb"><thead><tr><th>

Flow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Renew Subscriptions

</td><td>

Retrieves all the subscription records and renews the subscriptions that are about to expire.**Note:** Subscriptions that have Being Deleted as status, will not be considered for renewal.

</td></tr><tr><td>

Clean up Queue Records

</td><td>

Removes the records from Request Retry Queue based on state, execution status, and last updated time.

</td></tr><tr><td>

Scheduled Job

</td><td>

Processes records from the Request Retry Queue table.

</td></tr></tbody>
</table>## Spoke subflows

The Retry Handler Framework provides sample subflows to demonstrate automating Journey Accelerator tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

<table id="table_nrp_h43_wqb"><thead><tr><th>

Subflow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Calendar Synchronization

</td><td>

Retrieves the events from Exchange Online Calendar Events Transformed Data table and updates the events in Microsoft Exchange Online Events table. Checks if a valid subscription exists. Creates a subscription if the subscription does not exist.**Note:** You must update the required details in the Exchange Online Calendar Events Transformed Data table before synchronizing events data.

</td></tr><tr><td>

Create or Update Subscription Record

</td><td>

Checks if a subscription with the specified details exists in Microsoft Exchange Online. If the subscription exists, then the subscription record is updated. Otherwise, a subscription is created in Microsoft Exchange Online and an associated record is created.

</td></tr><tr><td>

Delete Calendar Scheduling Event

</td><td>

Deletes the specified event in Microsoft Exchange Online and the associated record from events tables, attachments, records from event attendees and event to subscription m2m tables.

</td></tr><tr><td>

Event Lifecycle Management

</td><td>

Retrieves the event details and updates the record details of the event, attendees, and event to subscription m2m tables.

</td></tr><tr><td>

Look up and Update Attachments to Event Record

</td><td>

Retrieves the specified event's attachments from Microsoft Exchange Online and updates the retrieved details to the specified event's record.

</td></tr><tr><td>

Look up and Update Calendar Scheduling Change

</td><td>

Retrieves the event details from Microsoft Exchange Online and updates the details to the specified event's record. If a subscription already does not exist, this subflow creates a subscription and links it with the event record. If an event does not exist in Microsoft Exchange Online, all the related local records are deleted.

</td></tr><tr><td>

Look up Calendar Details

</td><td>

Retrieves the calendar details.**Note:** This subflow cannot be reused as it is a part of the Event Lifecycle Management subflow.

</td></tr><tr><td>

Look up Event Details

</td><td>

Retrieves the event details.**Note:** This subflow cannot be reused as it is a part of the Update Calendar Scheduling Event subflow.

</td></tr><tr><td>

Recreate Removed Subscription

</td><td>

Recreates a removed webhook subscription using the details from the associated subscription record.

</td></tr><tr><td>

Renew Subscription

</td><td>

Renews a webhook subscription if a renewal is required based on the specified inputs.

</td></tr><tr><td>

Subscription Lifecycle Management

</td><td>

Demonstrates the process of subscription management for webhook subscriptions. This subflow creates an event and checks if a webhook subscription exists. If a webhook subscription does not exist, the subflow creates a webhook subscription, event, attendees, event to subscription m2m table records.

</td></tr><tr><td>

Sync up Events

</td><td>

Syncs the calendar view with the Exchange Online Calendar Events Transformed Data table. Use this subflow to manage missed life-cycle notifications for subscriptions.**Note:** You must update the Exchange Online Calendar Events Transformed Data table with the required information before syncing events data.

</td></tr><tr><td>

Update Calendar Scheduling Event

</td><td>

Updates the properties of an event object in Microsoft Exchange Online and the associated records in the events table.

</td></tr></tbody>
</table>**Note:** Look up and Update Attachments to Event Record, Look up Calendar Details, Look up Event Details, Renew Subscription subflows are hidden from subflow picker.

