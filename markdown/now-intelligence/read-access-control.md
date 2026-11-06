---
title: Fallback ACL evaluation
description: When a data visualization is run, report\_view access control lists \(ACLs\) are evaluated on the table and table fields that the report is based on. If no report\_view ACL exists, there is a fallback check on table-level read ACL roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/now-intelligence/read-access-control.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Report\_view access control, Configure, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Fallback ACL evaluation

When a data visualization is run, report\_view access control lists \(ACLs\) are evaluated on the table and table fields that the report is based on. If no report\_view ACL exists, there is a fallback check on table-level read ACL roles.

If no report\_view ACL for a table or table field exists, evaluation is conducted against the read ACL. Users can only view the visualization if they pass the read ACL.

**Note:** Before Zurich, it was possible to change the fallback read ACL behavior through the system property **glide.report.report\_view.read\_acl**. This change is no longer possible. Read ACLs are always enforced in the absence of a report\_view ACL.

As with report\_view rules, the fallback table-level read ACL check applies only roles and security attribute conditions. No other conditions are evaluated.

**Important:** Read ACLs only apply to read operations. Therefore, they do not affect access to the contents of visualizations that only show an aggregate, such as single-score visualizations. This limitation led to the development of report\_view ACLs.

**Parent Topic:**[Report\_view access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/report-view-access-control.md)

