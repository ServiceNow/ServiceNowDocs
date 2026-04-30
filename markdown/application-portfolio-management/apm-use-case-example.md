---
title: Enterprise Architecture \(formerly Application Portfolio Management\) use case - Legacy
description: Enterprise Architecture lets you define a single, version-agnostic entity that represents all instances, technologies, and data used for planning and reporting.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Enterprise Architecture and CSDM framework - Legacy, Configure - Legacy, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Enterprise Architecture \(formerly Application Portfolio Management\) use case - Legacy

Enterprise Architecture lets you define a single, version-agnostic entity that represents all instances, technologies, and data used for planning and reporting.

**Important:**

Starting with the Xanadu release, most Enterprise Architecture \(formerly Application Portfolio Management\) capabilities are available through the Enterprise Architecture Workspace.

Features such as data certification, application assessments, and total cost of ownership \(TCO\) are now accessed and managed from the Enterprise Architecture Workspace, not from the legacy APM pages. To learn more about Enterprise Architecture Workspace, see [Enterprise Architecture Workspace](ea-workspace.md).

## Enterprise Architecture use case

You can use a business application for planning and governance activities, such as funding, road mapping, and risk reporting. Rationalizing business applications is a continuous process, and is critically important to reducing costs and planning technology transformations. Rationalizing business applications is also critical for completing mergers, divestitures, or other broad-impact business-led changes.

## Key features of the Enterprise Architecture use case

The CMDB, when used by the CSDM framework, provides value to Enterprise Architecture in the following ways:

-   Application life cycle management. This includes:
    -   Registering a new business application \(included in the base system\).
    -   Updating a business application
    -   Decommissioning a business application, including all the related application services and infrastructure. Because application services are logical in nature, they should use the Logical life cycle states. Application services follow the same life cycle guidance as any other logical CI.
-   Business application portfolio assessments based on metrics or related impacts.
-   Roadmap planning and creating new ideas, demands and projects.
-   Data certification process
-   Total cost of ownership \(TCO\) calculations \(using the Financial Management module\)
-   Manage the following related entities:
    -   Information objects table \[cmdb\_ci\_information\_object\]
    -   Business capabilities table \[cmdb\_ci\_business\_capability\]

## Results of the Enterprise Architecture use case

With this use case, CSDM provides Enterprise Architecture a consistent way to model business applications and relate critical data. The use case ensures that the application services \(instances\) are defined as required for automating the technology risk scores, costs, and other metrics used for analysis.

## TPM use case

TPM gives you a better understanding of the risks associated with using software and hardware that is at the end-of-life \(EOL\) date. You can use the details provided by the CSDM framework to determine the risk of using software and hardware that is at EOL. Each product life cycle EOL date is calculated, then combined following the CSDM framework to provide a score at the Business Application level.

## Results of the TPM use case

The CSDM framework provides a consistent data structure. This consistent data structure makes it easier for you to manage the life cycles of your technology and analyze the combined technology risks.

Because of the way the CSDM framework is structured, you can leverage many products from ITOM, Service Management \(Service Portfolio Management\), and IT Application Management \(ITAM\).

The risks of using EOL technologies are calculated based on the life cycle of each software and hardware product model identified in the CMDB, and matched with a software and hardware product model.

You can enter the life-cycle data manually, import it from an external source, or use the data provided with your Software Asset Management Professional or Hardware Asset Management license.

The risks are calculated and displayed in a hierarchy. Business application is at the top level, SDLC Components are under the business application, then Application Services indicate each deployment \(instance\), and software and product models are at the lowest level. Risks are calculated in the order shown below, and are based on the time span between the current date and the EOL date.

**Note:** Configuring SDLC component is optional. Even without SDLC component configuration, you can connect business applications with the application services directly.

1.  Hardware and software product model — Displays the current life-cycle phases, sources, and indicates the specific models at-risk
2.  Application Service level — Displays the combined risk status of all underlying hardware and software product models used in the Application Service \(Instance\).
3.  SDLC Component — Displays the SDLC components along with the associated application services and business applications
4.  Business application level — Combines all the underlying Application Service \(Instances\) to determine the overall risk rating at a portfolio level.

The following information is used to determine the EOL impact to business applications and their installed application services \(instances\):

-   The business applications used in your organization are all linked to one or more application services. Each of the application services run on one or more technologies or software models.

    The name of the Application Service Software model table is \[sn\_apm\_tpm\_service\_software\_model\].

-   The software model has a sequence of life-cycle stages. The life-cycle stages range from the installation date to the retirement date.

    Some business organizations set an internal date based on the life-cycle phase of the software models. These software model phases can be Early Adopter, Mainstream, Declining use, and Retired.

    Similarly, the software vendors might also set a date for the software based on the vendor life-cycle phases, such as Pre-release, General Availability, End of Life, and Obsolete. Vendor support might vary depending on the phase of the technology. For example, when the software model reaches the Obsolete phase, the vendor might stop supporting the technology.

    The Software Model Life cycle table is named \[sam\_sw\_model\_lifecycle\].


**Parent Topic:**[Enterprise Architecture \(EA\) \(formerly Application Portfolio Management\) and the CSDM framework - Legacy](apm-use-case-product-view.md)

