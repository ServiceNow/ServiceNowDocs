---
title: Use Template Scripts in your Report Templates
description: Create a script to include the related lists data, date operations, and any other data that aren’t directly dot-walkable.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create a Report Template, Configure Major Security Incident status reports, Manage MSIM status reports, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Use Template Scripts in your Report Templates

Create a script to include the related lists data, date operations, and any other data that aren’t directly dot-walkable.

## Before you begin

Role required: sn\_msi.workspace\_manager

## About this task

You can use this predefined template script in your report templates to include any related data after the report templates are configured and customized.

Construct a template script to display the related list data on the report template. If you want to utilize and populate any template script, then you must add the tag template script tag as: `${template_script:script name}`.

Example: `${template_script:msi_collab_cards}`

**Note:** You can’t delete the predefined template scripts. An error message is displayed if a user with an admin role attempts to delete a template script record if it’s mapped with any report template.

## Procedure

1.  Navigate to **Major Security Incident Management** &gt; **MSI Administration** &gt; **Status Report Setup**.

    The MSI Status Report Setup page displays.

2.  Drill down to **Report Template** &gt; **Template Scripts**.

3.  Select **Configure**.

    The following are the predefined Template Scripts as a part of the base system, which you can use to configure and modify your status reports.

    |Template Script name|Description|
    |--------------------|-----------|
    |**formatted\_current\_date**|Returns the current local date and time in the DDMMYYYY 00.00 AM or p.m. format. For example, 21 Jan 2021 3:51 p.m. PST.|
    |**msi\_active\_team**|Generate HTML for active team cards.|
    |**msi\_collab\_cards**|Generate HTML for collaboration activity cards.|
    |**msi\_task\_activities**|Generate HTML for task cards.|
    |**msi\_timeline\_events**|Generate HTML for timeline event cards.|
    |**si\_affected\_users**|Returns the affected users from the related list in a tabular form.|
    |**si\_assessments**|Returns the post incident assessment results in a tabular form.|
    |**si\_associated\_phish\_emails**|Returns the associated phishing emails from the related list in a tabular form.|
    |**si\_associated\_phish\_headers**|Returns the associated phishing headers from the related list in a tabular form.|
    |**si\_business\_criticality**|Returns color-coded business criticality value.|
    |**si\_malicious\_observables**|Returns the malicious observables from the related list in a tabular form.|
    |**si\_observables**|Returns the observables from the related list in a tabular form.|
    |**si\_priority**|Returns a color-coded priority value.|
    |**si\_response\_tasks**|Returns the response tasks from the related list in a tabular form.|
    |**si\_time\_to\_identify**|Returns the duration spent in the Draft and Analysis state.|
    |**si\_time\_to\_resolve**|Returns the time to resolve the incident.|

    **Note:** You can also create your own template script to include the related lists data, date operations, and any other data that aren’t directly dot-walkable, in addition to the listed template scripts.


**Parent Topic:**[Create a Report Template](create-report-template.md)

