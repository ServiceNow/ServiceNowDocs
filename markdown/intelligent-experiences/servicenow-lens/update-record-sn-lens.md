---
title: Update a record in an instance by using ServiceNow AI Lens
description: Update a record in the ServiceNow instance by auto-filling the form fields with data that is extracted from one or more documents.
locale: en-US
release: australia
product: ServiceNow Lens
classification: servicenow-lens
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Update record using ServiceNow lens, Scan document using ServiceNow lens, Scan image using ServiceNow lens, Scan scanned document using ServiceNow lens, Scan email using ServiceNow lens]
breadcrumb: [Use, ServiceNow AI Lens, Enable AI experiences]
---

# Update a record in an instance by using ServiceNow AI Lens

Update a record in the ServiceNow instance by auto-filling the form fields with data that is extracted from one or more documents.

## Before you begin

You must perform this task in Core UI.

To access the ServiceNow AI Lens functionality, perform the following steps:

-   Install ServiceNow AI Lens on your ServiceNow instance. For more information, see [Install the ServiceNow Lens in the ServiceNow instance](install-sn-lens.md).
-   Turn on the ServiceNow AI Lens skill to add the generative AI capability. For more information, see [Activate the ServiceNow AI Lens skill](activate-lens-skill.md).
-   Download the ServiceNow AI Lens installer to scan your desktop screen. For more information, see [Download the ServiceNow AI Lens installer](download-sn-lens-msi.md).

Verify that ServiceNow AI Lens has access to record the screen on your system. For more information, see [Providing permission to ServiceNow AI Lens](download-sn-lens-msi.md#lens-permission).

Use the **Update with Lens** button to launch the ServiceNow AI Lens scanner window and scan the data from documents, and update a form on the instance. You must have create and update access privileges to see the **Create with Lens** button in the list view of any table.

Don't scan any personally identifiable information, such as medical reports, financial reports, or other sensitive data, when using ServiceNow AI Lens as you don't want to expose the large language model \(LLM\) to any sensitive information.

Role required: lens\_user

## Procedure

1.  On your ServiceNow instance, navigate to the list view of a table.

    Example of a table: Incidents

2.  Select the record that you want to update.

3.  Select **Update with Lens**.

    ![Update with Lens button on the ServiceNow instance.](../image/update-with-lens.png)

    **Note:** On sub-production instances, you can control which tables display the **Update with Lens** button using the following system properties:

    -   `sn_app_lens_core.show_lens_action_on_all_tables`: Primary toggle. Set to true \(default\) to show Lens actions on all tables, or false to restrict them to a defined list of tables.
    -   `sn_app_lens_core.lens_inclusion_table_list`: Comma-separated list of tables on which Lens actions should appear. Active only when the primary toggle is set to false.
    -   `sn_app_lens_core.lens_exclusion_table_list`: Comma-separated list of tables on which Lens actions should be hidden, even if the primary toggle is set to true.
4.  In the ServiceNow AI Lens.app dialog box, select Open ServiceNow AI Lens.app.

    **Tip:** This confirmation dialog appears when you select **Create with Lens** for the first time. You can make this a one-time step by selecting **Always allow &lt;instance-name.service-now.com&gt; to open links of this type in the associated app** before selecting Open ServiceNow AI Lens.app.

5.  On the onboarding journey widget, complete the onboarding and select **Got it**.

    ![Onboarding journey widget with three pages to show you the highlights of the application.](../image/onboarding-widget-lens.png)

    If you launch the ServiceNow AI Lens for the first time, the onboarding journey widget appears. You can select **Don't show me again** to hide the widget the next time you launch ServiceNow AI Lens.

6.  On your system, open an artifact that you want to scan.

    An artifact can be an image, scanned or handwritten note, website, or application.

7.  Place the ServiceNow AI Lensscannerwindow on the top of the artifact.

    You can resize the ServiceNow AI Lens scanner window by dragging its borders.

8.  Extract the data from multiple screenshots.

    1.  Select the **Multi-capture** button ![Button to capture multiple screenshots.](../image/multi-capture-icon.png).

    2.  Continue to take the required screenshots by selecting the **Capture** button ![Capture button.](../image/capture-icon.png).

        You can capture up to 10 images to ServiceNow AI Lens.

        You can take multiple screenshots of the same artifact or different artifacts.

    3.  When you're finished taking screenshots, select **Done** ![Image capture complete button.](../image/done-icon.png).

        ![Done button after capturing multiple screenshots.](../image/lens-capture-complete.png)

        The window shows the thumbnails of the images that ServiceNow Lens captured.

        ![Multiple screens captured.](../image/lens-scanner-analyze-multiple-scrns.png)

9.  In the ServiceNow instance, review the text that is auto-filled by Now Assist into your record.

    The fields that are auto-filled by Now Assist are highlighted with the Sparkle icon ![](../../../common/image/icon-ai-sparkle.png).

    Only the fields that are supported by ServiceNow AI Lens get auto-populated with the extracted data. If you don’t have any supported fields in your form, then ServiceNow AI Lens won’t update the record. For more information about the supported fields, see [Field types supported](../reference/field-types-supported.md).

<table id="choicetable_jjf_zx2_s2c"><thead><tr><th align="left" id="d57433e432">

Option

</th><th align="left" id="d57433e435">

Action

</th></tr></thead><tbody><tr><td id="d57433e441">

**If the auto-filled text looks good**

</td><td>

Save the record by selecting **Save**.

</td></tr><tr><td id="d57433e453">

**If the auto-filled text requires changes**

</td><td>

Do one of the following actions:-   Manually adjust the information in the fields and save the record.
-   In the ServiceNow AI Lens window, provide different instructions or take more screenshots and select **Analyze** so that ServiceNow AI Lens can extract, comprehend the data again, and auto-fill the data into the record. Save the record by selecting **Save**.

You can analyze the artifacts as many times as needed without reloading the form.

</td></tr></tbody>
</table>
**Related topics**  


[Supporting information for ServiceNow AI Lens](../concept/sn-lens-supporting-info.md)

[ServiceNow AI Lens limitations](../reference/sn-lens-limitations.md)

[Create a record in an instance by using ServiceNow AI Lens](create-record-sn-lens.md)

[Extract and analyze data with ServiceNow AI Lens desktop app](sn-lens-standalone-app.md)

