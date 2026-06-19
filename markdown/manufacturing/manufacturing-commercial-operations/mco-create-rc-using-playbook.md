---
title: Create a repair claim using playbook
description: Create a repair claim for the products under warranty or recall using the playbook experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/manufacturing/manufacturing-commercial-operations/mco-create-rc-using-playbook.html
release: australia
product: Manufacturing Commercial Operations
classification: manufacturing-commercial-operations
topic_type: task
last_updated: "2026-05-18"
reading_time_minutes: 1
breadcrumb: [Repair claim, Agent management, Use, Manufacturing Commercial Operations]
---

# Create a repair claim using playbook

Create a repair claim for the products under warranty or recall using the playbook experience.

## Before you begin

Role required: Manufacturing operations admin

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** &gt; **List** &gt; **Create Repair Claim Case** &gt; **All** &gt; **New**.

    The guided Repair claim case playbook displays.

2.  **Claim details**

    1.  On the Enter claim details form, fill-in the [Claim details form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/manufacturing-commercial-operations/mco-claim-details-form.md) details.
    2.  Select **Continue**.
3.  **Claim jobs**

    1.  Select **Add claim jobs**.
    2.  Set **Type** as **Warranty** or **Recall**.
    3.  On the Repair claim jobs form, fill in the [Repair claim form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/manufacturing-commercial-operations/repair-claim-form.md) details.
    4.  Select **Save**.
    5.  Select **Submit**.
4.  **Claim review**

    The claim job is successfully submitted for review and approval.

5.  **Review &amp; approve**

    The claim analysis and claim jobs summary are generated. Multiple claims jobs summary can be viewed by selecting **Show more**.

    Select an action from the following table.

    |Action|Description|
    |------|-----------|
    |Approve all|Select **Approve all** from the list. All claims are approved. The **Next steps** details are provided.|
    |Reject all|Select **Reject all** from the list. All claims are rejected. The **suggested action** will be provided.|
    |Partially approve|Select **Partially approved**. Approve, reject, or delete individual jobs, or enter a lesser approved amount for any job. The **Suggested action** will be provided.|
    |Send back|Select **Send back**. The claim is returned to the dealer for additional information. The **Suggested action** will be provided.|

6.  Select **Submit**.


**Parent Topic:**[Repair claim](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/manufacturing-commercial-operations/mco-use-repair-claim.md)

