---
title: Manage the Technology Portfolio Management \(TPM\) in Enterprise Architecture Workspace
description: Technology Portfolio Management helps Enterprise Architects to manage technology life-cycle risks and technology life-cycle exceptions. Enterprise Architects can evaluate all their business applications and application services by accessing the discovered technologies and auditing information in the Enterprise Architecture Workspace.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Exploring Technology Portfolio view, Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Manage the Technology Portfolio Management \(TPM\) in Enterprise Architecture Workspace

Technology Portfolio Management helps Enterprise Architects to manage technology life-cycle risks and technology life-cycle exceptions. Enterprise Architects can evaluate all their business applications and application services by accessing the discovered technologies and auditing information in the Enterprise Architecture Workspace.

The underlying technologies of the business applications used in your business enterprise have a shelf life that must be actively managed and diligently monitored to track their versions and life-cycle.

The software products used in your business applications can be operating systems, database management systems, development tools, and middle ware, each of which has a life cycle. If these life-cycle stages aren’t tracked, there are risks where the vendor may not support them any longer and the business applications that run on these technologies are at stake.

Creating an inventory of all technologies used in the enterprise helps to:

-   Track the versions of the software and manufacturer support dates for the software
-   Set an internal life-cycle guidance for the software
-   Assess the risks in using outdated software
-   Plan to retire them just like the applications they support, at a definite date
-   Support upgrade processes

The data for the software products are populated from the Computer \(CMDB\_CI\_Computer\) and all similar instances of the table, Docker Container \(CMDB\_CI\_Docker\_Container\), and Serverless Hardwares \(CMDB\_CI\_Serverless\_Hardware\) tables, by default. However, if you want to include other CMDB tables that contain software products, you must update the system property **sn\_apm\_tpm.configurationItemsWithSoftwareInstalls**. For information on how to update the system property, see [Update the system property to gather software products from a CMDB table](../../task/eaw-task/eaw-update-system-property-gather-software-cmdb.md).

## Installing the Technology Portfolio Management plugin

For instructions to install Technology Portfolio Management, see [Activate the Technology Portfolio Management \(TPM\) plugin](../../task/eaw-task/eaw-install-tpm.md).

