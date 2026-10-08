---
title: Export to PowerPoint release notes
description: The ServiceNow Export to PowerPoint for Strategic Portfolio Management add-in generates and downloads project status reports from your instance as a Microsoft PowerPoint file for sharing with stakeholders and teams. See the following sections for release notes by version.Dynamic timeline type selection for exported roadmaps, replacing a hardcoded value with range-based logic that selects months, quarters, or years based on the resolved export range.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/export-to-ppt-rn.html
release: brazil
topic_type: topic
last_updated: "2026-10-06"
reading_time_minutes: 1
keywords: [Export to PowerPoint, project status report, PowerPoint template, strategic portfolio management, Export to PowerPoint, roadmap export, timeline type, range-based logic]
breadcrumb: [Strategic Portfolio Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Export to PowerPoint release notes

The ServiceNow® Export to PowerPoint for Strategic Portfolio Management add-in generates and downloads project status reports from your instance as a Microsoft PowerPoint file for sharing with stakeholders and teams. See the following sections for release notes by version.

## About Export to PowerPoint

-   Generate and download project status reports as Microsoft PowerPoint files directly from your instance.
-   Create custom report templates using text, table, line chart, bar chart, and repeater data types.
-   Share status reports with stakeholders and teams to support collaboration and planning.
-   Use default templates for detailed project reviews or high-level executive summaries.

See [Export to PowerPoint for Strategic Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/export-ppt-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    The Export to PowerPoint for Strategic Portfolio Management application \(sn\_ppm\_ppt\_export\) is available on ServiceNow® Store. Install the application to activate it. The admin role is required.

-   **Additional requirements**

    Export to PowerPoint is unavailable for customers in FedRAMP, NSC DOD IL5, or Australia IRAP-Protected datacenters, self-hosted customers, or other restricted environments. Check for availability updates in future releases.


**Parent Topic:**[Strategic Portfolio Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/it-business-management-rn-landing.md)

## Version 2.5.0

Dynamic timeline type selection for exported roadmaps, replacing a hardcoded value with range-based logic that selects months, quarters, or years based on the resolved export range.

### What's changed

-   **Dynamic timeline type for roadmap exports**

    Get more granular roadmap exports with timeline types that now reflect the actual export range. Previously, the timeline type was hardcoded. The timeline type is now derived from the resolved export range length. Ranges of one year or less use months, ranges over one year up to two years use quarters, and ranges over two years use years.


