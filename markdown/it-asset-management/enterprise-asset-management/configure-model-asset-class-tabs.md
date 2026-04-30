---
title: Configure tabs in the Enterprise Asset Workspace
description: Configure the options to hide or display various tabs, including tabs that are associated with specific model categories, in the Enterprise model management view and Enterprise asset estate view of the Enterprise Asset Workspace.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Configure tabs in the Enterprise Asset Workspace

Configure the options to hide or display various tabs, including tabs that are associated with specific model categories, in the Enterprise model management view and Enterprise asset estate view of the Enterprise Asset Workspace.

## Before you begin

Role required: sn\_eam.enterprise\_admin

## Procedure

1.  Navigate to **Enterprise Asset Workspace** &gt; **Admin center**.

2.  In the navigation panel of the Admin center view, select **Model and asset tabs**.

3.  From the list of available tab configurations, select the configuration that you want to modify.

    The Enterprise Asset Management application includes the following tab configurations by default:

    -   Asset groups tab configuration
    -   Asset indoor map tab configuration
    -   Construction class tab configuration
    -   Enterprise class tab configuration
    -   Facilities class tab configuration
    -   Firmware class tab configuration
    -   Industrial class tab configuration
    -   Linear assets tab configuration
    -   Medical class tab configuration
    -   Retail class tab configuration
    -   Tactical Equipment class tab configuration
    -   Transportation class tab configuration
    -   Wearables class tab configuration
    **Important:**

    You can also select **New** to create an additional tab configuration for any custom top tier model category that you have added under the enterprise model category. However, ServiceNow strongly recommends that you use only existing top tier model categories, such as Medical or Construction, with custom sub-categories instead. For more information on creating custom model categories, see [Create model categories](create-custom-model-category.md).

    If you choose to create an additional tab configuration, you must also use UI Builder to manually add the corresponding model and asset tabs to the Enterprise model management view and Enterprise asset estate view. For detailed instructions, see [Add tabbed content to UI Builder pages](https://www.servicenow.com/docs/access?context=tabs-components&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

4.  On the tab configuration record, modify the fields as needed.

<table id="table_rhx_2rh_zgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the tab configuration.

</td></tr><tr><td>

Model category

</td><td>

Model category that is associated with the tab configuration. The specified model category corresponds with a model tab in the Enterprise model management view and an asset tab in the Enterprise asset estate view.**Note:** This field is editable only if you are creating a tab configuration.

</td></tr><tr><td>

Include in tab

</td><td>

Option to display the given tab in the Enterprise model management view or Enterprise asset estate view. If you enable this option, the tab appears in the applicable views. If you disable this option, the tab no longer appears in the applicable views.

 For example, if you enable this option in the Retail class tab configuration, the **Retail** tab appears in both the Enterprise model management view and Enterprise asset estate view.

**Warning:** If you enable the **Include in tab** option but disable the **Include in dialog box** option, the resulting tab configuration is invalid.

</td></tr><tr><td>

Include in dialog box

</td><td>

Option to display the associated model category in the dialog boxes for creating enterprise models and assets. If you enable this option, the model category appears in the **Model category** drop-down list of these dialog boxes. If you disable this option, the model category no longer appears in the drop-down list. You can access these dialog boxes by navigating to either the Enterprise model management view or Enterprise asset estate view, selecting the **All enterprise** tab, and then selecting **New**.

 **Note:** This option is editable only for tab configurations that are associated with a model category, such as the Tactical Equipment class tab configuration.

 **Warning:** If you enable the **Include in tab** option but disable the **Include in dialog box** option, the resulting tab configuration is considered invalid.

</td></tr><tr><td>

Domain

</td><td>

Domain that the tab configuration is available in.

</td></tr></tbody>
</table>5.  Select **Save**.


