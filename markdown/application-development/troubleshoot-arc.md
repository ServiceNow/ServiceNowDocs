---
title: Troubleshoot Arc
description: Resolve common Arc issues, such as a token page that keeps appearing, sign in errors, AI connection errors, and sandbox failures.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/troubleshoot-arc.html
release: australia
topic_type: reference
last_updated: "2026-10-28"
reading_time_minutes: 6
keywords: [troubleshooting, token page, Keychain, GAIC errors, AI connection errors, sandbox errors, sign in errors]
breadcrumb: [Reference, ServiceNow Arc, Extend, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Troubleshoot Arc

Resolve common Arc issues, such as a token page that keeps appearing, sign in errors, AI connection errors, and sandbox failures.

## Arc keeps showing the token page

If Arc keeps showing the token page instead of opening, try these fixes in order on a macOS.

1.  Quit every open copy of Arc by pressing **Command+Q**, and then open the latest version.
2.  If the token page still appears, quit Arc again. In Activity Monitor, search for `arc-server`, quit any process that's still running, and then open Arc.
3.  If the token page still appears, get your token from Keychain by running this command in Terminal, and then paste the token into the token page.

    ```bash
    security find-generic-password -s "ServiceNow Arc" -a "servicenow-arc-credentials" -w | python3 -c 'import json,sys; print(json.load(sys.stdin)["server-token"])'
    ```


**Important:** This command shows your Arc credentials in Terminal. Run it only on your own computer, and don't share the output.

## Sign in errors

If Arc shows an error when you sign in, check these two causes:

-   Your account on the instance doesn't have the sn\_app\_arc.user role. Ask your administrator to grant it.
-   The ServiceNow Arc plugin isn't installed on the instance you're connecting to. Ask your administrator to install it, and then sign in again.

## AI connection errors

When Arc can't get a response from the AI service on your instance, it shows a message that explains what went wrong.

|Message|Code|Likely cause|What to do|
|-------|----|------------|----------|
|`No ServiceNow instance connected`|GAIC\_NOT\_CONNECTED|No instance is set up in Arc.|Connect an instance in settings.|
|`Can't reach your ServiceNow instance`|GAIC\_UNREACHABLE|A network, VPN, proxy, or firewall is blocking the connection, or DNS failed.|Check your VPN and proxy, confirm that the instance URL loads in a browser, and then retry.|
|`Your ServiceNow sign-in expired`|GAIC\_AUTH\_EXPIRED|The OAuth refresh token expired or was revoked \(HTTP 401, invalid\_grant\).|Select **Reconnect** and sign in again. Your chat is saved. If this keeps happening, your administrator checks the OAuth application and its token lifespan.|
|`Arc AI isn't set up on this instance`|GAIC\_ENDPOINT\_MISSING|The Arc app isn't installed, active, or upgraded, so its REST endpoint returns HTTP 404.|Your administrator installs, activates, or upgrades sn\_app\_cowork and checks that its REST API path exists.|
|`Your instance's AI connection isn't set up correctly`|GAIC\_CONFIG\_INVALID|Capability validation failed, for example because the connection has no sys\_alias hierarchy, or the backend returned code 100002 to 100005, 200000, or 300002.|Share the error code with your administrator, who checks the model records and their connection aliases in sys\_generative\_ai\_config.|
|`Arc AI is busy`|GAIC\_RATE\_LIMITED|You reached the request limit or quota \(HTTP 429\).|Wait a minute, and then retry. If this happens often, your administrator reviews the rate limits and quota.|
|`The response stopped partway`|GAIC\_TIMEOUT|The model or instance responded slowly, or the response stream stalled.|Retry. If it keeps happening, shorten your request and ask your administrator to check instance performance.|
|`Your instance is asleep`|GAIC\_INSTANCE\_ASLEEP|A developer or demo instance is hibernating, or the instance returned a web page instead of a response.|Open the instance in a browser, wait about 2 minutes, and then retry.|
|`You don't have access to this AI capability`|GAIC\_ACCESS\_DENIED|Your user or role isn't entitled to the AI capability \(HTTP 403, skill\_access\_denied\).|Your administrator grants the required role or entitlement, and then you retry.|
|`Your request was blocked by a safety check`|GAIC\_CONTENT\_BLOCKED|A guardrail or moderation check blocked the request \(code 300000, 300100, 300200, or 300300\).|Rephrase your request. Sending the same text again hits the same block.|
|`Invalid input`|GAIC\_INVALID\_INPUT|The message was empty or malformed \(INVALID\_REQUEST or code 100001\).|Type a message with more detail and send it again.|
|`Something went wrong`|GAIC\_UNKNOWN|An error that doesn't match another type, such as HTTP 502 from the AI service, a privacy check failure \(code 100006\), or code 100010, 200001, 300001, 300400, 400001, or 400002.|Retry once. If it keeps happening, copy the diagnostics and give the log ID to your administrator.|

## Sandbox errors on a macOS

To investigate, check `~/.servicenow-cowork/arc-server.log` and the openshell-gateway log.

|Symptom|What to do|
|-------|----------|
|The sandbox shows as ready, but every command fails, or you see `Policy fetch failed ... transport error`.|Quit Arc, delete `~/.servicenow-cowork/openshell-vm-state`, and then restart Arc.|
|You see `CreateSandbox ... Connection refused`, or `Sandbox entered error state` repeats after a network or VPN change.|In Activity Monitor, search for `openshell-gateway` and quit it. Wait for Arc to recreate the sandbox.|
|`draft_policy_chunk` is stuck for more than 30 seconds.|Quit Arc, delete `~/.servicenow-cowork/openshell-vm-state/gateway.db`, and then restart Arc.|
|You see `compute-driver.sock` refused.|Quit Arc, delete `~/.servicenow-cowork/openshell-vm-state/gateway.db`, and then restart Arc.|
|You see `VM exited with status 1` with no console output.|Contact your administrator.|
|You see `tar extraction failed`, `Checksum mismatch`, or `download failed`.|Your administrator confirms that the `sn_app_cowork.cowork_plugins_manifest` system property has a `Sandbox Image` node with all its values, and that the property value is valid JSON. Also confirm that install.service-now.com isn't blocked on your computer.|

## Sandbox errors on Windows

To investigate, check `%USERPROFILE%\.servicenow-cowork\arc-server.log` and the sandbox logs in `%USERPROFILE%\.microsandbox\sandboxes\arc-sandbox-<guid>\logs`.

Use the following fix if you see any of these symptoms:

-   The sandbox shows as ready, but commands fail, for example with `spawn "/bin/sh": No such file or directory` in kernel.log.
-   Sandbox setup fails repeatedly with the same error.
-   A corrupted root file system or a checksum error appears the first time the sandbox is created. In this case, your administrator also confirms that the `sn_app_cowork.cowork_plugins_manifest` system property has an `Arc Windows Sandbox image` node with valid JSON, and that install.service-now.com isn't blocked on your computer.

To fix these issues:

1.  Quit Arc.
2.  Delete `%USERPROFILE%\.servicenow-cowork\microsandbox-vm-state`.
3.  Delete the `%USERPROFILE%\.microsandbox` folder.
4.  Restart Arc.

Arc runs every agent command inside an isolated sandbox, a lightweight virtual machine that uses the Windows Hypervisor Platform. If the sandbox doesn't start, check that CPU virtualization is turned on in the computer's BIOS and that the Windows Hypervisor Platform feature is turned on.

**Important:** Don't turn on the full Hyper-V role. Arc needs only the Windows Hypervisor Platform.

To check virtualization and the Windows Hypervisor Platform:

1.  Open Windows PowerShell as an administrator. Select **Start**, enter `PowerShell`, right-click **Windows PowerShell**, and select **Run as administrator**.
2.  Run these commands to check BIOS virtualization and the Windows Hypervisor Platform feature.

    ```powershell
    Get-ComputerInfo -Property "HyperVRequirementVirtualizationFirmwareEnabled","HyperVisorPresent"
    Get-WindowsOptionalFeature -Online -FeatureName HypervisorPlatform | Select FeatureName, State
    ```

    The output shows whether firmware virtualization is turned on and the state of the Windows Hypervisor Platform feature, for example:

    ```
    HyperVRequirementVirtualizationFirmwareEnabled : True
    HyperVisorPresent                              : True
    
    FeatureName        State
    -----------        -----
    HypervisorPlatform Enabled
    ```

3.  If HyperVRequirementVirtualizationFirmwareEnabled is False, turn on virtualization in the BIOS. These steps apply to most Intel based Lenovo ThinkPad computers. Other manufacturers follow a similar pattern, but the keys and menu names differ.
    1.  Restart the computer, and while it starts, press **F1** repeatedly to open BIOS Setup. On some Lenovo models, press **Enter** at the Lenovo screen first, and then press **F1**.
    2.  Navigate to **Security** &gt; **Virtualization**.
    3.  Set **Intel \(VMX\) Virtualization Technology** to **Enabled**, and if it's listed, set **Intel VT-d Feature** to **Enabled**.
    4.  Press **F10** and select **Save and Exit**. The computer restarts.
    5.  Run the check commands again, and confirm that HyperVRequirementVirtualizationFirmwareEnabled is True.
4.  If HypervisorPlatform is Disabled, turn on the Windows Hypervisor Platform feature.

    1.  Select **Start**, enter `Turn Windows features on or off`, and open it.
    2.  Select the **Windows Hypervisor Platform** check box.
    3.  Select **OK**, and wait for Windows to apply the change.
    4.  When prompted, select **Restart now**.
    You can also turn on the feature by running this command in PowerShell as an administrator, and then restarting the computer when prompted:

    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName HypervisorPlatform -All
    ```

    After the computer restarts, run the check commands again, and confirm that HyperVRequirementVirtualizationFirmwareEnabled is True and HypervisorPlatform is Enabled.


**Parent Topic:**[ServiceNow Arc reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-cowork-reference.md)

