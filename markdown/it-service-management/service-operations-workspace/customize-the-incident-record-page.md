---
title: Customize the incident record page
description: You can customize the Overview tab and the contextual side panel for an incident.Modify the Overview tab of an incident record page to display the summary and other information of the incident for an agent.Modify the Investigation tab of an incident record page.Customize the Remedial action playbook displayed on the contextual side panel of an incident record page.Modify the incident record information displayed on the contextual side panel of an incident record page.Configure the display of service level agreement \(SLA\) information in the incident record page.Enable quick updates for field values in a list in Service Operations Workspace.Customize on how the CI related metrics information is displayed on the Investigate tab of the Incident record.Configure the collection rules and map the rules to the metric definitions in the Investigate Framework module. This configuration enables you to define when the CI related metrics information is automatically retrieved on the Investigate tab of the Incident record.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 17
breadcrumb: [Customizing Service Operations Workspace for ITSM to align with your requirements, Service Operations Workspace for ITSM, IT Service Management]
---

# Customize the incident record page

You can customize the **Overview** tab and the contextual side panel for an incident.

**Parent Topic:**[Customizing Service Operations Workspace for ITSM to align with your requirements](customize-sow-landing-page.md)

**Related topics**  


[Create a copy of the Service Operations Workspace landing page](../task/create-copy-sow-landing-page.md)

[Customize Service Operations Workspace landing page](../task/configure-service-operations-workspace-landing-page.md)

## Customize the Overview tab for an incident

Modify the **Overview** tab of an incident record page to display the summary and other information of the incident for an agent.

### Before you begin

The demo data should be installed.

Role required: workspace\_admin, ui\_builder\_admin, or admin

### About this task

You can customize which fields are displayed on the various sections, such as Summary, Cause, and Resolution, in the **Overview** tab. Customize the fields by configuring the **SOW-Incident-Overview** view on the Incident form using the form layout or form design feature in the ServiceNow AI Platform.

**Note:** You must only configure the fields on the **SOW-Incident-Overview** view that are also available on the **Service Operation Workspace** view on the Incident form in the ServiceNow AI Platform.

For advanced customization of the **Overview** tab with SRP record, use the following procedure.

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  From the Experiences list, select **Service Operations Workspace**.

3.  In the Pages and Variants section under **Record**, select **SRP Record**.

    **Note:** If you're on a version prior to 4.0, you must navigate from **Record SNC** in UI Builder to customize the **Overview** tab of an Incident record page.

4.  Under **Contents** in the **Body** level, select **Main Tab**.

    ![Callout for the location of the Main Tab option in SRP record.](../image/SRP_Main_tab_SOW_edit.png "Main Tab")

    If the new copy is in a different application scope, select **Edit in original scope** before you start editing.

5.  In the Config section under Tabs, point to the **Page Collection SOW - Record tabs left** tab and select the Edit content icon \(![Edit content icon.](../image/SRP_Edit_overviewpage_left_icon.png)\).

    ![Callout for the location of the Page collection tile called SOW - Record tabs on the Overview tab.](../image/SRP_page_collection_tabs_left.png)

6.  Under **Overview**, point to the **Incident Overview SNC** variant and select the options icon \(![Options icon.](../image/options-variant.png)\).

7.  Select the duplicate variant icon \(![Duplicate variant icon.](../image/duplicate-variant.png)\).

    The Variant creation page is displayed.

8.  Enter the Name as `Incident Overview SNC Copy`.

    An error is displayed for the **Conditions** field.

    ![Error displayed for conditions.](../image/SRP_page_condition_error.png)

9.  Resolve this error by performing the following steps:

    1.  Close the Variant creation page.

    2.  Under **Overview**, point to the **Incident Overview SNC** variant, select the options icon \(![Options icon.](../image/options-variant.png)\), then select **View settings**.

    3.  Select **Open records**, then select **Variant record**.

        The Incident Overview SNC record is displayed.

    4.  Edit the record, copy, and store the information from the **Screen Condition** field, then remove the information.

        You use the information from the **Screen Condition** field in the later steps.

    5.  Select **Save** and close the record.

    6.  Repeat steps 6 through 9.

        No error is displayed for the **Conditions** field.

    7.  Open the Incident Overview SNC record again.

    8.  Edit the record and paste the **Screen Condition** information copied previously.

    9.  Select **Save** and close the record.

