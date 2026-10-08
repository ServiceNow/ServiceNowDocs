---
title: Configuring pages in AI Control Tower
description: View and govern your AI portfolio using terms and visualizations tailored to your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-configuring-page-widgets.html
release: brazil
topic_type: concept
last_updated: "2026-09-21"
reading_time_minutes: 3
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Configuring pages in AI Control Tower

View and govern your AI portfolio using terms and visualizations tailored to your organization.

## Key benefits

-   Present AI Control Tower charts and details in your organization's own terms instead of the default labels.
-   Provide data for a specific business unit or reporting period by building a condition into a card.
-   Direct users from a card to a different list, report, or page instead of the default destination.

AI Control Tower pages ship with a default set of cards, titles, and visualizations that you can configure as needed.

\[Omitted image "aict-edit-home-page.png"\] Alt text: AI Control Tower Home page with editable cards.

Every configurable card exposes a set of presentation settings, which let you match a page to the vocabulary and reporting style your organization already uses. For example, you can update a card title and subtitle, the chart type, its data labels and legends, and the number of rows and sort direction in a ranked list. The exact settings available depend on the card.

Cards that read directly from tables on your instance also provide a condition builder, so you can narrow a card to the subset of records a page is meant to report on. Cards that retrieve their data from an API provide presentation settings only.

## Required roles

The workspace administrator \[sn\_ai\_governance.workspace\_admin\] role is required to edit cards on AI Control Tower pages.

## How configurations are saved and applied

Card configurations apply to all AI Control Tower users. Every user sees a saved configuration the next time the page loads.

Configurations are stored as metadata that layers over the default card, rather than as a copy of the card. When editing a card, an unset or cleared value uses the original behavior.

**Note:** Hiding information in a card changes only what the page presents. It doesn't restrict access to the underlying records, which remain governed by the access controls on your instance.

## Configurations and application upgrades

Configurations remain in place through an application upgrade. When AI Control Tower is upgraded, saved configurations for cards that still exist are reapplied automatically, and the pages continue to show the configured titles, conditions, and display options.

Cards introduced by a new version appear with their shipped settings, which an administrator can then configure.

## Important considerations

-   Configurations aren't scoped to a domain. Separate domains on a domain-separated instance can't have different versions of the same page.
-   Card titles and labels that an administrator enters are stored as typed and aren't translated.
-   Configuration is available on all pages and tabs except Activity Center, the Inventory list views, the Policies tab, and Settings.
-   If the available settings don't cover a change your organization needs, you can extend pages with pro-code tools. For more information, see [Creating or extending pages with pro-code tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-create-extend-pages-pro-code-tools.md).

## Use cases

-   **Matching card titles to internal terminology**

    An organization refers to its onboarded AI systems as registered assets rather than inventory. A workspace administrator changes the title of the inventory card on the Home page to Registered AI assets, so the page uses the same term that appears in the organization's internal governance process. Every user who opens the Home page sees the new title.

-   **Preparing a page for a leadership review**

    A governance team presents AI system scores in a monthly leadership review, where a list of five systems is more detail than the meeting needs. A workspace administrator reduces the ranked list on the Monitor page to the two lowest-scoring systems and sets the sort direction to show the largest score declines first, so the page opens on the systems that need attention.

-   **Narrowing a card to a reporting period**

    An organization reports on the AI systems it onboarded during the current fiscal year, but the inventory card counts every system on the instance. Because the card reads directly from a table, a workspace administrator adds a condition that limits it to systems created in the last year. The card count and the page it navigates to both reflect the condition.


-   **[Configure a page card in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-configure-widget.md)**  
Change how a card presents its data so that a page matches the terminology, level of detail, and reporting focus your organization works with.

**Parent Topic:**[Configuring AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-configuring.md)

**Related topics**  


[Configure a page card in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-configure-widget.md)

