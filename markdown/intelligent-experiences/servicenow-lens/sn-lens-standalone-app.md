---
title: Extract and analyze data with ServiceNow AI Lens desktop app
description: Extract and analyze data from one or more screenshots that you capture or files that you upload, and then preview the data analysis.
locale: en-US
release: zurich
product: ServiceNow Lens
classification: servicenow-lens
topic_type: task
last_updated: "2025-03-18"
reading_time_minutes: 7
keywords: [standalone app, ServiceNow lens as standalone app, Start ServiceNow lens from desktop, Start ServiceNow lens from Windows, Start ServiceNow lens from MacOS, Use ServiceNow lens from desktop, Use ServiceNow lens from Windows, Use ServiceNow lens from MacOS]
breadcrumb: [Use, ServiceNow AI Lens, Enable AI experiences]
---

# Extract and analyze data with ServiceNow AI Lens desktop app

Extract and analyze data from one or more screenshots that you capture or files that you upload, and then preview the data analysis.

## Before you begin

To access the ServiceNow AI Lens functionality, perform the following steps:

-   Install ServiceNow AI Lens on your ServiceNow instance. For more information, see [Install the ServiceNow Lens in the ServiceNow instance](install-sn-lens.md).
-   Turn on the ServiceNow AI Lens skill to add the generative AI capability. For more information, see [Activate the ServiceNow AI Lens skill](activate-lens-skill.md).
-   Download the ServiceNow AI Lens installer to scan your desktop screen. For more information, see [Download the ServiceNow AI Lens installer](download-sn-lens-msi.md).

Don't scan any personally identifiable information, such as medical reports, financial reports, or other sensitive data, when using ServiceNow AI Lens as you don't want to expose the large language model \(LLM\) to any sensitive information.

Verify that you have provided permission to ServiceNow AI Lens to record the screen on your system.

Role required: lens\_user

## Procedure

1.  From your system, launch the ServiceNow AI Lens desktop application.

2.  On the login page, in the **Instance URL** field, enter the ServiceNow instance URL.

    For example, `https://<instance name>.service-now.com`.

3.  Select **Proceed**.

4.  Log in to your ServiceNow account by entering your username and password.

    Your account must have the lens\_user role.

5.  On the onboarding journey widget, complete the onboarding and select **Got it**.

    ![Onboarding journey widget with three pages to show you the highlights of the application.](../image/onboarding-widget-lens.png)

    If you launch the ServiceNow AI Lens for the first time, the onboarding journey widget appears. You can select **Don't show me again** to hide the widget the next time you launch ServiceNow AI Lens.

6.  Perform any one of the following methods to capture screenshots or upload files and analyze the data.

<table id="choicetable_xtj_f4t_g3c"><thead><tr><th align="left" id="d164121e249">

Method

</th><th align="left" id="d164121e252">

Steps

</th></tr></thead><tbody><tr><td id="d164121e258">

**Capture a single screenshot of a document and analyze the data.**

</td><td>

1.  Select **Capture**.

The ServiceNow AI Lens scanner window is launched.

**Note:** Use the scanner window to scan the data of the screenshot so you can submit it for analysis.

2.  Open a document that you want to scan.

Example of a document: image, scanned handwritten note, Excel sheet, web page, or any document that gives visual data.

3.  Place the ServiceNow AI Lensscannerwindow over the document.
4.  \(Optional step\). To provide instructions to analyze the data in the screenshot in a specific way, select the Edit icon \(![Edit icon.](../image/lens-instructions-icon.png)\), and enter the instructions.

![Field to enter instructions.](../image/lens-incident-email.png)

The default character limit is 500. Users with the admin role can increase this limit to up to 5000 characters by navigating to the `sn_lens_user_prompt_max_length` system property.

5.  To analyze the data in the screenshot that you captured, select **Analyze**.
6.  The preview of the analysis is displayed on the ServiceNow AI Lens preview window.

![Preview of the analysis of single image.](../image/lens-single-scrnsht-analysis.png "Preview of the analysis of the single image")

</td></tr><tr><td id="d164121e341">

**Capture multiple screenshots from one or more documents.**

</td><td>

1.  Select **Capture**.
2.  Open one or more documents from which you want to capture the screenshots.

Example of a document: image, scanned handwritten note, Excel sheet, web page, or any document that gives visual data.

3.  Select the Multi-capture icon \(![Multi-capture icon.](../image/lens-multi-capture-icon.png)\), and then place the scanner window over the document that you want to scan.

You can resize the scanner window by dragging its borders.

4.  \(Optional step\). To provide instructions to analyze the data in the screenshots in a specific way, select the Instructions icon \(![Instructions icon.](../image/lens-instructions-icon.png)\), and enter the instructions.

![Field to enter custom instructions.](../image/lens-incident-email.png)

The default character limit is 500. Users with the admin role can increase this limit to up to 5000 characters by navigating to the `sn_lens_user_prompt_max_length` system property.

5.  Select the Capture icon \(![Capture icon.](../image/capture-icon.png)\)

The first screenshot is captured.

6.  Place the ServiceNow AI Lensscannerwindow over the page of another or the same document and then select the Capture icon \(![Capture icon.](../image/capture-icon.png)\).

The second screenshot is captured.

Repeat the step to capture more screenshots, if required.

