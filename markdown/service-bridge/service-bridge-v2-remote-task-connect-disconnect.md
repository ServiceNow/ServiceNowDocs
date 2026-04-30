---
title: Connect and Disconnect remote tasks
description: Remote tasks associated with active remote task definitions enable you to sync data between two parent tasks on the provider and consumer instances.
locale: en-US
release: zurich
product: Service Bridge
classification: service-bridge
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create remote tasks to sync data, Install and configure for consumers, Service Exchange for Consumers, Service Exchange]
---

# Connect and Disconnect remote tasks

Remote tasks associated with active remote task definitions enable you to sync data between two parent tasks on the provider and consumer instances.

When you create a remote task for an active remote task definition, the Status of the remote task is set to **Connected** on the provider and consumer instances if there are no errors. This ensures that the remote task syncs data including field updates, attachments, and comments between the parent tasks.

To stop synching of data between the instances, navigate to the Remote Task page on the provider or consumer instance and click **Disconnect**. When disconnected, the remote task pauses copying or transfer of data including work notes and comments between the instances.

**Note:** To resume syncing of data, you can navigate to the Remote Task page and click **Connect**. This option works only if the existing configuration is valid and has not been modified, and the remote task definition is active.

