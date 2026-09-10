---
title: Auto-fill catalog item form in the Service Portal
description: Use ServiceNow AI Lens to extract data from documents and auto-fill catalog item forms in Service Portal. For example, auto-fill a new vendor onboarding form by extracting key details such as vendor name, address, contact email, and banking information from multiple documents, that includes Excel files, emails, images, and PDF documents.Capture a screen or upload files directly from your browser, and let ServiceNow AI Lens analyze the contents and auto-fill the form fields — no download or installation required.Use the ServiceNow AI Lens desktop app for the full range of capture and analysis capabilities, such as multi-image capture, auto-map Excel column headers with ServiceNow table fields, and file uploads.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/servicenow-lens/create-record-in-the-service-portal.html
release: australia
product: ServiceNow Lens
classification: servicenow-lens
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Use, ServiceNow AI Lens, Enable AI experiences]
---

# Auto-fill catalog item form in the Service Portal

Use ServiceNow AI Lens to extract data from documents and auto-fill catalog item forms in Service Portal. For example, auto-fill a new vendor onboarding form by extracting key details such as vendor name, address, contact email, and banking information from multiple documents, that includes Excel files, emails, images, and PDF documents.

## Before you begin

Role required: lens\_user

## About this task

You can auto-fill catalog item forms in the Service Portal in two ways:

-   **From your browser**: Use ServiceNow AI Lens to capture a screen from the browser, analyze the contents of the captured screen and auto-fill the form fields in the Service Portal — no download or installation of the desktop app required.

    **Note:**

    -   The screen capture experience may vary depending on your browser.

        **Tip:** For the best experience, use ServiceNow AI Lens on any Chromium-based browser.

    -   The browser-based experience supports single-screen capture.
-   **From the desktop app**: Use the ServiceNow AI Lens desktop app for the full range of capture and analysis capabilities, such as multi-image capture and file uploads.

## Procedure

1.  Navigate to the Service Portal and log in.

    The URL is

    ```
    https://<instance-name>.service-now.com/sp
    ```

    This procedure demonstrates how to request an iPhone from the Service Portal by capturing the browser screen and auto-filling the form.

2.  Navigate to the item that you want to request and select it.

3.  Select **Fill with Lens**.

    \[Omitted image "lens-select-fill-with-lens.png"\] Alt text: Fill with Lens button.

4.  Auto-fill catalog item forms in Service Portal by performing any of the following methods.

    -   [Using the Lens browser app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/create-record-in-the-service-portal.md)

        The ServiceNow AI Lens browser app opens in a new browser window.

    -   [Using the Lens desktop app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/create-record-in-the-service-portal.md)

        The ServiceNow AI Lens desktop app is launched.


## Using the Lens browser app

Capture a screen or upload files directly from your browser, and let ServiceNow AI Lens analyze the contents and auto-fill the form fields — no download or installation required.

### Before you begin

**Important:** Confirm that **Browser** is selected as a default preference in the Downloads and Preferences page. To view the steps, see [Set AI Lens to launch with the desktop app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/download-sn-lens-msi.md)

Role required: lens\_user

### About this task

When you select **Fill with Lens** on the Service Portal form, the ServiceNow AI Lens browser app opens in a new browser window.

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

        3.  \(Optional\) To specify the area of the captured screen that you want ServiceNow AI Lens to analyze, select **Crop**, and then use the crop handles.
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

    ServiceNow AI Lens notifies that it has auto-filled the catalog item form fields.

    \[Omitted image "lens-catalog-form-auto-filled.png"\] Alt text: Catalog form fields auto-fill notification.

4.  Navigate to the catalog item form that you wanted to auto-fill and verify that the fields are correctly filled.

    \[Omitted image "lens-catalog-form-autofilled.png"\] Alt text: Catalog form fields auto-filled.

    Only the field types that are supported by ServiceNow AI Lens get auto-populated with the extracted data. If the form doesn't have field types that are supported, then ServiceNow AI Lens won’t update the record. For more information about the supported fields, see [Field types supported](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/field-types-supported.md).

<table id="choicetable_g1q_l32_2hc"><thead><tr><th align="left" id="d88102e602">

Option

</th><th align="left" id="d88102e605">

Action

</th></tr></thead><tbody><tr><td id="d88102e611">

**If the auto-filled text looks good**

</td><td>

Save the record by selecting **Submit**.

</td></tr><tr><td id="d88102e623">

**If the auto-filled text requires changes**

</td><td>

Do one of the following actions:-   Manually adjust the information in the fields and save the record.
-   In the ServiceNow AI Lens window, provide different instructions or take more screenshots and select **Analyze** so that ServiceNow AI Lens can extract, comprehend the data again, and auto-fill the data into the record. Save the record by selecting **Submit**.

You can analyze the artifacts as many times as needed without reloading the form.

</td></tr></tbody>
</table>
## Using the Lens desktop app

Use the ServiceNow AI Lens desktop app for the full range of capture and analysis capabilities, such as multi-image capture, auto-map Excel column headers with ServiceNow table fields, and file uploads.

### Before you begin

**Important:** Confirm that **Desktop app** is selected as a default preference in the Downloads and Preferences page. To view the steps, see [Set AI Lens to launch with the desktop app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/download-sn-lens-msi.md)

Role required: lens\_user

### About this task

When you select **Fill with Lens** on the Service Portal form, the ServiceNow AI Lens desktop app is launched.

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

    The default character limit is 500. Users with the admin role can increase this limit to up to 5000 characters by navigating to the `sn_lens_user_prompt_max_length` system property.

5.  To let ServiceNow AI Lens analyze the captured screen, select **Analyze**.

    ServiceNow AI Lens notifies that it has auto-filled the catalog item form fields.

    \[Omitted image "lens-catalog-form-auto-filled.png"\] Alt text: Catalog form fields auto-fill notification.

6.  Navigate to the catalog item form that you wanted to auto-fill and verify that the fields are correctly filled.

    \[Omitted image "lens-catalog-form-autofilled.png"\] Alt text: Catalog form fields auto-filled.

    Only the field types that are supported by ServiceNow AI Lens get auto-populated with the extracted data. If the form doesn't have field types that are supported, then ServiceNow AI Lens won’t update the record. For more information about the supported fields, see [Field types supported](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/field-types-supported.md).

<table id="choicetable_g1q_l32_2hc"><thead><tr><th align="left" id="d88102e1251">

Option

</th><th align="left" id="d88102e1254">

Action

</th></tr></thead><tbody><tr><td id="d88102e1260">

**If the auto-filled text looks good**

</td><td>

Save the record by selecting **Submit**.

</td></tr><tr><td id="d88102e1272">

**If the auto-filled text requires changes**

</td><td>

Do one of the following actions:-   Manually adjust the information in the fields and save the record.
-   In the ServiceNow AI Lens window, provide different instructions or take more screenshots and select **Analyze** so that ServiceNow AI Lens can extract, comprehend the data again, and auto-fill the data into the record. Save the record by selecting **Submit**.

You can analyze the artifacts as many times as needed without reloading the form.

</td></tr></tbody>
</table>
