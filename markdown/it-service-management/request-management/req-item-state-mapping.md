---
title: Requested item state mapping
description: Map your requested items states to the universal request \(UR\) states to provide a better user experience during the requested item state transition and to track the progress of the request.
locale: en-US
release: zurich
product: Request Management
classification: request-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Request Management integration with Universal Request, Configure, Request Management, IT Service Management]
---

# Requested item state mapping

Map your requested items states to the universal request \(UR\) states to provide a better user experience during the requested item state transition and to track the progress of the request.

## Before you begin

Role required: admin

## About this task

Mapping the states of the requested item to the universal request state ensures that the status of request is also reflected on the state of universal request. As the request moves through different stages of the life cycle, the state of the universal request also gets updated to reflect the change.

For example, consider a universal request has a requested item as a primary ticket. When the state of the request changes from **Open** to **Work in Progress**, the universal request state changes from **New** to **In Progress**.

The following table lists the default state mapping of requested item state with UR states.

|Request item state|UR state|
|------------------|--------|
|Open|In Progress|
|Work in Progress|In Progress|
|Pending|In Progress|
|Closed Complete|Closed|
|Closed Skipped|Closed|
|Closed Incomplete|Closed|

If you change the state of the request to Close Incomplete, Closed Skipped, or Closed Complete without transferring the request back to the Universal Request queue or to another department, then one of the following action is performed:

-   If the **Needs resolution review** option is selected on the Universal Request, then the state of the request changes to Close Incomplete, Closed Skipped, or Closed Complete and the UR state reason is changed to Confirm response.
-   If the **Needs resolution review** option is not selected on the Universal Request, then the request is closed based on the state mapping.

**Note:** By default, the **Needs resolution review** on the Universal Request is set to false.

## Procedure

1.  Navigate to **All** &gt; **Universal Request** &gt; **Administration** &gt; **State Mapping**.

2.  Click **New**.

3.  On the form, fill in the fields.

    For more information, see [State mapping form](https://www.servicenow.com/docs/access?context=ur-state-mapping-form&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).


**Parent Topic:**[Request Management integration with Universal Request](../concept/request-mgmt-integration-ur.md)

