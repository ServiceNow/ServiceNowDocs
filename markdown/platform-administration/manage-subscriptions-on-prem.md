---
title: Manage subscriptions in an on-premise installation
description: Download licensing and usage definition data to view and manage subscriptions for your on-premise installation.After a request for on-premise entitlement data is processed, you can find and download the data through Now Support.Import entitlement data for your on-premise instance to manage subscriptions for the instance.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Subscription Management, Get started, Administer the ServiceNow AI Platform]
---

# Manage subscriptions in an on-premise installation

Download licensing and usage definition data to view and manage subscriptions for your on-premise installation.

## Before you begin

Role required: customer\_admin or partner\_admin

## About this task

You can view and manage entitlements for an on-premise installation by uploading entitlement information.An automated workflow is available through the Now Support portal to request the necessary licensing and usage definition data.

Licensing and usage definition data can only be requested for production, sub-production, and demo instances. Development instances aren't supported.

**Note:** Account-level entitlements aren’t available in an on-premise installation. To calculate entitlements across all your instances, you must log in to each individual instance to gather entitlement data and then aggregate the totals.

## Procedure

1.  Log in to Now Support.

2.  Navigate to **Automation Store** &gt; **Service Catalog** &gt; **Instance Management**.

3.  Find and select **Request On-Prem Licensing Information**.

4.  Select your company.

    If there are no child companies, the parent company is selected by default and the field is read-only.

5.  Select an instance whose data you want to request.

    Only on-premise instances for the Yokohama family release and above can be selected.

6.  Select **Submit**.


## Result

You receive an email when the request has been processed.

## What to do next

After the request has been processed, view on-premise licensing requests to download the data.

**Parent Topic:**[Configuring Subscription Management](../concept/configuring-subscription-management-v2.md)

## View on-premise licensing information requests

After a request for on-premise entitlement data is processed, you can find and download the data through Now Support.

### Before you begin

Role required: customer\_admin or partner\_admin

### Procedure

1.  Log in to Now Support.

2.  Navigate to **Automation Store** &gt; **Service Catalog** &gt; **My Licensing Requests**.

3.  From the completed licensing request, download the attached XML or JSON files.


### What to do next

Import the entitlement data to your on-premise instance.

## Import on-premise entitlement data

Import entitlement data for your on-premise instance to manage subscriptions for the instance.

### Before you begin

Role required: adminsn\_sub\_man.admin, or usage\_admin

### Procedure

1.  From the instance whose data you downloaded, navigate to **All** &gt; **Subscription Management** &gt; **Import Entitlement Data**.

2.  Upload the zip file as an attachment.

    If your instance doesn't enable zip files to be uploaded, attach the contents of the zip file instead.

3.  Select **Process**.


### Result

A few minutes after the state changes to "Processed," the data in the Subscription Management dashboard can be refreshed. If there are scheduled jobs running or queued, it might take longer for the Subscription Management dashboard to refresh.