![number of screenshots you've captured.](../image/lens-number0f-scrnshts-captured.png "View the number of screenshots you've captured")

**Note:**

    -   You can capture a total of 10 screenshots with the combined size of all captured screenshots not exceeding 10 MB.
    -   To enable the desktop app to send large screenshot data to the server, confirm that the following system properties are set exactly as shown below:

        |Property name|Type|Recommended value|
        |-------------|----|-----------------|
        |glide.rest.max\_content\_length|Integer|15|
        |glide.rest.scripted.max\_inbound\_content\_length\_mb|Integer|15|

For more information, see [Configure system property](https://www.servicenow.com/docs/access?context=r_ControllingMaxRequestSize&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

**Note:** You must have the admin role to set the system properties.

7.  \(Optional step\) To remove a screenshot that you had captured, select the Delete icon.

![Captured screenshot delete button.](../image/lens-scrnsht-delete-button.png)

**Tip:**

    -   Repeat the step as many times to remove as many screenshots.
    -   The last screenshot that you had captured is removed at the first click.
    -   You can capture one or more new screenshots after removing the screenshots.
8.  To complete the capture, select the Done icon \(![Capture complete icon.](../image/lens-capture-done-icon.png)\).
 The ServiceNow AI Lens preview window displays the screenshots that you've captured.

 ![Multiple screenshots captured.](../image/lens-multiple-images-captured.png "Multiple screenshots captured")

**Tip:**

-   To view the preview of a screenshot that you captured, select the card. The preview of the screenshot opens on its respective default application.
-   To remove a captured screenshot, select the ![Remove file](../image/lens-file-attch-remove.png) icon.
-   To capture one or more additional screenshots, select **Capture more**.

**Note:** You can capture a total of 10 screenshots with the combined size of all captured screenshots not exceeding 10 MB.

</td></tr><tr><td id="upload-files-steps">

**Upload one or more files**

</td><td>

Select **Upload** and perform any one of the following file upload methods.**Add one or more files**

1.  Select **+Add file**,
2.  On your computer, navigate to the location and select one or more files that you want to upload.

**Tip:**

    -   You can upload up to 10 unprotected files, with the combined size of the uploaded files not exceeding 10 MB.
    -   To enable the desktop app to send large data of the uploaded files to the server, confirm that the following system properties are set exactly as shown below:

        |Property name|Type|Recommended value|
        |-------------|----|-----------------|
        |glide.rest.max\_content\_length|Integer|15|
        |glide.rest.scripted.max\_inbound\_content\_length\_mb|Integer|15|

For more information, see [Configure system property](https://www.servicenow.com/docs/access?context=r_ControllingMaxRequestSize&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

**Note:** You must have the admin role to set the system properties.

    -   To remove a file that you attached, select the Remove file icon \(![Remove file](../image/lens-file-attch-remove.png)\).
3.  Select **Next**.
**Drag and drop files**1.  On your computer, navigate to the location and select one or more files that you want to upload.
2.  Drag the selected files to the Drag and drop section \(![Drag and drop section.](../image/lens-drag-and-drop.png)\).

**Note:**

    -   You can drag and drop up to 10 unprotected files, with the combined size of the uploaded files not exceeding 10 MB.
    -   To enable the desktop app to send large data of the uploaded files to the server, confirm that the following system properties are set exactly as shown below:

        |Property name|Type|Recommended value|
        |-------------|----|-----------------|
        |glide.rest.max\_content\_length|Integer|15|
        |glide.rest.scripted.max\_inbound\_content\_length\_mb|Integer|15|

For more information, see [Configure system property](https://www.servicenow.com/docs/access?context=r_ControllingMaxRequestSize&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

**Note:** You must have the admin role to set the system properties.

    -   To remove a file that you attached, select the Remove file icon \(![Remove file](../image/lens-file-attch-remove.png)\).
3.  Select **Next**

The ServiceNow AI Lens preview window displays the files that you've uploaded

![Multiple files attached.](../image/lens-multiple-images-attached.png "Multiple files attached") ![Multiple files attached.]( "Multiple files attached")

**Tip:**

    -   To view the preview of a file that you uploaded, select the card. The preview of the file opens on its respective default application.
    -   To remove an uploaded file, select the ![Remove file](../image/lens-file-attch-remove.png) icon.
    -   To capture one or more additional files, select **Upload**.

**Note:** You can upload a total of 10 unprotected files with the combined size of all files not exceeding 10 MB.

</td></tr></tbody>
</table>7.  Select **Analyze**.

    ServiceNow AI Lens displays the preview of the response

    ![Analysis response displayed under Preview window.](../image/lens-single-scrnsht-analyze-response.png)

8.  Select **Submit** to trigger post processing.

    The **Submit** button appears on the Preview window if the post-processing is enabled in the related ServiceNow AI Lens action.

9.  Copy the previewed data by selecting the Copy icon ![Copy icon.](../../../administer/document-intelligence/image/icon-docintel-na-copy.png).

10. End the current session by selecting **Start new session**.


**Related topics**  


[Supporting information for ServiceNow AI Lens](../concept/sn-lens-supporting-info.md)

[ServiceNow AI Lens limitations](../reference/sn-lens-limitations.md)

[Create a record in an instance by using ServiceNow AI Lens](create-record-sn-lens.md)

[Update a record in an instance by using ServiceNow AI Lens](update-record-sn-lens.md)

