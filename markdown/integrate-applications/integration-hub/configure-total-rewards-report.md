---
title: Configure Total Rewards Report
description: Configure the Total Rewards Report to use the Look up Total Rewards using Report action.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-12-30"
reading_time_minutes: 1
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Configure Total Rewards Report

Configure the Total Rewards Report to use the Look up Total Rewards using Report action.

## Before you begin

Role required: none

Confirm that the user has access to custom report creation and All Workers data source access.

## Procedure

1.  Access the Create Custom Report task.

2.  Provide the report name.

    Report name example: RPT total rewards.

3.  Select report type as **Advanced**.

4.  Deselect the **Optimized for performance** field.

5.  Select the data source as **All Workers**.

6.  Select **OK**.

    Confirm that the **temporary report** field is deselected.

    ![View custom report.](../image/total-rewards-report1.png)

7.  Provide the values in the report, as shown in the image.

    ![Column list.](../image/total-rewards-report2.png)

8.  Confirm that under the **Group Column Headings** section, the Group Column heading for business object is empty.

    ![Group column headings.](../image/total-rewards-report3.png)

9.  Set the Filter section, as shown in the image.

    ![Filter section.](../image/total-rewards-report4.png)

10. In the prompt section, select the **Populate Undefined Prompt defaults** check box.

    The all built-in prompts are populated.

    Confirm that the prompts are configured in the same way as provided in the image.

    ![Prompt defaults.](../image/total-rewards-report5.png)

11. In the advanced section, select **Enable as Webservice**, and then select **OK**.

12. Select the three dots icon \(![Three-dots icon.](../image/three-dots-icon.png)\) and navigate to **Web Service****&gt;** **View URLs**.

    ![View custom report.](../image/total-rewards-report6.png)

13. Select a currency and an employee id in below parameters, and then select **OK**. 

    ![View URLs Web Service.](../image/total-rewards-report7.png)

14. On  the **View URLs Web Service** page, select the icon under  the CSV  section, as shown in the image.

    ![View URLs Web Service.](../image/total-rewards-report8.png)

    A new  browser  tab opens .ß

15. View the  RaaS  URL  of the report in new browser tab.

    ![RaaS  URL  .](../image/total-rewards-report9.png)

    URL details:

    -   https://wd2-impl-services1.workday.com  represents  the  base URL of customer’s workday tenant. 
    -   Tenant\_Name  represents  customer’s workday tenant.
    -   Report\_Owner\_user\_name  represents  the user name of the report’s owner. 
    -   RPT\_total\_rewards Represents report name alias.

