---
title: Delete a namespace in Hermes
description: Prevent topics from being added to a namespace by deleting the namespace in Hermes.
locale: en-US
release: xanadu
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing namespaces in Hermes, Manage namespaces and topics, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Delete a namespace in Hermes

Prevent topics from being added to a namespace by deleting the namespace in Hermes.

## Before you begin

Role required: hermes\_admin or kafka\_namespace\_admin

## About this task

You can't delete a namespace if any active topics belong to it. You must delete or deactivate the topics in a namespace before you can delete the namespace.

## Procedure

1.  Navigate to **All** &gt; **Hermes Messaging Service** &gt; **Namespaces**.

2.  Select a namespace that you want to delete.

3.  Select **Delete**.


## Result

The namespace record is deleted from the Kafka Namespace \[sys\_kafka\_namespace\] table.

**Parent Topic:**[Managing namespaces in Hermes](../concept/managing-namespaces-hermes.md)

