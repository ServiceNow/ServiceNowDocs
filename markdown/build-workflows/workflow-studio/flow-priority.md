---
title: Flow priority
description: Specify the priority that you want a background flow to have in relation to other flows waiting to be run. Run a group of higher priority flows before running any lower priority flows.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Flow administration, Configure flows, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Flow priority

Specify the priority that you want a background flow to have in relation to other flows waiting to be run. Run a group of higher priority flows before running any lower priority flows.

You can only set a flow priority for flows that run in the background. Background flows run from the next available worker thread. By default, Workflow Studio can use up to half of the available worker threads to run background flows. If there’s no available worker thread to run a flow, the flow is queued until there’s an available worker thread to run it.

You can set background flows to have one of these priority values.

-   High
-   Medium
-   Low

By default, background flows run with medium priority.

**Note:** Flows that run in the foreground run in the current thread and don’t use flow priority to determine run order.

Setting a flow priority determines the order that worker threads pick flows from the queue. Worker threads run several higher priority flows before running a lower priority flow. This priority scheme ensures that some lower priority flows get run even when there are higher priority flows in the queue. When there’s a large work queue to run, most low-priority flows must wait until the high priority flows are run. After the high priority flows have run, the worker threads can run lower priority flows.

Should a flow remain in the queue for more than one minute, the system delegates the flow to another node to run. When a flow is delegated to another node, it loses its priority value. A delegated node pulls flows from the event queue in chronological order. The delegated node runs the oldest flows first and then runs the newest flows. Generally, delegating flows to run from another node only happens when all the available worker threads on a node are busy.

**Note:** Worker threads run all system events, not just flow events.

Flows also lose their priority value when they pause for any reason. Flows that resume from a pause run at the default Medium priority. For example, a flow could start running at high priority, then pauses to Wait for a Duration. When the flow resumes running, it runs at a Medium priority.

## Automatic pausing of low-priority flows

By default, the system checks for cases where high-priority flows are being blocked by running lower priority flows. Whenever a low-priority runs for longer than two minutes, the system checks whether any higher priority flows have run in the last five minutes. If no high-priority flows have run recently, then the system checks the number of flows waiting to run in the event queue. If there’s a backlog of at least 100 high-priority flows waiting to run in the event queue, the system pauses the running low-priority flow. Pausing a flow preserves its context and data. A paused flow returns to the event queue to run when there’s a worker available to process it.

If your low-priority flows aren’t running as expected, review the number of high-priority flows that your system generates and runs. See the design considerations for when to set a flow to high or low priority. If your low-priority flows are still not running, you can disable the pausing of low-priority with a system property. See [Workflow Studio flow system properties](../reference/flow-designer-system-properties.md) to change the value of the com.glide.hub.pause\_low\_priority\_flows\_enabled property.

## Quick API support

The quick API method retains the priority settings. Flows run by the quick API method run at the same priority that was previously defined for the flow.

## Design considerations

Follow these design considerations when setting flow priority.

-   **Avoid setting all flows to run at high priority**

    Use a mix of priorities rather than set all flows to high priority. Worker threads use the relative priority between flows to select work. If all of your flows run at high priority, then there are no lower-priority flows to make wait.

-   **Avoid setting flow priority for flows that have to pause**

    Keep flows that have to pause at the default medium priority since a flow that pauses loses its priority value when it resumes running.

-   **Use high priority for business critical flows**

    Limit high-priority to flows that have high business value, run rarely, and have a short runtime. Avoid setting high-volume flows to high priority as doing so limits the number of worker threads available to run other flows. A long-running high priority flow can also reduce the worker threads available to run other flows.

-   **Use low priority for high-volume flows**

    Run high-volume flows at low priority so that other time-sensitive flows can run first. Low-priority flows shouldn't be time-sensitive.

-   **Use medium priority for time-sensitive flows**

    Use the default flow priority when a flow has some time urgency when compared to other flows.


-   **[Show flow priority field](../task/show-flow-priority-field.md)**  
Configure the Setting list and form to show the Flow Priority field.
-   **[Set flow priority](../task/set-flow-priority.md)**  
Determine the order in which worker threads run background flows. Use a mix of flow priorities to distinguish between flows to defer and flows to run first.

**Parent Topic:**[Flow administration](flow-administration.md)

