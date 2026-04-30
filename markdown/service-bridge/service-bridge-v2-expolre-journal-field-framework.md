---
title: Journal field framework
description: The Journal Field Framework \(JFF\) enables real-time synchronization of journal type fields, such as comments and work notes, between provider and consumer.
locale: en-US
release: zurich
product: Service Bridge
classification: service-bridge
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Explore, Service Exchange]
---

# Journal field framework

The Journal Field Framework \(JFF\) enables real-time synchronization of journal type fields, such as comments and work notes, between provider and consumer.

JFF also enhances operational transparency, preserves historical context, and verifies that updates are attributed to actual users for greater transparency.

The synchronization of journal type fields between consumer and provider instances is enabled through a Remote Task Definition \(RTD\) configured with compatibility version 2.2.x or later.

With JFF, you can do the following.

-   **Journal field mapping**

    Map and synchronize any journal type fields between provider and consumer instances based on the **Inbound** and **Outbound** field configurations in a remote task definition.

    For example, while creating an RTD, you can create mappings such as:

    -   Comments to work notes
    -   Work notes to comments
    When a remote task is created based on the RTD, these mapped journal fields are automatically synchronized between the provider and consumer instances. As a result, when comments or work notes are posted in one instance, they appear in the connected instance as well.

    A comment-to-comment mapping is created by default in both the **Inbound** and the **Outbound** field configurations while creating a remote task definition from Service Exchange version 2.2.x. For more information, see [Create a remote task definition in Service Exchange for Providers](../task/service-bridge-v2-create-remote-tasks-defs.md).

    -   **Rules of journal field mapping**

        Journal field framework supports the following format \(source to target\).

        -   journal field \(source\) to journal field \(target\)
        -   journal field \(source\) to non-journal field \(target\)
    Journal field framework doesn’t supports non-journal field \(source\) to journal field \(target\) mapping.

    **Note:** In a Remote Task Definition \(RTD\), you cannot use the same journal source field twice for different mappings. For example, work notes to work notes and work notes to comments in the same RTD are not allowed.

-   **Write journal entries as an actual user**

    Write journal entries using user identities rather than a generic company name. For example, all comments for user David would appear as David \(xyz company\).

-   **Synchronize historical journal entries**

    Synchronize all historical journal entries between consumer and provider instances for a remote task.

    If the **Sync pre-existing entries** option is configured during Remote Task Definition \(RTD\) setup and while activating the RTD, all journal comments made in a task are synchronized between the consumer and provider instances when a remote task is connected.


## Considerations

Journal synchronization or synchronize of historical journals might not work for the following scenarios:

-   Synchronization of Journal fields won’t work if a remote task is deleted and a new remote task is later created for the same parent task and RTD.
-   Synchronization of historical journal entries stops and doesn’t resume if a remote task is disconnected and later reconnected, even if the **Sync pre-existing entries** option is enabled in the connected RTD.

**Related topics**  


[Create a remote task definition in Service Exchange for Providers](../task/service-bridge-v2-create-remote-tasks-defs.md)

[Activate a remote task definition record in Service Exchange](../task/service-bridge-v2-activate-remote-task.md)

