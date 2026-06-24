---
title: Sync chemical information with the 3E database
description: You can sync details of chemicals, such as hazard identification, chemical ingredients, and others, with the 3E database to ensure that current information is accessible.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/health-and-safety/hs-sync-chemical-data-with-3E.html
release: australia
product: Health and Safety
classification: health-and-safety
topic_type: task
last_updated: "2025-12-01"
reading_time_minutes: 1
breadcrumb: [3E Protect, 3E, Integration with third-party services, Health and Safety, Employee Service Management]
---

# Sync chemical information with the 3E database

You can sync details of chemicals, such as hazard identification, chemical ingredients, and others, with the 3E database to ensure that current information is accessible.

## Before you begin

The 3E credentials must be configured in the application registry for the sync with the service provider to process successfully. For more information, see [Configure the application registry for the 3E service provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/health-and-safety/hs-configure-application-registry-3E.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  In the primary navigation, select **Environmental Management** \(\[Omitted image "icon-hs-envt-mgmt.png"\] Alt text: environmental management icon\) icon.

3.  In the **Chemical** list, select **All** and the select a chemical record.

4.  On any of the related lists, select the \(\[Omitted image "agent-workspace-more-ui-actions-icon.jpg"\] Alt text: more actions icon\) icon.

5.  Select **Sync with service provider**.

6.  In the dialogue box, select the **Confirm** button.


## Result

The **Service provider requests** related list of the chemical record, displays the request submitted to sync the record with 3E with the status as **Work in progress**.

## What to do next

-   Depending on the request, the data from 3E can be instantly available or it can take up to 30 days to obtain. When the data is available, the service provider request will be marked as **Complete** by 3E. Once the request is completed by 3E service provider, the fields in the record are automatically updated.
-   If there are any error or status message from 3E system \(for example, for synchronization issues\), the error message is added to the activity stream of the service provider request. If 3E service provider cannot locate the chemical data or metadata, the 3E staff manually intervenes and send messages that appear in the activity stream.

**Parent Topic:**[3E Protect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/health-and-safety/hs-3e-protect.md)

