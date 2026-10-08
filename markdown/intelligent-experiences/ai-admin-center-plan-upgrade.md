---
title: Plan an instance upgrade \(Lux UI\)
description: Run an upgrade readiness pre-check and evaluate the current version against the target version to determine if you're ready to upgrade your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-admin-center-plan-upgrade.html
release: australia
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 4
keywords: [AI Admin Center, Now Assist Center, AI, AI setup]
breadcrumb: [Increasing AI readiness, AI Admin Center, Enable AI experiences]
---

# Plan an instance upgrade \(Lux UI\)

Run an upgrade readiness pre-check and evaluate the current version against the target version to determine if you're ready to upgrade your instance.

**Important:** Lux is the new user experience for AI Admin Center. For more information on the Lux experience, see [AI Admin Center user experience \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-admin-center-lux-user-experience.md).

The Next Experience AI Admin Center workspace is being prepared for deprecation in the November store release and will no longer be supported. For more information on the Next Experience UI, see [AI Admin Center workspace \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-center-workspace.md).

In AI Admin Center version 6.1, the Next Experience and Lux user interfaces are both available.

## Before you begin

You can select the LLM provider that generates the upgrade readiness pre-check results in the settings. For more information, see [Manage model providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/edit-model-providers.md).

Role required: sn\_na\_center.nac\_admin

## About this task

Before upgrading your ServiceNow instance, run a pre-upgrade scan against a target release to identify how the upgrade will affect your AI plugin configurations and customizations.

The scan provides an impact report for your instance highlighting any potential risks from new features, deprecated features, customization issues, compatibility issues, and behavior changes. Use the impact report when planning remediation to help prevent the upgrade from breaking functionality.

Each pre-upgrade scan and the resulting impact report reflects the configuration of the instance at that point in time. The system only retains the results of the current scan and the one immediately before it, so you can see what changed between them. Previous impact reports aren’t permanently saved. You can download a copy of the impact report to save for reference.

Follow these steps to run the upgrade readiness pre-check and review the results.

**Note:** This topic describes the AI Admin Center feature based on the Lux user experience \(UI\). There is no Next Experience UI version of this topic.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Center** &gt; **Home** or **Admin** &gt; **AI Admin Center**.

2.  Select **AI readiness** \(\[Omitted image "icon-aiac-lux-nav-readiness.png"\] Alt text: AI readiness icon.\) in the side navigation panel.

    The AI Readiness Assessment page opens.

    When a platform upgrade is available, a notification displays with a **Plan Upgrade** button.

    \[Omitted image "ai-admin-center-lux-plan-upgrade-banner.png"\] Alt text: New version notification on the AI readiness page.

3.  Select **Plan upgrade**.

    The Plan upgrade page opens showing the current version.

    The results of the last-run pre-check display, if applicable.

4.  Select a target version for comparison.

    If your instance is on the latest version, there is no option to select.

5.  Select **Run upgrade pre-check**.

    The results of the upgrade pre-check display in an **Upgrade readiness** list showing areas to address before upgrading.

    \[Omitted image "ai-admin-center-plan-upgrade.png"\] Alt text: Plan upgrade page showing the findings from the upgrade pre-check.

6.  Select **View details** for each result in the list.

    The selected details open in a side panel, grouped by issue type.

    \[Omitted image "ai-admin-center-lux-plan-upgrade-details.png"\] Alt text: Side panel showing detailed results of an upgrade pre-check.

    1.  Use the search and filter options to refine the list.

        -   Type in the search box and select the **Search** icon \(\[Omitted image "icon-now-assist-center-search.png"\] Alt text: Search icon.\) to filter by search criteria.
        -   Select one or more options from the **Types** filter menu.
    2.  Select the **Expand** icon \(\[Omitted image "icon-aiac-lux-expand.png"\] Alt text: Expand icon.\) for an issue type to view the issue details.

    3.  Select the **Close** icon \(\[Omitted image "icon-aiac-lux-close.png"\] Alt text: Close icon.\) to close the side panel.

7.  Select **Export** to download a copy of the upgrade readiness report.

    The upgrade readiness report downloads as a .csv file.

8.  Select **Proceed to upgrade in upgrade manager** to go to the Upgrade Console to manage your upgrade.

    For more information, see [Guided upgrade](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/um-guided-tour.md).


## What to do next

Plan remediation steps based on the results of the impact report and prepare your instance for the upgrade to the target release.

**Parent Topic:**[Increasing AI readiness in AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-center-using-readiness-evaluation.md)

**Related topics**  


[Run the AI readiness assessment job in AI Admin Center \(Next Experience UI\)]()

[Run the AI readiness assessment job in AI Admin Center \(Lux UI\)]()

[View an AI readiness assessment in AI Admin Center \(Next Experience UI\)]()

[View your AI readiness in AI Admin Center \(Lux UI\)]()

