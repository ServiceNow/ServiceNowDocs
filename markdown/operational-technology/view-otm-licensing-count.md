---
title: View CIs consuming OTM subscription units
description: Generate a list of currently countable CIs for each of the OTM applications: ServiceNow OT Foundation, ServiceNow OT Visibility and ServiceNow OT Vulnerability and Response.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Operational Technology Management licensing and subscriptions, Operational Technology]
---

# View CIs consuming OTM subscription units

Generate a list of currently countable CIs for each of the OTM applications: ServiceNow® OT Foundation, ServiceNow® OT Visibility and ServiceNow® OT Vulnerability and Response.

## Before you begin

-   Ensure your organization has active OTM subscriptions.
-   Ensure that you installed the latest available version of the ITOM SU Licensing from [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/4cce117e53b9301046dfddeeff7b12eb).

Role required: sn\_itom\_license.reader

## About this task

The CI list generated is strongly correlated to the most recent daily count of CIs. However, it's possible that the number of CIs on the generated list may display slight discrepancies compared to the latest daily count if any changes have occurred since the last daily count.

## Procedure

1.  Navigate to **All** &gt; **OTM License** &gt; **Report OTM Licensable CIs**.

    The **Report ITOM Licensable CIs** page appears.

2.  Select the application for which you want to see licensed CIs.

    -   Foundation
    -   Visibility
    -   HLA
    -   Health
    ![Applications for which you want to see licensed CIs](../../operational-technology-management/image/otm-application-ci-1.png)

3.  To create a report for the selected applications, select **Populate licensable CIs**.

4.  To accept the confirmation message and generate the report, select **Yes**.

    The new report replaces the data in the previously generated report. You can cancel the report by selecting the application and then opting for the **Cancel Job** option.

5.  Wait for a few minutes and then refresh the page.

    The application status is displayed as **Completed** once the report has finished processing.

6.  Select the application and then select **Show licensable CIs**.

    The ITOM Licensable CIs page for OTM SKU displays the list of CIs with an OTM license.


