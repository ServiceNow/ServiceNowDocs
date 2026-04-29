---
title: Delete a Certification template
description: Certification templates can be deleted.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Certification templates, CMDB Compliance, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Delete a Certification template

Certification templates can be deleted.

## About this task

Only users with the certification\_admin or admin role can delete template versions. You cannot delete a template version that is being used for an audit.

## Procedure

1.  To delete a single template version, open that version record and click **Delete**.

    The system hides the **Delete** button for templates that are in use. If you delete the latest, active version of a template, the previous version of that template is reset to Active.

2.  To delete all unused and inactive versions of a template, open any version of that template and click **Delete inactive versions** under **Related Links**.

    This control appears on all versions, whether they are used in an audit.

3.  When prompted, click **OK** to proceed.

    The system deletes only template versions that are not used in an audit. All protected versions are named in a message that appears in the header bar.


