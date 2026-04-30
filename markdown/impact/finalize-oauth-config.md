---
title: Finalize OAuth configuration
description: To finalize the OAuth configuration, perform the following steps.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-11-18"
reading_time_minutes: 1
breadcrumb: [Configure the OAuth authentication method, Register your instance, Scan Engine integrations, Scan Engine, Platform Health, Using Impact, Impact]
---

# Finalize OAuth configuration

To finalize the OAuth configuration, perform the following steps.

## Before you begin

Role required: admin

## Procedure

1.  Export the My SN record to the provider instance.

    **Note:** You should export the My SN record rather than individually create it as the system IDs must match for a proper configuration.

2.  Repeat steps 6 and 7 in [Configure the OAuth authentication method](configure-oauth-auth-method.md) for all additional instances that you want to configure with bidirectional communication, but designate a sub-production instance as the Provider, and the Production instance as the Consumer.

    Information such as name and URL will be taken from the sub-production instance.

    In the Development instance, the status field should now display **Connection Valid**. This indicates that setup is complete and the integration now moves bi-laterally.

    **Note:** When setting up instances on the **My SN instances** related list, verify that each instance is connected to their respective OAuth application registry. Developer instances should be connected to `[Developer Instance] – Consumer`. Provider instances should be connected to `[Production Instance] – Consumer`.


