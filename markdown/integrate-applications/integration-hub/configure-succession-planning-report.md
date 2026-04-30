---
title: Configure Succession Planning Report
description: Configure the Succession Planning report that the action Look up Succession Planning in the Workday HR spoke uses to view the details of succession planning.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-03-04"
reading_time_minutes: 1
breadcrumb: [Workday HR Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Configure Succession Planning Report

Configure the Succession Planning report that the action Look up Succession Planning in the Workday HR spoke uses to view the details of succession planning.

## Before you begin

Role required: Confirm that you have the privilege to create the report.

Confirm that you have the access to the data source of the Succession Plans by Organization.

Confirm that all reports are owned by the ISU user.

Confirm that the **Enable as webservice** option in the Advanced section is selected.

## Procedure

1.  Access the Create Custom Report task.

2.  Provide the report name.

3.  Select the report type as **Advanced**.

4.  Deselect the **Optimized for performance** option.

5.  Select the Succession Plans by Organization data source.

6.  Confirm that the temporary report option is deselected, and then select **Ok**.

    ![Workday report.](../image/workday-report63.png)

7.  Select the report business object and report fields as given in the image.

    ![Workday report.](../image/workday-report64.png)

    ![Workday report.](../image/workday-report65.png)

8.  In the Group column heading section, select all business object.

    The Group Column heading for each business object is empty.

    ![Workday report.](../image/workday-report66.png)

9.  In the Sort section, under Sub level sort, select the value as shown.

    ![Workday report.](../image/workday-report67.png)

10. In the Filter section, select the value as given below.

    Add parenthesis as given in the image.

    ![Workday report.](../image/workday-report68.png)

11. In the prompt section, click on **Populate Undefined Prompt Defaults** option.

    ![Workday report.](../image/workday-report69.png)

12. Select the value of prompts as given below under the Prompt default section.

    Make sure the Label For Prompt XML Alias of all prompt fields must be the same as given below.

    ![Workday report.](../image/workday-report70.png)

13. In the advanced section, select **enable as webservice**, and then click **OK**.

14. Select the three dots icon and go to **Web services&gt; view URLs**.

    ![Workday report.](../image/workday-report71.png)

15. Select the organization for which you want to run this report and select the box if you want to include the subordinate organizations.

    ![Workday report.](../image/workday-report72.png)

16. In the View URLs Web Service page, click on marked icon under CSV section.

    ![Workday report.](../image/workday-report73.png)

    A new browser tab displays the following results.

    Details:

    -   https://wd2-impl-services1.workday.com represents the Base URL of customer’s workday tenant.
    -   Tenant\_Name represents customer’s workday tenant.
    -   Report\_Owner\_user\_name represents user name of the report’s owner.
    -   Report\_Name Represents report name.
    ![Workdat report.](../image/workday-report74.png)


