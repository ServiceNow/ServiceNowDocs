---
title: Configure work schedule calendar report
description: Configure the report to use the Look up Schedule Calendars Reference WID Of An Employee action.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-12-29"
reading_time_minutes: 1
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Configure work schedule calendar report

Configure the report to use the Look up Schedule Calendars Reference WID Of An Employee action.

## Before you begin

Role required: none

Confirm that the user has access to custom report creation and report data source access.

## Procedure

1.  Access the **Create Custom Report** task.

2.  Provide a report name.

    Report name example: SNIH\_Work\_schedule\_calendar.

3.  Select the report type as **Advanced**.

4.  Deselect the **Optimized for performance** field.

5.  Select the data source as **All Workers**.

6.  Select **OK**.

    Confirm that you have deselected the **Uncheck** field.

    ![Work schedule calendar.](../image/work-schedule-calendar-report1.png)

7.  Provide the values in report as given in the image.

    ![Work schedule calendar.](../image/work-schedule-calendar-report2.png)

8.  Provide the values under the Group column heading section.

    Confirm that the Group Column heading for each business object is empty.

    ![Work schedule calendar report.](../image/work-schedule-calendar-report3.png)

9.  In the Filter section, provide the values, as shown in the image.

    ![Work schedule calendar report.](../image/work-schedule-calendar-report4.png)

10. In the prompt section, select **Populate Undefined Prompt defaults**.

    ![Work schedule prompt.](../image/work-schedule-calendar-report5.png)

    All prompts are populated.

11. Confirm that the prompts are configured, as shown in the image.

    ![Work schedule calendar report.](../image/work-schedule-calendar-report6.png)

12. In the advanced section, select **enable as webservice**.

13. Select **OK**, and then **Done**.

14. Select the three dots icon \(![Three-dots icon.](../image/three-dots-icon.png)\) and navigate to **Web Service****&gt;** **View URLs**.

    ![Work schedule calendar report.](../image/work-schedule-calendar-report7.png)

15. Provide an employee id in **Employee ID** box, and select **OK**. 

    ![Work schedule calendar report.](../image/work-schedule-calendar-report8.png)

16. In  the **View URLs Web Service** page, select the marked icon under the  CSV  section.

    ![Work schedule calendar report.](../image/work-schedule-calendar-report9.png)

    A new browser tab opens.

17. View the  RaaS  URL  of the report in new browser tab.

    ![RaaS URL.](../image/work-schedule-calendar-report10.png)

    URL details:

    -   https://wd2-impl-services1.workday.com  represents  the  Base URL of customer’s workday tenant. 
    -   Tenant\_Name  represents  customer’s workday tenant. 
    -   Report\_Owner\_user\_name represents user name of the report’s owner. 
    -   SNIH\_Work\_schedule\_calendar represents the report name alias.

