---
title: ERP Canvas content packs
description: Use ERP Canvas content packs as examples to help you implement and deploy applications faster with less manual work.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-development/erp-integration-framework/erp-canvas-content-packs.html
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2025-02-27"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, content, pack, content pack, model]
breadcrumb: [Building and managing ERP models to work with ERP data, Using ERP models, extraction tables, and remote tables, ERP Canvas, Building low-code applications, Developing your application, Building applications]
---

# ERP Canvas content packs

Use ERP Canvas content packs as examples to help you implement and deploy applications faster with less manual work.

**Note:** Currently, content packs work only with SAP systems.

ERP Canvas content packs are sets of pre-defined models and process extensions that are useful examples for developers with little or no SAP domain knowledge. For instance, you are integrating a ServiceNow application with SAP, but it's taking a long time because of the complexity of the SAP data. Content packs accelerate the work so that building uses cases involving SAP data becomes a faster process that more developers can accomplish.

After installing a content pack, the models it contains are listed on the ERP Canvas models page with a prefix of **DP**. The process extensions in the content pack are listed on the **Subflows** tab in Workflow Studio with a prefix of **ERP DP**.

Content pack models and process extensions are examples. Use them as accelerators that can be tailored to your requirements. The models and process extensions can't be edited, but can be viewed. If you see a model that looks similar to the integration you're trying to create, clone the model, give it a unique name, and edit it as needed. If you find a process extension you want to use, copy, rename, and edit the models it contains as needed.

## Prerequisites

You must have:

-   ERP Canvas installed
-   A linked SAP system from which to pull data
-   The sn\_erp\_integration.erp\_admin role

## Install from the ServiceNow Store

For detailed information about buying and installing an application, see the [ServiceNow Store Help](https://store.servicenow.com/$appstore.do#!/store/helpcenter) page.

-   **[ERP Canvas content pack process extensions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-content-pack-process-extensions.md)**  
Use the process extensions in ERP Canvas content packs as examples that can be copied to add subflows with business logic to one or more models.
-   **[Explore an ERP Canvas content pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-explore-a-content-pack.md)**  
Explore an ERP Canvas content pack to see what it contains, including models and process extensions. Content pack models and process extensions are examples.
-   **[Using ERP Canvas content packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-using-content-packs.md)**  
Learn how to use ERP Canvas content packs, from cloning a model to working within a scope. Content pack models and process extensions are examples.
-   **[Using ERP Canvas process extensions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-using-process-extensions.md)**  
Learn how to use the process extensions \(subflows\) in ERP Canvas content packs. Content pack models and process extensions are examples.
-   **[Available ERP Canvas content packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-available-content-packs.md)**  
The following content packs are available for use in ERP Canvas to implement and deploy applications faster with less manual work.
-   **[ERP Canvas Enterprise Data Foundation content pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-enterprise-data-foundation-content-pack.md)**  
Find details about the models and process extensions in the ERP Canvas Enterprise Data Foundation content pack.
-   **[ERP Canvas Quote to Cash content pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-sales-order-content-pack.md)**  
Find details about the models and process extensions in the ERP Canvas Sales Order content pack.

**Parent Topic:**[Building and managing ERP models to work with ERP data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/work-with-erp-data-models.md)

