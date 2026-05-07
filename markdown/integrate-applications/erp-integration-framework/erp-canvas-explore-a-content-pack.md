---
title: Explore a Zero Copy Connector for ERP content pack
description: Explore a Zero Copy Connector for ERP \(Enterprise Resource Planning\) content pack to see what it contains, including models and process extensions. Content pack models and process extensions are examples.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, content, pack, contents, model, process, extension]
breadcrumb: [Content packs, Building models, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Explore a Zero Copy Connector for ERP content pack

Explore a Zero Copy Connector for ERP \(Enterprise Resource Planning\) content pack to see what it contains, including models and process extensions. Content pack models and process extensions are examples.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP models page by selecting the models icon ![](../image/erpc-data-model-icon.png) in the side panel.

3.  Review the list of ERP models.

    Models that are part of a content pack have **DP** at the beginning of their ERP model name.

4.  Open a model from a content pack, for example **DP: Material Master**.

    **Note:** All fields are read only because content pack models can only be viewed, not edited.

5.  Review the model record for details including the short description, long text, and ERP module.

    ![Content pack model record page.](../image/erpc-explore-descriptions.png)

6.  Select the **Model entities** and **Entity fields** tabs to review the information.

7.  If you plan to use the content pack model, you will need to clone the model; select **Clone** now.

    1.  Enter a label.

    2.  Check that the correct target application is specified.

    3.  Select **Clone this model**.

        ![Clone this model modal with new name added.](../image/erpc-cloned-content-pack-model.png)

        Depending on the size of the model, the cloning process may take a few minutes. When the clone is complete, a success message in green is displayed.

    4.  Select the **Models** tab.

    5.  Select the refresh list model icon ![](../../../reuse/icons/product-icons/sync-fill-24.svg).

    6.  Confirm that the new cloned model is listed.

8.  Select the new, cloned model to open the record.

    **Note:** If you receive a message stating you aren't in the correct application scope, change your scope.

9.  Select **Manage model**.

10. Note that three operations have been added as part of the content pack: **Read**, **Update**, and **Create**.

11. Select the **Read** tile to see that an appropriate entity has been added.

    ![Manage model tab with manage entities page displayed.](../image/erpc-explore-read-tile.png)

12. Select **Specify inputs** to see that a mapping has been done with typical input parameters.

    ![Manage model tab with specify inputs page displayed.](../image/erpc-explore-read-input.png)

13. Select **Choose output** to see that a mapping has been done for the field or general information to send back when calling the model.

    ![Manage model tab with choose outputs page displayed.](../image/erpc-explore-read-output.png)

14. Select the back button on your browser three times to return to the model manager page.

15. Select the **Update** and **Create** tiles and repeat steps 12 through 14 for each tile to explore the predefined inputs and outputs.

    ![Manage model tab with create and update operation tiles highlighted.](../image/erpc-explore-update-create-tiles.png)

16. To see the process extensions in a content pack, navigate to **All** &gt; **Workflow Studio** and select **Subflows**.

    ![Workflow Studio landing page with subflows option highlighted.](../image/erpc-process-extensions-explore1.png)

17. In the **Name** column, select the filter icon, set the filter to **starts with ERP DP**, and select **Apply**.

    ![Filter expanded with conditions set to starts with ERP DP.](../image/erpc-process-extensions-explore2.png)

18. Select one of the material subflows, for example, **ERP DP: Material Update**.

    ![List of subflows containing ERP DP in the name with ERP DP material update highlighted.](../image/erpc-process-extensions-explore3.png)

19. View the subflow actions.

20. In the **Inputs &amp; Outputs** section, select **Subflow Inputs &amp; Outputs**.

21. View the inputs and outputs the subflow contains.

    ![ERP DP material update subflow inputs and outputs displayed.](../image/erpc-process-extensions-explore4.png)

22. Select the back button on your browser to return to the list of subflows.

23. Repeat steps 18 through 22 to explore more subflows.


## What to do next

When you're ready to create an application with a content pack, see [Using Zero Copy Connector for ERP content packs](erp-canvas-using-content-packs.md).

**Parent Topic:**[Zero Copy Connector for ERP content packs](../concept/erp-canvas-content-packs.md)

