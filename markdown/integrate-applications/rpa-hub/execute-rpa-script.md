---
title: Re-evaluate license distribution by executing RPA scripts
description: Run the Robotic Process Automation \(RPA\) script on demand to validate and unlock the robots in a domain and its child domains.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Re-evaluate license distribution by executing RPA scripts

Run the Robotic Process Automation \(RPA\) script on demand to validate and unlock the robots in a domain and its child domains.

## Before you begin

Familiarise with license distribution in RPA Hub concepts. For more information, see [Robot license distribution in RPA Hub](../concept/license-rpa-hub.md).

To unlock the robots in a domain, ensure that the license entitlement and consumption is compliant.

A schedule script runs every 12 hours to evaluate the utilized robots.

You must do this task in the classic environment.

Role required: rpa\_admin

## About this task

An RPA script is a scheduled job that is executed on demand.

If you want to execute this script on demand, follow the steps in this topic.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **Administration** &gt; **RPA Scripts**.

2.  Select **Re-evaluate License Distribution**.

3.  Select **Execute Now**.

    A scheduled job runs to reevaluate the distribution of attended and unattended robots across different domains. If there is any discrepancy, it locks that particular domain and related child domains.


