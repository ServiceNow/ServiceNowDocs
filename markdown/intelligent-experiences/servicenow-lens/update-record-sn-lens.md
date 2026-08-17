---
title: Update a record in an instance by using ServiceNow AI Lens
description: Update a record in the ServiceNow instance by auto-filling the form fields with data that ServiceNow AI Lens extracts from captured screens, documents, and files that you upload.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/servicenow-lens/update-record-sn-lens.html
release: zurich
product: ServiceNow Lens
classification: servicenow-lens
topic_type: task
last_updated: "2025-03-17"
reading_time_minutes: 13
keywords: [Update record using ServiceNow lens, Scan document using ServiceNow lens, Scan image using ServiceNow lens, Scan scanned document using ServiceNow lens, Scan email using ServiceNow lens]
breadcrumb: [Use, ServiceNow AI Lens, Enable AI experiences]
---

# Update a record in an instance by using ServiceNow AI Lens

Update a record in the ServiceNow instance by auto-filling the form fields with data that ServiceNow AI Lens extracts from captured screens, documents, and files that you upload.

## Before you begin

To access the ServiceNow AI Lens functionality, perform the following steps:

-   Install ServiceNow AI Lens on your ServiceNow instance. For more information, see [Install the ServiceNow Lens in the ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-lens/install-sn-lens.md).
-   Turn on the ServiceNow AI Lens skill to add the generative AI capability. For more information, see [Activate the ServiceNow AI Lens skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-lens/activate-lens-skill.md).
-   Download the ServiceNow AI Lens installer to scan your desktop screen. For more information, see [Download and set how you want to launch ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-lens/download-sn-lens-msi.md).

**Note:**

-   To use ServiceNow AI Lens from your browser, turn on the ServiceNow AI Lens skill.
-   For the full range of ServiceNow AI Lens capabilities, turn on the ServiceNow AI Lens skill, and download and install the desktop application.

Verify that ServiceNow AI Lens has access to record the screen on your system. For more information, see [Providing permission to ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-lens/download-sn-lens-msi.md).

Don't scan any personally identifiable information, such as medical reports, financial reports, or other sensitive data, when using ServiceNow AI Lens as you don't want to expose the large language model \(LLM\) to any sensitive information.

Role required: lens\_user

## About this task

You can update a record in the ServiceNow instance in two ways:

-   **From your browser**: Capture a screen or upload files directly from your browser, and let ServiceNow AI Lens analyze the contents and auto-fill the form fields — no download or installation required. For more information, see [Update records on your instance by using AI Lens from the browser](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-lens/update-record-sn-lens.md).

    **Note:**

    -   The screen capture experience may vary depending on the browser that you use.

        **Tip:** For the best experience, use ServiceNow AI Lens on any Chromium-based browser.

    -   The browser-based experience supports single-screen capture. To capture multiple screens, [Use ServiceNow AI Lens from the desktop application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-lens/create-record-sn-lens.md).
-   **From the desktop app**: Use the ServiceNow AI Lens desktop app for the full range of capture and analysis capabilities, such as multi-image capture, auto-map Excel column headers with ServiceNow table fields, and file uploads. For more information, see [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-lens/update-record-sn-lens.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-lens/update-record-sn-lens.md)

## Procedure

1.  Update a record in the ServiceNow instance by performing any of the following methods.

<table id="choicetable_cyz_stv_v3c"><thead><tr><th align="left" id="d78248e250">

Method

</th><th align="left" id="d78248e253">

Steps

</th></tr></thead><tbody><tr><td id="use-your-browser1">

**From your browser**

</td><td>

**Capture screen**1.  In your instance, navigate to the list view of any table, for example, Incidents.
2.  Open the record that you want to update.
3.  Select **Update with Lens**.

\[Omitted image "lens-update-with-lens-button.png"\] Alt text: Update with Lens button.

**Note:**

    -   If pop-up is blocked, ServiceNow AI Lens screen may not open. Confirm that you've already allowed pop-ups from your browser settings.
    -   On non-production instances, you can control on which tables the **Update with Lens** button appears using the following system properties:
        -   `sn_app_lens_core.show_lens_action_on_all_tables`: Set to true to show the **Update with Lens** button on all tables. Set to false to show it only on specific tables. Default is true.
        -   `sn_app_lens_core.lens_inclusion_table_list`: Enter the names of the tables as comma-separated values where you want the **Update with Lens** button to appear. Use this property only when the `sn_app_lens_core.show_lens_action_on_all_tables` property is set to false.
        -   `sn_app_lens_core.lens_exclusion_table_list:` Enter the names of the tables as comma-separated values where you want to hide the Create with Lens button, regardless of how the `sn_app_lens_core.lens_inclusion_table_list` property is set.
    -   On non-production instances, the **Update with Lens** button may appear even if the ServiceNow AI Lens skill is not activated. If you select the button, an error occurs. You can activate the skill or hide the button by entering the name of the table in the sn\_app\_lens\_core.lens\_inclusion\_table\_list property
    -   On production instances, the **Update with Lens** and **Update with Lens** buttons are visible only when the ServiceNow AI Lens skill is active and the user has the lens\_user role. To hide the buttons on all tables, set sn\_app\_lens\_core.show\_lens\_action\_on\_all\_tables to false and leave sn\_app\_lens\_core.lens\_inclusion\_table\_list empty.
