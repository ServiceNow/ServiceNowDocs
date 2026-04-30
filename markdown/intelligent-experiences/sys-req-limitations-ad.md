---
title: System requirements and limitations in AI Desktop Actions
description: Be aware of system requirements and a few limitations when you’re using the AI Desktop Actions application.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-11-18"
reading_time_minutes: 2
keywords: [reference]
breadcrumb: [Reference, AI Desktop Actions, Enable AI experiences]
---

# System requirements and limitations in AI Desktop Actions

Be aware of system requirements and a few limitations when you’re using the AI Desktop Actions application.

## Hardware requirements

|Resource|Minimum|Recommended|
|--------|-------|-----------|
|CPU|Intel Processor \(Core i5\)|Intel Processor \(Core i7\)|
|RAM|4-GB RAM|8-GB RAM|
|Disk space|Minimum 20-GB free disk space after installing the OS, patches, and base software|Minimum 50-GB free disk space after installing the OS, patches, and base software|

## Software requirements

-   Windows 11 operating system is used.
-   A .NET 9.0 runtime v9.0.10 and .NET 9 Desktop Runtime v9.0.10 is installed.
-   No extended monitors are connected.
-   Add the end users who interact with the Execution workspace of AI Desktop Actions to the Remote Desktop Users group on the target machine and provide Remote Desktop access permissions for seamless automation execution.

    If your organization uses Group Policy, add the end users to a Microsoft Active Directory group that is permitted to use Remote Desktop through Group Policy on each target machine where desktop actions run.

    -   Local changes to the Remote Desktop Users group are temporary unless they align with Microsoft Active Directory entitlements.
    -   If the user is not entitled, Group Policy refresh automatically removes them from the group.
-   Theme must match between the systems used for recording and execution.

**Note:** Screen resolution and scaling must be the same between the systems used for recording and execution of desktop actions that are created prior to AI Desktop Actions v1.0.1.

## Limitations

<table id="table_ptl_hjd_w2c"><thead><tr><th>

Limit

</th><th>

Description

</th></tr></thead><tbody><tr><td>

RPA Attended robot and AI Desktop Actions parallel execution

</td><td>

To avoid conflicts, do not run the AI Desktop Actions Execution workspace and RPA Attended Desktop mode at the same time.

</td></tr><tr><td>

Pause for human input

</td><td>

If your automation requires manual inputs, such as entering an OTP or CAPTCHA, you must provide instructions to the AI Agent to wait for user input during execution. Otherwise, the automation can't proceed.

</td></tr><tr><td>

Single execution

</td><td>

The system supports one automation execution at a time within the Execution workspace.

</td></tr><tr><td>

Screen elements

</td><td>

During recording, auto-assignment accuracy of screen elements depends heavily on the target application’s technology and interface characteristics. Applications with strong accessibility support, such as well-defined UI elements and controls, stable rendering performance, and simple, consistent layouts enable anchors to be detected more reliably. In contrast, UI complexity, such as dynamic elements, frequent layout shifts, animations, or poor accessibility metadata can reduce accuracy and may require manual anchor configuration or additional tuning.

</td></tr><tr><td>

Getting table information

</td><td>

The **Get Table** step doesn’t convert ordinary text to table data. For the step to capture table data successfully, the data must already be in the table form.

</td></tr><tr><td>

Browsers parallel execution

</td><td>

The Chrome or Edge browser must not be used in parallel in the main session and the desktop session on your system. You must close the session in the main session to execute automations that use the Chrome or Edge browser in the Execution workspace.

</td></tr><tr><td>

Sensitive information

</td><td>

The sensitive information isn’t masked during recording. Confirm that you don’t record any sensitive information.

</td></tr></tbody>
</table>**Parent Topic:**[AI Desktop Actions reference](agentic-desktop-reference.md)

