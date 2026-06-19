---
title: Anchor
description: An anchor is a unique identifier which is identified on the screen. It helps specify the target area for a simulated user interaction by defining a static area from which actions can be defined at a relative distance. The position of actions is calculated based on the anchor and the actions are performed relative to it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/anchor.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Actions \(UI\), Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Anchor

An anchor is a unique identifier which is identified on the screen. It helps specify the target area for a simulated user interaction by defining a static area from which actions can be defined at a relative distance. The position of actions is calculated based on the anchor and the actions are performed relative to it.

In the following image, the anchor is a rectangle that identifies the location of the text “The world works with ServiceNow.” The target template where the action is to take place shows as a rectangle whose position is relative to the top left corner of the anchor’s rectangle. When the action is executed, the center of the template is identified and targeted for action. \[Omitted image "anchor-concept1.png"\] Alt text: Use anchors.

You can use a single anchor to perform multiple actions, each with its own relative distance from the anchor.

When multiple actions are configured, they are executed in the order they were added.

However, if the location of the element on which an action is performed changes, the action may occur at the wrong place. To help prevent this, you can use multiple anchors.

When you add multiple actions, the component performs the actions in the order that they are added. Likewise, when you add multiple anchors, the actions connected to each anchor execute before the actions connected to the next anchor. You can change the order of the actions connected to each anchor. You can also change the order of the anchors themselves. Refer to the following image.\[Omitted image "anchor-concept3.png"\] Alt text: Reorder actions under the anchor

To reorder an action or an anchor, drag it to its new position. As you move it, its new location is indicated by a line \(\[Omitted image "reorder-actions.png"\] Alt text: Reorder actions under an anchor.\).

To delete an anchor, in the Anchoring Surface pane of the ActionSet Settings dialog, right-click the anchor, and then select **Delete**.

**Parent Topic:**[Actions \(UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/actions-ui.md)