4.  Select **Capture screen**.

\[Omitted image "lens-capture-screen-button.png"\] Alt text: Capture screen button for the browser-based experience.

5.  Select the screen that you want to capture, and then select **Share**.

**Note:**

    -   The screen capture options depend on your browser.
    -   For illustration purpose, the following steps show the capturing of an Outlook email screen from Chrome tab.
\[Omitted image "lens-select-capture-element.png"\] Alt text: Browser dialog to select a screen to capture.

ServiceNow AI Lens shows the captured Outlook email screen that it will analyze.

\[Omitted image "lens-image-captured.png"\] Alt text: Image captured

6.  \(Optional step\). To specify the area of the captured screen that you want ServiceNow AI Lens to analyze, select **Crop**, and then use the crop handles.
7.  Select **Confirm**.
8.  \(Optional steps\). Perform the following steps:
    -   In the Additional instructions field, enter specific instructions to guide ServiceNow AI Lens in extracting the information you need from the captured screen.
    -   Select **Re-capture** to discard the current capture and capture a new screen.
    -   Select **Revert to original** to undo the crop and restore the full captured image.
    -   Select **Crop** to further refine your selection by cropping the already cropped screen.
9.  To let ServiceNow AI Lens analyze the captured screen, select **Analyze**.

The form is auto-filled.

\[Omitted image "lens-notification-form-fill.png"\] Alt text: Form is auto-filled.

10. Navigate back to the instance form to review the fields that ServiceNow AI Lens has auto-filled.

\[Omitted image "image.lens-form-autofilled"\] Alt text: Incident form auto-filled.**Upload files**

1.  In your instance, navigate to the list view of any table, for example, Incidents.
2.  Open the record that you want to update.
3.  Select **Update with Lens**.

\[Omitted image "image.lens-upload-files-upload-rec"\] Alt text:

**Note:**

    -   If pop-up is blocked, ServiceNow AI Lens screen may not open. Confirm that you've already allowed pop-ups from your browser settings.
    -   On non-production instances, you can control on which tables the **Create with Lens** button appears using the following system properties:
        -   `sn_app_lens_core.show_lens_action_on_all_tables`: Set to true to show the **Create with Lens** button on all tables. Set to false to show it only on specific tables. Default is true.
        -   `sn_app_lens_core.lens_inclusion_table_list`: Enter the names of the tables as comma-separated values where you want the **Create with Lens** button to appear. Use this property only when the `sn_app_lens_core.show_lens_action_on_all_tables` property is set to false.
        -   `sn_app_lens_core.lens_exclusion_table_list:` Enter the names of the tables as comma-separated values where you want to hide the Create with Lens button, regardless of how the `sn_app_lens_core.lens_inclusion_table_list` property is set.
    -   On non-production instances, the **Create with Lens** button may appear even if the ServiceNow AI Lens skill is not activated. If you select the button, an error occurs. You can activate the skill or hide the button by entering the name of the table in the sn\_app\_lens\_core.lens\_inclusion\_table\_list property
    -   On production instances, the **Create with Lens** and **Update with Lens** buttons are visible only when the ServiceNow AI Lens skill is active and the user has the lens\_user role. To hide the buttons on all tables, set sn\_app\_lens\_core.show\_lens\_action\_on\_all\_tables to false and leave sn\_app\_lens\_core.lens\_inclusion\_table\_list empty.
4.  Select **Upload**.

\[Omitted image "image.lens-select-upload-button"\] Alt text: Upload button selection on browser.

5.  Perform any one of the following file upload methods.

**Add one or more files**

    1.  To attach files, select **+Add file**.
    2.  On your computer, navigate to the location and select one or more files that you want to attach.

**Note:**

        -   You can upload up to 10 unprotected files, with the combined size of the uploaded files not exceeding 10 MB.
        -   To remove a file that you attached, select the Remove file icon \(\[Omitted image "image.lens-delete-attached-file-icon"\] Alt text: Delete attached file icon.\).
        -   To rename the file that you attached, select the three-dots icon \(\[Omitted image "image.lens-three-dots-icon"\] Alt text: Three-dots icon.\), and then select **Rename**.
