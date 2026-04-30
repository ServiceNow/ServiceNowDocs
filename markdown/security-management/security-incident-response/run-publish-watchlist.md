---
title: Publish observables to a third-party watchlist
description: You can publish one or more observables or associated indicators to a third-party watchlist. Currently, the only implementation that supports this functionality is CrowdStrike Falcon Host.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage observables, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Publish observables to a third-party watchlist

You can publish one or more observables or associated indicators to a third-party watchlist. Currently, the only implementation that supports this functionality is CrowdStrike Falcon Host.

## Before you begin

Role required: sn\_si.analyst

## About this task

**Note:** If no implementations are available, capability actions are not displayed in product menus.

## Procedure

1.  Navigate to a security incident.

2.  Select **Observables** from the **Related List** tab.

3.  Click **Publish to Watchlist** in the **Actions on selected rows...** drop-down menu.

    ![Run Publish to Watchlist](../image/RunPublish2Watchlist.png)

    The dialog box appears.

    ![Publish to Watchlist dialog box](../image/Publish2WatchlistDiaglogBox.png)

4.  Enter or choose the implementation.

    **Note:** A workflow is triggered by the [Security Operations Integration- Publish to Watchlist capability](../concept/pubish-to-watchlist-capability.md) when you select the CrowdStrike Falcon Host implementation.

5.  Click **Submit**.


