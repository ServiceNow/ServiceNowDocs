---
title: Apply the CSDM guidelines to Digital Portfolio Management
description: Service data relates to each other using different applications and in different ways. Digital Portfolio Management \(DPM\) references the Common Service Data Model \(CSDM\) framework to bring service-related data together in a single view.
locale: en-US
release: australia
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Digital Portfolio Management, IT Service Management]
---

# Apply the CSDM guidelines to Digital Portfolio Management

Service data relates to each other using different applications and in different ways. Digital Portfolio Management \(DPM\) references the Common Service Data Model \(CSDM\) framework to bring service-related data together in a single view.

DPM enables you to organize service data in logical sequences that make sense for your business. You can see details about your own services as well as services that you don't own but may impact your business.

**Tip:** For CSDM set-up information, see [Implementing the CSDM framework in stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/common-service-data-model-csdm/csdm-implementation-stages.md).

## Personal portfolios and CSDM

See how DPM aligns with the CSDM framework to provide a holistic view of your IT landscape.

![DPM-and-CSDM.](../image/DPM_and_CSDM_infographic_V2-03.png "DPM and CSDM")

## CSDM life-cycle fields for business and technology management services

Service portfolios viewed in DPM display the phase \(or stage\) field and the status field in the header of each business and technology management service and service offering. The field values come from the service table \[cmdb\_ci\_service\].

**Important:** For the Australia release and later, the labels for the items in the \[cmdb\_ci\_service\_technical\] table and \[service\_offering\] table are Technology Management Service and Technology Management Service Offering, respectively. The label changes align with the CSDM, version 5. Prior to the Australia release, the labels are technology management service and technology management service Offering.

The following comparison shows the differences from the traditional Service Portfolio Management phase and status fields to the CSDM life-cycle stage and status fields.

These fields also display when you use the Performance Analytics \(PA\) indicators.

|Service Portfolio Management Phase and Status field names|CSDM life-cycle Stage and life-cycle Status field names|
|---------------------------------------------------------|-------------------------------------------------------|
|Pipeline \| Requirements|Ideation \| Under evaluation|
|Pipeline \| Definition|Ideation \| Under evaluation|
|Pipeline \| Analysis|Ideation \| Under evaluation|
|Pipeline \| Approved|Ideation \| Under evaluation|
|Pipeline\| Chartered|Design \| Chartered|
|Catalog\| Design|Design \| Design|
|Catalog \| Development|Design \| Design|
|Catalog \| Build/Test/Release|Deploy \| Test|
|Catalog \| Operational|Operational \| In-use|
|Catalog \| Retiring|Operational \| Pending Retirement|
|Retired \| Retired|End of life \| Retired|
|Retired \| Obsolete|End of life \| Obsolete|

## CSDM relationships in DPM

To confirm that you see the data that you want in DPM, you must establish the correct CSDM relationships.

How you establish relationships between your solutions and configuration items \(CIs\) varies depending on your situation. For more information, see [CI relationships in the CSDM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/common-service-data-model-csdm/ci-relationships.md).

-   **[CSDM terms for Digital Portfolio Management](dpm-common-terms.md)**  
Because both ServiceNow® products of Digital Portfolio Management \(DPM\) and Service Portfolio Management closely align with the Common Service Data Model \(CSDM\), it's helpful to know the common terms when working in these applications.

**Parent Topic:**[Configuring Digital Portfolio Management](../concept/dpm-configure-cfw.md)

**Related topics**  


[CSDM terms for Digital Portfolio Management](dpm-common-terms.md)

[Implementing the CSDM framework in stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/common-service-data-model-csdm/csdm-implementation-stages.md)

