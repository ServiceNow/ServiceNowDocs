---
title: Create or update a record in an instance by using ServiceNow AI Lens
description: Create or update a record in the ServiceNow instance by auto-filling the form fields with data that ServiceNow AI Lens extracts from screens and files.Capture a screen or upload files directly from your browser, and let ServiceNow AI Lens analyze the contents and auto-fill the form fields — no download or installation required.Use the ServiceNow AI Lens desktop app for the full range of capture and analysis capabilities, such as multi-image capture, auto-map Excel column headers with ServiceNow table fields, and file uploads.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/servicenow-lens/create-record-sn-lens.html
release: australia
product: ServiceNow Lens
classification: servicenow-lens
topic_type: task
last_updated: "2025-03-17"
reading_time_minutes: 13
keywords: [Create record using ServiceNow lens, Scan document using ServiceNow lens, Scan image using ServiceNow lens, Scan scanned document using ServiceNow lens, Scan email using ServiceNow lens]
breadcrumb: [Use, ServiceNow AI Lens, Enable AI experiences]
---

# Create or update a record in an instance by using ServiceNow AI Lens

Create or update a record in the ServiceNow instance by auto-filling the form fields with data that ServiceNow AI Lens extracts from screens and files.

## Before you begin

To access the ServiceNow AI Lens functionality, perform the following steps:

-   Install ServiceNow AI Lens on your ServiceNow instance. For more information, see [Install the ServiceNow Lens in the ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/install-sn-lens.md).
-   Turn on the ServiceNow AI Lens skill to add the generative AI capability. For more information, see [Activate the ServiceNow AI Lens skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/activate-lens-skill.md).
-   Download the ServiceNow AI Lens installer to scan your desktop screen. For more information, see [Download and set how you want to launch ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/download-sn-lens-msi.md).

**Note:**

-   To use ServiceNow AI Lens from your browser, turn on the ServiceNow AI Lens skill.
-   For the full range of ServiceNow AI Lens capabilities, turn on the ServiceNow AI Lens skill, and download and install the desktop application.

Verify that ServiceNow AI Lens has access to record the screen on your system. For more information, see [Providing permission to ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/download-sn-lens-msi.md).

Don't scan any personally identifiable information, such as medical reports, financial reports, or other sensitive data, when using ServiceNow AI Lens as you don't want to expose the large language model \(LLM\) to any sensitive information.

Role required: lens\_user

## About this task

You can create a record in the ServiceNow instance in two ways:

-   **From your browser**: Capture a screen or upload files directly from your browser, and let ServiceNow AI Lens analyze the contents and auto-fill the form fields — no download or installation required. For more information, see [Using the Lens browser app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/create-record-sn-lens.md).

    **Note:**

    -   The screen capture experience may vary depending on the browser that you use.

        **Tip:** For the best experience, use ServiceNow AI Lens on any Chromium-based browser.

    -   The browser-based experience supports single-screen capture. To capture multiple screens, [Use ServiceNow AI Lens from the desktop application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/create-record-sn-lens.md).
-   **From the desktop app**: Use the ServiceNow AI Lens desktop app for the full range of capture and analysis capabilities, such as multi-image capture, auto-map Excel column headers with ServiceNow table fields, and file uploads. For more information, see [Using the Lens desktop app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/create-record-sn-lens.md).

## Procedure

1.  In your instance, navigate to the list view of any table, for example, Incidents.

2.  Select **Create with Lens** or **Update with Lens**.

    \[Omitted image "luanch-from-sn-instance.png"\] Alt text: Create with Lens button on the ServiceNow form view.

    \[Omitted image "lens-update-with-lens-button.png"\] Alt text: Update with Lens button.

    **Note:**

    -   If pop-up is blocked, ServiceNow AI Lens screen may not open. Confirm that you've already allowed pop-ups from your browser settings.
    -   On non-production instances, you can control on which tables the **Create with Lens** and **Update with Lens** buttons appear using the following system properties:
        -   **sn\_app\_lens\_core.show\_lens\_action\_on\_all\_tables**: Set to true to show the **Create with Lens** and **Update with Lens** buttons on all tables. Set to false to show it only on specific tables. Default is true.
        -   **sn\_app\_lens\_core.lens\_inclusion\_table\_list**: Enter the names of the tables as comma-separated values where you want the **Create with Lens** and **Update with Lens** buttons to appear. Use this property only when the **sn\_app\_lens\_core.show\_lens\_action\_on\_all\_tables** property is set to false.
        -   **sn\_app\_lens\_core.lens\_exclusion\_table\_list**: Enter the names of the tables as comma-separated values where you want to hide the **Create with Lens** and **Update with Lens** buttons, regardless of how the**sn\_app\_lens\_core.lens\_inclusion\_table\_list** property is set.
    -   On non-production instances, the **Create with Lens** and **Update with Lens** buttons may appear even if the ServiceNow AI Lens skill is not activated. If you select the button, an error occurs. You can activate the skill or hide the button by entering the name of the table in the **sn\_app\_lens\_core.lens\_inclusion\_table\_list** property
    -   On production instances, the **Create with Lens** and **Update with Lens** buttons are visible only when the ServiceNow AI Lens skill is active and the user has the lens\_user role. To hide the buttons on all tables, set **sn\_app\_lens\_core.show\_lens\_action\_on\_all\_tables** to false and leave**sn\_app\_lens\_core.lens\_inclusion\_table\_list** empty.
