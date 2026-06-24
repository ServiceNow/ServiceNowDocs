---
title: Smart prioritization
description: Smart prioritization uses a numeric priority score to automatically rank AI content, such as Employee Hub and AIUX Portal content types, for each content schedule.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/ec-smart-prioritization-content.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-05-29"
reading_time_minutes: 2
breadcrumb: [Content engagement, Setup employee communications, Configuring Employee Center Pro, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Smart prioritization

Smart prioritization uses a numeric priority score to automatically rank AI content, such as Employee Hub and AIUX Portal content types, for each content schedule.

## Overview of Smart prioritization

The Smart prioritization score governs the sequence in which content is presented to users. This score is generated, recorded, and administered exclusively by the system; content managers aren't responsible for assigning it manually.

## How Smart prioritization works

The score priority is based on the combination of the following factors:

**Note:** The content author sets this on the content record, choosing from four available options.

-   **Low** is the lowest priority boost
-   **Medium** is the default value for new content
-   **High** is the higher priority boost
-   **Critical** is the highest priority boost

**Note:** Because other configurable factors exist, a higher priority doesn't result in a higher score, though it typically does.

## Freshness

Freshness indicates current content availability. A content item attains maximum freshness on its publication date, with the score decreasing linearly to zero over a specified period \(default: 30 days\). Once this period has passed, freshness no longer contributes to the overall score. Consequently, newly published content receives a temporary ranking advantage that diminishes as time progresses.

## Order

The manual Order field within a content schedule determines ranking, with lower order values resulting in higher priority \(for example, content set to order = 1 will be ranked before content at order = 100\). This criterion is applicable only when the Order Override system property is deactivated.

|Factor|Default weight|
|------|--------------|
|Order|90|
|Priority|7|
|Freshness|3|

**Note:** By default, Order is still the biggest factor because it contributes to 90% of the score, but this is configurable. Per-content-type configuration \(sn\_cd\_prioritization\_config\). Property is readable by **sn\_cd.content\_manager** role and writable by **sn\_cd.content\_admin** role.

|Field|Default|Description|
|-----|-------|-----------|
|Order weight|90|How much the Order field influences the score.|
|Priority weight|7|How much the content Priority level influences the score.|
|Freshness weight|3|How much current content influences the score.|
|Freshness decay days|30|How many days until freshness fully decays to zero.|

**Note:** If no configuration record exists for a given content type, the system falls back to the defaults shown before. The **priority score** is updated automatically.

<table id="table_k1h_tw2_kjc"><thead><tr><th>

Change

</th><th>

Description

</th></tr></thead><tbody><tr><td>

A content item's Priority field changes

</td><td>

All schedules attached to that content is re-scored immediately.

</td></tr><tr><td>

A schedule's availability starts date changes

</td><td>

That schedule is re-scored immediately

 \(since freshness is based on start date\).

</td></tr><tr><td>

A schedule's Order field changes

</td><td>

A flow fires in the background and re-scores all impacted schedules.

</td></tr><tr><td>

Daily at 10:00 a.m.

</td><td>

Scheduled job recalculates scores for all currently live or soon-to-be-live schedules.

 This verifies freshness decay is reflected over time even when no one edits the content.

</td></tr></tbody>
</table>