---
title: Auto-generate product models for logical CIs
description: Use the CSDM Product Model Assignment job to auto-generate a product model record \(application model, service model, or software model\) for each logical CI that is not yet associated with a product model. Product models are ideal for associating CIs that are parts of a single digital product.
locale: en-US
release: zurich
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Foundation tab on the dashboard, Reference, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Auto-generate product models for logical CIs

Use the CSDM Product Model Assignment job to auto-generate a product model record \(application model, service model, or software model\) for each logical CI that is not yet associated with a product model. Product models are ideal for associating CIs that are parts of a single digital product.

## Before you begin

Users with read access to modified CI records can view the new product models.

Role required: admin

## About this task

Application, service, and software class instance CIs are not created through Discovery, so their **Model ID \[model\_id\]** values might not refer to product model records. To assist you in migrating to a product-centric management paradigm, each instance of a logical CI should be associated with a product model. The CSDM Product Model Assignment job operates on the following classes and uses the name of the class instance as the name of the new product model.

-   Service Offering
-   Technology Management Service \(formerly Technical service\)
-   Service Instance \(called application service before CSDM v5\): The script adds the version \(as it relates to the business application\) to the associated software model name. For example, the software model for the MyAppService service instance CI might be **MyAppService - version: 2.1**.
-   Business Service
-   Business Application

The CSDM Product Model Assignment job calls the CSDMModelUtil script. The script performs these actions for each instance of the supported CSDM classes that does not refer to a product model:

1.  Create a new application model, service model, or software model record with the same name as the CI. If the requisite info for generating the name value does not appear in the CI, the script uses the default value that you specified.
2.  For the CI, add a reference to the new product model in the **Model ID \[model\_id\]** field.

Operation of the script:

-   The script observes the access rules of the CMDB admin that runs the script.
-   If an auto-generated product model record for a class instance CI would be identical to an existing record, then the existing record is used for that CI.
-   If your data includes CIs with identical names \(this is actually an error\), then the resulting model\_id values might conflict. Validate the resulting model\_ids after running the script.

## Procedure

1.  Specify the default name to use if the name / version values of a CI are insufficient to auto-generate the name for the new product model.

    1.  Navigate to **Configuration** &gt; **CI Class Manager** and then select **Open Hierarchy**.

    2.  Navigate to each of the supported classes in turn \(service instance, business service, and so on\).

    3.  On the **Basic Info** page for the class, enter a name in the **Default Product Model** field.

        ![Specify the default name to use for new product models.](../image/csdm-ci-class-mgr-basic-info.png)

2.  Run the CSDM Product Model Assignment job.

    1.  Navigate to **System Scheduler** &gt; **Scheduled Jobs** &gt; **Scheduled Jobs**.

    2.  Search for and open the CSDM Product Model Assignment job.

    3.  Select **Execute Now**.

    The script runs and generates the product models.

3.  Review the created product models to ensure that the new **Model ID \[model\_id\]** values are correct.

    Use:

    -   **All** &gt; **Product Catalog** &gt; **Product Models** &gt; **Application Models**
    -   **All** &gt; **Product Catalog** &gt; **Product Models** &gt; **Service Models**
    -   **All** &gt; **Product Catalog** &gt; **Product Models** &gt; **Software Models**
4.  Run the job whenever you want to create product model settings for new class instances.


**Parent Topic:**['Foundation' stage reports on the CSDM Data Foundations dashboard](../reference/csdm-datafdn-dash-foundation-tab.md)