3.  Create or update a record in the ServiceNow instance by performing any of the following methods.

    -   [Using the Lens browser app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/create-record-sn-lens.md)

        The ServiceNow AI Lens browser app opens in a new browser window.

    -   [Using the Lens desktop app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/create-record-sn-lens.md)

        The ServiceNow AI Lens desktop app is launched.


**Related topics**  


[Supporting information for ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/sn-lens-supporting-info.md)

[ServiceNow AI Lens limitations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/sn-lens-limitations.md)

[Extract and analyze data with ServiceNow AI Lens desktop app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/sn-lens-standalone-app.md)

## Using the Lens browser app

Capture a screen or upload files directly from your browser, and let ServiceNow AI Lens analyze the contents and auto-fill the form fields — no download or installation required.

### Before you begin

**Important:** Confirm that **Browser** is selected as a default preference in the Downloads and Preferences page. To view the steps, see [Set AI Lens to launch with the desktop app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/download-sn-lens-msi.md)

Role required: lens\_user

### About this task

When you select **Create with Lens** or **Update with Lens** for a form, the ServiceNow AI Lens browser app opens in a new browser window.

**Note:**

-   The screen capture experience may vary depending on the browser that you use.

    **Tip:** For the best experience, use ServiceNow AI Lens on any Chromium-based browser.

-   The browser-based experience supports single-screen capture. To capture multiple screens, [Use ServiceNow AI Lens from the desktop application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/create-record-sn-lens.md).

### Procedure

1.  Select one of the following methods.

    \[Omitted image "lens-capture-screen-button.png"\] Alt text: Capture screen button for the browser-based experience.

    -   **Capture screen**

        1.  Select **Capture screen**.
        2.  Select the screen that you want to capture, and then select **Share**.

            **Note:**

            -   The screen capture options depend on your browser.
            -   For illustration purpose, the following steps show the capturing of an Outlook email screen from Chrome tab.
            \[Omitted image "lens-select-capture-element.png"\] Alt text: Browser dialog to select a screen to capture.

            ServiceNow AI Lens shows the captured Outlook email screen that it will analyze.

            \[Omitted image "lens-image-captured.png"\] Alt text: Image captured

        3.  \(Optional\). To specify the area of the captured screen that you want ServiceNow AI Lens to analyze, select **Crop**, and then use the crop handles.
        4.  Select **Confirm**.
        5.  \(Optional\). Perform the following steps:
            -   Select **Re-capture** to discard the current capture and capture a new screen.
            -   Select **Revert to original** to undo the crop and restore the full captured image.
            -   Select **Crop** to further refine your selection by cropping the already cropped screen.
    -   **Upload**

        1.  Select **Upload**.
        2.  Perform any one of the following file upload methods.

            -   Upload one or more files by selecting the **+Add file** option.
            -   Upload one or more files by dragging the selected files to the Drag and drop files section and then select **Upload all**.
            \[Omitted image "lens-browser-upload-file-window.png"\] Alt text: File upload window.

            **Note:**

            -   You can upload up to 10 unprotected files, with the combined size of the uploaded files not exceeding 10 MB.
            -   To remove a file that you attached, select the Remove file icon \[Omitted image "lens-delete-attached-file-icon.png"\] Alt text:.
            -   To rename the file that you attached, select the More options icon \[Omitted image "lens-three-dots-icon.png"\] Alt text:, and then select **Rename**.
        3.  Select **Next**.

            The ServiceNow AI Lens preview window displays the files that you have uploaded

            \[Omitted image "lens-preview-uploaded-files.png"\] Alt text: Preview of uploaded files.

