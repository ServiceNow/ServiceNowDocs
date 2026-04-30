---
title: Workday configuration for compensation change event report
description: Retrieve compensation change event data based on time duration by creating the compensation change event report.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-12-04"
reading_time_minutes: 2
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Workday configuration for compensation change event report

Retrieve compensation change event data based on time duration by creating the compensation change event report.

## Before you begin

Role required: User with access to report creation and the Business Process Transactions data source.

-   Create all calculated fields for this report before developing the report, so that while creating report all fields are available.
-   While creating the report, ensure that the report name, report field names or column heading override for the respective field \(if given in report document\) is same as it is in report document.

    Report field label should be same as in report doc. Else, the developed action will fail.

-   While creating filter, ensure that you add parenthesis on filter.
-   All reports must be owned by the ISU user which will be used for accessing these actions on the ServiceNow platform.
-   In the **Advanced** section, **Enable as webservice** option should be selected.

## Procedure

1.  Access the Create Custom Report task.

2.  Provide the report name such as, `RPT_Compensation_change_event`.

3.  Select report type as **Advanced**.

4.  Clear the **Optimized for performance** option.

5.  Select **Data Source** as **Business Process Transactions**.

6.  Do not select the **Temporary report** option and click **OK**.

    ![RPT_Compensation_change_event report.](../image/wdhr-conf-comp-chng-event-rep-1.jpg)

7.  Select the report business object and report fields.

    ![Report business object and report fields.](../image/wdhr-conf-comp-chng-event-rep-2.jpg)

8.  In **Group column Headings** section, select the business object.

    **Group Column heading** for each business object is blank.

    ![Select the business object.](../image/wdhr-conf-comp-chng-event-rep-3.jpg)

9.  In the **Filter** section, select the value.

    Ensure that you add parenthesis.

    ![Select the value.](../image/wdhr-conf-comp-chng-event-rep-4.jpg)

10. In **Prompts** section, select the **Populate Undefined Prompt Defaults** option.

    ![Select the Populate Undefined Prompt Defaults option.](../image/wdhr-conf-comp-chng-event-rep-5.jpg)

11. Select the value of prompts and ensure the **Label For Prompt XML Alias** of all prompt fields is as shown.

    ![Label For Prompt XML Alias of all prompt fields.](../image/wdhr-conf-comp-chng-event-rep-6.jpg)![Label For Prompt XML Alias of all prompt fields.](../image/wdhr-conf-comp-chng-event-rep-7.jpg)

12. In the **Advanced** section, select the **Enable as webservice** option and click **OK**.

13. After report configuration, click the three dots icon and navigate to **Web Services** &gt; **View URLs**.

    ![Click View URLs.](../image/wdhr-conf-comp-chng-event-rep-8.jpg)

14. Select **Business Processes**, **Transaction Status** as **In Progress**, required time range in **Start Date** and **End Date**, and click **OK**.

    **Note:** This step is one-time process required to get the WID of business process and transaction status. After the initial full load, transaction status ID is not needed as details of all events will be retrieved; **In Progress** as well as **Completed**.

    ![Provide the required details.](../image/wdhr-conf-comp-chng-event-rep-9.jpg)![Provide the required details.](../image/wdhr-conf-comp-chng-event-rep-10.jpg)

15. In View URLs Web Service page, click the marked icon under the **CSV** section.

    A new browser tab is opened.

    ![CSV section.](../image/wdhr-conf-comp-chng-event-rep-11.jpg)

    The RaaS URL of the report is displayed in new browser tab and you can obtain these details from the link.

    ![RaaS URL of the report.](../image/wdhr-conf-comp-chng-event-rep-12.jpg)

    -   `https://wd2-impl-services1.workday.com` is the base URL of customer’s workday tenant.
    -   **Tenant\_Name** is the customer’s workday tenant.
    -   **Report\_Owner\_user\_name** represents user name of the report’s owner.
    -   **Report\_Name** is the report name.
    -   **Business\_Processes%21WID=\(32 character code\)** is the business process WID and **Transaction\_Status%21WID=\(32 character code\)** is the Transaction WID.
    **Note:** After the initial full load, Transaction Status WID is not used as parameter as all in progress and completed transactions will be retrieved.

    |Usecase|Business process|Workday ID|
    |-------|----------------|----------|
    |Compensation change|Propose Compensation Hire|cd0a03bc446c11de98360015c5e6daf6|
    |Change Default Compensation|cd0cabbc446c11de98360015c5e6daf6|
    |Requisition Compensation|448e44df783a100005ba3ddd7e1a021c|
    |Propose Compensation Change|cd0a18a2446c11de98360015c5e6daf6|
    |Request Compensation Change|cd09f2e6446c11de98360015c5e6daf6|
    |Request Compensation Change for Leave of Absence|6766cfa1f9444f9ab8dffbff5ba87b50|

    Workday ID of **In Progress** transaction status is e2d08afc53614c37b32b31270bb8bee3.


