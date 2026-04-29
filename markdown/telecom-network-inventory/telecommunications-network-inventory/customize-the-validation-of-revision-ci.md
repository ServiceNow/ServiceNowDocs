---
title: Customize the Validation of Revision CI
description: Added as per STRY57127942 - DOC1092072Customize the validation process of a CI \(Configuration Item\) using the Telecommunications Network Inventory application. You can customize the validation process by providing adjustable parameters based on the script.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Decision tables, Configure, Telecommunications Network Inventory]
---

# Customize the Validation of Revision CI

Customize the validation process of a CI \(Configuration Item\) using the Telecommunications Network Inventory application. You can customize the validation process by providing adjustable parameters based on the script.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin

## About this task

You can specify criteria and rules that fit your requirements, enabling a tailored approach to verify data accuracy and integrity.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio** &gt; **Flow Designer** &gt; **Actions**.

2.  Select **Validate CI Revision**.

3.  Select **Script Step** under Action Outline section.

4.  From the script, you can change the values of the CI relations or related items or both to false.

    The field value having value as False isn’t included in the validation process.


**Parent Topic:**[Configuring decision tables for Telecommunications Network Inventory](decision_tables.md)