2.  To guide ServiceNow AI Lens in extracting the information you need from the uploaded files, enter specific instructions in the **Additional instructions** field.

    The default character limit is 500. Users with the admin role can increase this limit to up to 5000 characters by navigating to the `sn_lens_user_prompt_max_length` system property.

3.  To let ServiceNow AI Lens analyze the captured screen, select **Analyze**.

    The form is auto-filled.

    \[Omitted image "lens-notification-form-fill.png"\] Alt text: Form is auto-filled.

4.  In the ServiceNow instance, review the text that is auto-filled by AI into your record.

    The fields that are auto-filled by AI are highlighted with the Sparkle icon \[Omitted image "icon-ai-sparkle.png"\] Alt text: AI sparkle icon.

    \[Omitted image "lens-form-autofilled.png"\] Alt text: Incident form auto-filled.

    Only the fields that are supported by ServiceNow AI Lens get auto-populated with the extracted data. If you don’t have any supported fields in your form, then ServiceNow AI Lens won’t update the record. For more information about the supported fields, see [Field types supported](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/field-types-supported.md).

<table id="choicetable_jjf_zx2_s2c"><thead><tr><th align="left" id="d205405e896">

Option

</th><th align="left" id="d205405e899">

Action

</th></tr></thead><tbody><tr><td id="d205405e905">

**If the auto-filled text looks good**

</td><td>

Save the record by selecting **Save**.

</td></tr><tr><td id="d205405e917">

**If the auto-filled text requires changes**

</td><td>

Do one of the following actions:-   Manually adjust the information in the fields and save the record.
-   In the ServiceNow AI Lens window, provide different instructions or take more screenshots and select **Analyze** so that ServiceNow AI Lens can extract, comprehend the data again, and auto-fill the data into the record. Save the record by selecting **Save**.

You can analyze the artifacts as many times as needed without reloading the form.

</td></tr></tbody>
</table>
## Using the Lens desktop app

Use the ServiceNow AI Lens desktop app for the full range of capture and analysis capabilities, such as multi-image capture, auto-map Excel column headers with ServiceNow table fields, and file uploads.

### Before you begin

**Important:** Confirm that **Desktop app** is selected as a default preference in the Downloads and Preferences page. To view the steps, see [Set AI Lens to launch with the desktop app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/download-sn-lens-msi.md)

Role required: lens\_user

### About this task

When you select **Create with Lens** or **Update with Lens** for a form, the ServiceNow AI Lens desktop app is launched.

### Procedure

1.  In the ServiceNow AI Lens.app dialog box, select **Open ServiceNow AI Lens.app**.

    **Note:**

    -   This confirmation dialog appears when you select **Create with Lens** or **Update with Lens** for the first time. You can make this a one-time step by selecting **Always open &lt;instance-name.service-now.com&gt; links of this type in the associated app** before selecting **Open ServiceNow AI Lens.app**.
    -   On macOS, when you launch ServiceNow AI Lens desktop app for the first time, your mac asks whether ServiceNow AI Lens can store your login credentials. Select **Always Allow** to avoid entering your credentials every time you open the application.
2.  On the onboarding journey widget, complete the onboarding and select **Got it**.

    \[Omitted image "onboarding-widget-lens.png"\] Alt text: Onboarding journey widget with three pages to show you the highlights of the application.

