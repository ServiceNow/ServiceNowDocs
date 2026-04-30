---
title: Activate a system property to close a long-running legal request
description: As an admin, activate the sn\_lg\_ops.allow\_request\_closure\_with\_open\_matters system property to close legal requests even when they’re linked to long-running requests.
locale: en-US
release: xanadu
product: Legal Request Management
classification: legal-request-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up Legal Request Management, Legal Request Management, Legal Service Delivery, Employee Service Management]
---

# Activate a system property to close a long-running legal request

As an admin, activate the `sn_lg_ops.allow_request_closure_with_open_matters` system property to close legal requests even when they’re linked to long-running requests.

## Before you begin

Role required: sn\_lg\_ops.legal\_admin

## About this task

`sn_lg_ops.allow_request_closure_with_open_matters` is a configurable system property that is used to configure a legal request to close even though it is linked to long-running requests. The property has no dependency on any other feature. By default, the property is set to **False** and legal requests can’t be closed when they are open. To close legal requests even if the primary legal request is open, activate the property by changing it to **True**.

## Procedure

1.  In the filter navigator, enter `sys_properties.list`.

2.  In the **Name** column, search for the `sn_lg_ops.allow_request_closure_with_open_matters` property.

3.  Select the property.

4.  If you aren’t able to edit the property in the current application scope, select the word **here** in the message at the top of the page.

5.  Update the **Value** field to `true`.

6.  Select **Update**.


## Result

The `sn_lg_ops.allow_request_closure_with_open_matters` system property is activated and the related legal requests can be closed even if the primary legal request is open.

**Parent Topic:**[Setting up Legal Request Management](../concept/legal-ops-administration.md)

