---
title: Trigger ServiceNow AI Lens from the desktop app
description: Trigger ServiceNow AI Lens from the desktop app by using a Lens action to preview the extracted data and initiate post processing or auto-fill a form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/servicenow-lens/preview-desktop-others-lens.html
release: australia
product: ServiceNow Lens
classification: servicenow-lens
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Use, ServiceNow AI Lens, Enable AI experiences]
---

# Trigger ServiceNow AI Lens from the desktop app

Trigger ServiceNow AI Lens from the desktop app by using a Lens action to preview the extracted data and initiate post processing or auto-fill a form.

## Before you begin

To access the ServiceNow AI Lens functionality, perform the following steps:

-   Install ServiceNow AI Lens on your ServiceNow instance. For more information, see [Install the ServiceNow Lens in the ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/install-sn-lens.md).
-   Turn on the ServiceNow AI Lens skill to add the generative AI capability. For more information, see [Activate the ServiceNow AI Lens skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/activate-lens-skill.md).
-   Download the ServiceNow AI Lens installer to scan your desktop screen. For more information, see [Download and set how you want to launch ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/download-sn-lens-msi.md).

Verify that you've defined the Lens action for this purpose. For more information, see [Define a Lens action.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/servicenow-lens-actions.md)

Verify that ServiceNow AI Lens has access to record the screen on your system. For more information, see [Providing permission to ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/download-sn-lens-msi.md).

You must have create and update access privileges for creating or updating a record using ServiceNow AI Lens.

Don't scan any personally identifiable information, such as medical reports, financial reports, or other sensitive data, when using ServiceNow AI Lens as you don't want to expose the large language model \(LLM\) to any sensitive information.

Role required: lens\_user

## About this task

By using Lens actions, you can perform one of the following tasks:

-   **Fill a form**

    In the Lens action configuration, when **Trigger From** is Desktop and **Trigger For** is Form, and a table is selected, ServiceNow AI Lens can be triggered from the desktop to auto-fill a form. It first shows a preview of the data, and if the preview is editable, you can edit the fields before saving. After you select **Submit** in the preview window, it saves the form with the updated data on the ServiceNow instance.

-   **Preview the extracted data**

    In the Lens action configuration, when **Trigger From** is Desktop and **Trigger For** is Others, ServiceNow AI Lens can be triggered from the desktop to show preview of the extracted data. If the preview is editable, you can edit the fields before saving. After you select **Submit and close preview** in the preview window, it saves the data and initiates post processing.


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

6.  Select a Lens action.

7.  Select **Proceed with Lens**.

    \[Omitted image "lens-actions-home-screen-proceed.png"\] Alt text: Proceed with Lens button.

    Lens scanner opens in a separate window.

8.  Perform one of the following methods to enable ServiceNow AI Lens to extract data from documents.

    -   Extract data from a single screen.
        1.  On your system, open an artifact that you want to scan.

            An artifact can be an image, scanned or handwritten note, website, or application.

        2.  Place the ServiceNow AI Lensscannerwindow on the top of the artifact.

            You can resize the ServiceNow AI Lens scanner window by dragging its borders.

    -   Extract data from multiple screenshots.
        1.  Select the **Multi-capture** button \[Omitted image "multi-capture-icon.png"\] Alt text:.
        2.  Select the Capture icon \[Omitted image "capture-icon.png"\] Alt text:.
        3.  Place the ServiceNow AI Lensscannerwindow over another document or page and then select the Capture icon \[Omitted image "capture-icon.png"\] Alt text:.
        4.  Repeat the step to capture more screenshots, if required.

            \[Omitted image "lens-action-multi-capture-scrnshts.png"\] Alt text: Display of the number of screenshots captured.

            **Note:**

            -   You can capture a total of 10 screenshots with the combined size of all captured screenshots not exceeding 10 MB.
            -   To enable the desktop app to send large screenshot data to the server, confirm that the following system properties are set exactly as shown below:

                |Property name|Type|Recommended value|
                |-------------|----|-----------------|
                |glide.rest.max\_content\_length|Integer|15|
                |glide.rest.scripted.max\_inbound\_content\_length\_mb|Integer|15|

                For more information, see [Configure system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/r_ControllingMaxRequestSize.md)

                **Note:** You must have the admin role to set the system properties.

        5.  To complete the capture, select the Done icon \[Omitted image "lens-capture-done-icon.png"\] Alt text:.
    -   Extract data from uploaded documents.
        1.  Select the Upload files icon \[Omitted image "lens-file-upload-icon.png"\].s
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

9.  To provide instructions to analyze the data in screenshots in a specific way, select the Edit icon \[Omitted image "lens-instructions-icon.png"\] Alt text:, and enter the instructions.

    The default character limit is 500. Users with the admin role can increase this limit to up to 5000 characters by navigating to the **sn\_lens\_user\_prompt\_max\_length** system property.

10. To analyze the data in the screenshots that you captured, select **Analyze**.

    The ServiceNow AI Lens preview window displays the extracted output in an editable form.

    \[Omitted image "lens-action-form-preview-window.png"\] Alt text: Preview of extracted output displayed

11. Depending on the type of Lens action selected, perform the following steps.

<table id="choicetable_vdv_pdx_mgc"><thead><tr><th align="left" id="d208971e758">

Task

</th><th align="left" id="d208971e761">

Steps

</th></tr></thead><tbody><tr><td id="d208971e767">

**Filling form**

</td><td>

1.  \(Optional\) In case of editable preview, if necessary, edit the auto-filled field values before saving.
2.  On the form header in the Preview window, select **Submit** to save the filled form on the instance.


</td></tr><tr><td id="d208971e788">

**Previewing extracted data**

</td><td>

1.  \(Optional\) In case of editable preview, if necessary, edit the auto-filled field values before saving or copying the values.
2.  \(Optional\) Copy the previewed data by selecting the Copy icon \[Omitted image "icon-docintel-na-copy.png"\] Alt text:.


</td></tr></tbody>
</table>12. End the current session by selecting **Start new session**.


