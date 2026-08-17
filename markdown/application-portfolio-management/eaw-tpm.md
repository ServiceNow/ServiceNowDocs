---
title: Manage the Technology Lifecycle Management \(TLM\) in Enterprise Architecture Workspace
description: Technology Lifecycle Management helps Enterprise Architects to manage technology life-cycle risks and technology life-cycle exceptions. Enterprise Architects can evaluate all their business applications and application services by accessing the discovered technologies and auditing information in the Enterprise Architecture Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-tpm.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Exploring Technology Portfolio view, Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Manage the Technology Lifecycle Management \(TLM\) in Enterprise Architecture Workspace

Technology Lifecycle Management helps Enterprise Architects to manage technology life-cycle risks and technology life-cycle exceptions. Enterprise Architects can evaluate all their business applications and application services by accessing the discovered technologies and auditing information in the Enterprise Architecture Workspace.

**Important:**

Technology Lifecycle Management \(TLM\) was previously known as Technology Portfolio Management \(TPM\). TPM and TLM refer to the same feature. Table names and scheduled job names continue to use TPM and haven't been renamed.

Whether your instance displays TPM or TLM also depends on your application versions. TLM labels appear only when both the Enterprise Architecture Workspace application \(version 9.2.1 or later\) and the Technology Lifecycle Management plugin, sn\_apm\_tpm \(version 1.11.0 or later\), are installed. If either application is on an earlier version, the interface continues to show TPM.

The underlying technologies of the business applications used in your business enterprise have a shelf life. You must actively manage and monitor them to track their versions and life-cycle.

The software products used in your business applications can be operating systems, database management systems, development tools, and middle ware, each of which has a life cycle. If these life-cycle stages aren't tracked, the vendor may not support them any longer. The business applications that run on these technologies are at stake.

Creating an inventory of all technologies used in the enterprise helps to:

-   Track the versions of the software and manufacturer support dates for the software
-   Set an internal life-cycle guidance for the software
-   Assess the risks in using outdated software
-   Plan to retire them just like the applications they support, at a definite date
-   Support upgrade processes

By default, the data for the software products are populated from the Computer \(CMDB\_CI\_Computer\), Docker Container \(CMDB\_CI\_Docker\_Container\), and Serverless Hardwares \(CMDB\_CI\_Serverless\_Hardware\) tables and all similar instances. To include other CMDB tables that contain software products, update the system property **sn\_apm\_tpm.configurationItemsWithSoftwareInstalls**. For information on how to update the system property, see [Update the system property to gather software products from a CMDB table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-update-system-property-gather-software-cmdb.md).

## Installing the Technology Lifecycle Management plugin

For instructions to install Technology Lifecycle Management, see [Activate the Technology Lifecycle Management \(TLM\) plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-install-tpm.md).

**Important:** Technology Lifecycle Management \(TLM\) fetches the hardware life-cycle data for your enterprise. To fetch the software life-cycle data, you must activate the Software Asset Management \(SAM\) Professional plugin. Before installing the SAM Foundation plugin, carefully review the [Software Asset Management Foundation plugin migration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/c_SAMMigrationSAMF.md) documentation.

## TLM indicators in EA Workspace

The following are the indicators for Technology Lifecycle Management \(TLM\) in EA Workspace:

|Indicator|Description|
|---------|-----------|
|Technology Lifecycle Risk \[sn\_apm\_tpm\_technology\_risk\]|Calculates the lifecycle risk score for business applications.|

## TLM reference model in EA Workspace

In EA Workspace, the Technology Lifecycle Management enables you to align technologies using the **Update TPM data** action from a business application record or using the schedule job **Populate TPM Discovered Technologies and Lifecycles**.

\[Omitted image "new-tpm-ref-model.png"\] Alt text: TLM Reference Model in Enterprise Architecture Workspace

## Technology discovery process in EA Workspace

The following is the technology discovery and alignment process for business applications in the EA Workspace.

-   Query and fetch the Consumes::Consumed by Application Services.

    **Note:** It must be an Application Service and these Application Services must be mapped. The Service Configuration Item Associations \[svc\_ci\_assoc\] table is populated for each Application Service and its Computers.

    \[Omitted image "eaw-tpm-serv-con-item-asso.png"\] Alt text: Service Configuration Item Associations

-   For each computer identified in the Service Configuration Item Associations \[svc\_ci\_assoc\] table, you can see the installed software by selecting the Software Installations tab. Also, if a Hardware Model is associated with the computer, you can see the Hardware type details in the TLM Discovered Technologies tab.
-   For each software install, you can see the associated discovery model. The software discovery models must be of a product type Licensable or Unknown and they must be normalized or manually normalized to get any appropriate information. You can also also use the **sn\_apm\_tpm.softwareDiscoveryModelProductFilterForTPMsystem** property to gather data on non-licensable software products. For information see, [Filter software results using an encoded query in TLM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/use-tpm-encoded-query.md).
-   For each discovery model, create a TLM Discovered Technology record.
-   When you create a record for the TLM Discovered Technology, it triggers the creation of an associated TLM Technology Lifecycles record and it fetches the lifecycle information for the hardware or software technology. An unique TLM lifecycle record identifier is also generated. On selecting the record identifier, more information on the TLM lifecycle record is displayed.

    \[Omitted image "tpm-lifecycle-record.png"\] Alt text: TLM lifecycle record identifier highlighted on the Technology Portfolio page.

    **Note:**

    -   TLM lifecycle record identifiers are automatically generated on creating a TLM record using the Technology Lifecycle Management \(sn\_apm\_tpm\) plugin version 1.9.0. However, for TLM lifecycle records generated using previous versions of the TLM plugin don't have any lifecycle record identifiers. The TLM record identifiers of these TLM lifecycle records must be generated using the Populate Number field in **TPM Discovered Technologies** job. For information, see [Run a scheduled job to populate Technology Lifecycle Management lifecycle record identifier](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-run-job-to-populate-tpm-lifecycle-identifier.md).

    -   You can zoom on this page to 200% or 400% through your browser settings without the loss of content or functionality. Page layouts are transformed into a vertical, stacked view automatically.

