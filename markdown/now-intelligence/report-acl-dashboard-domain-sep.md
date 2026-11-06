---
title: Report assessment and domain separation
description: In domain separated instances, the ACL Assessment for Data Visualizations has certain limitations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/now-intelligence/report-acl-dashboard-domain-sep.html
release: australia
topic_type: concept
last_updated: "2026-10-22"
reading_time_minutes: 1
breadcrumb: [ACL Assessment for Data Visualizations, Configure, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Report assessment and domain separation

In domain separated instances, the ACL Assessment for Data Visualizations has certain limitations.

Configure the true/false property **sn\_report\_acl.run\_scan\_with\_queryNoDomain** to specify whether the assessment applies to the whole instance or to an individual domain.

This property is only valid on domain-separated instances. It defines whether the app considers the user domain when you run the query. If false, security\_admins gets results only for the domains they have visibility to.

A global security\_admin can set the property to true and view the results for all the domains on the instance. The individual security\_admins can then retrieve the collected results for their own domains. For more information, see [Filter report assessment scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/filter-report-assessment-scans.md).

The assessment runs as a normal query when this property is set to true on a single domain instance. If the property is deleted, the application treats the assessment as if the property were false.

**Important:** When you run the assessment as a global security\_admin, be sure to set the property back to false. If true, any security\_admin can query the entire instance. Other security\_admins don't see data that they don't have the right to view, but collected data is overwritten.

**Parent Topic:**[ACL Assessment for Data Visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/report-view-acl-dashboard.md)

