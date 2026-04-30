---
title: Explore an Zero Copy Connector for ERP content pack
description: Explore an Zero Copy Connector for ERP content pack to see what it contains, including models and process extensions. Content pack models and process extensions are examples.
locale: en-US
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2025-04-16"
reading_time_minutes: 3
breadcrumb: [Zero Copy Connector for ERP content packs, Building and managing ERP models to work with ERP data, Using ERP models, extraction tables, and remote tables, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Explore an Zero Copy Connector for ERP content pack

Explore an Zero Copy Connector for ERP content pack to see what it contains, including models and process extensions. Content pack models and process extensions are examples.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP models page by selecting the ERP models icon \(![ERP model icon](../image/erpc-data-model-icon.png)\) in the side panel.

3.  Review the list of ERP models.

    Models that are part of a content pack have **DP** at the beginning of their ERP model name.

4.  Open a model from a content pack, for example **DP: Material Master**.

    **Note:** All fields are read only because content pack models can only be viewed, not edited.

5.  Review the model record for details including the short description, long text, ERP module, and ERP software.

    ![Content pack model record page.](../image/erpc-explore-descriptions.png)

6.  Select the **Model entities** and **Entity fields** tabs to review the information.

7.  If you plan to use the content pack model, then you need to clone by selecting **Clone**.

    1.  Enter a new model name.

    2.  Check that the correct target application is specified.

    3.  Select **Clone this model**.

        ![Clone this model modal with new name added.](../image/erpc-cloned-content-pack-model.png)

        Depending on the size of the model, the cloning process may take a few minutes. When the clone is complete, a success message in green is displayed.

    4.  Select the **Models** tab.

    5.  Select the refresh list model icon ![](../../../reuse/icons/product-icons/sync-fill-24.svg).

    6.  Confirm that the new cloned model is listed.

8.  Select the new, cloned model to open the record.

    **Note:** If you receive a message stating you are not in the correct application scope, change your scope.

9.  Select **Manage model**.

10. Three operations have already been added as part of the content pack: **Read**, **Update**, and **Create**.

11. Select the **Read** tile to see that an appropriate entity has already been added.

    ![Read operation with pre-defined entity highlighted.](../image/erpc-explore-read-tile.png)

12. Select **Specify inputs** to see that a mapping has already been done with typical input parameters.

    ![Read operation with pre-defined inputs listed.](../image/erpc-explore-read-input.png)

13. Select **Choose output** to see that a mapping has already been done for the field or general information to send back when calling the model.

    ![Read operation with pre-defined outputs listed.](../image/erpc-explore-read-output.png)

14. Select the back button on your browser three times to return to the model manager page.

15. Select the **Update** and **Create** tiles and repeat steps 12 through 14 for each tile to explore the predefined inputs and outputs.

    ![Model manager page with update and create tiles highlighted.](../image/erpc-explore-update-create-tiles.png)

16. To see the process extensions in a content pack, navigate to **All** &gt; **Workflow Studio** and select **Subflows**.

    ![Workflow Studio subflows list.](../image/erpc-process-extensions-explore1.png)

    **Note:** In the following steps, you simply view a process extension. When you are actually working with process extensions, you copy the subflow and adjust the copy of the subflow so it uses cloned models. For more information, see Using ERP Canvas process extensions.

17. In the **Name** column, select the filter icon, set the filter to **starts with ERP DP**, and select **Apply**.

    ![Workflow Studio filter opened on name column.](../image/erpc-process-extensions-explore2.png)

18. Select one of the material subflows, for example, **ERP DP: Material Update**.

    ![List of filtered subflows with ERP DP Material Update highlighted.](../image/erpc-process-extensions-explore3.png)

19. View the subflow actions.

20. In the **Inputs &amp; Outputs** section, select **Subflow Inputs &amp; Outputs**.

21. View the inputs and outputs the subflow contains.

    ![Inputs and outputs section expanded showing the inputs and outputs in the subflow.](../image/erpc-process-extensions-explore4.png)

22. Select the back button on your browser to return to the list of subflows.

23. Repeat steps 19-23 to explore more subflows.


## What to do next

When you're ready to create an application with a content pack, see [Using Zero Copy Connector for ERP content packs](erp-canvas-using-content-packs.md).

**Parent Topic:**[Zero Copy Connector for ERP content packs](../concept/erp-canvas-content-packs.md)

