---
title: Configure the holiday calendar report
description: Configure the holiday calendar report to use the action.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-12-28"
reading_time_minutes: 1
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Configure the holiday calendar report

Configure the holiday calendar report to use the action.

## Before you begin

Role required: none

Confirm that

-   The user has access to custom report creation.
-   The user has access to All Workers data source access.

## Procedure

1.  Access the Create Custom Report task.

2.  Provide the name of the report.

    Example of a name: CRPT\_holiday\_calendar.

3.  Select the report type as **Advanced**.

4.  Deselect **Optimized for performance** field.

5.  Select the Data Source as **All Workers**.

6.  Confirm that the temporary report option is deselected.

7.  Select **OK**.

8.  Provide the values in report as given in the image.

    ![Holiday calendar report.](../image/holiday-calendar-report1.png)

9.  Provide the values in the **Group Column Headings** section, as shown in the image.

    ![Holiday calendar report.](../image/holiday-calendar-report2.png)

10. Provide the values in the **filter** section.

    ![Holiday calendar report.](../image/holiday-calendar-report3.png)

11. In the prompt section, select Populate Undefined Prompt Defaults and confirm that the prompts are configured as shown in the image below.

    All prompts are populated.

    ![Holiday calendar report.](../image/holiday-calendar-report4.png)

12. In the advanced section, select **enable as webservice**, and select **OK**.

13. Select the three dots icon \(![Three-dots icon.](../image/three-dots-icon.png)\) and navigate to **Web Service****&gt;** **View URLs**.

    ![Holiday calendar report.](../image/holiday-calendar-report5.png)

14. Enter an employee id in the Employee ID box, and select **OK**. 

    ![Holiday calendar report.](../image/holiday-calendar-report6.png)

15. In  the View URLs Web Service page, select the marked icon under  CSV section. It will open a new browser tab. 

    The details are shown in a new browser tab.

    ![Holiday calendar report.](../image/holiday-calendar-report7.png)

16. View the RaaS  URL of the report in new browser tab.

    ![Holiday Calendar report.](../image/holiday-calendar-report8.png)

    URL details:

    -   https://wd2-impl-services1.workday.com  represents  the  Base URL of customer’s workday tenant. 
    -   Tenant\_Name  represents the  customer’s workday tenant. 
    -   Report\_Owner\_user\_name  represents  the user name of the report’s owner. 
    -   CRPT\_holiday\_calendar represents report name alias.

