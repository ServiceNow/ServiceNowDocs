---
title: Configure the chemical request approval flow
description: Modify the chemical request approval flow using Flow designer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/health-and-safety/hs-modify-approval-flow-environmental-mgmt.html
release: zurich
product: Health and Safety
classification: health-and-safety
topic_type: task
last_updated: "2025-11-27"
reading_time_minutes: 1
breadcrumb: [Configure, Health and Safety Environmental Management, Health and Safety, Employee Service Management]
---

# Configure the chemical request approval flow

Modify the chemical request approval flow using Flow designer.

## Before you begin

The approval flows are built on Flow Designer. Before modifying, make sure that you're familiar with the basics of ServiceNow® Workflow Studio.

Role required: Flow designer

## About this task

Modifying the approval flow is an optional configuration step for a chemical request. The approval flow is ready to use but can be modified to meet your company’s requirements.

If you decide to modify the flow, deactivate the original flow and make a copy. Make any desired changes to the new flow, and then activate it. Modifying the copy makes it easier when you must upgrade your ServiceNow® instance.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow designer**.

2.  Select More actions \[Omitted image "agent-workspace-more-ui-actions-icon.jpg"\] Alt text: more actions iconicon, then select **Copy flow**.

3.  Enter a name for the new flow.

4.  In the **Application** field, select **Chemical request approval**.

5.  Select **Copy**.

6.  Make desired changes to the new flow.

7.  Select **Save** and then select **Activate**.


-   **[Configure the chemical request approver based on location](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/health-and-safety/hs-configure-approver-by-location.md)**  
Configure approvers according to the location name entered on the request form. Multiple approvers can be associated with a single location.

**Parent Topic:**[Setting up Health and Safety Environmental Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/health-and-safety/hs-setting-up-environmental-management.md)

