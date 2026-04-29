---
title: Set up the Voice Controls Simulator tool
description: Integrate with Interaction Controls Component \(ICC\) to manage voice call features. Then, use the Voice Controls Simulator tool to set up your call experience.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Voice Controls Simulator tool, Integrating with contact centers, Integrate, Customer Service Management]
---

# Set up the Voice Controls Simulator tool

Integrate with Interaction Controls Component \(ICC\) to manage voice call features. Then, use the Voice Controls Simulator tool to set up your call experience.

1.  Open the tool: Launch the Voice Controls Simulator tool from your workspace.
2.  Explore call flows: Use the simulator to try out different voice call scenarios.
3.  Customize your experience: Configure call scenarios in the CSM Configurable Workspace as required.

## Voice Controls Simulator tool dependencies

Before you start, make sure you have the following:

1.  Required plugins: Install ICC plugin.

    **Note:** After installation, the **Voice Test Tool Config** is available in the OpenFrame configurations.

2.  OpenFrame configuration:
    1.  Navigate to **All** &gt; **OpenFrame Configurations**.
    2.  Search for **Voice Test Tool Config**, and set the active flag to ‘true’.

        **Note:** You can access the test tool only if you have been added to the **Voice Test Tool User Group**.

    3.  Verify user access:
        -   Navigate to **Group** &gt; **Voice Test Tool Users** and check user access or add new users here.
        -   Check the roles assigned to each user in the group. The key role for this tool is: `sn_int_control_sim.voice_test_tool_user`.
3.  User roles: Users added to the tool inherits these roles:
    -   virtual\_agent\_admin
    -   sn\_int\_control\_sim.voice\_test\_tool\_user
4.  Supported workspaces: This tool works only in the CSM Configurable Workspace.

You are now ready to launch the Voice Controls Simulator tool. See [Launching the simulator](../task/launch-voice-controls-simulator.md).