\[Omitted image "eaw-tpm-lifecycle-process.png"\] Alt text: TLM lifecycle process in EA Workspace

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

## Update TLM Data for a business application or application service

You can manually refresh the TLM life-cycle data manually for a selected business application or application service. A scheduled job **Populate TPM Discovered Technologies and Life-cycles** is also run on schedule or on-demand to update the life-cycle data for all business applications and application services​​. For more details, see [Update TLM data for a business application or application service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/update-tpm-data.md) and [Run a scheduled job to generate TLM lifecycle data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-run-scheduled-job-update-tpm-data.md).

## View insights for technology life-cycle risks

You can track the technology lifecycle risk for business applications, application services, servers, software products, and hardware models. The**Populate TPM Discovered Technologies and Life-cycles** scheduled job shows the lifecycle results in the **Insights** section of the EA Workspace home page. Select the **Technology Portfolio** tab in the **Insights** section and then select the **View all technology lifecycle risks**.\[Omitted image "eaw-tpm-insights.png"\] Alt text: Insights for Technology Lifecycle risks

-   Use this filter to see the risks for the next 1 month, 3 months, 6 months, 12 months, and 18 months. By default, the 1 month filter is applied.
-   Use the **Show only production instances** toggle button to see only production instances that are having technology lifecycle risks. By default, this filter is off.
-   Select the **View all technology lifecycle risks** link to see the list of all technology lifecycle risks sorted by earliest lifecycle date. This is the earliest date when a technology lifecycle risk is to happen. You can export the information to Excel, CSV, JSON, or PDF as required.

    The data in the Technology lifecycle risks table is fetched from the TLM Discovered Technologies \[sn\_apm\_tpm\_discovered\_technology\] table.

-   Execute the Populate Technology Lifecycle Risks scheduled job to generate the TLM technology lifecycle risks. This scheduled job populates the risk scores for business applications \(BA\), application services \(AS\), software products, and hardware models. The scores are calculated for a fiscal period of type month in the Technology lifecycle risks \(sn\_apm\_tpm\_technology\_risk\) table. For more details, see [Schedule a job to generate TLM technology risk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-schedule-job-generate-tpm-risk.md).

## View TLM analysis run logs

You can track the progress of TLM analysis by examining the TPM Discovered Technology Run Logs \[sn\_apm\_tpm\_discovered\_technology\_run\_log\] table. Each time the analysis is run, an entry is added to this table. Navigate to **EA Workspace** &gt; **Setup** &gt; **Logs** section view the logs.

## TLM lifecycle timelines on Gantt chart

For the Technology Lifecycle Management \(TLM\), the business applications and their related application services \(associated hardware models and software products\) are displayed in a hierarchical structure. The corresponding timelines of the application services are displayed as bars on the Gantt chart.

The application services \(composed of software products and hardware models\) have lifecycle timelines determined for them. On the Gantt chart, the earliest TLM phase start date of either the software products or hardware models are rolled up. This calculates the TLM phase start date of the overall application service. That is, the earliest TLM phase start date of any software product or hardware model is taken as the TLM phase start date of the application service, overall. For more details, see [TLM lifecycle timelines on Gantt chart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-tpm-lifecycle-timelines-on-gantt-chart.md) and [View TLM and TRM lifecycle timelines on the Gantt chart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-view-tpm-and-trm-lifecycle-timelines-in-gantt-chart.md).

\[Omitted image "TPM-gantt-chart.png"\] Alt text: TLM Gantt chart

## Data visualization for TLM data

In the Enterprise Architecture Workspace Dashboard, the 'Top 10 business applications with normalized TLM risk' widget shows the top 10 business applications having normalized TLM risk. For more details, see [Explore the Enterprise Architecture Workspace dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-workspace-dashboard.md).

-   **[Technology risk calculation in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-technology-risk-calc.md)**  
Assess the technology risks of your business applications by calculating their risks. Technology risks are calculated at the hardware model and software product levels to determine the risk at the business application level.
-   **[Working with technology portfolio audit details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-view-technology-portfolio-audit-risk.md)**  
The  **Technology portfolio audit** tab shows audit information for your applications. An entry in this table indicates that at least one lifecycle for that software product or hardware model was either approximated, or not found, or doesn’t exist.

**Parent Topic:**[Exploring Technology Portfolio view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-technology-portfolio-view.md)

**Related topics**  


[Working with Technology Lifecycle Management \(TLM\) in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-work-with-tpm.md)

[Gantt view of TLM and TRM lifecycle timelines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-gantt-view-of-tpm-and-trm-lifecycle-timelines.md)

[TLM lifecycle timelines on Gantt chart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-tpm-lifecycle-timelines-on-gantt-chart.md)

[View TLM and TRM lifecycle timelines on the Gantt chart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-view-tpm-and-trm-lifecycle-timelines-in-gantt-chart.md)

