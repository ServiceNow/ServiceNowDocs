---
title: Configure ServiceNow Otto context menu
description: Activate the Dashboard Summary skills.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/configure-dashboard-summary.html
release: australia
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 1
keywords: [configure]
breadcrumb: [Dashboard Summary, ServiceNow Otto for Platform Analytics, Platform Analytics]
---

# Configure ServiceNow Otto context menu

Activate the Dashboard Summary skills.

The Dashboard Summary skill is a generative AI capability that automatically produces a concise, structured summary of a Platform Analytics experience dashboard. The summary is based only on data that is already visible to the user, using a Now Assist skill.

When triggered, the skill analyzes the dashboard's visual elements, such as tables, indicators, and charts, along with the active filters and time range, and generates:

-   Short summary of the dashboard's current state
-   What changed since the last analysis \(when applicable\)
-   A set of Key Highlights derived from the underlying data

AI Skills used:

-   **Dashboard Facts Generator**

    Extracts all observable facts from dashboard elements \(such as tables, indicators, and visualizations\) and identifies cross‑element relationships. This step focuses on comprehensive, data‑level fact extraction without interpretation or prioritization.

-   **Dashboard Highlights**

    Synthesizes the extracted facts and indicator insights into a small set of business‑significant highlights, along with a brief overall summary. This step prioritizes meaningful changes, large relative differences, patterns across elements, and notable anomalies.

-   **Change Summary**

    Compares the current analysis to a previous run to identify what has materially changed, focusing on direction and magnitude of change rather than restating the current state. This summary applies if the dashboard was previously analyzed with the same configuration, and changes in the data are detected.


