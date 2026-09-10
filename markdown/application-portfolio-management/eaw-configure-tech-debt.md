---
title: Configure technical debt settings
description: Configure whether the server is part of a technical debt record's identity and select which reasons the scheduled job uses to create technical debt.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-configure-tech-debt.html
release: australia
topic_type: task
last_updated: "2026-08-24"
reading_time_minutes: 2
breadcrumb: [Technical debt settings, Configure EA Workspace using the Setup page, Configuring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Configure technical debt settings

Configure whether the server is part of a technical debt record's identity and select which reasons the scheduled job uses to create technical debt.

## Before you begin

The Technical debt settings page requires Technology Portfolio Management plugin \(sn\_apm\_tpm\) version 1.12.1 or later. If this version isn't installed, contact your system administrator to update the plugin.

Role required: sn\_apm.apm\_admin

## About this task

\[Omitted image "trm-tech-debt-settings.png"\] Alt text: Technical debt settings page in the EA Workspace Setup page.

Use the technical debt settings to control how the scheduled job **Populate TRM technical debts in the EA Workspace** identifies and creates technical debt records.

## Procedure

1.  Navigate to **Workspace** &gt; **Enterprise Architecture Workspace**.

2.  Open the Setup page by selecting the Setup icon \[Omitted image "setup-icon.png"\] Alt text:.

3.  Select **Technical debt**, and then select **Settings**.

4.  Under **Create technical debt records**, select an option.

    -   **One technical debt record per server**: Creates a separate technical debt record for each server on which the software runs. This is the default option.
    -   **One technical debt record for all identified servers**: Creates a single technical debt record for the software, regardless of how many servers it runs on. The record doesn't show an installed-on server value.
    **Note:**

    Regardless of which option you select, you can view all the servers a software product is installed on from the **Discovered Technology** related list on the technical debt record.

5.  Select **Save**.

    **Note:**

    If technical debt records already exist, you must delete all of them before you can change this option. Contact your system administrator to run a background script that deletes the existing records.

6.  Under **Create technical debt when any of these conditions are met**, select or clear the check boxes for the reasons you want the job to use.

    -   When the software is not defined in the TRM
    -   When the software is not approved for production
    -   When the software version is not defined in the TRM Product Lifecycle
    -   When the software version is not approved for production
    **Note:**

    At least one reason must be selected. If you clear all the check boxes, an error message appears and the setting isn't saved.

7.  Select **Save**.

    A confirmation message appears. Any active technical debt records whose reason you cleared move to the **Archived** state on the next run of the scheduled job.


## Result

The scheduled job **Populate TRM technical debts in the EA Workspace** uses the updated server and reason configuration starting with its next run. You don't need to restart the instance or re-register the job.

**Parent Topic:**[Technical debt settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-setup-tech-debt.md)

**Related topics**  


[Technical debt settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-setup-tech-debt.md)

[TRM technical debt states and transitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-trm-technical-debt-states.md)

[Update TRM technical debt data using scheduled job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-run-job-trm-tech-debts.md)

[Technical debt calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-trm-technical-debt-calc.md)

