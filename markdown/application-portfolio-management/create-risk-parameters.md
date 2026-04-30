---
title: Create a risk parameter - Legacy
description: The risk on a software model is calculated based on four preconfigured parameters such as external aging risk, internal aging risk, external stage risk, and internal stage risk.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use - Legacy, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Create a risk parameter - Legacy

The risk on a software model is calculated based on four preconfigured parameters such as external aging risk, internal aging risk, external stage risk, and internal stage risk.

## Before you begin

Role required: sn\_apm.apm\_admin

## About this task

In addition to the preconfigured parameters, you can also create risk parameters as per your business application requirements and the software models that it is based on. However, if you create a parameter, then you must also write a script with the logic to calculate that parameter risk.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Administration** &gt; **TPM Risk Parameters**.

2.  Click **New** or open a record.

3.  Fill in the form fields.

    For field information, see [Risk Parameter form](../reference/risk-parameter-form.md).

4.  Click **Submit** or **Update**.


## What to do next

After creating the risk parameters [run the TPM risk engine to load the risk parameters and compute the application service risks](run-scheduled-job-to-calculate-risks.md).

**Parent Topic:**[Using Enterprise Architecture \(formerly Application Portfolio Management\) - Legacy](../concept/using-apm.md)

