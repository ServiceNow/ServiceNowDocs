---
title: The report\_view ACLs list
description: View the entire list of report\_view ACLs and their associated roles to have a higher-level view of the access control on your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/now-intelligence/view-report-acls-list.html
release: australia
topic_type: concept
last_updated: "2026-10-22"
reading_time_minutes: 1
breadcrumb: [ACL Assessment for Data Visualizations, Configure, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# The report\_view ACLs list

View the entire list of report\_view ACLs and their associated roles to have a higher-level view of the access control on your instance.

Each instance has a different number of report\_view ACLs. The number depends on the plugins activated on the instance.

To view a list of report\_view ACLs, navigate to **All** &gt; **Platform Analytics Administration** &gt; **ACL Assessment for Data Visualizations** &gt; **Report View ACLs List**. What you see is a list of Access Role \[sys\_security\_acl\_role\] records filtered on ACL Operation Name = report\_view.

## Report\_view ACLs list columns

ACLs apply to only one role at a time. There can be multiple instances of an ACL if there are multiple roles that it applies to. For example, the same ACL grants greater access to an admin than to an itil user.

The following table shows all available columns. The only ones shown by default are ACL, Role, and Created.

|Column|Description|
|------|-----------|
|ACL|The name of the report\_view ACL.|
|Active|Indicates whether the ACL is active. True/False.|
|Application|The application the ACL applies to.|
|Package|The plugin associated with the ACL.|
|Description|What the ACL prevents or allows for the associated role.|
|Role|The name of the role the ACL applies to.|
|Description|Description of the role.|

**Parent Topic:**[ACL Assessment for Data Visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/report-view-acl-dashboard.md)

