---
title: Creating rules for application vulnerable items in the Software Bill of Materials Workspace
description: Before you can see application vulnerable items \(AVITs\) in the Software Bill of Materials \(SBOM\) Workspace, you must set up the conditions under which AVITs are created.
locale: en-US
release: australia
product: SBOM Core
classification: sbom-core
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Viewing reports and dashboards in the Software Bill of Materials workspace, Use, Software Bill of Materials, Unified Security Exposure Management, Security Operations]
---

# Creating rules for application vulnerable items in the Software Bill of Materials Workspace

Before you can see application vulnerable items \(AVITs\) in the Software Bill of Materials \(SBOM\) Workspace, you must set up the conditions under which AVITs are created.

## AVITs in the SBOM Workspace

If you’ve installed and activated the SBOM Response application, AVITs are created for SBOM files if any of the imported data matches the conditions of your existing AVIT creation rules.

The SBOM Response and Vulnerability Response applications are required to set up rules for creating application vulnerable items \(AVITs\) automatically and remediating them with the Application Vulnerability Response workflow. See [Exploring Software Bill of Materials](../concept/vr-sbom-exploring.md) for more information.

As a user with the sn\_sbom\_resp.manage\_avi\_rule role, you must add AVIT creation rules in the SBOM Workspace before you can create AVITs for the vulnerabilities that are found in your ingested SBOM data. AVITs enable you to evaluate the integrity of the third-party components in your applications. An AVIT is created in your instance when an application is matched to a component that has an associated vulnerability.

In the SBOM Workspace, you can view only SBOM AVITs. However You can view SBOM AVITs along with other types of vulnerable items in the Vulnerability Manager Workspace in Vulnerability Response. You can view all the AVITs that have been created in the SBOM Workspace in the List Module. The list module also includes all the NVD and CWE entries and Application Vulnerabilities.

You can also assign AVITs for remediation based on recommendations from known vulnerability lists such as the National Vulnerability Database \(NVD\). A scheduled job is triggered, and if the conditions of your creation rules match the ingested data, AVITs are created.

You can track and remediate AVITs by setting up customized rules.

See [Create an application vulnerable item rule in the Software Bill of Materials Workspace](vr-sbom-create-avi-rule.md) for information about how to create a rule.

## SBOM AVITs in Vulnerability Manager Workspace in Vulnerability Response

You can view any SBOM AVITs that are created in the SBOM Workspace in the Vulnerability Manager Workspace if you have access to it.

**Note:** To view only SBOM AVITs from the Application Vulnerable Items list in the Vulnerability Manager Workspace rather than all AVITs, set the condition **\[Source\] \[is\] \[SBOM\]** **AND** **\[Scan type\] \[is\] \[SBOM-SCA\]** on the Application Vulnerable Items \[sn\_vul\_app\_vulnerable\_item\] table. To view the table, navigate in your instance to **All** and enter **sn\_vul\_app\_vulnerable\_item.list** in the filter navigator.

For more information about the Vulnerability Manager Workspace, how to view watch topics, application remediation efforts, and application remediation task rules for AVITs that are configured from the Vulnerability Response application in the Vulnerability Manager Workspace, see [Use watch topics in the Vulnerability Manager Workspace](../../../vulnerability-response/task/vr-ws-wtopic-ui-options.md).

Remediation tasks \(AVULs\) are created from AVITs and assigned automatically to groups for remediation based on your assignment rules. For more information about how to create these rules, see the following topics:

-   [Create or edit Vulnerability Response assignment rules](../../../vulnerability-response/task/create-vul-assign-rules.md)
-   [Create or edit Vulnerability Response remediation task rules](../../../vulnerability-response/task/create-vul-group-rules.md) and [Create a remediation effort in the Vulnerability Manager Workspace](../../../vulnerability-response/task/vr-ws-create-rev16.md).

## Reopening application vulnerable items in SBOM Response

A **Closed** application vulnerable item \(AVIT\) for a component with an associated vulnerability is re-opened automatically and visible in the SBOM Workspace if the following conditions exist:

-   The AVIT with the associated vulnerability is detected again by a third-party integration's vulnerability scans or the component with the vulnerability is part of a subsequent SBOM upload.
-   You have not deactivated the Reopen AVITs if detected \(**sn\_sbom\_resp.reopen\_avits\_if\_detected**\) system property. This system property is activated by default.
-   The substate of the **Closed** AVIT is not one of the following: **Mitigation Control in Place**, **Not Affected**, or **False Positive**. AVITs with these substates are not reopened by the system property.

Deactivate this system property only if you do not want **Closed** AVITs to reopen automatically.

