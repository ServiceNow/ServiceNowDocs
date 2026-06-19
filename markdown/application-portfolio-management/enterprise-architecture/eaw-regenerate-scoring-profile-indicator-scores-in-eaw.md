---
title: Regenerate scoring profile indicator scores on-demand in Enterprise Architecture Workspace
description: You can update the scoring profile indicator scores on-demand. Updating the scoring profile indicators scores is necessary when the scoring profile is updated with new indicators.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/enterprise-architecture/eaw-regenerate-scoring-profile-indicator-scores-in-eaw.html
release: australia
product: Enterprise Architecture
classification: enterprise-architecture
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure scoring profiles, Configure EA Workspace using the Setup page, Configuring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Regenerate scoring profile indicator scores on-demand in Enterprise Architecture Workspace

You can update the scoring profile indicator scores on-demand. Updating the scoring profile indicators scores is necessary when the scoring profile is updated with new indicators.

## Before you begin

Role required: sn\_apm.apm\_admin

## About this task

On-demand generation of the indicator scores is more efficient than running scheduled jobs, when immediate results for the updated data and conditions, if necessary.

## Procedure

1.  Navigate to **Workspace** &gt; **Enterprise Architecture Workspace**.

2.  Open the Setup page by selecting the Setup icon \[Omitted image "setup-icon.png"\] Alt text: Setup icon.

3.  Select the expand row icon \(\[Omitted image "ExpandIcon.png"\] Alt text: Expand Row icon.\) next to **Scoring Profiles**.

4.  Select **All**.

5.  Select the scoring profile that you want to generate the indicator score for.

6.  Select **Regenerate indicator score**.

    The **Regenerate scores** pop-up window appears.

7.  In the **Fiscal Period** box, enter the fiscal period that you want to generate the indicator score for.

    You can also select the lookup using list icon \[Omitted image "lookup-using-list-icon.png"\] Alt text: Lookup using list icon. to view the list of available fiscal periods.

8.  Select **OK**.

    This action doesn’t update the existing capability indicator scores but deletes them and generates new scores.


**Parent Topic:**[Configure scoring profiles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/enterprise-architecture/eaw-setup-scroring-prof.md)

