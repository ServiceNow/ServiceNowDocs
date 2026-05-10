---
title: Configure Legal Tracker instance URL
description: Update the system properties to generate the URL specific to External Matter that is displayed in the Legal Tracker matter link field. By selecting the URL, the user can directly open the matter in the Legal Tracker application.
locale: en-US
release: australia
product: Legal Matter Management
classification: legal-matter-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Legal Matter Management with outside counsel, Configure, Legal Matter Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Configure Legal Tracker instance URL

Update the system properties to generate the URL specific to External Matter that is displayed in the Legal Tracker matter link field. By selecting the URL, the user can directly open the matter in the Legal Tracker application.

## Before you begin

Ensure you have installed and activated Legal Tracker spoke. For more information, see [Legal Tracker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/legal-tracker-spoke.md).

Role required: admin

## Procedure

1.  In the navigation filter, type `sys_properties.list`.

2.  On the System Properties page, in the Name search field, enter `sn_lg_matter.legal_tracker_host_url`.

3.  Select the system property.

4.  In the information message at the top of the page about the current application, select **here** to be able to edit the form.

5.  In the **Value** field, enter the instance URL for the Legal Tracker application.

6.  Select **Update**.


## Result

The system property update to add the new URL to directly open external matters for the Legal Tracker application that is to be integrated with Legal Matter Management.

**Parent Topic:**[Configure Legal Matter Management to engage with outside counsel using Legal Tracker](../concept/configurations-for-legal-tracker-integration.md)

