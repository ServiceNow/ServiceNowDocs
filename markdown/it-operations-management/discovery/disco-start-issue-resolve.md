---
title: Discovery start and classification issue resolution
description: Use the Discovery Admin Workspace Diagnostics page to identify and resolve the cause when Discovery fails to start or classify a device.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/disco-start-issue-resolve.html
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-09-03"
reading_time_minutes: 3
breadcrumb: [Discovery monitoring and issue resolution, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery start and classification issue resolution

Use the Discovery Admin Workspace Diagnostics page to identify and resolve the cause when Discovery fails to start or classify a device.

Most start and classification failures have one of a few causes: the MID Server can't reach the target, the configured account lacks the required rights on the target, or software on the target host blocks Discovery scripts from running. The [Diagnostics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/discovery-admin-workspace-diagnostics.md) page identifies most of these causes with a refined code that includes the root cause and remediation steps.

## Requirements

The **Diagnostics** page, refined codes, and AI Insights described here require the Error Framework. Confirm the following:

-   The ServiceNow AI Platform is running the Brazil release, or the Australia release beginning with Patch 3.
-   Discovery Admin Workspace, beginning with v1.17.0, is installed.
-   The **sn\_disco\_workspace.enable\_error\_framework** system property is set to `true` \(default behavior\).
-   You have the discovery\_admin role.

To use AI Insights, install the plugins listed in the following table.

|Plugin name|Plugin ID|Availability|
|-----------|---------|------------|
|ServiceNow Otto for Error Framework|com.sn\_ef\_gen\_ai|Australia Patch 3|
|ServiceNow Otto|sn\_genai\_platform|Required by ServiceNow Otto for Error Framework|

## Issue resolution process

The **Diagnostics** page displays Discovery errors that have been refined and assigned a specific error code. Each refined code identifies the error type and includes the root cause and recommended remediation steps. Start and classification failures fall into two groups. When a cause can be refined, the **Diagnostics** page provides guidance to help resolve it. When a cause cannot be refined, no error code is available and you must verify the cause manually. Work through the causes in the order that follows.

\[Omitted image "daw-errors-diagnostics.png"\] Alt text: Discovery Admin Workspace Diagnostics page

## Review the Errors tab

Navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Diagnostics** and review the **Errors** tab. Locate the error by refined code, then open it to view the root cause and remediation steps. Errors that stop Discovery for a device or schedule display with **Critical** severity.

The following refined codes commonly correspond to start and classification failures.

<table id="table_tjr_3qt_fkc"><thead><tr><th>

Refined code

</th><th>

Cause

</th></tr></thead><tbody><tr><td>

SN-DISC-5602

</td><td>

MID Server isn't running on Windows.

</td></tr><tr><td>

SN-DISC-1007

</td><td>

SSH connection failed.

</td></tr><tr><td>

SN-DISC-3486

</td><td>

Probe skipped because a previous probe failed.

</td></tr><tr><td>

SN-DISC-3888

</td><td>

Discovery ECC Queue is missing or empty.

</td></tr><tr><td>

SN-DISC-6004

</td><td>

The target's SSL certificate isn't trusted.**Note:** Requires Discovery Admin Workspace v1.20.0.

</td></tr></tbody>
</table>## Verify connectivity and credentials

If Discovery still fails after you follow the remediation steps for a refined code, verify connectivity and credentials.

Confirm that the MID Server can reach the target on the ports that the protocol requires, and that no firewall blocks that path. For Windows targets, confirm that inbound traffic is enabled on the SMB port 445.

Confirm that the account Discovery uses has the rights on the target that the protocol requires. For Windows targets, confirm that the account can create and read files in the administrative share used during classification.

## Check host configuration

The following conditions don't produce a refined code. If the earlier refined codes don't resolve the failure, confirm each one manually.

-   **PowerShell execution policy**

    The execution policy on the target host must allow Discovery to run PowerShell commands, including any policy applied through Group Policy. If a restrictive policy is blocking scripts, update the policy or add an exemption for Discovery.

-   **Endpoint security**

    Confirm that endpoint protection software on the target isn't blocking the Discovery PowerShell script. If script control is enabled, add an exclusion for the Discovery script and add the ServiceNow publisher to the trusted publisher list.


## Legacy Diagnostics experience

The refined codes and AI Insights described here require the Error Framework. If your instance runs on an earlier version of Discovery Admin Workspace, the **Diagnostics** page shows the legacy experience instead. In that case, review the Diagnostics tab to review Discovery errors by error code and severity, then apply the same environmental checks.

**Related topics**  


[Error Framework in Discovery Admin Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/error-framework-daw.md)

[Discovery Admin Workspace Error Details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/daw-error-details.md)

