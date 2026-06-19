---
title: Using Zero Copy Connector for ERP process extensions
description: Learn how to use the process extensions \(subflows\) in Zero Copy Connector for ERP data products. Data product models and process extensions are examples.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/erp-integration-framework/erp-canvas-using-process-extensions.html
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, content, pack, content pack, process, extension]
breadcrumb: [Data products, Building models, Use, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Using Zero Copy Connector for ERP process extensions

Learn how to use the process extensions \(subflows\) in Zero Copy Connector for ERP data products. Data product models and process extensions are examples.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

Follow these steps to copy a process extension \(subflow\) and edit the copy to use the correct cloned model or models. Use the cloned version of the models or models inside your copy of the subflow.

**Note:** You must have a cloned model created within its own application scope. For more information, see [Using Zero Copy Connector for ERP data products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-canvas-using-content-packs.md).

Before completing the procedure, it may be helpful to review the following pages:

-   [Zero Copy Connector for ERP data product process extensions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-canvas-content-pack-process-extensions.md)
-   [Available Zero Copy Connector for ERP data products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-canvas-available-content-packs.md)
-   [Explore a Zero Copy Connector for ERP data product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-canvas-explore-a-content-pack.md)

## Procedure

1.  Navigate to **All** &gt; **Workflow Studio** and select **Subflows**.

    \[Omitted image "erpc-process-extensions-explore1.png"\] Alt text: Workflow Studio subflows list.

2.  In the **Name** column, select the filter icon, set the filter to **starts with ERP DP**, and select **Apply**.

    \[Omitted image "erpc-process-extensions-explore2.png"\] Alt text: Workflow Studio filter opened on name column.

3.  Select a process extension to copy, for example, **ERP DP: Read Blocked Sales Orders**.

4.  Select the more actions menu icon and select **Copy subflow**.

    \[Omitted image "erpc-process-extension-use1.png"\] Alt text: More actions menu icon expanded with copy subflow option highlighted.

5.  Specify a unique name for the subflow.

6.  In **Application**, select the application scope containing the model you want to use in the subflow.

    \[Omitted image "erpc-process-extension-use2.png"\] Alt text: Create copy of subflow modal with name and application fields.

7.  Select **Copy**.

8.  In the new copied subflow record, select **Use ERP data** and replace the models used by the action to use cloned models instead.

    \[Omitted image "erpc-process-extension-use3.png"\] Alt text: Subflow displayed in flow view with use erp data link highlighted.

    For more information, see [Use ERP Data action details for flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-canvas-flow-reference-2.md).


**Parent Topic:**[Zero Copy Connector for ERP data products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-canvas-content-packs.md)

