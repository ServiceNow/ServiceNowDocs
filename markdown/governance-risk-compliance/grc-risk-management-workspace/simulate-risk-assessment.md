---
title: Simulate a risk assessment
description: Simulate a risk assessment to verify the associated risk assessment methodology \(RAM\) configuration when it is in the draft state.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Perform Advanced Risk Assessment, Use, Risk Management, Governance, Risk, and Compliance]
---

# Simulate a risk assessment

Simulate a risk assessment to verify the associated risk assessment methodology \(RAM\) configuration when it is in the draft state.

## Before you begin

Role required: sn\_risk.admin

## About this task

To modify the configuration of a published RAM, you need to delete all its assessments manually and change the RAM state to Draft. The simulation of risk assessment enables you to verify the RAM configuration when the RAM is in the draft state. This feature helps you to validate a factor, scoring logic, and the workflow and make necessary changes to the RAM before it is published. The simulated risk assessments are not used for risk aggregation and are deleted after the RAM is modified or published.

## Procedure

1.  Navigate to **All** &gt; **Advanced Risk Assessment** &gt; **Administration** &gt; **Risk Assessment Methodologies**.

2.  Select and open the RAM for which you want to verify the configuration.

    **Important:** You should select a RAM that is in the draft state.

3.  Click **Simulate**.

    **Important:** This button appears only when all the assessment types for the selected RAM are published.

    A dialog box appears for the risk or object selection.

4.  Select a risk or object that you want to simulate.

    **Important:** You can select risks and objects that belong to the entity classes and tables specified in the RAM.

5.  Click **Submit**.

    A simulated risk assessment is created, and a success message appears with the risk assessment number. You can click and open the risk assessment number to perform the assessment.

6.  To view all the simulated assessments for the selected RAM, click **View simulated assessments**.


**Parent Topic:**[Perform Advanced Risk Assessment](../concept/use-advanced-risk-assessment.md)

