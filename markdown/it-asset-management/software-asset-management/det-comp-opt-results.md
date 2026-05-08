---
title: Evaluate Microsoft 365 compliance and optimization results
description: Evaluate Microsoft 365 compliance and optimization results to find actual and potential cost savings and recommended licensing optimizations.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating with Microsoft 365, Microsoft 365 integration, Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Evaluate Microsoft 365 compliance and optimization results

Evaluate Microsoft 365 compliance and optimization results to find actual and potential cost savings and recommended licensing optimizations.

## Before you begin

Role required: sam\_admin or sam\_user

The discovery of Microsoft 365 must be complete to evaluate the software compliance. For more information about using Discovery and Microsoft SCCM together, see Discovery and SCCM together.

The usage of Microsoft 365 plans must be available from both Microsoft certified APIs and Microsoft SCCM to evaluate the software optimization.

## Procedure

1.  Navigate to **Software Asset Workspace** &gt; **License operations**.

2.  In the left pane, select **Licensing** &gt; **Software entitlements**.

3.  Select **New**.

4.  Create entitlements for Microsoft 365 by selecting the correct Publisher Part Number \(PPN\) to verify compliance.

    For more information about creating entitlements, see [Create entitlements in workspace](create-entitlements-workspace.md).

    **Note:** Ensure that the License metric value is User Subscription.

5.  Navigate to **License usage** in the left pane.

6.  Select the **Reconciliation** tab.

7.  Select **Run reconciliation**.

8.  View compliance analysis results in [Office 365 &amp; Adobe Cloud dashboard in Software Asset Management classic](../concept/sam-saas-subscription-dash.md) and [SaaS overview dashboard in workspace](../reference/saas-dashboard-workspace.md).

    For more information about running software reconciliation, see [Run software reconciliation in Software Asset Management classic](t_RunReconciliation.md) and Run Software Asset Management Foundation plugin software reconciliation in classic.

9.  View all optimized plans for Microsoft 365 subscription on the [Optimization and savings dashboard in workspace](../reference/optimization-dashboard-workspace.md).


