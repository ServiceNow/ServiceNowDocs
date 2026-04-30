---
title: Configure input form screens with signature inputs
description: Configure input fields that your users can use to sign electronically on the input form screen. Users can sign on the screen or type their name to record their signature.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure input form screens with signature inputs

Configure input fields that your users can use to sign electronically on the input form screen. Users can sign on the screen or type their name to record their signature.

## Before you begin

You must create an input form screen before you create inputs. For information about creating an input form screen, see [Configure an input form screen](parameter-screen-config.md).

Role required: admin

## About this task

Signature inputs support both declarative and scripted writeback actions in action items. For information about action items, see [Configure an action item](sg-studio-create-action-item.md).

Configure these inputs by using the signature input type with the optional **IsOverlay** attribute. By default, signatures are rendered in the full modal window. If you set the **IsOverlay** attribute to `true`, the signature renders in a half modal window. When a signature input is configured as the only input on a page and the **IsOverlay** attribute is set to `true`, the attribute is ignored. In this case, the signature is rendered in the full modal window.

**Important:** For HR workflows that use a precondition for an HR Task Signature, these preconditions must be replaced with the new signature input type. Don’t configure both the precondition as an HR Task Signature and the signature input type. Using both is a misconfiguration.

Signature inputs are available [offline](../concept/mobile-offline-mode.md). [Mobile UI rules](../concept/mobile-ui-rules.md) apply to signature inputs.

## Procedure

1.  Navigate to **All** and enter `sys_sg_parameter_screen_list.do` in the filter.

2.  Select the input form screen to which you want to add the signature input.

3.  Select the **Inputs** tab.

4.  Double-click the **Insert a new row…** and enter the following information for your signature input as needed.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the input|
    |Label|Label that displays for the input|
    |Input Type|The type of input. Select **Signature**.|
    |Placeholder|Text that appears in an input field before the user enters a value.|
    |Page|Input form screen page on which the signature input appears.|
    |Order|Order in which the signature input appears in the input form screen.|
    |Mandatory|Option to mark the signature input as required.|
    |Readonly|Option to mark the signature input as read-only.|
    |Auto-fill Variable|The auto-fill variable used for this signature input.|

5.  Right-click the Input form screen banner and select **Save** to save the signature input and stay on the form.

6.  If you want to configure the **IsOverlay** attribute to open the signature in a half modal window, double-click the **Name** of the signature input you just created to configure the attribute.

    1.  Scroll down to the **Attributes** section of the form and then double-click **Insert a new row…**.

    2.  In the **Name** field, enter `IsOverlay` and select the check mark to save the attribute name.

    3.  Double-click the **Value** field and enter `true` to configure the signature to open in a half modal window.

    If you want the signature to open in a full modal window, don’t configure the **IsOverlay** attribute. By default signature inputs open in a full modal window.

7.  When you finish configuring all the fields you want, select **Update**.


## What to do next

If you want to configure a scripted writeback action to save the signature input for this input form screen, add the scripted writeback action to the action item. For details, see [Configure a scripted writeback action that saves a signature input](signature-input-writeback-action.md).

