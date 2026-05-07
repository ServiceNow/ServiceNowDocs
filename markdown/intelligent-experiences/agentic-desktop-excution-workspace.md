---
title: AI Desktop Actions Execution workspace
description: Execution workspace enables you to test, run, and monitor your desktop actions. It enables you to observe how your automations interact with desktop applications, including handling situations where human input is needed.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-11-17"
reading_time_minutes: 3
breadcrumb: [Defined desktop actions for desktop, Explore, AI Desktop Actions, Enable AI experiences]
---

# AI Desktop Actions Execution workspace

Execution workspace enables you to test, run, and monitor your desktop actions. It enables you to observe how your automations interact with desktop applications, including handling situations where human input is needed.

**Important:** Access to the Design workspace and Execution workspace depends on the user’s role.

-   When users with the AI Agent Admin \(sn\_aia.admin\) role sign in from their desktop, they can access the Home page and Design workspace to create desktop actions. When they test a desktop action, the Execution workspace launches automatically.
-   When users with the Now Assist panel user \(now\_assist\_panel\_user\) role trigger an automation from the Now Assist panel, the Execution workspace launches automatically to run the desktop action.

You don’t open the Execution workspace directly. It launches automatically when you test or run a desktop action.

This session acts as a virtual environment where the automations run in isolation. While desktop actions run in the Execution workspace, you can continue working on other desktop tasks.

**Note:**

To avoid conflicts, do not run the AI Desktop Actions Execution workspace and RPA Attended Desktop mode at the same time.

![AI Desktop Actions Execution workspace displaying "Listening for instructions" message for desktop session activation.](../image/execution-workspace-ready-ad.png "Execution workspace before executing automation")

![AI Desktop Actions showing the Shipping Management app with fields on a Windows 10 background.](../image/execution-workspace-ad.png "Execution workspace running the automation")

## Execution workspace features

Execution workspace offers the following features:

-   **Desktop-in-Desktop \(DiD\) mode**

    A virtual environment where your automation executes. You can monitor the execution of your desktop actions and how they interact with desktop applications.

-   **Step in/Step out**

    You can manually take control to provide an input by selecting **Step in**. Once done, you can leave the control by selecting **Step out**.

    **Note:** If your automation requires manual inputs, such as entering an OTP or CAPTCHA, you must provide instructions the AI Agent to wait for user input during execution. Otherwise, the automation cannot proceed.

-   **Single execution**

    The system supports one automation execution at a time within the workspace.

-   **Smart sizing**

    Smart Sizing enables your desktop sessions automatically adapt to your display. This ensures each captured desktop session is fully visible, readable, and usable, regardless of the device resolution and scaling.

    **Fit to window**: Automatically scales the desktop session to fit within the Execution workspace while keeping it fully visible and readable.

    **Original resolution**: Displays the desktop session at its original resolution. Scroll bars appear if the desktop session is larger than the Execution workspace.


## Execution statuses

Execution workspace shows the following statuses throughout the execution process.

<table id="table_nqp_t4k_3hc"><thead><tr><th>

Execution status

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Ready

</td><td>

Automation execution is ready to be initiated. The workspace is waiting for instructions from AI Agent Studio.

</td></tr><tr><td>

Initiated

</td><td>

Automation execution is initiated. The workspace has received the execution plan from AI Agent Studio.**Note:** When you launch Execution workspace for the first time, it takes longer to move to the Running state because it is setting things up for you.

</td></tr><tr><td>

Running

</td><td>

Automation execution is running. The workspace executes the steps defined in the desktop actions.

</td></tr><tr><td>

Success

</td><td>

Automation execution is completed successfully. The workspace executed the steps defined in the desktop actions and the outcome is shown on the Now Assist panel, such as the automation execution completed successfully and incident created successfully.

</td></tr><tr><td>

Failed

</td><td>

Automation execution is failed. The workspace couldn't execute the automation due to an error.

</td></tr><tr><td>

Canceled

</td><td>

Automation execution is canceled. The user canceled the execution manually.

</td></tr></tbody>
</table>**Related topics**  


[Example: Use AI agents to process badge-related requests automatically](../task/example-use-badging-ai-agent-ad.md)

[Example: Use AI agents to automatically enter data into the shipping management app](../task/example-use-shipping-ai-agent-ad.md)

