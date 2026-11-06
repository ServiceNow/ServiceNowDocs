---
title: Add report\_view ACL blocked user to authorized group
description: From a report view ACL assessment, you can add an affected user to a group that has a required role. The user can then view the data visualization or Core UI report.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/now-intelligence/add-report-view-blocked-user-group.html
release: australia
topic_type: task
last_updated: "2026-10-22"
reading_time_minutes: 2
breadcrumb: [Manage report view ACL assessments, ACL Assessment for Data Visualizations, Configure, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Add report\_view ACL blocked user to authorized group

From a report view ACL assessment, you can add an affected user to a group that has a required role. The user can then view the data visualization or Core UI report.

## Before you begin

As the result of a report view ACL assessment, you see that a user who should be able to view a visualization cannot. Of the various remedies you could apply, you decide that the best one is to add the user to an authorized group.

Before you begin, see [Perform the Report View Assessment scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/perform-report-view-acl-assessment-scan.md) and [Manage report view ACL assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/view-report-acl-remediation.md).

Role required: admin with elevation to security\_admin

## Procedure

1.  Open a report view ACL assessment record and select **Show affected users**, as described in [Manage report view ACL assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/view-report-acl-remediation.md).

2.  Choose one or more affected users.

    Choose the users by ticking the box at the beginning of their rows.

3.  Select `Assign to group` from the list **Actions on selected rows**.

    \[Omitted image "rep-acl-report-options-3-pol.png"\] Alt text: Report view ACL affected users

4.  Choose a group and a role \(if available\) to add the selected users to and select **Submit**.

    Move any users that you don't want to add to the same group into the **Available** column.

    \[Omitted image "rep-acl-add-users-to-group.png"\] Alt text: Report view ACL affected users

5.  If no groups have at least one role in a relevant ACL rule, select an appropriate group and add one of the roles.

    If no groups are appropriate for the users, create a group and assign one of the required roles to it outside of the application. Then within the application, grant access to the selected blocked users. For more information on creating groups, see [Create a user group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateAGroup.md).

6.  Select **Submit**.


**Parent Topic:**[Manage report view ACL assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/view-report-acl-remediation.md)

