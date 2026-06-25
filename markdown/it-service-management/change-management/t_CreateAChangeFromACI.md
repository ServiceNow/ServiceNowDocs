---
title: Create a change request from a configuration item \(CI\)
description: Create a change request from a list of configuration items \(CIs\), or add selected CIs from a list to a change record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/t\_CreateAChangeFromACI.html
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a change request, Use, Change Management, IT Service Management]
---

# Create a change request from a configuration item \(CI\)

Create a change request from a list of configuration items \(CIs\), or add selected CIs from a list to a change record.

## Before you begin

Role required: itil, admin, or sn\_change\_write

## Procedure

1.  Navigate to **All** &gt; **Configuration** and select a CIs class.

    For example, select **Servers** or **Service**.

    The list of CIs for the selected CI class displays.

2.  Select one or more CIs from the list.

3.  Select one of the following options from the Actions list.

<table id="choicetable_b3q_mzg_mw"><tbody><tr><td id="d326983e89">

**Add to existing Change Request**

</td><td>

Select this option to associate the CIs with an existing change request.

</td></tr><tr><td id="d326983e98">

**Add to new Change Request**

</td><td>

Select this option to associate the CIs with a new change request.

</td></tr></tbody>
</table>    \[Omitted image "Create-Change-from-CIs.png"\] Alt text: List action options that you can choose from.

    **Note:** CIs with a **Business Service** CI class are added to the **Impacted Services/CIs** related list on the change request. The remaining CIs are added to the **Affected CIs** related list.

    Depending on your selection, either an existing change requested is updated with the selected CIs or a new change request record is created with the selected CIs.

4.  Continue to create or modify the change record as required.


**Parent Topic:**[Create a change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/t_CreateAChange.md)

**Related topics**  


[Create a standard change request from the catalog]()

[Copy a change request]()

[Create a change task]()

[Unauthorized change request]()

