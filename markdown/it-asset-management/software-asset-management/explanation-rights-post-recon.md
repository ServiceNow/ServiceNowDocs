---
title: Explanation of license rights post reconciliation
description: Get visibility into how your rights are calculated and consumed post the reconciliation process.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Software reconciliation for compliance, Explore, Software Asset Management, IT Asset Management]
---

# Explanation of license rights post reconciliation

Get visibility into how your rights are calculated and consumed post the reconciliation process.

## Overview of explanation of rights

Understand how the Software Asset Management application calculates the number of licenses for your software assets.

A detailed explanation of license rights is provided for the following metric groups:

-   Microsoft
-   IBM
-   Red Hat
-   VMware
-   Oracle
-   SAP
-   Citrix
-   Common

For details on viewing the explanation of license rights, see [View calculations for your licenses in workspace](../task/licenses-required-workspace.md)

## Use case for Per Device license metric

The following is an example of how an explanation of license rights for a Per Device license metric appears on the Licenses Required by page:

-   The MacBook Air 15" device has installations of Microsoft Office 2016.
-   License consumption explanation: The device D9WW4HYV - MacBook Pro 15" has installs of Microsoft Office 2016. The calculation shows that rounding off the value of licensable installs \(1\) divided by maximum installs per right \(1\) is one licensable install. Since this value can be 0 when the maximum installs per right is infinite, we take the maximum of either the licensable installs calculated \(1\) or 1, which is 1 right. Based on per device licensing, D9WW4HYV - MacBook Pro 15" requires 1 right.

![License consumption explanation](../image/explanation-rights-usecase.png)

**Parent Topic:**[Software reconciliation for compliance](c_SAMReconciliation.md)