3.  Use one of the following methods to extract data from documents.

    **Note:** A document can be an image, a scanned handwritten note, web page, Excel sheet, or a Microsoft Word document.

    -   **Capture screen**

        1.  On your system, open one or more documents that you want to scan.
        2.  Auto-fill the form on the instance with data extracted from a single screenshot.
            1.  Place the ServiceNow AI Lens scanner window on top of the document.
            2.  Resize the ServiceNow AI Lens scanner window by dragging its borders.
        3.  \(Optional\) Auto-fill the form on the instance with data extracted from multiple screenshots.
            1.  Select the **Multi-capture** button \[Omitted image "multi-capture-icon.png"\] Alt text: Multi-capture icon.
            2.  Select the Capture icon \[Omitted image "capture-icon.png"\] Alt text:.
            3.  Place the ServiceNow AI Lensscannerwindow over another document or page and then select the Capture icon \[Omitted image "capture-icon.png"\] Alt text:.
            4.  Repeat the step to capture more screenshots, if required.

                **Note:**

                -   You can capture a total of 10 screenshots with the combined size of all captured screenshots not exceeding 10 MB.
                -   To enable the desktop app to send large screenshot data to the server, verify that the following system properties are set exactly as shown:

                    |Property name|Type|Recommended value|
                    |-------------|----|-----------------|
                    |glide.rest.max\_content\_length|Integer|15|
                    |glide.rest.scripted.max\_inbound\_content\_length\_mb|Integer|15|

                    For more information, see [Configure system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/r_ControllingMaxRequestSize.md).

                    **Note:** You must have the admin role to set the system properties.

            5.  To complete the capture, select the Done icon \[Omitted image "lens-capture-done-icon.png"\] Alt text:.
    -   **Upload**

        1.  Select **Upload**.

            **Note:**

            -   You can upload up to 10 unprotected files, with the combined size of the uploaded files not exceeding 10 MB.
            -   To enable the desktop app to send large data of the uploaded files to the server, confirm that the following system properties are set exactly as shown below:

                |Property name|Type|Recommended value|
                |-------------|----|-----------------|
                |glide.rest.max\_content\_length|Integer|15|
                |glide.rest.scripted.max\_inbound\_content\_length\_mb|Integer|15|

                For more information, see [Configure system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/r_ControllingMaxRequestSize.md)

                **Note:** You must have the admin role to set the system properties.

            -   To remove a file that you attached, select the Remove file icon \[Omitted image "lens-file-attch-remove.png"\] Alt text:.
        2.  Perform any one of the following file upload methods.

            -   Upload one or more files by selecting the **+Add file** option.
            -   Upload one or more files by dragging the selected files to the Drag and drop files section and then select **Upload all**.
            \[Omitted image "lens-browser-upload-file-window.png"\] Alt text: File upload window.

            **Note:**

            -   You can upload up to 10 unprotected files, with the combined size of the uploaded files not exceeding 10 MB.
            -   To remove a file that you attached, select the Remove file icon \[Omitted image "lens-delete-attached-file-icon.png"\] Alt text:.
            -   To rename the file that you attached, select the More options icon \[Omitted image "lens-three-dots-icon.png"\] Alt text:, and then select **Rename**.
        3.  Select **Next**.

            The ServiceNow AI Lens preview window displays the files that you've uploaded\[Omitted image "lens-prev-window-instructions.png"\] Alt text: Provide instructions after capturing screenshots or uploading files

            **Tip:**

            -   To view the preview of a file that you uploaded, select the card. The preview of the file opens on its respective default application.
            -   To remove an uploaded file, select the Remove file icon \[Omitted image "lens-file-attch-remove.png"\] Alt text:.
            -   To capture one or more additional files, select **Upload**.

                **Note:** You can upload a total of 10 unprotected files with the combined size of all files not exceeding 10 MB.

4.  To guide ServiceNow AI Lens in extracting the information you need from the uploaded files, enter specific instructions in the **Additional instructions** field.

    The default character limit is 500. Users with the admin role can increase this limit to up to 5000 characters by navigating to the **sn\_lens\_user\_prompt\_max\_length** system property.

5.  To let ServiceNow AI Lens analyze the captured screen, select **Analyze**.

    The form is auto-filled.

    \[Omitted image "lens-form-filled-instance.png"\] Alt text: Form is filled with extracted data.

6.  In the ServiceNow instance, review the text that is auto-filled by AI into your record.

    The fields that are auto-filled by AI are highlighted with the Sparkle icon \[Omitted image "icon-ai-sparkle.png"\] Alt text: AI sparkle icon.

    \[Omitted image "lens-form-autofilled.png"\] Alt text: Incident form auto-filled.

    Only the fields that are supported by ServiceNow AI Lens get auto-populated with the extracted data. If you don’t have any supported fields in your form, then ServiceNow AI Lens won’t update the record. For more information about the supported fields, see [Field types supported](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/field-types-supported.md).

<table id="choicetable_jjf_zx2_s2c"><thead><tr><th align="left" id="d205405e1553">

Option

</th><th align="left" id="d205405e1556">

Action

</th></tr></thead><tbody><tr><td id="d205405e1562">

**If the auto-filled text looks good**

</td><td>

Save the record by selecting **Save**.

</td></tr><tr><td id="d205405e1574">

**If the auto-filled text requires changes**

</td><td>

Do one of the following actions:-   Manually adjust the information in the fields and save the record.
-   In the ServiceNow AI Lens window, provide different instructions or take more screenshots and select **Analyze** so that ServiceNow AI Lens can extract, comprehend the data again, and auto-fill the data into the record. Save the record by selecting **Save**.

You can analyze the artifacts as many times as needed without reloading the form.

</td></tr></tbody>
</table>
