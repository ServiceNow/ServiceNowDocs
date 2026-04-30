---
title: Remote Process Sync actions
description: Learn how to use actions in outbound and inbound flows for your Integration Hub Remote Process Sync integration.
locale: en-US
release: xanadu
product: Integration Hub Remote Process Sync
classification: integration-hub-remote-process-sync
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Integration Hub Remote Process Sync, Creating integrations with applications]
---

# Remote Process Sync actions

Learn how to use actions in outbound and inbound flows for your Integration Hub Remote Process Sync integration.

Remote Process Sync provides you with a collection of Workflow Studio actions that you can use to customize the default [outbound and inbound flow](getting-started-with-remote-process-sync.md#outbound-flows-and-inbound-flows) templates. These actions let you:

-   Create correlations between records on local and remote instances
-   Manage attachments between local and remote instances
-   Send captured payloads to a remote instance
-   Transform inbound payloads to complex objects

## Remote Process Sync action dependencies

Certain Remote Process Sync actions are dependent upon other actions, and thus are generally intended for you to use together. The following use cases describe situations in which you might consider using dependent Remote Process Sync actions in your outbound and inbound flows.

Correlate a record with a captured payload: Use these actions in the following order to automatically correlate a record with a captured payload to be sent to a remote system:

1.  [Look Up Correlation By Local Correlation ID](look-up-correlation-local-id-action.md) - Use this action to determine if a correlated record exists between your staged local record and a record on the remote system.
2.  [Send Captured Payload to Remote System](send-captured-payload-remote-system-action.md) - Use the `Correlation Detail` output data pill from the **Look Up Correlation By Local Correlation ID** record as the value for the Correlation Detail input in this action. This enables you to correlate the local record containing the outbound payload to a record on the remote system.

**Note:** The **Remote Process Sync Outbound Flow Template - Basic** provides you with these two actions so that you don't need to set up this correlation yourself.

Identify and request missing attachments from a remote system: Use these actions in the following order to automatically look up and request attachments from a remote system that don't exist in your local system:

1.  [Identify New Attachments](identify-new-attachments-action.md) - Use this action to look up any attachments that exist on the remote system but don't exist on your local system for correlated records.
2.  [Request Attachments from Remote System](request-attachments-remote-system-action.md) - Use this action to request the transfer of identified attachments from the remote system to your local system.

