---
title: Configure the Employee Latest Performance Review report
description: Set up the report to enable the Look up Employee Latest Performance Review action to fetch the latest performance review report.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/configure-employee-latest-performance-review-report.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Configure the Employee Latest Performance Review report

Set up the report to enable the Look up Employee Latest Performance Review action to fetch the latest performance review report.

## Before you begin

Role required: Confirm that you have the access to create the reports.

Confirm that you have the access to the Workers by Organization report data source.

Create all calculated fields for this report before developing the report.

Confirm that the report name, field names, and column headings match exactly as they appear in the report document.

Confirm that you have added parentheses to the filters.

Confirm that reports are owned by the ISU user, which will be used to access these actions on the ServiceNow platform.

Confirm that you have enabled the **Enable as webservice** option.

## Procedure

1.  Create all calculated fields so that these fields can be used while developing report.

    1.  Create True False condition type calculated field named CF\_review\_period.

        \[Omitted image "workday-report1.png"\] Alt text: True/False condition.

    2.  Create Extract multi instance calculated field named CF\_latest\_review.

        \[Omitted image "workday-report2.png"\] Alt text: Workday HR report.

    3.  Create Aggregate Related Instances Calculated Field named CF\_Competencies.

        \[Omitted image "workday-report3.png"\] Alt text: Workday report.

    4.  Create Aggregate Related Instances Calculated Field named CF Content Evaluation – Accomplishments.

        \[Omitted image "workday-report4.png"\] Alt text: Workday report.

    5.  Create Aggregate Related Instances Calculated Field named CF\_Content Evaluation - Areas for Development.

        \[Omitted image "workday-report5.png"\] Alt text: Workday report.

    6.  Create Aggregate Related Instances Calculated Field named CF\_Content Evaluation - Career Interests.

        \[Omitted image "workday-report6.png"\] Alt text: Workday report.

    7.  Create Aggregate Related Instances Calculated Field named CF\_Content Evaluation - Goals.

        \[Omitted image "workday-report7.png"\] Alt text: Workday report.

    8.  Create Aggregate Related Instances Calculated Field named CF\_Content Evaluation - Responsibilities.

        \[Omitted image "workday8.png"\] Alt text: Workday report.

    9.  Create Extract Multi Instances Calculated Field named CF\_latest\_review.

        \[Omitted image "workday-report9.png"\] Alt text: CF\_latest\_review.

    10. Create True False Condition Calculated Field named CF\_evaluated by manager.

        \[Omitted image "workday-report10.png"\] Alt text: Workday report.

2.  Create the report.

    1.  Access the Create Custom Report task.

    2.  Provide a report name.

        An example of report name: CR Employee latest performance review and feedback details.

    3.  Select report type as Advanced.

    4.  Deselect the Optimized for performance box.

    5.  Select Data Source as Workers by Organization.

    6.  Deselect temporary report box and then Click **OK**.

        \[Omitted image "workday-report11.png"\] Alt text: Workday report.

    7.  Select the report business object and report fields as given below.

        \[Omitted image "workday-report12.png"\] Alt text: Workday report.

    8.  In the Group column heading section, select all business object as below.

        Group Column heading for each business object will be blank.

        \[Omitted image "workday-13.png"\] Alt text: Workday report.

    9.  In the Filter section, select the value as given below.

        Confirm that you have added parenthesis as given in below image.

        \[Omitted image "workday-report14.png"\] Alt text: Workday report.

    10. In the Sort section, under the Sub level sort, select the value as shown in the image.

        \[Omitted image "workday-report15.png"\] Alt text: Workday report.

        \[Omitted image "workday-report16.png"\] Alt text: Workday report.

    11. In Filter section, select the value as given below.

        Confirm that you have added parenthesis as given in below image.

        \[Omitted image "workday-report17.png"\] Alt text: Workday report.

    12. In the Sub-Filter section, select the value as given below.

        Confirm that you have added parenthesis as given in below image.

        \[Omitted image "workday-report18.png"\] Alt text: Workday report.

        \[Omitted image "workday-report19.png"\] Alt text: Workday report.

        \[Omitted image "workday-report20.png"\] Alt text: Workday report.

    13. In prompt section, click on the populate undefined prompt defaults check box.

        \[Omitted image "workday-report21.png"\] Alt text: Workday report.

    14. Select the value of prompts as given below under Prompt default section.

        Confirm that the Label For Prompt XML Alias of all prompt fields is the same as given in the image below.

        \[Omitted image "workday-report22.png"\] Alt text: Workday report.

    15. In the advanced section, select the **enable as webservice** and then click OK.

    16. Click on three dots icon and navigate to **web services&gt; view URLs**.

        \[Omitted image "workday-report23.png"\] Alt text: Workday report.

    17. Select the Organization for which you want to run this report and check the box if you want to include subordinate organization and manager and select the date range for which you want to see the data.

        \[Omitted image "workday-report24.png"\] Alt text: Workday report.

    18. In the View URLs Web Service page, click on marked icon under CSV section.

        A new browser tab opens.

        \[Omitted image "workday-report25.png"\] Alt text: Workday report.

    19. View the RaaS URL of the report in new browser tab and can get the below details from this link.

        \[Omitted image "workday-report26.png"\] Alt text: Workday report.