10. On the Variant creation page, select the **Settings** tab.

    If the new copy is in a different application scope, select **Edit in original scope** before you start editing.

11. Edit the **Order** value to modify the display order of the variants,

    The variant with the lowest number is the default configuration.

12. Add the criteria to display a page or tab in **Variant conditions**.

13. Select **Save**.

14. Select the **Editor** tab to start editing the page components for customizing the **Overview** tab.

    1.  Select the **Body** level of the **Content** tree next to the main page area of UI Builder.

    2.  Edit the page by configuring components as required.

    For more information on working with pages, see Work with pages.


## Customize the Investigation tab for an incident

Modify the **Investigation** tab of an incident record page.

### Before you begin

The demo data should be installed.

Role required: workspace\_admin, ui\_builder\_admin, or admin

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  From the **Experiences** list, select **Service Operations Workspace**.

3.  In the **Pages and Variants** section under **Record**, select **SRP Record**.

    **Note:** If you are on a version prior to 4.0, you must navigate from **Record SNC** in **UI Builder** to customize the **Investigation** tab of an Incident record page.

4.  Under **Contents** in the **Body** level, select **Main Tab**.

    ![Callout for the location of the Main Tab option in SRP record](../image/SRP_Main_tab_SOW_edit.png "Main Tab")

5.  If the new copy is in a different application scope, select the **Edit in original scope** button before you start editing.

6.  In the Config section under Tabs, point to the **Page Collection SOW - Record tabs left** tab and select the Edit content \(![Edit content icon](../image/SRP_Edit_overviewpage_left_icon.png)\) icon.

    ![Callout for the location of the Page collection tile called SOW - Record tabs for the leftside on the Overview tab](../image/SRP_page_collection_tabs_left.png)

7.  Under **Investigation**, point to **SOW Investigate SNC** variant and select the options \(![options icon](../image/options-variant.png)\) icon.

8.  Select the **Duplicate variant** icon \(![Duplicate icon](../image/duplicate-variant.png)\).

    The Variant creation page is displayed.

9.  Enter the **Name** as`SOW Investigate SNC copy`.

    An error is displayed for the **Conditions** field.

    ![Error displayed for conditions](../image/SRP_page_condition_error.png)

10. To resolve this error, perform the following steps:

    1.  Close the Variant creation page.

    2.  Under **Investigation**, point to **SOW Investigate SNC** variant, select the options icon \(![options icon](../image/options-variant.png)\), and then select **View settings**.

    3.  Select **Open records** and then select **Variant record**.

        SOW Investigate SNC record is displayed.

    4.  Edit the record, copy and store the information from the **Screen Condition** field, and then remove the information.

        You use the information from the **Screen Condition** field in the later steps.

    5.  Select **Save**.

    6.  Repeat the steps from Step 6 to Step 9.

        No error is displayed for the **Conditions** field.

    7.  Open the SOW Investigate SNC record again.

    8.  Edit the record and paste the **Screen Condition** information copied previously.

    9.  Select **Save** and close the record.

11. On the Variant creation page, select the **Settings** tab.

12. If the new copy is in a different application scope, select **Edit in original scope** before you start editing.

13. To modify the display order of the variants, edit the **Order** value.

    The variant with the lowest number is the default configuration.

14. Add the criteria to display a page or tab in **Variant conditions**.

15. Select **Save**.

16. Select the **Editor** tab to start editing the page components for customizing the **Investigation** tab.

    1.  Select the **Body** level of the **Content** tree to the left of the main page area of UI Builder.

    2.  Edit the page by configuring components as required.

    For more information on working with pages, see Work with pages.


## Customize the Remedial action playbook for an incident

Customize the Remedial action playbook displayed on the contextual side panel of an incident record page.

### Before you begin

The demo data should be installed.

Role required: workspace\_admin, ui\_builder\_admin, or admin

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  From the **Experiences** list, select **Service Operations Workspace**.

3.  In the **Pages and Variants** section under **Record**, select **SRP Record**.

    **Note:** If you are on a version prior to 4.0, you must navigate from **Record SNC** in **UI Builder** to customize the remedial action playbook.

4.  Under **Contents** in the **Body** level, select **Tab sidebar**.

    ![Callout for the location of Tab sidebar view](../image/SRP_tab_sidebar.png "Tab sidebar")

5.  If the new copy is in a different application scope, select the **Edit in original scope** button before you start editing.

