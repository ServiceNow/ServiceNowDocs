---
title: Archive data query examples
description: Query examples demonstrate how to combine live and archive data for IT operations reporting, customer service case history, and HR compliance audits.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/archive-data-query-examples.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [archive data, SQL query, UNION ALL, incident reporting, case history]
breadcrumb: [Live Archive, Explore, RaptorDB Professional, Extend ServiceNow AI Platform capabilities]
---

# Archive data query examples

Query examples demonstrate how to combine live and archive data for IT operations reporting, customer service case history, and HR compliance audits.

## IT operations: incident volume and MTTR

Report on incident volume and MTTR \(mean time to resolve\) over a rolling three-year period, broken down by priority and assignment group.

```
SELECT
    date_trunc('month', opened_at) AS month,
    priority,
    DV(assignment_group) AS group_name,
    COUNT(*) AS incident_count,
    AVG(
        CASE WHEN closed_at IS NOT NULL
        THEN CAST(
            (CAST(closed_at AS FLOAT) - CAST(opened_at AS FLOAT)) * 1440
            AS FLOAT)
        END
    ) AS avg_mttr_minutes
FROM (
    SELECT opened_at, closed_at, priority, assignment_group
    FROM incident
    WHERE opened_at >= date_trunc('month',
        CAST(NOW() AS DATE) - INTERVAL '36 months')
    UNION ALL
    SELECT opened_at, closed_at, priority, assignment_group
    FROM ar_incident
    WHERE opened_at >= date_trunc('month',
        CAST(NOW() AS DATE) - INTERVAL '36 months')
) AS three_year_history
GROUP BY month, priority, DV(assignment_group)
ORDER BY month DESC, priority ASC;
```

## Customer service: full case history for an account

Return all cases for a specific account over five years, regardless of whether they are still active or have been archived.

```
SELECT
    number,
    short_description,
    priority,
    state,
    opened_at,
    closed_at,
    resolved_by,
    'live' AS source
FROM sn_customerservice_case
WHERE account = 'Acme Corporation'
  AND opened_at >= '2020-01-01'

UNION ALL

SELECT
    number,
    short_description,
    priority,
    state,
    opened_at,
    closed_at,
    resolved_by,
    'archive' AS source
FROM ar_sn_customerservice_case
WHERE account = 'Acme Corporation'
  AND opened_at >= '2020-01-01'

ORDER BY opened_at ASC;
```

## HR and compliance: employee request history

Return all service requests associated with a specific employee across their full tenure. Because archive tables store resolved display values, filter directly on the display name without resolving a `sys_id`.

```
SELECT
    number,
    short_description,
    category,
    opened_at,
    closed_at,
    state,
    requested_for,
    'live' AS source
FROM sc_request
WHERE requested_for = 'Jane Smith'
   OR opened_by = 'Jane Smith'

UNION ALL

SELECT
    number,
    short_description,
    category,
    opened_at,
    closed_at,
    state,
    requested_for,
    'archive' AS source
FROM ar_sc_request
WHERE requested_for = 'Jane Smith'
   OR opened_by = 'Jane Smith'

ORDER BY opened_at ASC;
```

