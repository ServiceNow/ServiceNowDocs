---
title: CSDM implementation stages — Walk
description: In the Walk stage, you identify and populate the network infrastructure CIs and applications that your organization's technical teams support.
locale: en-US
release: xanadu
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Implement, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CSDM implementation stages — Walk

In the Walk stage, you identify and populate the network infrastructure CIs and applications that your organization's technical teams support.

## Benefits of the operations that you perform in the Walk stage

-   **Managing discovered infrastructure CIs**

    The operations facilitate managing the discovered infrastructure CIs. You might manually managing the metadata on these CIs, such as support group and technical approval group. By identifying the technical service offering that manages these CIs, you can manage the following items:

    -   Configure the instance to populate and synchronize this metadata onto the related child objects.
    -   Eliminate the manual effort of maintaining the metadata on thousands of CIs.
-   **View supported CIs**

    The operations establish a view of the CIs that your organization's technical teams support.

    You can see the specific support assignments, which you can change as needed based on your support structure, operational-level agreements \(OLAs\), and commitments.

    Also, this view enables you to formalize for your process for supporting applications and technology owners.

-   **Prepare for Service Portfolio Management**

    The operations build the foundation for using Service Portfolio Management \(SPM\).

    You can start using Service Portfolio Management more quickly because your service data are in the right place.

-   **Use the request catalog**

    The operations enable you to order technology service offerings through the request catalog. You can also automate ordering some offerings to enhance the request workflow and update or create related CIs. Catalogs are described in detail in [Service Catalog](../../service-catalog-management/concept/service-catalog.md).

    **Note:** The request catalog is not a CMDB table.

-   **Prepare for ITOM\) products**

    The operations build the foundation for Information Technology Operations Management \(ITOM\) products, such as Service Mapping and Discovery.

-   **Enable Automation**

    The operations enable more automated methods of grouping CIs for identification and management by Technical Service Offerings.


## Tables that you work on during the Walk stage

The walk stage includes base-system CMDB tables that identify the technology provider.

**Note:** Some of the classes that you implement in this stage are logical CIs. Logical CIs aren’t created through Discovery, so their **Model ID** values might not refer to product model \(application model, service model, or software model\) records. To help you to migrate to a product-centric management paradigm, each instance of a logical CI should be associated with a product model. See [Auto-generate product models for logical CIs](../task/csdm-auto-create-prod-model-for-ci.md).

![Tables that you work on during the Walk stage.](../image/walk-stage.png)

-   **Technical service table \[cmdb\_ci\_service\_technical\], or \[cmdb\_query\_based\_services\] for Event Management**

    The Technical service table has a service classification of "technical service". This base-system CMDB table identifies the provider of the technology that your business consumes.

-   **Technology service offering table \[service\_offering\]**

    A Technical service offering is a service offering with a service classification of "technical service". Technical service offerings may be further divided as follows:

    -   Location and geography
    -   Environment \(production or non-production\)
    -   Pricing
    -   Availability
    -   Support group \(for Incident Management\)
    -   Technical approval group \(for Change Management\)
    -   Packaging options \(commitments\)
    The technical service offering comes from the service, based on how the parent serves a specific technical need. Every operational technical service must be associated with at least one technical service offering.

    **Note:** Not all technical service offerings have to be related to applications or infrastructure CIs. Managed Service Providers can provide technical service offerings.

-   **Dynamic CI group table \[cmdb\_ci\_query\_based\_service\]**

    A Dynamic CI group is a collection of CIs based on the results of saved Query Builder queries, encoded queries, or manual entries. Query Builder is described in [Exploring CMDB Query Builder](../../configuration-management/concept/querying-cmdb.md). For more information about Dynamic CI groups and how you can use them, see [Manage Technical Services domain of the CSDM framework](manage-tech-servs-domain.md).


**Parent Topic:**[Implementing the CSDM framework in stages](csdm-implementation-stages.md)