6.  In the Config section under Tabs, point to the **Page Collection SOW - Sidebar tabs top** tab and select the Edit content \(![Edit content icon](../image/SRP_Edit_overviewpage_left_icon.png)\) icon.

    ![Callout for the location of the Page collection SOW sidebar tabs top on the Tab sidebar](../image/SRP_page_collection_sidebar_top.png)

7.  Under **Playbook**, point to **Playbook SNC** variant and select the options icon \(![options icon](../image/options-variant.png)\).

8.  Select the **Duplicate variant** icon \(![Duplicate icon](../image/duplicate-variant.png)\).

    The Variant creation page is displayed.

9.  Enter the **Name** as `Playbook SNC copy`.

    An error is displayed for the **Conditions** field.

    ![Error displayed for conditions](../image/SRP_page_condition_error.png)

10. To resolve this error, perform the following steps:

    1.  Close the Variant creation page.

    2.  Under **Playbook**, point to **Playbook SNC** variant, select the options icon \(![options icon](../image/options-variant.png)\), and then select **View settings**.

    3.  Select **Open records** and then select **Variant record**.

        Playbook SNC record is displayed.

    4.  Edit the record, copy and store the information from the **Screen Condition** field, and then remove the information.

        You use the information from the **Screen Condition** field in the later steps.

    5.  Select **Save**.

    6.  Repeat the steps from Step 6 to Step 9.

        No error is displayed for the **Conditions** field.

    7.  Open the Playbook SNC record again.

    8.  Edit the record and paste the **Screen Condition** information copied previously.

    9.  Select **Save** and close the record.

11. On the Variant creation page, select the **Settings** tab.

12. If the new copy is in a different application scope, select the **Edit in original scope** button before you start editing.

13. To modify the display order of the variants, edit the **Order** value.

    The variant with the lowest number is the default configuration.

14. Add the criteria to display a page or tab in **Variant conditions**.

15. Select **Save**.

16. Select the **Editor** tab to start editing the page components for customizing the remedial action playbook .

    1.  Select the **Body** level of the **Content** tree to the left of the main page area of UI Builder.

    2.  Edit the page by configuring components as required.

    For information on working with pages, see Work with pages.


## Customize the incident record information in the contextual side panel

Modify the incident record information displayed on the contextual side panel of an incident record page.

### Before you begin

The demo data should be installed.

Role required: workspace\_admin, ui\_builder\_admin, or admin

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  From the Experiences list, select **Service Operations Workspace**.

3.  In the Pages and Variants section under **Record**, select **SRP Record**.

    **Note:** If you're on a version prior to 4.0, you must navigate from **Record SNC** in UI Builder to customize the incident record information.

4.  Under **Contents**, in the **Body** level, select **Tab sidebar**.

    ![Callout for the location of the Tab sidebar view.](../image/SRP_tab_sidebar.png "Tab sidebar")

    If the new copy is in a different application scope, select **Edit in original scope** before you start editing.

5.  In the Config section under Tabs, point to the **Page Collection SOW - Sidebar tabs top** tab and select the edit content icon \(![Edit content icon.](../image/SRP_Edit_overviewpage_left_icon.png)\).

    ![Callout for the location of the Page collection SOW sidebar tabs top view in the Tab sidebar.](../image/SRP_page_collection_sidebar_top.png)

6.  Under **Record Information**, point to the **Record Information SNC** variant and select the options icon \(![Options icon.](../image/options-variant.png)\).

7.  Select the duplicate variant icon \(![Duplicate variant icon.](../image/duplicate-variant.png)\).

    The Variant creation page is displayed.

8.  Enter the Name as `Record Information SNC copy`.

    An error is displayed for the **Conditions** field.

    ![Error displayed for conditions.](../image/SRP_page_condition_error.png)

9.  To resolve this error, perform the following steps:

    1.  Close the Variant creation page.

    2.  Under **Record Information**, point to the **Record Information SNC** variant, select the options icon \(![Options icon,](../image/options-variant.png)\), and then select **View settings**.

    3.  Select **Open records** then select **Variant record**.

        The Record Information SNC record is displayed.

    4.  Edit the record, copy and store the information in the **Screen Condition** field, and then remove the information.

        You use the information from the **Screen Condition** field in the later steps.

    5.  Select **Save**.

    6.  Repeat steps 6 to 9.

        No error is displayed for the **Conditions** field.

    7.  Open the Record Information SNC record again.

    8.  Edit the record and paste the **Screen Condition** information copied previously.

    9.  Select **Save** and close the record.