\[Omitted image "lens-browser-upload-file-window.png"\] Alt text: File upload window.

    3.  Select **Next**.

The ServiceNow AI Lens preview window displays the files that you have uploaded

\[Omitted image "image.lens-preview-uploaded-files"\] Alt text: Preview of uploaded files.

    4.  \(Optional\). Do one or more of the following steps.
        -   To remove an uploaded file, select the Remove file icon \(\[Omitted image "image.lens-delete-attached-file-icon"\] Alt text: Delete attached file icon.\).
        -   To upload more files, select **Upload**.
        -   To capture one or more screens from the browser, select **Capture**.
        -   To guide ServiceNow AI Lens in extracting the information you need from the uploaded files, enter specific instructions in the **Additional instructions** field.
    5.  Select **Analyze**.

ServiceNow AI Lens updates the form fields.

\[Omitted image "image.lens-screen-capture-success-msg"\] Alt text: Capture success message.

    6.  Navigate to the form and verify that the fields are correctly updated.

\[Omitted image "image.lens-form-autofilled"\] Alt text: Incident form auto-filled.

**Drag and drop files**

    1.  On your computer, navigate to the location and select one or more files that you want to attach.
    2.  Drag the selected files to the Drag and drop files section.

\[Omitted image "image.lens-drag-and-drop-section"\] Alt text: Drag and drop section.

    3.  \(Optional\). To rename a file, select the file name and update it.
    4.  Select **Upload all**.
    5.  Select **Next**.
    6.  The ServiceNow AI Lens preview window displays the files that you have uploaded

\[Omitted image "image.lens-preview-uploaded-files"\] Alt text: Preview of uploaded files.

    7.  \(Optional\). Do one or more of the following steps.
        -   To remove an uploaded file, select the Remove file icon \(\[Omitted image "image.lens-delete-attached-file-icon"\] Alt text: Delete attached file icon.\).
        -   To upload more files, select **Upload**.
        -   To capture one or more screens from the browser, select **Capture**.
        -   To guide ServiceNow AI Lens in extracting the information you need from the uploaded files, enter specific instructions in the **Additional instructions** field.
    8.  Select **Analyze**.

ServiceNow AI Lens updates the form fields.

\[Omitted image "image.lens-screen-capture-success-msg"\] Alt text: Capture success message.

    9.  Navigate to the form and verify that the fields are correctly updated.

\[Omitted image "image.lens-form-autofilled"\] Alt text: Incident form auto-filled.

</td></tr><tr><td id="use-desktop-app1">

**From the desktop app**

</td><td>

1.  In your instance, navigate to the list view of any table, for example, Incidents.
2.  Open the record that you want to update.
3.  Select **Update with Lens**.

\[Omitted image "lens-update-with-lens-button.png"\] Alt text: Update with Lens button.

4.  **Note:** On non-production instances, you can control which tables display the **Update with Lens** button using the following system properties:

-   `sn_app_lens_core.show_lens_action_on_all_tables`: Set to true \(default\) to show Lens actions on all tables, or false to restrict them to a defined list of tables.
-   `sn_app_lens_core.lens_inclusion_table_list`: Comma-separated list of tables on which Lens actions should appear. Active only when the primary toggle is set to false.
-   `sn_app_lens_core.lens_exclusion_table_list`: Comma-separated list of tables on which Lens actions should be hidden, even if the primary toggle is set to true.
5.  Select **Open AI Lens desktop**.

\[Omitted image "lens-select-open-ai-lens-desktop.png"\] Alt text: Open AI Lens desktop button.

6.  In the ServiceNow AI Lens.app dialog box, select **Open ServiceNow AI Lens.app**.

**Note:**

**Note:**

    -   This confirmation dialog appears when you select **Update with Lens** for the first time. You can make this a one-time step by selecting **Always open &lt;instance-name.service-now.com&gt; links of this type in the associated app** before selecting **Open ServiceNow AI Lens.app**.
    -   On macOS, when you launch ServiceNow AI Lens desktop app for the first time, your Mac asks whether ServiceNow AI Lens can store your login credentials. Select **Always Allow** to avoid entering your credentials every time you open the application.
7.  On the onboarding journey widget, complete the onboarding and select **Got it**.

\[Omitted image "onboarding-widget-lens.png"\] Alt text: Onboarding journey widget with three pages to show you the highlights of the application.

8.  On your system, open a document that you want to scan.

**Note:** A document can be an image, a scanned handwritten note, web page, Excel sheet, or a Microsoft Word document.

9.  Place the ServiceNow AI Lensscannerwindow on top of the document.
10. You can resize the ServiceNow AI Lens scanner window by dragging its borders.
11. Auto-fill the form on the instance with data extracted from a single screenshot or file.
    1.  To provide additional instructions to extract, analyze, and organize data, select the Edit icon \(\[Omitted image "lens-instructions-icon.png"\] Alt text: Edit icon.\) and then enter the instructions.

