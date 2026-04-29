---
title: Inherit from multiple providers
description: Inherit individual control requirements from different provider packages to create a fully inherited control within an authorization package.
locale: en-US
release: australia
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [RMF step 2 - Select controls for an authorization package, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Inherit from multiple providers

Inherit individual control requirements from different provider packages to create a fully inherited control within an authorization package.

## Before you begin

-   The authorization package must be in the Select step.
-   Provider packages must be in the Monitor state.
-   The control objective must be marked as common in the provider packages.

Role required: sn\_irm\_cont\_auth.system owner, sn\_irm\_cont\_auth.info\_system\_sec\_officer, or sn\_irm\_cont\_auth.admin

## About this task

A fully inherited control inherits all its requirements from multiple provider packages, with each requirement sourced from the provider responsible for it. Use this task when different providers manage individual control requirements.

Unlike inherited controls from a single provider, fully inherited controls generate a control instance and test templates in the Implement step. This enables Security Control Assessors \(SCAs\) to test the inherited controls within their engagements.

Fully inherited controls differ from hybrid controls in one key way: in a hybrid control, at least one requirement is self-implemented by the current package. In a fully inherited control, all requirements must be inherited.

## Procedure

1.  Navigate to **All** &gt; **Continuous Authorization &amp; Monitoring** &gt; **All Authorization Packages**.

2.  Select an authorization package record that is in a **Select** state and has the Baseline controls added.

3.  To inherit controls from multiple providers, select a control objective from the Baseline Controls related list.

    1.  Select **Inherit from Multiple Providers**.

    2.  Select the requirements.

    3.  Select **Add**.


## Result

The list displays all controls that have been configured with fully inherited allocation for the current package.

When controls are generated in the Implement step, the system creates a control instance and test template for the control. The control record shows each requirement with its assigned provider package and an Inherited status. The Control Location field displays Fully Inherited.

## What to do next

To return a control to the baseline, open the control in the Fully Inherited Controls related list and select Move to Baseline.

