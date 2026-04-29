---
title: Configure Succession Pool report
description: Configure the Succession Pool report to fetch Succession pool data based on Succession pool and employee.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Configure Succession Pool report

Configure the Succession Pool report to fetch Succession pool data based on Succession pool and employee.

## Before you begin

Role required: Confirm that you have the access to create reports.

Confirm that you have report data source “All Succession Pools” access.

Create all calculated fields for this report before developing the report.

Confirm that the report name, report field names or column heading override for the respective field \(if given in report doc\) are the same as it is in report document.

Confirm that the report field label is the same as in report.

Confirm that all reports are owned by the ISU user.

Confirm that in the advanced section, **Enable as webservice** is selected.

## Procedure

1.  Create Aggregate Related Instances type calculated field named CF\_worker succession pool.

    ![Workday report.](../image/workday-report51.png)

2.  Create the report.

    1.  Access the Create Custom Report task.

    2.  Provide the report name.

    3.  Select the report type as Advanced.

    4.  Deselect the Optimized for performance option.

    5.  Select Data Source as All Succession Pools.

    6.  Deselect the temporary report box and then click ok.

        ![Workday report.](../image/workday-report52.png)

    7.  Select the report business object and report fields as given below.

        ![Workday report.](../image/workday-report53.png)

        ![Workday report.](../image/workday-report54.png)

    8.  In the Group column heading section, select all business object as shown below.

        The Group Column heading for each business object will be blank.

        ![Workday report.](../image/workday-report55.png)

    9.  In the Filter section, select the value, as given below.

        ![Workday report.](../image/workday-report56.png)

    10. In prompt section, select the highlighted effective date as prompt for effective as of date and then click on populate undefined prompt defaults check box.

        ![Workday report.](../image/workday-report58.png)

    11. Select the value of prompts as given below under Prompt default section.

        Make sure the Label For Prompt XML Alias of all prompt fields must be same as the image below.

        ![Workday report.](../image/workday-report59.png)

    12. In the advanced section, select **enable as webservice** and then click ok.

    13. Click on three dots icon and then go to **web services&gt; view URLs** option.

        ![Workday report.](../image/workday-report60.png)

    14. Select succession pool for which you want to run this report.

        If you want any specific worker from the succession pool, select worker otherwise leave it blank.

        ![Workday report.](../image/workday-report61.png)

    15. In the View URLs Web Service page, click on marked icon under CSV section.

        A new browser tab opens and you can see the RaaS URL of the report in new browser tab.

        ![Workday report.](../image/workday-report62.png)


