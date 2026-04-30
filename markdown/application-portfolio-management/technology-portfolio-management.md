---
title: Technology Portfolio Management
description: The underlying technologies of the business applications used in your business enterprise have a shelf life that must be actively managed and diligently monitored to track their versions and life cycle. Use the timeline view of the Technology Portfolio Management to track their dates, and then create a demand or a project to upgrade or retire them.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Explore, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Technology Portfolio Management

The underlying technologies of the business applications used in your business enterprise have a shelf life that must be actively managed and diligently monitored to track their versions and life cycle. Use the timeline view of the Technology Portfolio Management to track their dates, and then create a demand or a project to upgrade or retire them.

**Important:**

Starting with the Xanadu release, the legacy Technology Portfolio Management module is moved to the Enterprise Architecture Workspace. To learn more, see [Managing the Technology Portfolio Management \(TPM\) in Enterprise Architecture Workspace](eaw-concept/eaw-tpm.md).

The technology of a business application is also known as a software model. A software model is a specific version or configuration of software.

The software models used in your business applications can be operating systems, database management systems, development tools, and middleware, each of which has a life cycle. If these life-cycle stages are not tracked, there are risks where the vendor may not support them any longer and the business applications that run on these technologies are at stake.

Creating an inventory of all technologies used in the enterprise helps to:

-   Track the versions of the software and manufacturer support dates for the software.
-   Set an internal life-cycle guidance for the software.
-   Assess the risks in using outdated software.
-   Plan to retire them just like the applications they support, at a definite date.
-   Support upgrade processes.

## Internal and external lifecycle stages of the software product

The business applications used in your organization are all linked to one or more application services. Each of the application services runs on one or more technologies or software models.

**Note:** In the context of Application Portfolio Management, an application instance is an application service.

The software product \(each model and full version\) has a sequence of life cycle stages/phases from its installation to retirement. Internally, business organizations set a date based on the life-cycle phase of the software products. These phases can be Early Adopter, Mainstream, Declining use, and Retired.

The vendor also sets a date for the software based on the vendor life-cycle phases such as Pre-release, General Availability, End of Life, and Obsolete. The support from the vendor may vary depending on the phase of the technology. When the software model reaches the stage of obsolescence, the vendor may stop supporting the technology.

**Note:** The **Publisher** choice type of the **Lifecycle type** field in the [Software Product Lifecycle](https://www.servicenow.com/docs/access?context=record-terms-software-licenses&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US) form is the same as the External Lifecycle that is being used in Enterprise Architecture.

As a software asset management user or a software model manager, you can add the software product life-cycle details to the software model for each full version. To use a TPM screen with data on the timeline, ensure that the software life-cycle data is populated in the software product life-cycle table. Similarly, ensure that the hardware life-cycle data is populated in the hardware model table after the technology model suggestion engine runs.

## Integration with Service Mapping to use Technology Portfolio Management

Create application instances in the Mapped Application Service \[cmdb\_ci\_service\_discovered\] table and relate business applications to corresponding application services.

Enterprise Architecture no longer integrates with Service Mapping through the **Instances** tab. The application **Instances** tab has been removed and the apm\_app\_instance table has been deprecated, which is replaced by the Mapped Application Service \[cmdb\_ci\_service\_discovered\] table. Any data existing in the application instances table must be migrated to the application service table. If you are upgrading to the Madrid release, then contact the ServiceNow personnel for migrating the data.

**Note:** If you are using the Mapped Application Service \[cmdb\_ci\_service\_discovered\] table for application instances, then you can proceed to upgrade from Kingston. However, if you are using the deprecated apm\_app\_instance table to store application instances, then migrate the data in the apm\_app\_instance table to the Mapped Application Service \[cmdb\_ci\_service\_discovered\] table.

![APM or TPM dependencies in mature ServiceNow implementation](../image/APMTPMDependency.png "Connecting software product life cycles to business application")

## TPM depends on Software Asset Management \(SAM\) to retrieve the technology information of the software product

**Warning:** TPM and TRM require installation of either SAM Foundation or SAM Professional. Before installing the SAM Foundation plugin, carefully review the [Software Asset Management Foundation plugin migration](https://www.servicenow.com/docs/access?context=c_SAMMigrationSAMF&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) documentation. Contact ServiceNow Support if you do not have either SAM Foundation or SAM Professional installed on your instance.

You can use Technology Portfolio Management even if you do not have Software Asset Management \(SAM\) installed. A preconfigured Software Product Model table is available to all TPM users. You can create a list of all software models that your organization uses either manually or import from an existing database or source.

![Connecting software lifecycles to business application](../image/APMSAMDependency.png "Connecting software product life cycles to business application")

Using TPM depends on SAM plugins. The dependency is as follows:

-   **With SAM Premium plugin**

    To access the Product Classification \[samp\_sw\_product\] table, you need the Software Asset Management Premium plugin. Reference to samp\_sw\_product\_classification is in samp\_sw\_product table. This content table is referenced in the Software Product Model \[cmdb\_software\_product\_model\] table to retrieve the technology information. Subscribing to the SAM Premium plugin enables you to view the applications by Business Applications as well as by Product Classification in the TPM timeline.

    ![TPM timeline showing By Product Classification view](../image/tpm-by-product-class_v2.png "TPM timeline showing By Product Classification view")

-   **Without SAM plugin**

    Product classification is not available without this plugin. Viewing by Product Classification is not available in the TPM timeline view. Software model information is retrieved from the SW Product Model \[cmdb\_software\_product\_model\] table. Populate this table manually or export the content from an excel sheet.


**Related topics**  


[View technology risks in timeline](../task/view-technology-risks-in-timeline.md)

[Relate business application to application service using CI relationship editor](../task/relate-business-application-to-business-service.md)

[Associate an application service to hardware model](../task/associate-application-service-hardware-model.md)

[Associate an application service to a software model](../task/associate-business-service-to-software-model.md)

[Create a risk parameter](../task/create-risk-parameters.md)

[Technology risk calculation](technology-risks-calculation.md)

[Run scheduled job to generate risk values](../task/run-scheduled-job-to-calculate-risks.md)

