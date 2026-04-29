---
title: Create an enterprise asset in the Mobile Agent application
description: Use the ServiceNow Mobile Agent application to create a serialized or multi-component enterprise asset.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Managing enterprise assets and tasks using the Mobile Agent application, Enterprise Asset Management, IT Asset Management]
---

# Create an enterprise asset in the Mobile Agent application

Use the ServiceNow® Mobile Agent application to create a serialized or multi-component enterprise asset.

## Before you begin

Role required: sn\_eam.enterprise\_admin or sn\_eam.enterprise\_asset\_manager

## About this task

**Important:** The enterprise assets that you create through the Mobile Agent application can be associated only with enterprise models that are classified through the Enterprise good model \[sn\_ent\_model\] class within the Configuration Management Database \(CMDB\) class hierarchy. See [Expanded Model and Asset Classes](../concept/enterprise-model-asset-classes-app.md) for more information on enterprise model classes.

## Procedure

1.  From your mobile device, launch the Mobile Agent application.

2.  On the navigation bar at the bottom of the screen, tap the **Enterprise Asset** tab.

    The navigation bar displays tabs for the ServiceNow applications and applets that you have access to through the Mobile Agent application. The navigation bar also displays tabs for your Mobile Agent application settings and notifications.

    The home screen for the Enterprise Asset Management application opens.

    ![Enterprise Asset Management home screen in the ServiceNow Mobile Agent application.](../image/eam-mobile-agent-app-home-screen.png)

3.  Tap **Create Asset**.

    The Serial Number screen opens.

4.  If your enterprise asset contains a serial number, scan or enter the serial number to verify if the asset already exists.

    If you want to skip this verification, tap the back arrow at the top left corner of the screen to proceed directly to the Create Asset form. You can then proceed either to [step 5](create-enterprise-asset-mobile-agent-app.md#verification-asset-tag) to verify the asset existence based on asset tags or to [step 6](create-enterprise-asset-mobile-agent-app.md#create-asset) to skip both verifications and continue with the asset creation process.

    1.  Use the camera on your mobile device to scan the serial number.

        You can also enter the serial number manually in the **Serial Number** field.

    2.  Depending on whether the enterprise asset exists or not, proceed with one of the following options:

        -   If the enterprise asset already exists, verify the asset details in the corresponding asset record:
            1.  Return to the home screen for the Enterprise Asset Management application.
            2.  Tap **Asset lookup**.

                The Asset lookup screen opens.

            3.  Use the camera on your mobile device to scan the asset tag of the enterprise asset.
            4.  Tap **Submit**.

            5.  From the list of corresponding asset records, tap the asset record through which you want to verify the asset details.

                The asset record opens.

            6.  Verify all asset details for the given enterprise asset.
            7.  Update any asset details if needed.
        -   If the enterprise asset does not already exist, proceed to [step 7](create-enterprise-asset-mobile-agent-app.md#more-options-menu) to continue with the asset creation process.
5.  If your enterprise asset contains an asset tag, scan the asset tag or enter the asset tag value to verify if the asset already exists.

    If you want to skip this verification, proceed directly to [step 6](create-enterprise-asset-mobile-agent-app.md#create-asset) to continue with the asset creation process.

    1.  On the Create Asset form, tap the **Asset Tag** field.

    2.  Use the camera on your mobile device to scan the asset tag.

        You can also enter the asset tag value manually in the **Asset Tag** field.

    3.  Depending on whether the enterprise asset exists or not, proceed with one of the following options:

        -   If the enterprise asset already exists, verify the asset details in the corresponding asset record:
            1.  Return to the home screen for the Enterprise Asset Management application.
            2.  Tap **Asset lookup**.

                The Asset lookup screen opens.

            3.  Use the camera on your mobile device to scan the asset tag of the enterprise asset.
            4.  Tap **Submit**.

                The list of corresponding asset records opens.

            5.  Tap the asset record through which you want to verify the asset details.

                The asset record opens.

            6.  Verify all asset details for the given enterprise asset.
            7.  Update any asset details if needed.
        -   If the enterprise asset does not already exist, proceed to [step 7](create-enterprise-asset-mobile-agent-app.md#more-options-menu) to continue with the asset creation process.
6.  On the Create Asset form, tap **Submit**.

    The complete list of your enterprise assets opens.

7.  Tap the more options menu at the top right corner of the screen.

8.  When the menu opens, tap **Create Asset**.

    The Asset Tag screen opens.

9.  Depending on whether your enterprise asset does or does not contain an asset tag, proceed with one of the following options:

    -   If your enterprise asset contains an asset tag, use the camera on your mobile device to scan the tag. You can also enter the asset tag value manually in the **Asset Tag** field. After you successfully scan the asset tag or enter the asset tag value, tap the back arrow at the top left corner of the screen to proceed to the Create Asset form. The **Asset Tag** field on the Create Asset form automatically updates with the asset tag value that you scanned or entered.
    -   If your enterprise asset does not contain an asset tag, tap the back arrow at the top left corner of the screen to skip the asset tag scan and proceed directly to the Create Asset form.
10. If your enterprise asset contains a serial number, scan or enter the serial number.

    1.  On the Create Asset form, tap the **Serial Number** field.

        The Serial Number screen opens.

    2.  Use the camera on your mobile device to scan the serial number.

        You can also enter the serial number manually in the **Serial Number** field.

    3.  Tap the back arrow at the top left corner of the screen to return to the Create Asset form.

        The **Serial Number** field on the Create Asset form automatically updates with the serial number that you scanned or entered.

11. Associate the enterprise asset with an enterprise model.

    1.  On the Create Asset form, tap the **Model** field.

        The Model screen opens.

    2.  From the list of available enterprise models, select the model that you want to associate the enterprise asset with.

        The screen closes and you return to the Create Asset form.

    The **Model** field on the Create Asset form automatically updates with the enterprise model that you selected.

12. Specify the state of the enterprise asset.

    1.  On the Create Asset form, tap the **State** field.

        The State screen opens.

    2.  From the list of available states, select the current state of the enterprise asset.

        The screen closes and you return to the Create Asset form.

    The **State** field on the Create Asset form automatically updates with the state that you selected. Based on this selected state, additional fields appear on the Create Asset form.

13. Based on the enterprise asset state that you specified in [step 11](create-enterprise-asset-mobile-agent-app.md#asset-state), fill in the additional fields that appear on the Create Asset form.

14. Tap **Submit**.

    The form closes and you automatically return to the home screen for the Enterprise Asset Management application.


## Result

The enterprise asset is created along with a corresponding configuration item \(CI\).

