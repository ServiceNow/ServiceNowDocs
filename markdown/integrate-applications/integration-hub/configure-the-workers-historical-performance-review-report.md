---
title: Configure the Worker's Historical Performance Review report
description: Configure the report to fetch Workers Historical performance review information.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-02-28"
reading_time_minutes: 2
breadcrumb: [Workday HR Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
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

        ![Workday report.](../image/workday-report27.png)

    2.  Create Aggregate Related Instances Calculated Field named CF Content Evaluation - Accomplishments all.

        ![Workday report.](../image/workday-report28.png)

    3.  Create Aggregate Related Instances Calculated Field CF\_Content Evaluation - Areas for Development all.

        ![Workday report.](../image/workday-report29.png)

    4.  Create Aggregate Related Instances Calculated Field named CF\_Content Evaluation - Career Interests all.

        ![Workday report.](../image/workday-report30.png)

    5.  Create Aggregate Related Instances Calculated Field named CF\_Content Evaluation - Goals all.

        ![Workday report.](../image/workday-report31.png)

    6.  Create Aggregate Related Instances Calculated Field named CF\_Content Evaluation - Responsibilities all.

        ![Workday report.](../image/workday-report32.png)

2.  Create the report.

    1.  Access the Create Custom Report task.

    2.  Enter a report name.

    3.  Select report type as Advanced.

    4.  Deselect the Optimized for performance option.

    5.  Select Data Source as Workers by Organization.

    6.  Deselect the temporary report box and then click ok.

        ![Workday report.](../image/workday-report33.png)

    7.  Select the report business object and report fields.

        ![Workday report.](../image/workday-report34.png)

        ![Workday report.](../image/workday-report35.png)

        ![Workday report.](../image/workday-report36.png)

    8.  In the Group column heading section, select all business object as given below.

        Group Column heading for each business object will be blank.

        ![Workday report.](../image/workday-report37.png)

    9.  In the Sort section, select the value.

        ![Workday report.](../image/workday-report38.png)

    10. In Sort section, under Sub level sort, select the value.

        ![Workday report.](../image/workday-report39.png)

        ![Workday report.](../image/workday-report40.png)

        ![Workday report.](../image/workday-report41.png)

    11. In the Filter section, select the value as given below.

        Add parenthesis as given in the image.

        ![Workday report.](../image/workday-report42.png)

    12. In Sub-Filter section, select the value.

        Add parenthesis as given in the image.

        ![Workday report.](../image/workday-report43.png)

        ![Workday report.](../image/workday-report44.png)

        ![Workday report.](../image/workday-report45.png)

    13. In the prompt section, click on populate undefined prompt defaults check box.

        ![Workday report.](../image/workday-report46.png)

    14. Select the value of prompts as given below under Prompt default section.

        Confirm that the Label For Prompt XML Alias of all prompt fields is the same as the image below.

        ![Workday report.](../image/workday-report47.png)

    15. In the advanced section, select **enable as webservice**, and click OK.

    16. Select the three dots icon and go to **web services&gt; view URLs** option.

        ![Workday report.](../image/workday-report48.png)

    17. Select the organization for which you want to run this report and check the box if you want to include subordinate organization and managers.

        ![Workday report.](../image/workday-report49.png)

    18. In the View URLs Web Service page, click on marked icon under CSV section.

        A new browser tab opens.

        ![Workday report.](../image/workday-report50.png)

        You can see the RaaS URL of the report in new browser tab.


