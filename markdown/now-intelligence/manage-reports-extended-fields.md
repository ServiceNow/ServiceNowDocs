---
title: Manage visualizations with ACLs on extended fields
description: Add a system property to identify data visualizations and Core UI reports affected by report\_view ACLs on dot-walked fields.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/now-intelligence/manage-reports-extended-fields.html
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Manage report view ACL assessments, ACL Assessment for Data Visualizations, Configure, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Manage visualizations with ACLs on extended fields

Add a system property to identify data visualizations and Core UI reports affected by report\_view ACLs on dot-walked fields.

## Before you begin

Role required: admin and security\_admin.

## Procedure

1.  Create the system property **sn\_report\_acl.com.par\_report\_acl\_assessment.collect\_dotwalk** and set it to `true`.

    For more information on creating system properties, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_AddAPropertyUsingSysPropsList.md).

2.  [Perform the Report View Assessment scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/perform-report-view-acl-assessment-scan.md).


## Result

The Affected Data Visualizations list has a new column, **Dot walk fields**. This column is visible only when an affected report is identified based on an ACL on a field on an extended table.

**Parent Topic:**[Manage report view ACL assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/view-report-acl-remediation.md)

**Related topics**  


[Dot-walking from reference fields in a data visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/ext-table-fields-dot-walk-vis-des.md)

[Report on extended tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/reporting/t_AccessFieldExtendedTable.md)

