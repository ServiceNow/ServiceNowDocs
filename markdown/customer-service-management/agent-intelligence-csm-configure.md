---
title: Configure Predictive Intelligence for case management
description: Activate the Predictive Intelligence plugin and enable the related system property and client script to use Predictive Intelligence with Customer Service Management.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Predictive Intelligence for case management, Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Configure Predictive Intelligence for case management

Activate the Predictive Intelligence plugin and enable the related system property and client script to use Predictive Intelligence with Customer Service Management.

## Before you begin

Role required: admin

## Procedure

1.  Activate the Predictive Intelligence plugin \(com.glide.platform\_ml\).

2.  Enable the **Enable/Disable the prediction for case** property \(**sn\_customerservice.case.mlpredictor.enable**\).

    1.  Navigate to **Customer Service** &gt; **Administration** &gt; **Properties.**

    2.  Enable the **Enable/Disable the prediction for case** check box.

    3.  Click **Save**.

3.  Enable the **Predict Case Values** client script.

    1.  Navigate to **System Definition** &gt; **Client Scripts**.

    2.  Click **Predict Case Values** in the Client Scripts list.

    3.  Enable the **Active** check box.

    4.  Click **Update**.


