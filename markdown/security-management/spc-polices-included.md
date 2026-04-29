---
title: Policies included with the Security Posture Control application
description: There are a few policies that are included with the Security Posture Control application that are tied to important use cases and are ultimately shown as key insights on the dashboard on the landing page \(Home module\) in the SPC Workspace.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Policies, Explore, Security Posture Control, Security Operations]
---

# Policies included with the Security Posture Control application

There are a few policies that are included with the Security Posture Control application that are tied to important use cases and are ultimately shown as key insights on the dashboard on the landing page \(Home module\) in the SPC Workspace.

## Viewing policies

To view these policies, navigate to **Workspaces** &gt; **Security Posture Control** &gt; **Policies and findings** &gt; **All**.

These policies are deactivated by default. You must activate them before you can view returned results \(Findings\). You cannot edit these policies, but you can use them to help you create other policies by cloning their conditions as a starting point. See [Clone a policy or create a child policy in Security Posture Control](../task/spc-clone-policy.md) for more information.

You can clone these policies to create your own custom policies but note that any policies you clone are not reflected as key insights on the dashboard on the Home landing page with the key insights that are included with the application. However, you can configure findings for these cloned policies and see the returned results from these policies.

You can configure custom insights or reports for the cloned policies, or, alternatively configure findings for these cloned policies to manage remediation. You can also create your own custom policies from scratch to monitor security controls coverage as per your internal requirements.

The policies shipped with the application include the following categories:

-   Policies that monitor security controls coverage \(endpoint protection and vulnerability scanner\).
-   Policies that identify unmanaged devices.
-   Policies that monitor toxic combinations that involve critical combinations such as missing security controls, internet exposure, and so on.
-   Policies for SPC API Integrations for Mitigation Controls Monitoring.

After you clone and activate any policies you create, you must create your own custom insight record on the Custom insight builder module in the workspace \(the last module in the navigator panel\). Only then can you view the data from your policies on the Custom insights dashboard \(the second icon from the top in the workspace\).

## Policies and asset profiles included with the application

Get insights into your overall security posture and configuration gaps in your security tools using the policies and asset proﬁles that are included with the application. Activate these asset proﬁles and policies in the Security Posture Control workspace so that you can identify gaps in configuration or coverage of the following tools:

-   CrowdStrike
-   Microsoft Intune, Defender, and SCCM
-   HCL Big Fix
-   Qualys
-   Rapid7

## Creating your own policies

See [Creating your own policies in the Security Posture Control application](../task/spc-creating-policies.md) for more information about how to create your own policies.

For example policies, see [Examples of base, child, and cloned policies for Security Posture Control](spc-policy-examples.md).

See [Create and activate custom policies for Security Posture Control](../task/spc-create-policy.md) for more information about the steps required to create a policy.

See [Mitigation controls policies](spc-mitigation-policies.md) for more information for more information about policies used for mitigation controls monitoring.

