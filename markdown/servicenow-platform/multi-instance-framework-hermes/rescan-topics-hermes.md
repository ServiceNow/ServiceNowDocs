---
title: Rescan topics in Hermes
description: Synchronize topic records in your instance with topics in the Hermes Kafka cluster by rescanning.
locale: en-US
release: zurich
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Managing topics, Manage namespaces and topics, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Rescan topics in Hermes

Synchronize topic records in your instance with topics in the Hermes Kafka cluster by rescanning.

## Before you begin

Role required: kafka\_admin

## Procedure

1.  Navigate to **All** &gt; **Hermes Messaging Service** &gt; **Rescan Topics**.

2.  Synchronize topics by selecting **Confirm**.

3.  After the rescan finishes, view the script execution history.


## Result

Topic records are added to the Kafka Topics \[sys\_kafka\_topic\] table for each topic discovered in the Hermes Kafka cluster. The topic refresh date and time that appears in **All** &gt; **Hermes Messaging Service** &gt; **Topics** is updated.

**Parent Topic:**[Managing topics in Hermes](../concept/managing-topics-hermes.md)

