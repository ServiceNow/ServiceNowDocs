---
title: Overview tab in AI Control Tower
description: Explore the overview tab in AI Control Tower and the widgets available on the tab.
locale: en-US
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [AI Control Tower Home, AI Control Tower dashboard, Exploring AI Control Tower, AI Control Tower, Enable AI experiences]
---

# Overview tab in AI Control Tower

Explore the overview tab in AI Control Tower and the widgets available on the tab.

## Overview dashboard

**Prerequisites**

Role required: AI steward \[sn\_ai\_governance.ai\_steward\]

The **Overview** tab of the AI Control Tower dashboard provides a comprehensive view of all metrics of AI systems.

![Overview tab that displays all the metric types for AI systems.](../image/aict-overview.png)

The following widgets are available, showing various metrics. You can view the data in detail on each widget.

-   **All AI systems**

    This section shows all the AI systems classified into four stages:

    -   New
    -   Assess
    -   Build and test
    -   Deploy
    For more information about the AI asset lifecycle stages, see [AI asset lifecycle](ai-asset-lifecycle.md)

-   **AI systems by type**

    This section shows all the AI systems categorized into

    -   Agentic AI
    -   Generative AI
    -   Classic AI
-   **Risk classification**

    This section shows the risk score of AI systems. The risks are qualitatively classified as

    -   High
    -   Low
    -   Medium
    -   Unacceptable
-   **AI systems by provider**

    This section shows the number of AI systems, categorized by the providers.

    **Note:** The AI system by provider donut chart doesn’t display the **Other** category when there are more than five providers, which can cause a mismatch between the number of metric labels and the items shown in the list when selecting a metric label.

-   **Compliance**

    This section shows the compliance effectiveness percentage of different statuses of active controls applied on **Authority documents** and **Policies**. You can drill down respective sectors of the bar graph to access and view the list of active controls.

-   **AI cases by priority**

    This section shows the total number of AI cases with breakdown analysis by priority rating. You can drill down to respective sectors of the donut chart to access and view a list of recorded AI cases.


