---
title: Update a record in an instance by using ServiceNow AI Lens
description: Update a record in the ServiceNow instance by auto-filling the form fields with data that is extracted from one or more documents.
locale: en-US
release: zurich
product: ServiceNow Lens
classification: servicenow-lens
topic_type: task
last_updated: "2025-03-17"
reading_time_minutes: 6
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

6.  On your system, open a document that you want to scan.

    A document can be an image, a scanned handwritten note, web page, Excel Sheet or a Microsoft Word document.

7.  Place the ServiceNow AI Lensscannerwindow on the top of the document.

    You can resize the ServiceNow AI Lens scanner window by dragging its borders.

8.  Update the form on the instance with data extracted from a single screenshot or file.

    1.  To provide additional instructions to extract, analyze, and organize data, select the Edit icon \(![Edit icon.](../image/lens-instructions-icon.png)\) and then enter the instructions.

        The default character limit is 500. Users with the admin role can increase this limit to up to 5000 characters by navigating to the `sn_lens_user_prompt_max_length` system property.

        **Note:** This is an optional step.

        ![Extract data from a single screenshot or uploaded files](../image/lens-auto-fill-form-single-scrnsht.png "Extract data from a single screenshot or uploaded files")

        **Tip:** Use the Upload file icon to upload one or more files from which data is extracted and auto-filled in the form. For more information, see [sn-lens-standalone-app.md\#upload-files-steps](sn-lens-standalone-app.md#upload-files-steps)

    2.  Select **Analyze**.

        The form is updated with the extracted data.

        ![Form is filled with extracted data.](../image/lens-form-filled-instance.png)

    3.  Verify that the form fields are correctly updated.

9.  Auto-fill the form on the instance with data extracted from multiple screenshots or uploaded files.

    1.  To provide additional instructions to extract, analyze, and organize data, select the Edit icon \(![Edit icon.](../image/lens-instructions-icon.png)\) and then enter the instructions.

        The default character limit is 500. Users with the admin role can increase this limit to up to 5000 characters by navigating to the `sn_lens_user_prompt_max_length` system property.

        **Note:** This is an optional step.

    2.  Select the **Multi-capture** button ![Multi-capture icon.](../image/multi-capture-icon.png).

        **Tip:** Use the Upload file icon \(![File Upload icon.](../image/lens-file-upload-icon.png)\) to upload one or more files from which data is extracted and auto-filled in the form. For more information, see [sn-lens-standalone-app.md\#upload-files-steps](sn-lens-standalone-app.md#upload-files-steps)

    3.  Select the Capture icon \(![Capture icon.](../image/capture-icon.png)\)

        The first screenshot is captured.

    4.  Place the ServiceNow AI Lensscannerwindow over another document or page and then select the Capture icon ![Capture icon.](../image/capture-icon.png)\).

        The second screenshot is captured.

        Repeat the step to capture more screenshots, if required.

        **Note:**

        -   You can capture a total of 10 screenshots with the combined size of all captured screenshots not exceeding 10 MB.
        -   To enable the desktop app to send large screenshot data to the server, confirm that the following system properties are set exactly as shown below:

            |Property name|Type|Recommended value|
            |-------------|----|-----------------|
            |glide.rest.max\_content\_length|Integer|15|
            |glide.rest.scripted.max\_inbound\_content\_length\_mb|Integer|15|

            For more information, see [Configure system property](https://www.servicenow.com/docs/access?context=r_ControllingMaxRequestSize&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

            **Note:** You must have the admin role to set the system properties.

    5.  To complete the capture, select the Done icon \(![Capture complete icon.](../image/lens-capture-done-icon.png)\).

    6.  Select **Analyze**.

        The form is auto-filled.

        ![Form is filled with extracted data.](../image/lens-form-filled-instance.png)

    7.  Verify that the form fields are correctly filled.

10. In the ServiceNow instance, review the text that is auto-filled by Now Assist into your record.

    The fields that are auto-filled by Now Assist are highlighted with the Sparkle icon ![](../../../common/image/icon-ai-sparkle.png).

    Only the field types that are supported by ServiceNow AI Lens get auto-populated with the extracted data. If the form doesn't have field types that are supported, then ServiceNow AI Lens won’t update the record. For more information about the supported fields, see [Field types supported](../reference/field-types-supported.md).

<table id="choicetable_jjf_zx2_s2c"><thead><tr><th align="left" id="d58737e643">

Option

</th><th align="left" id="d58737e646">

Action

</th></tr></thead><tbody><tr><td id="d58737e652">

**If the auto-filled text looks good**

</td><td>

Save the record by right-clicking on the form header and then selecting **Save**.

</td></tr><tr><td id="d58737e664">

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

