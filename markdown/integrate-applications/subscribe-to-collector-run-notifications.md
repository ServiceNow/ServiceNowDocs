---
title: Subscribe to metadata collector run notifications
description: Opt in to email notifications for metadata collector run completion and failure through Notification preferences.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/subscribe-to-collector-run-notifications.html
release: australia
topic_type: task
last_updated: "2026-09-25"
reading_time_minutes: 1
keywords: [metadata collector notifications, collector run notification, DCG Metadata Collector Run Completed, DCG Metadata Collector Run Failed, notification preferences]
breadcrumb: [Running metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Subscribe to metadata collector run notifications

Opt in to email notifications for metadata collector run completion and failure through Notification preferences.

## Before you begin

Role required: connection\_admin

## About this task

The platform sends an email when a metadata collector run completes or fails. You subscribe to these notifications through the standard Notification preferences UI. You can subscribe to run completion notifications, failure notifications, or both.

## Procedure

1.  Open Notification preferences.

    Select your profile icon, then select **Notification preferences**.

2.  Enable the **Allow Notifications** toggle at the top of the page.

    **Warning:** If **Allow Notifications** is off, no notifications are delivered regardless of individual subscription settings.

3.  Select the **System notifications** tab.

4.  Enable the **System notifications** toggle.

5.  In the search field, enter `metadata` to filter to the **Collector Run Notification** category.

    The **DCG Metadata Collector Run Completed** and **DCG Metadata Collector Run Failed** notifications appear. \[Omitted image "dc-mcollector-notification-prefs.png"\] Alt text: Enable notifications for metadata collectors

6.  Enable the toggle for each notification you want to receive.

    -   Enable **DCG Metadata Collector Run Completed** to receive an email when a collector run succeeds.
    -   Enable **DCG Metadata Collector Run Failed** to receive an email when a collector run fails.

## Result

You receive an email within one minute of a collector run completing or failing. The email includes the collector name, source name, start and end times, and — for failures — an error summary with a link to the run log.

## What to do next

To stop receiving notifications, return to Notification preferences and disable the relevant toggles.

**Parent Topic:**[Running metadata collectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/run-metadata-collectors-dc.md)

