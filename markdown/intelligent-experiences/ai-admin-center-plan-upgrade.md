---
title: Plan an instance upgrade \(Lux UI\)
description: Run an upgrade readiness pre-check and evaluate the current version against the target version to determine if you're ready to upgrade your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-admin-center-plan-upgrade.html
release: zurich
topic_type: task
last_updated: "2026-08-19"
reading_time_minutes: 2
keywords: [AI Admin Center, Now Assist Center, AI, AI setup]
breadcrumb: [Increasing AI readiness, AI Admin Center, Enable AI experiences]
---

# Plan an instance upgrade \(Lux UI\)

Run an upgrade readiness pre-check and evaluate the current version against the target version to determine if you're ready to upgrade your instance.

## Before you begin

The Lux experience for AI Admin Center must be enabled to perform this task. For more information, see Configure the AI Admin Center user experience.

Role required: sn\_na\_center.nac\_admin

## About this task

Before upgrading your ServiceNow instance, run a pre-upgrade scan against a target release to identify how the upgrade will affect your AI plugin configurations and customizations.

The scan provides an impact report for your instance highlighting any potential risks from new features, deprecated features, customization issues, compatibility issues, and behavior changes. Use the impact report when planning remediation to help prevent the upgrade from breaking functionality.

Each pre-upgrade scan and the resulting impact report reflects the configuration of the instance at that point in time. Previous impact reports aren't saved in the system. You can download a copy of the impact report to save for reference.

Follow these steps to run the upgrade readiness pre-check and review the results.

**Note:** This topic describes the AI Admin Center feature based on the Lux user experience \(UI\). There is no Next Experience UI version of this topic.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Center** or **Workspaces** &gt; **AI Admin Center**.

2.  Select **AI readiness** \(\[Omitted image "icon-aiac-lux-nav-readiness.png"\] Alt text: AI readiness icon.\) in the side navigation panel.

    The AI Readiness Assessment page opens.

3.  Select **Plan upgrade**.

    The Plan upgrade page opens showing the current version.

4.  Select a target version for comparison.

    If your instance is on the latest version, there is no option to select.

5.  Select **Run upgrade pre-check**.

    The results of the upgrade pre-check display in an **Upgrade readiness** list showing areas to address before upgrading.

    \[Omitted image "ai-admin-center-plan-upgrade.png"\] Alt text: Plan upgrade page showing the findings from the upgrade pre-check.

6.  Select **View details** for each result in the list.

    The selected details open in a side panel, grouped by issue type.

    \[Omitted image "ai-admin-center-plan-upgrade-details-panel.png"\] Alt text: Side panel showing detailed results of an upgrade pre-check.

    1.  Use the search and filter options to refine the list.

        -   Type in the search box and select the **Search** icon \(\[Omitted image "icon-now-assist-center-search.png"\] Alt text: Search icon.\) to filter by search criteria.
        -   Select one or more options from the Types filter menu.
    2.  Select the **Expand** icon \(\[Omitted image "icon-aiac-lux-expand.png"\] Alt text: Expand icon.\) for an issue type to view the issue details.

    3.  Select a filter over the issues to refine the list.

    4.  Select the **Close** icon \(\[Omitted image "icon-aiac-lux-close.png"\] Alt text: Close icon.\) to close the side panel.

7.  Select **Export** to download a copy of the upgrade readiness report.

    The upgrade readiness report downloads as a .csv file.


## What to do next

Plan remediation steps based on the results of the impact report and prepare your instance for the upgrade to the target release.

**Parent Topic:**[Increasing AI readiness in AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-center-using-readiness-evaluation.md)

**Related topics**  


[Run the AI readiness assessment job in AI Admin Center]()

[View your AI readiness assessment in AI Admin Center]()

