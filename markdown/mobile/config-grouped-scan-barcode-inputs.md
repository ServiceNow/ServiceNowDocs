---
title: Configure input form screens with grouped scan barcode inputs
description: Configure input form screens that support grouped scans. Grouped scans enable you to scan multiple barcodes that are associated with assets that must be scanned in a set.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure input form screens with grouped scan barcode inputs

Configure input form screens that support grouped scans. Grouped scans enable you to scan multiple barcodes that are associated with assets that must be scanned in a set.

## Before you begin

You must create an input form screen before you create inputs. For information about creating an input form screen, see [Configure an input form screen](parameter-screen-config.md).

Role required: admin

## About this task

Grouped scan barcode inputs are supported for scripted writeback actions that are used in action items only. For information about action items, see [Configure an action item](sg-studio-create-action-item.md).

Grouped scan barcode inputs are available [offline](../concept/mobile-offline-mode.md) and [Mobile UI rules](../concept/mobile-ui-rules.md) apply to them.

## Procedure

1.  Navigate to **All** and enter `sys_sg_parameter_screen_list.do` in the filter.

2.  Select the input form screen to which you want to add the barcode inputs.

3.  On the **Settings** tab, select the **Advanced** check box.

4.  Right-click the banner at the top of the page and select **Save.**.

5.  Enter `sys_sg_parameter_section_m2m.do` in the filter and create a section mapping.

6.  Enter `sys_sg_parameter_section.do` in the filter and create an input form section:

    1.  Select the **Inputs** tab and add inputs with **Input Type** of **Barcode** only.

    2.  Select the **Attributes** tab and add the following section attributes:

        1.  Enter `SectionType` in the **Name** field and enter `barcode`for the **Value**.

            **Important:** The **SectionType** attribute is required.

        2.  Enter `MaxEntries` in the **Name** field and enter the number of times the user can scan for the **Value**.

            The **MaxEntries** attribute is optional.

        3.  Right-click the banner at the top of the page and select **Save**.
7.  Navigate to the configured action item by navigating to **System Mobile** &gt; **Action Items**.

8.  Select the action item that you want to use for the grouped barcode scan inputs.

9.  Add the grouped barcode scan script in the **Execution Script** field.

    For example, to define a barcode section named "barcodes" for grouped scan inputs, you could define two barcode inputs:

    -   asset\_number
    -   model\_number
    Then you could add the following script in the **Execution Script** field:

    ```
    (function WriteBackAction (parm_input, parm_variable, ActionResult) {
        for (i=0; i< parm_input["barcodes.asset_number"].length;i++) {
            var assetNumber= parm_input["barcodes.asset_number"][i];
            var modelNumber=parm_input["barcodes.model_number"] [i];
            var SMAssetUsage=new global.SMAssetUsage();
            SMAssetUsage.addAssetToStockroom(assetNumber, modelNumber);
    }
    }) (parm_input, parm_variable, actionResult);
    ```

10. Select **Update** to save the configuration.


