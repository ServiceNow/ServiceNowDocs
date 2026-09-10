---
title: Engagement brief
description: The engagement brief summarizes recent signals across risk, adoption, and market activity for a specific engagement.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/account-lifecycle-exec-insight-gen.html
release: australia
topic_type: concept
last_updated: "2026-08-31"
reading_time_minutes: 3
keywords: [Executive Insight Generator, engagement brief, AI-generated insights, engagement updates, Customer Success Management]
breadcrumb: [Engagement home page, Manage engagements, Customer success, Use, Customer Success Management]
---

# Engagement brief

The engagement brief summarizes recent signals across risk, adoption, and market activity for a specific engagement.

The Executive Insight Generator skill analyzes engagement metrics and generates actionable insights organized by category. The generated brief highlights important and recent changes in metrics, helping customer success agents identify risks and opportunities and take proactive actions.

The brief appears in the **Engagement updates** component at the top of the engagement record page. It loads automatically when the page opens and displays a one-line overview followed by a category-wise breakdown of recent signals.\[Omitted image "engagement-brief.jpg"\] Alt text: Engagement brief

**Note:**

-   The engagement brief is displayed if the following plugins have been installed:
    -   Technology Account Management Experiences \(sn\_tech\_exp\)
    -   ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) \(sn\_tmt\_gen\_ai\)
-   The Executive Insight Generator skill has been activated. See  for details.

The Executive Insight Generator skill must be activated. See  for details.

## Insight categories

The following categories are examples included in the base system. You can define your own categories when configuring custom triggers.

-   **Risks**

    Signals that indicate active threats to engagement health, such as a health score entering the red zone or an overdue play.

-   **Declining metrics**

    Signals that show a downward trend in key metrics, such as low product usage or a health score that has dropped significantly without entering the red zone.

-   **Opportunities**

    Signals that indicate positive momentum or expansion potential, such as a critical product adoption threshold being crossed for the first time or a new product being activated.

-   **Team activity changes**

    Signals related to personnel changes, such as a CSM reassignment or a champion job change.

-   **Upcoming changes**

    Signals related to lifecycle transitions, such as an engagement stage change.

-   **Market changes**

    External signals gathered through web search, such as leadership changes, mergers and acquisitions, funding events, or competitive activity related to the account.


## Trigger types

The Executive Insight Generator uses two types of triggers to detect signals:

-   **Data-driven triggers**

    Triggered when a field changes or a threshold is crossed. When a trigger condition is met, an activity record is created and is used to generate the engagement brief. Activity records are created by one of the following:

    -   Business rules: Detect event-based conditions as they happen, such as a case being reassigned or a product being deactivated.
    -   Scheduled jobs: Run on a daily basis to evaluate conditions that require comparing values over time, such as a health score that has declined within the specified time period.
    -   Performance Analytics indicators: Track metric trends over time, such as product adoption scores or health score trajectories.
    The base system includes triggers that detect conditions such as low product usage, value realization at risk, and critical product adoption thresholds.

-   **Prompt-driven triggers**

    Triggered when external signals are detected through daily AI-powered web searches, such as leadership changes, mergers, or competitive activity.

    The base system includes triggers that detect changes such as executive leadership change, competitive threat detected, and strategic technology investment.


**Note:** You can also create custom triggers to capture additional signals that are relevant to your business. See [Configure a custom trigger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-exec-insight-custom-trigger.md) for details.

-   **[Refresh the engagement insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-exec-insight-refresh.md)**  
Request a new AI-generated brief for an engagement to reflect signals that occurred since the brief was last generated.
-   **[Configure a custom trigger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-exec-insight-custom-trigger.md)**  
Create a custom trigger to capture a business signal that is specific to your organization and include it in the AI-generated engagement brief.

**Parent Topic:**[Engagement home page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-view-engage.md)

**Related topics**  


[bundle-telmt.now-assist-tmt-exec-insight-gen]

[Configure a custom trigger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-exec-insight-custom-trigger.md)

