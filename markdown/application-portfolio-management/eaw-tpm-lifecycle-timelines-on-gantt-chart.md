---
title: TLM lifecycle timelines on Gantt chart
description: For Technology Lifecycle Management \(TLM\), the business applications and their related application services \(associated hardware models and software products\) are displayed in a hierarchical structure. The corresponding timelines of the application services are displayed as bars on the Gantt chart.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-portfolio-management/eaw-tpm-lifecycle-timelines-on-gantt-chart.html
release: zurich
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Gantt view of TLM and TRM lifecycle timelines, Explore, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# TLM lifecycle timelines on Gantt chart

For Technology Lifecycle Management \(TLM\), the business applications and their related application services \(associated hardware models and software products\) are displayed in a hierarchical structure. The corresponding timelines of the application services are displayed as bars on the Gantt chart.

**Important:**

Technology Lifecycle Management \(TLM\) was previously known as Technology Portfolio Management \(TPM\). TPM and TLM refer to the same feature. Table names and scheduled job names continue to use TPM and haven't been renamed.

Whether your instance displays TPM or TLM also depends on your application versions. TLM labels appear only when both the Enterprise Architecture Workspace application \(version 9.2.1 or later\) and the Technology Lifecycle Management plugin, sn\_apm\_tpm \(version 1.11.0 or later\), are installed. If either application is on an earlier version, the interface continues to show TPM.

\[Omitted image "TPM-gantt-chart.png"\] Alt text: TLM view of the Gantt chart.

**Note:** The lifecycle data for software products is displayed only when the Software Asset Management \(SAM\) Foundation or Software Asset Management \(SAM\) Professional plugin is installed.

It displays the following TLM phase-related information:

-   **End of support**
-   **End of extended support**
-   **End of life**

    You can point to an individual bar in the Gantt chart to view the phase information.


The **Application** column values are populated from the TPM Discovered Technology table \(sn\_apm\_tpm\_discovered\_technology\).

All versions of a particular software product are grouped. Each software product has a unique combination of product name, product version, and product edition. A lifecycle record is created for each product and the timelines are displayed on the Gantt chart.

## Lifecycle end-date calculation logic

For each TLM lifecycle phase, the end date of one phase is the start date of the next phase. Assuming that there are three TLM phases that are end of support, end of extended support, and end of life, the respective phase end dates are as follows:

-   The end of support phase end date will coincide with the start date of the next phase, end of extended support.
-   The end of extended support phase end date will coincide with the start date of the next phase, end of life.

For example, Product A has two TLM phases that are **End of Support** and **End of Extended Support**. The start date for the **End of Support** phase is 12/01/2023 and the start date for the **End of Extended Support** phase is 12/30/2023. No phase end date has been mentioned for the **End of Support** phase. In such a scenario, the end date of the **End of Support** phase will be considered as 12/30/2023.

If only one TLM phase is available for a TLM product, then the TLM phase lifecycle end date is calculated by adding the time value as defined in the system property **sn\_apm.endRangeofTPMLifecycle** with the current date. This time value enables the Gantt chart to display only known lifecycle dates.

For example, today is 12/01/2023 and the end date value as defined in the system property **sn\_apm.endRangeofTPMLifecycle** is three years from the current date. Then, the end date of the phase will be 12/01/2026.

## Application service and business application timelines

The application services \(composed of software products and hardware models\) have lifecycle timelines determined for them. On the Gantt chart, the earliest TLM phase start date of either the software products or hardware models is rolled up. This calculates the TLM phase start date of the overall application service. That is, the earliest TLM phase start date of any software product or hardware model is taken as the TLM phase start date of the application service, overall.

For example, assume that all hardware models and software products have lifecycle dates for these TLM phases: end of support, end of extended support, and end of life. Application service A consists of one software product and one hardware model. The end of support start date phase of the software product is 12/01/2023 and the end of support start date of the hardware model is 12/15/2023. The end of support start date of the software product \(12/01/2023\) is considered the TLM phase start date of that application service. The Gantt chart bar for that application service starts from 12/01/2023.

Similarly, the TLM phase start date of the business application is considered as the earliest TLM phase start date of any of its associated application services. For example, application X has two application services, A and B. The end of support start date of application service A is 12/01/2023 and of application service B is 12/12/2023. In this scenario, the end of support start date of application service A \(12/01/2023\) is considered the TLM phase start date of the business application. The Gantt chart bar for that business application starts from 12/01/2023.

## TLM risk calculation

The TLM view also displays the upcoming TLM risks associated with any application services, based on their lifecycle dates. To calculate the risk associated with an application service, run the **Populate Technology Lifecycle Risks** scheduled job. For more details, see [Schedule a job to generate TLM technology risk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-schedule-job-generate-tpm-risk.md). To learn more about technology lifecycle risk, see [Technology risk calculation in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-technology-risk-calc.md).

The hardware model and software product risk scores are derived from the TPM Technology Risk table \(sn\_apm\_tpm\_technology\_risk\). The risk values are rolled up to the application service level. The highest risk value of hardware models and software products associated with a single application service is considered the risk value of that application service. For example, application service A consists of two hardware models and three software products. The two hardware models have moderate risk while the two software products have low risk. However, one software product has high risk. In this scenario, the risk value of the application service is considered high.

Similarly, the risk values of the application services are rolled up to the business application level. The highest risk value of an application service associated with a business application is considered the risk value of that business application. For example, business application X has three application services associated with it. The three applications services have risk values as high, moderate, and low respectively. In such a scenario, the risk value of the business application is considered as high.

## Color coding

The colors of the bars on the Gantt chart are based on their TLM phase. The TLM phase and its corresponding colors are as follows.

|Color|TRM Phase|
|-----|---------|
|\[Omitted image "color-lavender.png"\] Alt text: Lavender color.|End of support|
|\[Omitted image "color-pink.png"\] Alt text: Pink color.|End of extended support|
|\[Omitted image "color-azalea.png"\] Alt text: Azalea color.|End of life|

To see the colors associated with each TLM risk type in the Upcoming TLM risk column, select the legend button \(\[Omitted image "legend-icon.png"\] Alt text: Legend button.\).

**Parent Topic:**[Gantt view of TLM and TRM lifecycle timelines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-gantt-view-of-tpm-and-trm-lifecycle-timelines.md)

**Related topics**  


[View TLM and TRM lifecycle timelines on the Gantt chart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-view-tpm-and-trm-lifecycle-timelines-in-gantt-chart.md)

