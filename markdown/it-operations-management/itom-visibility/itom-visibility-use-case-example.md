---
title: ITOM Visibility use case
description: The ITOM Visibility use cases are described in this section.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ITOM Visibility and CSDM reference, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
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

![Application Services flow.](../../csdm-implementation/image/itom-visibility-flow.png "Application Services flow")

## Application services view in Operator Workspace

You can specify a life-cycle status for an application service. Application services with an Operational life-cycle status can be used on service maps for the relevant workflows, such as Artificial Intelligence for IT Operations \(AIOPs\) workflows.

![Life-cycle status for application services.](../../csdm-implementation/image/lifecycle-status-app-svcs.png)

You can view information about the services, such as the criticality, in the Operator Workspace.

![Operator Workspace.](../../csdm-implementation/image/operator-workspace.png "Operator Workspace")

The Service Map tab displays a visual representation of the service.

![Service map diagram.](../../csdm-implementation/image/service-map-diagram.png "Service map diagram")

**Parent Topic:**[ITOM Visibility and CSDM reference](itom-visibility-use-case-product-view.md)

**Related topics**  


[Life cycle of document and contract entities](https://www.servicenow.com/docs/access?context=csdm-lifecycle-document&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

[Life cycle of tangible/physical CIs](https://www.servicenow.com/docs/access?context=csdm-lifecycle-hardware&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

[Life cycle of location entities](https://www.servicenow.com/docs/access?context=csdm-lifecycle-location&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

[Life cycle of intangible/logical entities](https://www.servicenow.com/docs/access?context=csdm-lifecycle-logical&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

[Life cycle of product entities](https://www.servicenow.com/docs/access?context=csdm-lifecycle-product&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

