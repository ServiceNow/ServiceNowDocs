---
title: Run Block Request
description: Blocks communication with observables associated with a security incident.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Security Operations Integration- Block Request capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Run Block Request

Blocks communication with observables associated with a security incident.

## Before you begin

Role required: sn\_si.analyst

## About this task

**Note:** If no implementations are available, capability actions are not displayed in product menus.

The **Security Operations Integration - Block Request** flow can be triggered from an observable form, or from the **Security Incident Observables** related list on a security incident.

This example shows a Block Request from a security incident.

## Procedure

1.  Navigate to a security incident.

2.  Select observables from the **Related List** tab.

3.  Click **Block Request** in the **Actions on selected rows...** drop-down menu.

    ![Block Request](../image/RunBlockRequest.png)

    The dialog box appears.

    ![Block Request dialog box](../image/BlockRequestDialogBox.png)

4.  Choose the implementation.

5.  Click **Block**.

    The flow execution audit is displayed in the work notes section.

    ![Block Request work note example](../image/run-block-request-worknote.png)


**Parent Topic:**[Security Operations Integration- Block Request capability](../concept/block-request-capability.md)

