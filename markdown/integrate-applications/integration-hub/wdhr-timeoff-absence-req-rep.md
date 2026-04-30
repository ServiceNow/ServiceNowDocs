---
title: Workday configuration for worker time-off and leave of absence request report
description: Create report in Workday to extract worker’s time off and leave of absence request based on Employee ID.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-12-06"
reading_time_minutes: 2
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Workday configuration for worker time-off and leave of absence request report

Create report in Workday to extract worker’s time off and leave of absence request based on Employee ID.

## Before you begin

Role required: User with access to report creation and the All Active and Terminated Workers data source.

-   Create all calculated fields for this report before developing the report, so that while creating report all fields are available.
-   While creating the report, ensure that the report name, report field names or column heading override for the respective field \(if given in report document\) is same as it is in report document.

    Report field label should be same as in report doc. Else, the developed action will fail.

-   While creating filter, ensure that you add parenthesis on filter.
-   All reports must be owned by the ISU user which will be used for accessing these actions on the ServiceNow platform.
-   In the **Advanced** section, **Enable as webservice** option should be selected.

Create all calculated fields so that these fields can be used while developing report.

Calculated field 1:

-   Create **True/False Condition** type cal field named **CF\_time\_off\_is\_approved**.

    ![](../image/wdhr-timeoff-absence-req-rep-1.jpg)

-   Create **Extract Multi-Instance** type cal field named **CF\_approved\_time\_off**.

    ![](../image/wdhr-timeoff-absence-req-rep-2.jpg)


## Procedure

1.  Access the **Create Custom Report** task.

2.  Provide the report name such as, **CR\_Worker\_time\_off\_and\_leave\_of\_absence\_request**.

3.  Select report type as **Advanced**.

4.  Clear the **Optimized for performance** option.

5.  Select **Data Source** as **All Active and Terminated Workers**.

6.  Do not select the **Temporary report** option and click **OK**.

    ![](../image/wdhr-timeoff-absence-req-rep-3.jpg)

7.  Select the report business object and report fields.

    ![](../image/wdhr-timeoff-absence-req-rep-4.jpg)

8.  In **Group Column Headings**, select the value.

    ![](../image/wdhr-timeoff-absence-req-rep-5.jpg)

9.  In the **Filter** section, select the values.

    ![](../image/wdhr-timeoff-absence-req-rep-6.jpg)

10. In **Prompts** section, select the **Populate Undefined Prompt Defaults** option.

    ![](../image/wdhr-timeoff-absence-req-rep-7.jpg)

11. Select the value of prompts as given below under Prompt default section.

    Make sure the **Label For Prompt XML Alias** of all prompt fields must be same.

    ![](../image/wdhr-timeoff-absence-req-rep-8.jpg)

12. In **Advanced** section, select **Enable as webservice** option and click **OK**.

13. Click on three dots icon and navigate to **Web Services** &gt; **View URLs** option once report configuration is done.

    ![](../image/wdhr-timeoff-absence-req-rep-9.jpg)

14. Provide the **Employee ID** for which you want to extract the data.

    ![](../image/wdhr-timeoff-absence-req-rep-10.jpg)

15. In View URLs Web Service page, click the marked icon under the **CSV** section.

    A new browser tab is opened.

    ![](../image/wdhr-timeoff-absence-req-rep-11.jpg)

    The RaaS URL of the report is displayed in new browser tab and you can obtain these details from the link.

    ![](../image/wdhr-timeoff-absence-req-rep-12.jpg)

    -   `https://wd2-impl-services1.workday.com` is the base URL of customer’s workday tenant.
    -   **Tenant\_Name** is the customer’s workday tenant.
    -   **Report\_Owner\_user\_name** represents user name of the report’s owner.
    -   **Worker\_time\_off\_and\_leave\_of\_absence\_request** is the report name.

