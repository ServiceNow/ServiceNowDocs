---
title: Set a breakpoint to pause a component in RPA Desktop Design Studio
description: Set a breakpoint on a component in RPA Desktop Design Studio so that you can pause it for debugging purposes during an automation execution. You can set a breakpoint for any number of components.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/set-breakpoint-rpa-studio.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Set a breakpoint to pause a component in RPA Desktop Design Studio

Set a breakpoint on a component in RPA Desktop Design Studio so that you can pause it for debugging purposes during an automation execution. You can set a breakpoint for any number of components.

## Before you begin

Ensure that the component or components where you want to set a breakpoint in are a part of your automation.

Configure a component. For more information, see [Use a component in RPA Desktop Design Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/configure-components.md).

Role required: none

## Procedure

1.  In the RPA Desktop Design Studio, on the Design surface, right-click the title bar of the component where you want to set the breakpoint and then select **Breakpoint**.

    After a breakpoint is set on a component, you can see a red icon as shown in the following example.

    \[Omitted image "set-breakpoint-red.png"\] Alt text: Red icon that appears after a breakpoint is set on a component.

    During the automation execution, when the robot reaches a component that has a breakpoint, the execution pauses and the component is highlighted with a red border, as shown in the following example.

    \[Omitted image "set-breakoint-red-border.png"\] Alt text: Red border that appears when the robot reaches a component that has a breakpoint.

2.  Choose an option and complete the action.

<table id="choicetable_otx_hcg_wrb"><thead><tr><th align="left" id="d92239e122">

Option

</th><th align="left" id="d92239e125">

Action

</th></tr></thead><tbody><tr><td id="d92239e131">

**To execute the component where the breakpoint is set**

</td><td>

Click **Move next** under the **Design** tab or press the **Ctrl+F8** keys.For a step-by-step execution of the workflow, continue clicking the **Move next** button.

</td></tr><tr><td id="d92239e155">

**To continue the execution of the remaining components**

</td><td>

Click **Run** under the **Design** tab.

</td></tr><tr><td id="d92239e170">

**To find all the breakpoints in the automation**

</td><td>

Click the down arrow button next to the **Clear Breakpoints** button under the **Design** tab and select **Find all**.A list of breakpoints appears in the Find All References section.

</td></tr><tr><td id="d92239e191">

**To remove a breakpoint**

</td><td>

Right-click a desired component and select **Breakpoint**.

</td></tr><tr><td id="d92239e204">

**To remove all the breakpoints**

</td><td>

Click **Clear breakpoints** under the **Design** tab.

</td></tr></tbody>
</table>
**Parent Topic:**[Using automations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/rpa-studio-use.md)

