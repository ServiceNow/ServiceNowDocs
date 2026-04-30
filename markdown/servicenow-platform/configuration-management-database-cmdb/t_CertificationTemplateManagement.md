---
title: Manage Certification template versions
description: You can view and manage all versions of a template from the Template form.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Certification templates, CMDB Compliance, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Manage Certification template versions

You can view and manage all versions of a template from the Template form.

## Procedure

1.  Open any version of a template.

    The **Other Versions** related list displays all other versions of this template, both active and inactive.

2.  Click any version in the related list to display the record for that version.

3.  Update the template to create a new version.

    The system increments a version of the template when you edit any field except **Description** and **Active**. You can manage the template versions without returning to the list view.

4.  To make an inactive template the current version, open that version, edit it if desired, and then click **Revert**.

    This action does:

    -   Deactivates the previously active version of the template.
    -   Copies the inactive template.
    -   Makes the new copy the current, active version.
5.  Select the **Audits** related list to view all audits configured to use this template.

6.  Click **New** to create a new audit record with the template selection and table pre-populated.


