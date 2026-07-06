---
title: Configure the Worker's Historical Performance Review report
description: Configure the report to fetch Workers Historical performance review information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/configure-the-workers-historical-performance-review-report.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Configure the Worker's Historical Performance Review report

Configure the report to fetch Workers Historical performance review information.

## Before you begin

Role required: Confirm that you have the access to create reports.

Confirm that you have report data source “Workers by Organization” access.

Create all calculated fields for this report before developing the report.

Confirm that the report name, report field names or column heading override for the respective field \(if given in report doc\) are the same as it is in report document.

Confirm that the report field label is the same as in report.

Confirm that all reports are owned by the ISU user.

Confirm that in the advanced section, **Enable as webservice** is selected.

## Procedure

1.  Create the calculated fields.

    1.  Create Aggregate Related Instances Calculated Field named CF\_Competencies\_all.

        \[Omitted image "workday-report27.png"\] Alt text: Workday report.

    2.  Create Aggregate Related Instances Calculated Field named CF Content Evaluation - Accomplishments all.

        \[Omitted image "workday-report28.png"\] Alt text: Workday report.

    3.  Create Aggregate Related Instances Calculated Field CF\_Content Evaluation - Areas for Development all.

        \[Omitted image "workday-report29.png"\] Alt text: Workday report.

    4.  Create Aggregate Related Instances Calculated Field named CF\_Content Evaluation - Career Interests all.

        \[Omitted image "workday-report30.png"\] Alt text: Workday report.

    5.  Create Aggregate Related Instances Calculated Field named CF\_Content Evaluation - Goals all.

        \[Omitted image "workday-report31.png"\] Alt text: Workday report.

    6.  Create Aggregate Related Instances Calculated Field named CF\_Content Evaluation - Responsibilities all.

        \[Omitted image "workday-report32.png"\] Alt text: Workday report.

2.  Create the report.

    1.  Access the Create Custom Report task.

    2.  Enter a report name.

    3.  Select report type as Advanced.

    4.  Deselect the Optimized for performance option.

    5.  Select Data Source as Workers by Organization.

    6.  Deselect the temporary report box and then click ok.

        \[Omitted image "workday-report33.png"\] Alt text: Workday report.

    7.  Select the report business object and report fields.

        \[Omitted image "workday-report34.png"\] Alt text: Workday report.

        \[Omitted image "workday-report35.png"\] Alt text: Workday report.

        \[Omitted image "workday-report36.png"\] Alt text: Workday report.

    8.  In the Group column heading section, select all business object as given below.

        Group Column heading for each business object will be blank.

        \[Omitted image "workday-report37.png"\] Alt text: Workday report.

    9.  In the Sort section, select the value.

        \[Omitted image "workday-report38.png"\] Alt text: Workday report.

    10. In Sort section, under Sub level sort, select the value.

        \[Omitted image "workday-report39.png"\] Alt text: Workday report.

        \[Omitted image "workday-report40.png"\] Alt text: Workday report.

        \[Omitted image "workday-report41.png"\] Alt text: Workday report.

    11. In the Filter section, select the value as given below.

        Add parenthesis as given in the image.

        \[Omitted image "workday-report42.png"\] Alt text: Workday report.

    12. In Sub-Filter section, select the value.

        Add parenthesis as given in the image.

        \[Omitted image "workday-report43.png"\] Alt text: Workday report.

        \[Omitted image "workday-report44.png"\] Alt text: Workday report.

        \[Omitted image "workday-report45.png"\] Alt text: Workday report.

    13. In the prompt section, click on populate undefined prompt defaults check box.

        \[Omitted image "workday-report46.png"\] Alt text: Workday report.

    14. Select the value of prompts as given below under Prompt default section.

        Confirm that the Label For Prompt XML Alias of all prompt fields is the same as the image below.

        \[Omitted image "workday-report47.png"\] Alt text: Workday report.

    15. In the advanced section, select **enable as webservice**, and click OK.

    16. Select the three dots icon and go to **web services&gt; view URLs** option.

        \[Omitted image "workday-report48.png"\] Alt text: Workday report.

    17. Select the organization for which you want to run this report and check the box if you want to include subordinate organization and managers.

        \[Omitted image "workday-report49.png"\] Alt text: Workday report.

    18. In the View URLs Web Service page, click on marked icon under CSV section.

        A new browser tab opens.

        \[Omitted image "workday-report50.png"\] Alt text: Workday report.

        You can see the RaaS URL of the report in new browser tab.


