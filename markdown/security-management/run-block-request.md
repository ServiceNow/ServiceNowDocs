---
title: Run Block Request
description: Blocks communication with observables associated with a security incident.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/security-management/run-block-request.html
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

    \[Omitted image "RunBlockRequest.png"\] Alt text: Block Request

    The dialog box appears.

    \[Omitted image "BlockRequestDialogBox.png"\] Alt text: Block Request dialog box

4.  Choose the implementation.

5.  Click **Block**.

    The flow execution audit is displayed in the work notes section.

    \[Omitted image "run-block-request-worknote.png"\] Alt text: Block Request work note example


**Parent Topic:**[Security Operations Integration- Block Request capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/block-request-capability.md)

