---
title: Configure fields for escalation triggers
description: Configure additional fields for on-call escalation triggers in Service Reliability Management \(SRM\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/service-reliability-management/srm-configure-trigger-fields.html
release: zurich
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2025-11-18"
reading_time_minutes: 2
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

<table id="choicetable_uxy_qdw_3hc"><thead><tr><th align="left" id="d388268e108">

Table

</th><th align="left" id="d388268e111">

Supported fields

</th></tr></thead><tbody><tr><td id="d388268e117">

**em\_alert**

</td><td>

-   Assigned to
-   Flap count
-   Flap last state
-   Initial event generation time
-   Last event generation time
-   Number of Work Notes
-   Overall Event Count


</td></tr><tr><td id="d388268e151">

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

To set up an escalation trigger, see [Create an escalation trigger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-reliability-management/sr-trigger-escalation-policy.md).

**Parent Topic:**[Configuring Service Reliability Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-reliability-management/configuring-service-reliability-management.md)

**Related topics**  


[Install Service Reliability Management from Admin Center or ServiceNow Store]()

[Assign an administrator to Service Reliability Management]()

[Activate teams and services in SRM]()

[Customize service approval settings]()

[Customize team approval settings]()

[Configure error budget actions for breached SRM SLOs]()

[Approve a change request for SRM]()

[Configure Twilio to send notifications in SRM]()

[Install the Alert Automation application]()

