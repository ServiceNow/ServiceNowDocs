---
title: Verify EAP configuration for migration from SAFe
description: Ensure that the right EAP configuration which suits your current SAFe configuration is active and that the required work types are selected.
locale: en-US
release: xanadu
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Migrate from SAFe, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Verify EAP configuration for migration from SAFe

Ensure that the right EAP configuration which suits your current SAFe configuration is active and that the required work types are selected.

## Before you begin

Check the SAFe application \(Essential SAFe or Portfolio SAFe\) that is currently in use in your ServiceNow instance.

Role required: admin

## About this task

Verify EAP configuration to start migration of SAFe data. 

## Procedure

1.  Navigate to **All** &gt; **Strategic Planning** &gt; **Enterprise Agile Planning** &gt; **EAP Configurations**.

2.  Activate the EAP configuration that you need and verify that the required work types are allowed.

    1.  Open the EAP configuration record.

    2.  Enable the **Active** field.

        -   For Essential SAFe: Activate Essential Configuration.
        -   For Portfolio SAFe: Activate Portfolio Configuration.
    3.  In the **Work types allowed** field, ensure that **Epic**, **Feature**, and **Story** are added to the Selected list.

3.  Save the form.


## What to do next

[Verify table, field, and choice mapping between SAFe and EAP](verify-table-field-and-choice-mapping-between-safe-and-eap.md).

