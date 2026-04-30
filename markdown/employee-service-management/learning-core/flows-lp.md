---
title: Activate Learning Core flows
description: Activate the flows that run on a schedule basis to pull learning course items from the Cornerstone OnDemand, Udemy, Pluralsight, Sumtotal , and Saba applications into the ServiceNow application.
locale: en-US
release: xanadu
product: Learning Core
classification: learning-core
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Integrating Learning Core with third-party learning management systems, Configuring Learning Core, Learning Core, HR Service Delivery, Employee Service Management]
---

# Activate Learning Core flows

Activate the flows that run on a schedule basis to pull learning course items from the Cornerstone OnDemand, Udemy, Pluralsight, Sumtotal, and Saba applications into the ServiceNow application.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Process Automation** &gt; **Flow Designer** &gt; **Designer**.

2.  In the **Flows** section, activate the flows that you need.

    To change the frequency and time at which you want to run the flow, click **Trigger**.

<table id="table_dx3_gb1_wdb"><thead><tr><th>

Flow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Trigger Cornerstone Learning Sync

</td><td>

By default, runs on a scheduled basis to pull course items from Cornerstone Ondemand into a ServiceNow application. **Important:** The flow does not run if you do not activate the Cornerstone Ondemand record in [Learning System Configuration](create-source-ln.md).

</td></tr><tr><td>

Trigger Pluralsight Learning Sync

</td><td>

By default, runs on a scheduled basis to pull course items from Pluralsight into a ServiceNow application.**Important:** The flow does not run if you do not activate the Pluralsight record in [Learning System Configuration](create-source-ln.md).

</td></tr><tr><td>

Trigger Udemy Learning Sync

</td><td>

By default, runs on a scheduled basis to pull course items from Udemy into a ServiceNow application. **Important:** The flow does not run if you do not activate the Udemy record in [Learning System Configuration](create-source-ln.md).

</td></tr><tr><td>

Trigger Sumtotal Learning Sync

</td><td>

By default, runs on a scheduled basis to pull course items from Sumtotal into a ServiceNow application. **Important:** The flow does not run if you do not activate the Sumtotal record in [Learning System Configuration](create-source-ln.md).

</td></tr><tr><td>

Trigger Saba Learning Sync

</td><td>

By default, runs on a scheduled basis to pull course items from the Saba system into a ServiceNow application. **Important:** The flow does not run if you do not activate the Saba record in [Learning System Configuration](create-source-ln.md).

</td></tr></tbody>
</table>
**Parent Topic:**[Integrating Learning Core with third-party learning management systems](setup-learning-third-party-1.md)