10. On the Variant creation page, select the **Settings** tab.

    If the new copy is in a different application scope, select **Edit in original scope** before you start editing.

11. Edit the **Order** value to modify the display order of the variants.

    The variant with the lowest number is considered as the default configuration.

12. Add the criteria to display a page or tab in **Variant conditions**.

13. Select **Save**.

14. Select the **Editor** tab to start editing the page components for customizing the incident information in the contextual side panel.

    1.  Select the **Body** level of the **Content** tree next to the main page area of UI Builder.

    2.  Edit the page by configuring components as required.

    For information on working with pages, see Work with pages.


## Customize the display of service level agreements for an incident

Configure the display of service level agreement \(SLA\) information in the incident record page.

### Before you begin

Role required: admin

The following SLA timer configurations display the response and resolution SLA for an incident.

-   Incident Response
-   Incident Resolution

You should configure SLA timer configuration mappings for these timer configurations. For information on how you can configure these mappings, see [Configure the SLA timer](../../service-level-management/task/sla-timer-configurations.md).

### Procedure

1.  Navigate to **System Definition** &gt; **Script Includes**.

2.  From the Script Includes list, select **SOWIncidentInfo**.

3.  In the **Script** field, modify the display information for SLAs.

    ```
    getSLAConfig: function() {
            var config = [{
                    "configId": "af871ab3532730102d05ddeeff7b124f",
                    "slaTimerLabel": gs.getMessage("Response SLA"),
                    "timeLabel": gs.getMessage("Time to respond")
                },
                {
                    "configId": "aca7d6b3532730102d05ddeeff7b12ec",
                    "slaTimerLabel": gs.getMessage("Resolution SLA"),
                    "timeLabel": gs.getMessage("Time to resolve")
                }
            ];
            return config;
        },
    ```

    For information about how the SLA information is displayed for an incident, see [View service level agreement information for an incident](slm-sow.md#).


## Enable inline editing for lists in Service Operations Workspace

Enable quick updates for field values in a list in Service Operations Workspace.

### Before you begin

Role required: admin

### About this task

If the Hardware Asset Management Professional plugin \(com.sn\_hamp\) is installed, you should enable inline list editing to specify asset actions for a configuration item \(CI\) from the Affected CI related list of an incident.

### Procedure

1.  From the **All** menu, navigate to **sys\_properties.list**.

2.  For the **glide.lists.inline\_editing\_enabled** property, set the **Value** field to `true`.

3.  Click **Update**.


## Customize the Investigate tab

Customize on how the CI related metrics information is displayed on the **Investigate** tab of the Incident record.

### Before you begin

Role required: script\_include\_admin

### About this task

Use this task to customize and configure the **Investigate** tab of the Incident record to do the following:

-   Add, remove or customize the view of the CI metrics information on the Investigate tab. For example, remove Asset Utilization metrics or add a new metric to the Investigation tab.
-   Modify the threshold \(warning or critical\) values of the metrics.
-   Modify the label names of the metrics.
-   Change the units in which the metric values are displayed.
-   Add or remove rows and columns from the metric information cards.
-   Add, remove or rename the remedial action labels.

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

2.  From the script Include list, select **sn\_sow.SOWInvestigateConfigSNC**.

3.  Copy the required function from the **Script** field.

4.  From the Script Includes list, select **sn\_sow.SOWInvestigateConfig**.

    For example, refer the screen shot for sn\_sow.SOWInvestigateConfig script include record.

    ![sn_sow.SOWInvestigateConfig script includes record](../image/script_includes_sowinvestigate.png)

5.  In the **Script** field, paste the required function and edit to customize the UI elements that are displayed on the different sections of the **Investigate** tab.

    The `sn_sow.SOWInvestigateConfigSNC` script include record contains the configuration that is required to render the Investigate tab UI. Use this script include record as a reference to override the configuration as required, using the `sn_sow.SOWInvestigateConfig` script include record.

6.  Click **Save**.

7.  From the Script Includes list, select the provider specific script include SNC record.

    -   **sn\_acc\_adapter.AccTransformUtilsSNC** for Agent Client Collector for Investigation \(ACC\).
    -   **sn\_mecm\_adapter.MecmTransformUtilsSNC** for Microsoft Endpoint Configuration Manager for Investigation \(MECM\).
8.  Copy the required function from the **Script** field.

9.  From the Script Includes list, select the provider specific script include record.

    -   **sn\_acc\_adapter.AccTransformUtils** for Agent Client Collector for Investigation \(ACC\).
    -   **sn\_mecm\_adapter.MecmTransformUtils** for Microsoft Endpoint Configuration Manager for Investigation \(MECM\).
    For example, refer the screen shot for sn\_acc\_adapter.AccTransformUtils script include record.

    ![sn_acc_adapter.AccTransformUtils script includes record](../image/script_includes_acctransform.png)

10. In the **Script** field, paste and edit the script to configure the display of the metrics information on the customized UI of the **Investigate** tab.

    The `sn_acc_adapter.AccTransformUtilsSNC` script include record contains the configuration such as which data to store and how much data must be displayed on the Investigate tab UI. Use this script include record as a reference to override the configuration as required, using the `sn_acc_adapter.AccTransformUtils` script include record.

11. Click **Save**.


### What to do next

On the **Investigate** tab of the Incident record in the Service Operations Workspace, click the get latest metrics icon \(![get latest matrix refresh](../image/get-latest-matrix.png)\) to refresh and view the customizations. For more information, see [Incident Management in Service Operations Workspace](incident-sow.md).

## Configure the collection rules for the Investigate tab

Configure the collection rules and map the rules to the metric definitions in the Investigate Framework module. This configuration enables you to define when the CI related metrics information is automatically retrieved on the **Investigate** tab of the Incident record.

### Before you begin

Agent Client Collector for Investigation \(sn\_acc\_adapter\) and Investigation Framework \(sn\_invest\_fwk\) must be installed on the instance to view the Investigate Framework module. For more information, see [Install Agent Client Collector for Investigation](../task/install-acc-adapter.md).

The Agent Client Collector framework \(sn\_agent\) plugin must be installed on the instance, and Agent Client Collector must be installed to the affected CI. These installations are required to view the **Investigate** tab on the Incident record and the CI related metrics information displayed on the **Investigate** tab of the Incident record. For more information on the Agent Client Collector framework plugin and the installation, see  and Agent Client Collector installation.

Role required: sn\_cimaf.sn\_cimaf\_admin or sn\_invest\_fwk.sn\_investigate\_admin

### Procedure

1.  Navigate to **All** &gt; **Metrics and CI Actions Framework** &gt; **Administration** &gt; **Collection Rules**.

2.  Click **New**.

3.  On the form, fill in the fields.

    Trigger conditions are conditions under which the collection rule is activated. These conditions trigger the automatic retrieval of the CI related metrics information on the **Investigate** tab of the Incident record.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the collection rule.|
    |Active|Option to activate the collection rule. This option is selected by default.|
    |Trigger Conditions|
    |Source table|Table where the collection rule is applicable. For this task, select **Incident**.|
    |CI field|Type of CI applicable to the source table. For this task, select **Configuration item**.|
    |Table conditions|Condition builder to define the criteria for the fields related to the incidents under which the collection rule is triggered.|
    |CI class|Class of the affected CI associated with the incident.|
    |CI conditions|Condition builder to define the criteria for the fields related to the CI under which the collection rule is triggered.|
    |Allow matching CI extensions|Option to enable the selection of the child CI classes associated with the selected CI class. For example, if the **CI class** is set as **cmbi\_ci\_computer**, and if the **Allow matching CI extensions** option is selected, then you can select CI classes such as the cmbi\_ci\_computer server that is a child CI of cmbi\_ci\_computer.|

4.  Click **Submit**.

    The collection rule is created.

5.  Click the collection rule record.

6.  On the Collection Rule Metric Associations related list, click **New**.

    Use the Collection Rule Metric Associations related list to associate and map the collection rule with the metric definition \(information\).

7.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Collection rule|Collection rule that you want to map with the metric definition.|
    |Metric definition|Metric definition that you want to map with the collection rule. Metric definition is the CI related metrics information for which you want to implement the collection rule.|

    **Note:** You can configure multiple collection rules with multiple metric definitions.

8.  Click **Submit**.


### Result

The collection rule is created and mapped to the metric definition. When the collection rule is triggered, the mapped metric definition is retrieved and displayed on the **Investigate** tab of the Incident record. The configured collection rule is triggered only when the **Configuration Item** field is modified on the Incident record.

