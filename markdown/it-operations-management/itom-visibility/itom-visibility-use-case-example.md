---
title: ITOM Visibility use case
description: The ITOM Visibility use cases are described in this section.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-operations-management/itom-visibility/itom-visibility-use-case-example.html
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ITOM Visibility and CSDM reference, ITOM Visibility, IT Operations Management]
---

# ITOM Visibility use case

The ITOM Visibility use cases are described in this section.

## Discovery use case

-   Gain increased visibility into your on-premises and cloud resources.
-   Keep track of changes in your on-premises, cloud, and serverless infrastructure in the Configuration Management Database \(CMDB\).
-   Set a strong foundation with accurate data and relationship views for ServiceNow products, including Change Management, Software Asset Management, Customer Service Management \(CSM\), and Security Operations.

## Key features of the Discovery use case

-   Set up and manage Discovery jobs.
-   See IT resources and dependencies at-a-glance.
-   Build queries to validate discovered IT resources.
-   Manage your public key infrastructure \(PKI\) certificates in one dashboard.

## Results of the Discovery use case

The CSDM framework gives Discovery a prescribed model for how infrastructure and software CIs relate to other areas, such as application services, business applications, and assets.

## Service Mapping use case

You can create application services manually, using an API, or by having Service Mapping discover them. Regardless of creation method, all application services are stored in the Mapped Application Service table \[cmdb\_ci\_service\_discovered\].

## Results of the Service Mapping use case

Service Mapping automates a critical aspect of CSDM with a consistent, automated approach to connect the logical layer of the CSDM model to the physical model CIs in the CMDB. This approach lets you more effectively manage your business applications. The approach also enables you to automate modeling of your business applications for impact assessment and analysis. For impact assessments and analysis, you can use a number of ServiceNow products including Change Management, Incident Management, or the CMDB Query Builder.

\[Omitted image "itom-visibility-flow.png"\] Alt text: Application Services flow.

## Application services view in Operator Workspace

You can specify a life-cycle status for an application service. Application services with an Operational life-cycle status can be used on service maps for the relevant workflows, such as Artificial Intelligence for IT Operations \(AIOPs\) workflows.

\[Omitted image "lifecycle-status-app-svcs.png"\] Alt text: Life-cycle status for application services.

You can view information about the services, such as the criticality, in the Operator Workspace.

\[Omitted image "operator-workspace.png"\] Alt text: Operator Workspace.

The Service Map tab displays a visual representation of the service.

\[Omitted image "service-map-diagram.png"\] Alt text: Service map diagram.

**Related topics**  


[Document life cycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/common-service-data-model-csdm/csdm-lifecycle-document.md)

[Hardware life cycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/common-service-data-model-csdm/csdm-lifecycle-hardware.md)

[Location life cycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/common-service-data-model-csdm/csdm-lifecycle-location.md)

[Logical life cycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/common-service-data-model-csdm/csdm-lifecycle-logical.md)

[Product life cycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/common-service-data-model-csdm/csdm-lifecycle-product.md)

