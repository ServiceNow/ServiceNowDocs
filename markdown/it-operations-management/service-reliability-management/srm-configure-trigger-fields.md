---
title: Configure fields for escalation triggers
description: Configure additional fields for on-call escalation triggers in Service Reliability Management \(SRM\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-reliability-management/srm-configure-trigger-fields.html
release: australia
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Service Reliability Management, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Configure fields for escalation triggers

Configure additional fields for on-call escalation triggers in Service Reliability Management \(SRM\).

## Before you begin

Role required: admin

## About this task

Configure additional fields that teams can use when setting up escalation triggers. By default, escalation triggers run only when the Assignment group field changes. Completing the following procedure makes other fields available, giving teams more flexibility and helping them respond to issues quickly.

## Procedure

1.  Navigate to **All** &gt; **On-Call Scheduling** &gt; **Administration** &gt; **Trigger Rule Table Config**.

2.  Select **em\_alert** or **incident** to configure additional trigger fields for alerts or incidents.

3.  In **Trigger condition fields**, add fields from the following table.

    **Note:** Selecting fields not listed in the table might cause performance issues.

<table id="choicetable_uxy_qdw_3hc"><thead><tr><th align="left" id="d99039e110">

Table

</th><th align="left" id="d99039e113">

Supported fields

</th></tr></thead><tbody><tr><td id="d99039e119">

**em\_alert**

</td><td>

-   Assigned to
-   Flap count
-   Flap last state
-   Initial event generation time
-   Last event generation time
-   Number of Work Notes
-   Overall Event Count


</td></tr><tr><td id="d99039e153">

**incident**

</td><td>

-   Assigned to
-   Category
-   Escalation
-   Impact
-   Reopen count
-   State
-   Urgency


</td></tr></tbody>
</table>4.  Select **Update** to save your changes.

    The selected fields now appear as options for teams configuring escalation triggers.


## What to do next

To set up an escalation trigger, see [Create an escalation trigger for an SRM team](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-reliability-management/sr-trigger-escalation-policy.md).

**Parent Topic:**[Configuring Service Reliability Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-reliability-management/configuring-service-reliability-management.md)

**Previous topic:**[Approve a change request for SRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-reliability-management/sr-approve-change-req.md)

**Next topic:**[Configure Twilio to send notifications in SRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-reliability-management/sr-add-twilio-key.md)