**Important:** Technology Portfolio Management \(TPM\) fetches the hardware life-cycle data for your enterprise. To fetch the software life-cycle data, you must activate the Software Asset Management \(SAM\) Professional plugin. Before installing the SAM Foundation plugin, carefully review the [Software Asset Management Foundation plugin migration](https://www.servicenow.com/docs/access?context=c_SAMMigrationSAMF&version=australia&pubname=australia-it-service-management&ft:locale=en-US) documentation.

## TPM indicators in EA Workspace

The following are the indicators for Technology Portfolio Management \(TPM\) in EA Workspace:

|Indicator|Description|
|---------|-----------|
|Technology Lifecycle Risk \[sn\_apm\_tpm\_technology\_risk\]|Calculates the lifecycle risk score for business applications.|

## TPM reference model in EA Workspace

In EA Workspace, the Technology Portfolio Management enables you to align technologies using the **Update TPM data** action from a business application record or using the schedule job **Populate TPM Discovered Technologies and Lifecycles**.

![TPM Reference Model in Enterprise Architecture Workspace](../../image/eaw-image/new-tpm-ref-model.png "TPM Reference Model")

## Technology discovery process in EA Workspace

The following is the technology discovery and alignment process for business applications in the EA Workspace.

-   Query and fetch the Consumes::Consumed by Application Services.

    **Note:** It must be an Application Service and these Application Services must be mapped. The Service Configuration Item Associations \[svc\_ci\_assoc\] table is populated for each Application Service and its Computers.

    ![Service Configuration Item Associations](../../image/eaw-image/eaw-tpm-serv-con-item-asso.png "Service Configuration Item Associations")

-   For each computer identified in the Service Configuration Item Associations \[svc\_ci\_assoc\] table, you can see the installed software by selecting the Software Installations tab. Also, if a Hardware Model is associated with the computer, you can see the Hardware type details in the TPM Discovered Technologies tab.
-   For each software install, you can see the associated discovery model. The software discovery models must be of a product type Licensable or Unknown and they must be normalized or manually normalized to get any appropriate information. You can also also use the **sn\_apm\_tpm.softwareDiscoveryModelProductFilterForTPMsystem** property to gather data on non-licensable software products. For information see, [Filter software results using an encoded query in TPM](../../task/eaw-task/use-tpm-encoded-query.md).
-   For each discovery model, create a TPM Discovered Technology record.
-   When you create a record for the TPM Discovered Technology, it triggers the creation of an associated TPM Technology Lifecycles record and it fetches the lifecycle information for the hardware or software technology. An unique TPM lifecycle record identifier is also generated. On selecting the record identifier, more information on the TPM lifecycle record is displayed.

    ![TPM lifecycle record identifier highlighted on the Technology Portfolio page.](../../image/eaw-image/tpm-lifecycle-record.png)

    **Note:**

    -   TPM lifecycle record identifiers are automatically generated on creating a TPM record using the Technology Portfolio Management \(sn\_apm\_tpm\) plugin version 1.9.0. However, for TPM lifecycle records generated using previous versions of the TPM plugin don't have any lifecycle record identifiers. The TPM record identifiers of these TPM lifecycle records must be generated using the Populate Number field in TPM Discovered Technologies job. For information, see [Run a scheduled job to populate Technology Portfolio Management lifecycle record identifier](../../task/eaw-task/eaw-run-job-to-populate-tpm-lifecycle-identifier.md).

    -   You can zoom on this page to 200% or 400% through your browser settings without the loss of content or functionality. Page layouts are transformed into a vertical, stacked view automatically.

![TPM lifecycle process in EA Workspace](../../image/eaw-image/eaw-tpm-lifecycle-process.png "Technology life-cycle discovery process in EA Workspace")

For successful software alignment records, you must have the following tables populated:

-   Business Application \[cmdb\_ci\_business\_app\]
-   CI Relationship \[cmdb\_rel\_ci\] - Consumes::Consumed by
-   Service Instance \[cmdb\_ci\_service\_auto, discovered, calculated, query\_based, tag\_based, manual\]
-   Service CI Association \[svc\_ci\_assoc\] - note: Only table used to find App Service
-   Computers/Hardware Computer \[cmdb\_ci\_computer\]
-   Software Installation \[cmdb\_sam\_sw\_install\]
-   Software Discovery Model \[cmdb\_sam\_sw\_discovery\_model\]
-   Software Product \[samp\_sw\_product\]
-   Software Product Lifecycle \[sam\_sw\_product\_lifecycle\]

    **Note:** Depending on your how you have setup your instance, other tables can also contain software records. Check with your administrator.


Hardware requires the Hardware Model reference on the Computer be populated.

## Update TPM Data for a business application or application service

You can manually refresh the TPM life-cycle data manually for a selected business application or application service. A scheduled job **Populate TPM Discovered Technologies and Life-cycles** is also run on schedule or on-demand to update the life-cycle data for all business applications and application services​​. For more details, see [Update TPM data for a business application or application service](../../task/eaw-task/update-tpm-data.md) and [Run a scheduled job to generate TPM lifecycle data](../../task/eaw-task/eaw-run-scheduled-job-update-tpm-data.md).

## View insights for technology life-cycle risks

You can track the technology lifecycle risk for business applications, application services, servers, software products, and hardware models. The **Populate TPM Discovered Technologies and Life-cycles** scheduled job shows the lifecycle results in the **Insights** section of the EA Workspace home page. Select the **Technology Portfolio** tab in the **Insights** section and then select the **View all technology lifecycle risks**.![Insights for Technology Lifecycle risks](../../image/eaw-image/eaw-tpm-insights.png)

-   Use this filter to see the risks for the next 1 month, 3 months, 6 months, 12 months, and 18 months. By default, the 1 month filter is applied.
-   Use the **Show only production instances** toggle button to see only production instances that are having technology lifecycle risks. By default, this filter is off.
-   Select the **View all technology lifecycle risks** link to see the list of all technology lifecycle risks sorted by earliest lifecycle date, which means the earliest date when a technology lifecycle risk is to happen. You can also export the Technology lifecycle risks information to Excel, CSV, JSON, or PDF as required.

    The data in the Technology lifecycle risks table is fetched from the TPM Discovered Technologies \[sn\_apm\_tpm\_discovered\_technology\] table.

-   Execute the Populate Technology Lifecycle Risks scheduled job to generate the TPM technology lifecycle risks. This scheduled job populates the risk scores for business applications \(BA\), application services \(AS\), software products, and hardware models for a fiscal period of type month in the Technology lifecycle risks \(sn\_apm\_tpm\_technology\_risk\) table. For more details, see [Schedule a job to generate TPM technology risk](../../task/eaw-task/eaw-schedule-job-generate-tpm-risk.md).

## View TPM analysis run logs

You can track the progress of TPM analysis by examining the TPM Discovered Technology Run Logs \[sn\_apm\_tpm\_discovered\_technology\_run\_log\] table. Each time the analysis is run, an entry is added to this table. Navigate to **EA Workspace** &gt; **Setup** &gt; **Logs** section view the logs.

## TPM lifecycle timelines on Gantt chart

For the Technology Portfolio Management \(TPM\), the business applications and their related application services \(associated hardware models and software products\) are displayed in a hierarchical structure. The corresponding timelines of the application services are displayed as bars on the Gantt chart.

The application services \(composed of software products and hardware models\) have lifecycle timelines determined for them. On the Gantt chart, the earliest TPM phase start date of either the software products or hardware models are rolled up to calculate the TPM phase start date of the overall application service. That is, the earliest TPM phase start date of any software product or hardware model is taken as the TPM phase start date of the application service, overall. For more details, see [TPM lifecycle timelines on Gantt chart](eaw-tpm-lifecycle-timelines-on-gantt-chart.md) and [View TPM and TRM lifecycle timelines on the Gantt chart](../../task/eaw-task/eaw-view-tpm-and-trm-lifecycle-timelines-in-gantt-chart.md).

![TPM Gantt chart](../../image/eaw-image/TPM-gantt-chart.png)

## Data visualization for TPM data

In the Enterprise Architecture Workspace Dashboard, the 'Top 10 business applications with normalized TPM risk' widget shows the top 10 business applications having normalized TPM risk. For more details, see [Explore the Enterprise Architecture Workspace dashboard](../../../../use/dashboards/concept/eaw-workspace-dashboard.md).

-   **[Working with technology portfolio audit details](eaw-view-technology-portfolio-audit-risk.md)**  
The  **Technology portfolio audit** tab shows audit information for your applications. An entry in this table indicates that at least one lifecycle for that software product or hardware model was either approximated, or not found, or doesn’t exist.

**Parent Topic:**[Exploring Technology Portfolio view](eaw-technology-portfolio-view.md)

**Related topics**  


[Working with Technology Portfolio Management \(TPM\) in EA Workspace](eaw-work-with-tpm.md)

[Gantt view of TPM and TRM lifecycle timelines](eaw-gantt-view-of-tpm-and-trm-lifecycle-timelines.md)

[TPM lifecycle timelines on Gantt chart](eaw-tpm-lifecycle-timelines-on-gantt-chart.md)

[View TPM and TRM lifecycle timelines on the Gantt chart](../../task/eaw-task/eaw-view-tpm-and-trm-lifecycle-timelines-in-gantt-chart.md)

