---
title: Extract and analyze data with ServiceNow AI Lens desktop app
description: Extract and analyze data from one or more screenshots that you capture or files that you upload, and then preview the data analysis.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/servicenow-lens/sn-lens-standalone-app.html
release: australia
product: ServiceNow Lens
classification: servicenow-lens
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [standalone app, ServiceNow lens as standalone app, Start ServiceNow lens from desktop, Start ServiceNow lens from Windows, Start ServiceNow lens from MacOS, Use ServiceNow lens from desktop, Use ServiceNow lens from Windows, Use ServiceNow lens from MacOS]
breadcrumb: [Use, ServiceNow AI Lens, Enable AI experiences]
---

# Extract and analyze data with ServiceNow AI Lens desktop app

Extract and analyze data from one or more screenshots that you capture or files that you upload, and then preview the data analysis.

## Before you begin

To access the ServiceNow AI Lens functionality, perform the following steps:

-   Install ServiceNow AI Lens on your ServiceNow instance. For more information, see [Install the ServiceNow Lens in the ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/install-sn-lens.md).
-   Turn on the ServiceNow AI Lens skill to add the generative AI capability. For more information, see [Activate the ServiceNow AI Lens skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/activate-lens-skill.md).
-   Download the ServiceNow AI Lens installer to scan your desktop screen. For more information, see [Download and set how you want to launch ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/download-sn-lens-msi.md).

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

    **Note:**

    -   If your administrator has enabled auto-login, you can skip signing in every time you launch ServiceNow AI Lens. After your first login, ServiceNow AI Lens automatically takes you to the home page on subsequent launches as long as your session is active. If your session expires or you sign out, ServiceNow AI Lens shows the login screen again. For more information, see [Set up auto-login for ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/configure-instance-url-and-auto-login.md).
    -   On macOS, when you launch ServiceNow AI Lens desktop app for the first time, your Mac asks whether ServiceNow AI Lens can store your login credentials. Select **Always Allow** to avoid entering your credentials every time you open the application.
5.  On the onboarding journey widget, complete the onboarding and select **Got it**.

    \[Omitted image "onboarding-widget-lens.png"\] Alt text: Onboarding journey widget with three pages to show you the highlights of the application.

    If you launch the ServiceNow AI Lens for the first time, the onboarding journey widget appears. You can select **Don't show me again** to hide the widget the next time you launch ServiceNow AI Lens.

6.  Select one of the following methods.

    -   **Capture screen**

        1.  Select **Capture**.

            The ServiceNow AI Lens scanner window is launched.

        2.  On your system, open one or more documents that you want to scan.

            Example of a document: image, scanned handwritten note, Excel sheet, web page, or any document that gives visual data.

        3.  Extract data from a single screenshot.
            1.  Place the ServiceNow AI Lens scanner window on top of the document.
            2.  Resize the ServiceNow AI Lens scanner window by dragging its borders.

                \[Omitted image "lens-scanner-incident-capture.png"\] Alt text: Scan and capture data from screenshot

        4.  \(Optional\) Extract data from multiple screenshots.
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
        2.  Perform any one of the following file upload methods.

            -   Upload one or more files by selecting the **+Add file** option.
            -   Upload one or more files by dragging the selected files to the Drag and drop files section and then select **Upload all**.
            \[Omitted image "lens-browser-upload-file-window.png"\] Alt text: File upload window.

            **Note:**

            -   You can upload up to 10 unprotected files, with the combined size of the uploaded files not exceeding 10 MB.
            -   To enable the desktop app to send large data of the uploaded files to the server, confirm that the following system properties are set exactly as shown below:

                |Property name|Type|Recommended value|
                |-------------|----|-----------------|
                |glide.rest.max\_content\_length|Integer|15|
                |glide.rest.scripted.max\_inbound\_content\_length\_mb|Integer|15|

                For more information, see [Configure system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/r_ControllingMaxRequestSize.md)

                **Note:** You must have the admin role to set the system properties.

            -   To remove a file that you attached, select the Remove file icon \[Omitted image "lens-delete-attached-file-icon.png"\] Alt text:.
            -   To rename the file that you attached, select the More options icon \[Omitted image "lens-three-dots-icon.png"\] Alt text:, and then select **Rename**.
        3.  Select **Next**.

            The ServiceNow AI Lens preview window displays the files that you have uploaded

            \[Omitted image "lens-analyze-multiple-screenshots.png"\] Alt text: The desktop app showing preview of uploaded files.

7.  To provide instructions to analyze the data in screenshots in a specific way, select the Edit icon \[Omitted image "lens-instructions-icon.png"\] Alt text:, and enter the instructions.

    The default character limit is 500. Users with the admin role can increase this limit to up to 5000 characters by navigating to the **sn\_lens\_user\_prompt\_max\_length** system property.

8.  To analyze the data in the screenshots that you captured, select **Analyze**.

    ServiceNow AI Lens displays the preview of the response

    \[Omitted image "lens-single-scrnsht-analysis.png"\] Alt text: Preview of the analysis of single image.

9.  Select **Submit** to trigger post processing.

    The **Submit** button appears on the Preview window if the post-processing is enabled in the related ServiceNow AI Lens action.

10. Copy the previewed data by selecting the Copy icon \[Omitted image "icon-docintel-na-copy.png"\] Alt text:.

11. End the current session by selecting **Start new session**.


**Related topics**  


[Supporting information for ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/sn-lens-supporting-info.md)

[ServiceNow AI Lens limitations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/sn-lens-limitations.md)

[Create or update a record in an instance by using ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/create-record-sn-lens.md)

