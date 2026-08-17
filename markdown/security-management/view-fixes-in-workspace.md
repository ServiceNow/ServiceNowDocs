---
title: View fixes in USEM Workspace
description: Open the Fix list and form in Unified Security Exposure Management Workspace to review the fixes that Fix Intelligence for SEM has identified, and see the findings and assets each one resolves.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/view-fixes-in-workspace.html
release: zurich
topic_type: task
last_updated: "2026-07-29"
reading_time_minutes: 2
keywords: [view fixes, Security Exposure Management Workspace, Fix list]
breadcrumb: [Use, Fix Intelligence for Security Exposure Management, Integrations, Unified Security Exposure Management, Security Operations]
---

# View fixes in USEM Workspace

Open the Fix list and form in Unified Security Exposure Management Workspace to review the fixes that Fix Intelligence for SEM has identified, and see the findings and assets each one resolves.

## Before you begin

Role required: `sn_vul_fix.read`, or a Vulnerability Response role that contains it.

Prerequisites:

-   ServiceNow Support has configured the Armis Centrix™ for ViPR integration, and at least one sync has completed. See [Install Fix Intelligence for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/install-fix-intel.md).

## About this task

Fixes appear in Unified Security Exposure Management Workspace as a list and a form. For general workspace navigation, such as opening lists and using the Remediation view, see the linked USEM Workspace topics; this task covers only what is specific to fixes.

## Procedure

1.  Open Unified Security Exposure Management Workspace.

2.  Open the **Remediation overview** and select the **Fix Intelligence** tab.

    The **Fix Intelligence** tab summarizes findings that have a fix identified, the number of unique fixes, and the top fixes to act on. To review the fixes themselves, open the Fix list from this tab or select **View All** on a widget. For how to use these widgets to prioritize, see [Prioritize remediation by fix](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/prioritize-remediation-by-fix.md).

3.  Open the Fix list.

    The list shows each fix with its **Description**, **Findings** count, **Assets** count, **Risk rating**, **Risk score**, **Remediation category**, and **Software package**.

4.  Select a fix to open its form.

    The form header highlights the fix description with its assets, findings, remediation category, and risk rating; the risk rating is color-coded from Critical to None.

    From the fix, you can review the following information:

    -   General information \(software package and version, remediation category, and finding category\).
    -   Vulnerable items the fix remediates.
    -   The remediation task that groups those findings, if one exists.
5.  Review the fix's fields to understand what it remediates and how much risk it removes.

    For what each field means, see [Understanding Fix records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/understanding-fix-records.md).


## Result

You can see the ingested fixes and the scope of each one.

## What to do next

Prioritize which fixes to act on first: [Prioritize remediation by fix](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/prioritize-remediation-by-fix.md).

**Parent Topic:**[Using Fix Intelligence for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/using-fix-intel-security-exposure-management.md)

**Related topics**  


[Remediation view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-workspaces-ui-remediation-module.md)

[Use the List view in the Security Exposure Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-ws-list-view.md)

