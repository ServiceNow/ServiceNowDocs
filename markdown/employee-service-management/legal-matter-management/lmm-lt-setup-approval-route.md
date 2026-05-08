---
title: Add approval route details
description: Add approval route details in Legal Matter Management to enable matter creation in Legal Tracker.
locale: en-US
release: australia
product: Legal Matter Management
classification: legal-matter-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure data to enable matter creation in Legal Tracker, Configure Legal Matter Management with outside counsel, Configure, Legal Matter Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Add approval route details

Add approval route details in Legal Matter Management to enable matter creation in Legal Tracker.

## Before you begin

Ensure you have installed and activated Legal Tracker spoke. For more information, see Legal Tracker.

Role required: sn\_lg\_matter.matter\_config, sn\_lg\_matter.matter\_fulfiller

## About this task

To create a matter in Legal Tracker, the information related to the approval route should be present in both Legal Tracker and Legal Matter Management.

As there is no scheduled job to pull the approval route details, you must manually add it in Legal Matter Management.

## Procedure

1.  Collect the approval route details from Legal Tracker.

2.  In the navigation filter, enter: `sn_lg_matter_legal_tracker_invoice_approval_route.list`

3.  Select **New**.

4.  On the form, fill in the details as present in the Legal Tracker.

    |Field|Description|
    |-----|-----------|
    |Invoice Approval Route Name|Invoice Approval Route Name from the Legal Tracker.|
    |Active|Option to make the approval route active.|
    |Domain|Name of the outside counsel.|
    |Invoice Approval Route ID|Invoice Approval Route Name from the Legal Tracker.|

5.  Select **Submit** to save the record.


**Parent Topic:**[Configure data to enable matter creation in Legal Tracker](lmm-config-data-mtemplates.md)

