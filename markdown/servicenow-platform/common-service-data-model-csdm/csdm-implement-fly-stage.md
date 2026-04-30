---
title: CSDM implementation stages — Fly stage
description: When you reach the Fly stage, you've accomplished all or most of the process of implementing the CSDM framework. The fly stage completes the process.
locale: en-US
release: yokohama
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Implement, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CSDM implementation stages — Fly stage

When you reach the Fly stage, you've accomplished all or most of the process of implementing the CSDM framework. The fly stage completes the process.

## Benefits of the operations that you perform in the Fly stage

-   **The Fly stage is a foundation for using APM capabilities**

    You can use APM capabilities to rationalize your business applications. Ask questions such as the following:

    -   Are you spending too much on your business capabilities?
    -   Are you spending too little on your business capabilities?
    -   Should you increase the amount you spend on emerging business capabilities?
-   **The Fly stage is a foundation for using APM with Service Portfolio Management capabilities**

    You can use APM with Service Portfolio Management capabilities to rationalize your business services and related offerings. Ask questions such as the following:

    -   Are you spending too much or too little on services?
    -   Are you spending too little or too little on services?
    -   Are they the right services compared to emerging capabilities?
-   **The Fly stage is a foundation for using ITSM capabilities**

    Use a request catalog to relate a service offering to a catalog item. You can also enhance the request workflow to automatically populate the “Subscribe by” table. Service catalogs are described in detail in [Service Catalog](../../service-catalog-management/concept/service-catalog.md).

    **Note:** The request catalog is not a CMDB table.

-   **The Fly stage can hep you to manage business services**

    If your environment has a combination of CIs from each of the CSDM domains, this stage provides away to manage business services.

-   **The Fly stage is a way to identify the types of data that may be contained in or used by your business applications**

    The information object table helps you see what's in your information portfolio.


## Tables that you work on during the Fly stage

You reach the fly stage after you have accomplished all or most of the earlier stages.

![Tables that you work on during the Fly stage.](../image/fly-stage.png)

**Note:** Some of the classes that you implement in this stage are logical CIs. Logical CIs aren’t created through Discovery, so their **Model ID** values might not refer to product model \(application model, service model, or software model\) records. To help you to migrate to a product-centric management paradigm, each instance of a logical CI should be associated with a product model. See [Auto-generate product models for logical CIs](../task/csdm-auto-create-prod-model-for-ci.md).

The fly stage completes the remaining aspects of CSDM framework:

-   **Business capability table \[cmdb\_ci\_business\_capability\]**

    A business capability is a high-level capability that supports a business model or fulfills a mission for your organization.

-   **Information object table \[cmdb\_ci\_information\_object\]**

    You capture asset information as information objects. You can connect the information objects to your business applications to create an application portfolio that you can use at any time.

    You can use the Information Object table to identify the types of data that a business application uses, including highly sensitive data such as:

    -   Personally Identifiable Information \(PII\)
    -   Payment Card Industry Data Security Standard \(PCI DSS\) data
    -   Health Insurance Portability and Accountability Act \(HIPAA\) data
    Information objects are part of the information portfolio. The information portfolio links to the following data:

    -   Data Domains: Total number of records in the Data Domain table \[sn\_apm\_data\_domain\].
    -   Information Objects: Total number of records in the Information Object table \[cmdb\_ci\_information\_object\].
    -   Database Instances: Total number of records in the Database Instance table \[cmdb\_ci\_db\_instance\].
    -   Database Catalogs: Total number of records in the Database Catalog table \[cmdb\_ci\_db\_catalog\].
    **Important:** You might need to implement the Information object table \[cmdb\_ci\_information\_object\] as part of an earlier stage. Your business requirements determine the right stage for implementing the table.

-   **Request catalog**

    Users request services through the request catalog. The request catalog is not a CMDB table. Catalogs are described in detail in [Service Catalog](../../service-catalog-management/concept/service-catalog.md).

-   **The fly stage includes these components:**
    -   Business service portfolio table \[service\_portfolio\]
    -   Business service table \[cmdb\_ci\_service\_business\]; \(service classified as a "business service"\)
    -   Business service offering table \[service\_offering\]; \(service offering classified as a "business service"\)

**Parent Topic:**[Implementing the CSDM framework in stages](csdm-implementation-stages.md)

