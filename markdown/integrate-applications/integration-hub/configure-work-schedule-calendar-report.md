---
title: Configure work schedule calendar report
description: Configure the report to use the Look up Schedule Calendars Reference WID Of An Employee action.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/configure-work-schedule-calendar-report.html
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

    \[Omitted image "work-schedule-calendar-report1.png"\] Alt text: Work schedule calendar.

7.  Provide the values in report as given in the image.

    \[Omitted image "work-schedule-calendar-report2.png"\] Alt text: Work schedule calendar.

8.  Provide the values under the Group column heading section.

    Confirm that the Group Column heading for each business object is empty.

    \[Omitted image "work-schedule-calendar-report3.png"\] Alt text: Work schedule calendar report.

9.  In the Filter section, provide the values, as shown in the image.

    \[Omitted image "work-schedule-calendar-report4.png"\] Alt text: Work schedule calendar report.

10. In the prompt section, select **Populate Undefined Prompt defaults**.

    \[Omitted image "work-schedule-calendar-report5.png"\] Alt text: Work schedule prompt.

    All prompts are populated.

11. Confirm that the prompts are configured, as shown in the image.

    \[Omitted image "work-schedule-calendar-report6.png"\] Alt text: Work schedule calendar report.

12. In the advanced section, select **enable as webservice**.

13. Select **OK**, and then **Done**.

14. Select the three dots icon \(\[Omitted image "three-dots-icon.png"\] Alt text: Three-dots icon.\) and navigate to **Web Service****&gt;** **View URLs**.

    \[Omitted image "work-schedule-calendar-report7.png"\] Alt text: Work schedule calendar report.

15. Provide an employee id in **Employee ID** box, and select **OK**. 

    \[Omitted image "work-schedule-calendar-report8.png"\] Alt text: Work schedule calendar report.

16. In  the **View URLs Web Service** page, select the marked icon under the  CSV  section.

    \[Omitted image "work-schedule-calendar-report9.png"\] Alt text: Work schedule calendar report.

    A new browser tab opens.

17. View the  RaaS  URL  of the report in new browser tab.

    \[Omitted image "work-schedule-calendar-report10.png"\] Alt text: RaaS URL.

    URL details:

    -   https://wd2-impl-services1.workday.com  represents  the  Base URL of customer’s workday tenant. 
    -   Tenant\_Name  represents  customer’s workday tenant. 
    -   Report\_Owner\_user\_name represents user name of the report’s owner. 
    -   SNIH\_Work\_schedule\_calendar represents the report name alias.