The default character limit is 500. Users with the admin role can increase this limit to up to 5000 characters by navigating to the `sn_lens_user_prompt_max_length` system property.

\[Omitted image "lens-auto-fill-form-single-scrnsht.png"\] Alt text: Extract data from a single screenshot or uploaded files

**Note:** Use the Upload file icon to upload one or more files from which data is extracted and auto-filled in the form. For more information, see [Upload one or more files](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-lens/sn-lens-standalone-app.md).

    2.  Select **Analyze**.

The form is auto-filled with the extracted data.

\[Omitted image "lens-form-filled-instance.png"\] Alt text: Form is filled with extracted data.

    3.  Verify that the form fields are correctly filled.
    4.  Auto-fill the form on the instance with data extracted from multiple screenshots or uploaded files.
        1.  To provide additional instructions to extract, analyze, and organize data, select the Edit icon \(\[Omitted image "lens-instructions-icon.png"\] Alt text: Edit icon.\) and then enter the instructions.

**Note:** The default character limit is 500. Users with the admin role can increase this limit to up to 5000 characters by navigating to the `sn_lens_user_prompt_max_length` system property.

        2.  Select the **Multi-capture** button \[Omitted image "multi-capture-icon.png"\] Alt text: Multi-capture icon..

**Note:** Use the Upload file icon \(\[Omitted image "lens-file-upload-icon.png"\] Alt text: File Upload icon.\) to upload one or more files from which data is extracted and auto-filled in the form. For more information, see [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-lens/sn-lens-standalone-app.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-lens/sn-lens-standalone-app.md).

        3.  Select the Capture icon \(\[Omitted image "capture-icon.png"\] Alt text: Capture icon.\).

The first screenshot is captured.

        4.  Place the ServiceNow AI Lensscannerwindow over another document or page and then select the Capture icon \(\[Omitted image "capture-icon.png"\] Alt text: Capture icon.\).

Repeat the step to capture more screenshots, if required.

**Note:**

            -   You can capture a total of 10 screenshots with the combined size of all captured screenshots not exceeding 10 MB.
            -   To enable the desktop app to send large screenshot data to the server, verify that the following system properties are set exactly as shown:

                |Property name|Type|Recommended value|
                |-------------|----|-----------------|
                |glide.rest.max\_content\_length|Integer|15|
                |glide.rest.scripted.max\_inbound\_content\_length\_mb|Integer|15|

For more information, see [Configure system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/r_ControllingMaxRequestSize.md).

**Note:** You must have the admin role to set the system properties.

        5.  To complete the capture, select the Done icon \(\[Omitted image "lens-capture-done-icon.png"\] Alt text: Capture complete icon.\).
        6.  Select **Analyze**.

The form is auto-filled.

\[Omitted image "lens-form-filled-instance.png"\] Alt text: Form is filled with extracted data.

        7.  Verify that the form fields are correctly filled.


</td></tr></tbody>
</table>2.  In the ServiceNow instance, review the text that is auto-filled by AI into your record.

    The fields that are auto-filled by AI are highlighted with the Sparkle icon \[Omitted image "icon-ai-sparkle.png"\] Alt text: AI sparkle icon.

    Only the fields that are supported by ServiceNow AI Lens get auto-populated with the extracted data. If you don’t have any supported fields in your form, then ServiceNow AI Lens won’t update the record. For more information about the supported fields, see [Field types supported](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-lens/field-types-supported.md).

<table id="choicetable_jjf_zx2_s2c"><thead><tr><th align="left" id="d78248e1250">

Option

</th><th align="left" id="d78248e1253">

Action

</th></tr></thead><tbody><tr><td id="d78248e1259">

**If the auto-filled text looks good**

</td><td>

Save the record by selecting **Save**.

</td></tr><tr><td id="d78248e1271">

**If the auto-filled text requires changes**

</td><td>

Do one of the following actions:-   Manually adjust the information in the fields and save the record.
-   In the ServiceNow AI Lens window, provide different instructions or take more screenshots and select **Analyze** so that ServiceNow AI Lens can extract, comprehend the data again, and auto-fill the data into the record. Save the record by selecting **Save**.

You can analyze the artifacts as many times as needed without reloading the form.

</td></tr></tbody>
</table>
**Related topics**  


[Supporting information for ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-lens/sn-lens-supporting-info.md)

[ServiceNow AI Lens limitations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-lens/sn-lens-limitations.md)

[Create a record in an instance by using ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-lens/create-record-sn-lens.md)

[Extract and analyze data with ServiceNow AI Lens desktop app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-lens/sn-lens-standalone-app.md)

