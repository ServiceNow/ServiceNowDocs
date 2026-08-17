---
title: Configuring RIDAC in Strategic Planning Workspace
description: Run the scheduled job to populate the planning item field on RIDAC records that were created before the Strategic Planning was installed. This job ensures legacy RIDAC records appear correctly in related lists and reports.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/strategic-planning/configure-ridac-spw.html
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: concept
last_updated: "2026-07-29"
reading_time_minutes: 1
keywords: [configure]
breadcrumb: [RIDAC, Strategic Planning, Strategic Portfolio Management]
---

# Configuring RIDAC in Strategic Planning Workspace

Run the scheduled job to populate the planning item field on RIDAC records that were created before the Strategic Planning was installed. This job ensures legacy RIDAC records appear correctly in related lists and reports.

## Configuration overview

The primary administrative task for RIDAC in Strategic Planning Workspace is to populate planning items on the existing RIDAC records. This ensures that all RIDAC items created in your system are properly linked to their associated planning items and appear correctly in the RIDAC home page, filter views, and integration points. For step-by-step instructions, see [Populate planning items on RIDAC records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/update-ridac-planning-items-spw.md).

## RIDAC configuration benefits

Populating planning items on RIDAC records provides the following benefits:

-   **Complete RIDAC visibility:** RIDAC items appear correctly in the RIDAC home page and all filter views \(All RIDAC, Project RIDAC, Portfolio RIDAC, Program RIDAC\).
-   **Proper planning item linkage:** All RIDAC records are linked to their associated planning items \(projects, demands, goals, iterations\), ensuring data integrity across the system.
-   **Accurate reporting and analysis:** Planning item information is populated on RIDAC records, enabling accurate filtering, sorting, and analysis across portfolio, program, and project hierarchies.
-   **Seamless integration:** When integration is enabled, RIDAC items created on planning items automatically appear on execution tasks, and vice versa, maintaining bidirectional synchronization.
-   **Legacy record support:** Legacy RIDAC records are properly integrated into the new RIDAC structure so they appear consistently across all views.

