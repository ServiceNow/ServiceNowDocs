---
title: Create a standard change request from the catalog
description: You can create a standard change request from the published standard change catalog templates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-service-management/change-management/t\_RaiseNewStdCngeFmTempl.html
release: yokohama
product: Change Management
classification: change-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a change request, Using Change Management, Change Management, IT Service Management]
---

# Create a standard change request from the catalog

You can create a standard change request from the published standard change catalog templates.

## Before you begin

Role required: itil, admin, or sn\_change\_write

## About this task

A standard change is a repeatable, pre-approved template in the standard change catalog. Change requests created from the standard change template do not require change approval.

To create a change request from a pre-approved template, follow the procedure below.

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Standard Change** &gt; **Standard Change Catalog**.

2.  Select one of the following options depending on the type of standard change you want to create.

<table id="choicetable_g1t_3h4_rw"><tbody><tr><td id="d280773e82">

**Network Standard Changes**

</td><td>

Create a standard change request for the network.

</td></tr><tr><td id="d280773e91">

**Server Standard Changes**

</td><td>

Create a standard change request for servers and attached storage.

</td></tr></tbody>
</table>3.  Select a template from the **Items** section.

    For example, **Add network switch to datacenter cabinet** in the **Network Standard Changes** &gt; **Items** section.

    When you select the catalog item, a standard change is created. The Change Request form is displayed with values from the standard change template.

4.  Complete the form with additional information you have.

    For example, add the **Configuration item** and the **Assignment group**.

5.  Open the form context menu and select **Save**.

6.  Complete any information in the related lists that apply to the standard change request.

7.  Select **Update**.


**Parent Topic:**[Create a change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-service-management/change-management/t_CreateAChange.md)

**Related topics**  


[Create a change request from a configuration item \(CI\)]()

[Copy a change request]()

[Create a change task]()

[Unauthorized change request]()

