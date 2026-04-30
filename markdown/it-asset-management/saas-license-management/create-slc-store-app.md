---
title: Create a store app for a custom integration
description: Publish your custom integration application on the ServiceNow Store to make it available for others to use.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [SaaS License Connections, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Create a store app for a custom integration

Publish your custom integration application on the ServiceNow Store to make it available for others to use.

## Before you begin

Role required: admin

## About this task

You must complete these steps so that your custom integration works correctly when other users download it from the ServiceNow Store.

## Procedure

1.  Create a fix script in your custom integration application.

    When a new integration profile is created using your application, the subflows and connection alias you created are automatically linked to the profile through this fix script.

    1.  Navigate to **System Applications** &gt; **Studio**.

    2.  Select your custom integration application.

    3.  On the Welcome to Studio page, click **+ Create New**.

        The Create Application File dialog box opens.

    4.  On the dialog box, search for and select `Fix Script`.

    5.  Click **Create**.

    6.  On the Fix Script form, fill in the following fields.

        |Field|Value|
        |-----|-----|
        |Name|Name of the fix script. For example, `Custom Integration Fix Script`.|
        |Unloadable|Option to create Customer Update \[sys\_update\_xml\] records when the fix script runs. Do not select this option.|
        |Application|Your custom integration application. This field is populated automatically.|
        |Before|Option that enables you to run the fix script before installing or upgrading the application. Do not select this option.|
        |Description|Description of the fix script.|

    7.  Enter the following script in the **Script** field.

        For the subflows and connection alias, replace the example ids with the real ids. You can find the id in the URL for each item.

        ```
        new global.CustomIntegrationProfileUtils().createCustomIntegration({
        	name: 'Name', // choose a name for the integration
        	downloadSubscriptionSubflow: '3a23e189a1400010fa9bed1383c83d38', //replace example id
        	updateActivitySubflow: '77a66d23e5500010fa9bc9581d0c0f47', //replace example id
        	reclamationSubflow: 'e62b672e39400010fa9b4845e477fe02', //replace example id
        	connectionAlias: '629ad2bfdb1893005963ff041d961971' //replace example id
        });
        ```

        **Note:** The update activity and reclamation subflows are not required. If you do not include a subflow to update activity, the integration does not get user activity unless your download subscription subflow includes user activity. If you do not include a reclamation subflow, the integration cannot deactivate SaaS user subscriptions.

    8.  Click **Submit**.

2.  Create a cross scope privilege record.

    This record allows the fix script you created to access the CustomIntegrationProfileUtils\(\) script include.

    1.  Navigate to **System Applications** &gt; **Application Cross-Scope Access**.

    2.  Click **New**.

    3.  On the form, fill in the fields.

<table id="table_dcv_pkm_4kb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Source Scope

</td><td>

Your custom integration application. This field is populated automatically.

 To select a different application, click the Settings \(![Settings icon](../../../common/image/List_PersonalizeListIcon.png)\) icon on the banner frame of your ServiceNow instance. On the System Settings dialog box, select the **Developer** tab and then choose an application from the **Application** drop-down list.

</td></tr><tr><td>

Target Scope

</td><td>

Application from which resources are being requested. Click the search \(![Search icon](../image/search-icon.png)\) icon to locate and select the **Global** application.

</td></tr><tr><td>

Target Name

</td><td>

Name of the script include. Set this field to `CustomIntegrationProfileUtils`.

</td></tr><tr><td>

Target Type

</td><td>

Type of request. Select **Script Include**.

</td></tr><tr><td>

Application

</td><td>

Your custom integration application. This field is populated automatically.

</td></tr><tr><td>

Operation

</td><td>

Operation that the script performs on the target scope. Select **Execute API**.

</td></tr><tr><td>

Status

</td><td>

Authorization for this cross scope privilege record. Select **Allowed**.

</td></tr></tbody>
</table>    4.  Click **Submit**.


## What to do next

Before you publish your custom integration application on the ServiceNow Store, make sure that your actions and subflows are active, published, and saved in your application.

**Parent Topic:**[SaaS License Connections](../concept/saas-license-connections.md)

**Previous topic:**[Publish a custom integration profile](publish-integration-custom.md)

**Next topic:**[Review a software reclamation rule](add-reclamation-rule-sub.md)

