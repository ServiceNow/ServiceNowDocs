---
title: Use Proactive Code Check for the Impact Store Application
description: Developers can identify issues and prevent defects before they are deployed to production.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Proactive Code Check, Platform Health, Using Impact, Impact]
---

# Use Proactive Code Check for the Impact Store Application

Developers can identify issues and prevent defects before they are deployed to production.

## Before you begin

**Note:** Starting with Impact Zurich version 6.0.8 ServiceNow Store release, Proactive Code Check is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Developers execute Proactive Code Check \(PCC\) on update sets in development in non-production instances. PCC displays a list of identified findings for the update set related list with details such as type, severity, and location. Filters and sorting options for the findings are available, also the ability to directly open the individual finding record to resolve the issues found in the scan report.

**Note:** The code check parameters must be configured prior to running a scan.

Role required: admin

## Procedure

1.  In the non-production instance, navigate to **All** &gt; **System Update Sets** &gt; **Local Update Sets** &gt; **.**

    Verify that the page view is set to **Proactive Code Check**.

    The Customer Updates tab displays the pending development changes to be pushed to the production instance.

2.  Select the **Proactive Code Check** UI action to initiate the scan.

    A progress bar displays that also includes the total number of warnings, errors, and findings.

3.  Select **Go to Result/Refresh** the current update set form to view findings  in the related list.

    The Scan Findings are displayed in a table. You can review the system check for background information for a particular result or link externally to a KB article that explains resolution and configuration details.

4.  Address the issues that were reported during the scan to validate the changes resolved the issues.

5.  On the update set, select **Rescan** on the Scan Result page for an updated report.

    Repeat the scan and resolution process, as needed, before promoting the Update Set to the production instance.

    New findings are referenced to the specific Update Set from which they originated, including findings related to child update sets, allowing for easy navigation between findings and the update set in the user interface.


