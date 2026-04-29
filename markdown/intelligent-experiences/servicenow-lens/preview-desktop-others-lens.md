---
title: Trigger ServiceNow AI Lens from the desktop app
description: Trigger ServiceNow AI Lens from the desktop app by using a Lens action to preview the extracted data and initiate post processing or auto-fill a form.
locale: en-US
release: australia
product: ServiceNow Lens
classification: servicenow-lens
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Use, ServiceNow AI Lens, Enable AI experiences]
---

# Trigger ServiceNow AI Lens from the desktop app

Trigger ServiceNow AI Lens from the desktop app by using a Lens action to preview the extracted data and initiate post processing or auto-fill a form.

## Before you begin

To access the ServiceNow AI Lens functionality, perform the following steps:

-   Install ServiceNow AI Lens on your ServiceNow instance. For more information, see [Install the ServiceNow Lens in the ServiceNow instance](install-sn-lens.md).
-   Turn on the ServiceNow AI Lens skill to add the generative AI capability. For more information, see [Activate the ServiceNow AI Lens skill](activate-lens-skill.md).
-   Download the ServiceNow AI Lens installer to scan your desktop screen. For more information, see [Download the ServiceNow AI Lens installer](download-sn-lens-msi.md).

Verify that you've defined the Lens action for this purpose. For more information, see [Define a Lens action.](../concept/servicenow-lens-actions.md#)

Verify that ServiceNow AI Lens has access to record the screen on your system. For more information, see [Providing permission to ServiceNow AI Lens](download-sn-lens-msi.md#lens-permission).

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

1.  From your system, launch the ServiceNow AI Lens application.

2.  On the login page, in the **Instance URL** field, enter the ServiceNow instance URL.

    For example, `https://<instance name>.service-now.com`.

3.  Select **Proceed**.

4.  Log in to your ServiceNow account by entering your username and password.

    Your account must have the lens\_user role.

5.  On the onboarding journey widget, complete the onboarding and select **Got it**.

    ![Onboarding journey widget with three pages to show you the highlights of the application.](../image/onboarding-widget-lens.png)

    If you launch the ServiceNow AI Lens for the first time, the onboarding journey widget appears. You can select **Don't show me again** to hide the widget the next time you launch ServiceNow AI Lens.

6.  Select a Lens action.

7.  Select **Proceed with Lens**.

    Lens scanner opens in a separate window.

    **Note:** Use the scanner window to scan the data of the screenshot so you can submit it for analysis.

8.  On your system, open an artifact that you want to scan.

    An artifact can be an image, scanned or handwritten note, website, or application.

9.  Place the ServiceNow AI Lensscannerwindow on the top of the artifact.

    You can resize the ServiceNow AI Lens scanner window by dragging its borders.

10. Extract data from a single screen.

    1.  Enter additional instructions to extract, analyze, and organize data by selecting the Edit icon \(![Edit icon.](../image/lens-instructions-icon.png)\) and then enter the instructions.

        The default character limit is 500. Users with the admin role can increase this limit to up to 5000 characters by navigating to the `sn_lens_user_prompt_max_length` system property.

        **Note:** This is an optional step.

    2.  Select **Analyze**.

        The ServiceNow AI Lens preview window displays the extracted output in an editable form.

11. Extract data from multiple screenshots.

    1.  To provide additional instructions to extract, analyze, and organize data, select the Edit icon \(![Edit icon.](../image/lens-instructions-icon.png)\) and then enter the instructions.

        The default character limit is 500. Users with the admin role can increase this limit to up to 5000 characters by navigating to the `sn_lens_user_prompt_max_length` system property.

        **Note:** This is an optional step.

    2.  Select the **Multi-capture** button ![Multi-capture icon.](../image/multi-capture-icon.png).

        **Tip:** Use the Upload file icon \(![File Upload icon.](../image/lens-file-upload-icon.png)\) to upload one or more files. For more information, see [sn-lens-standalone-app.md\#upload-files-steps](sn-lens-standalone-app.md#upload-files-steps)

    3.  Select the Capture icon \(![Capture icon.](../image/capture-icon.png)\)

        The first screenshot is captured.

    4.  Place the ServiceNow AI Lensscannerwindow over another document or page and then select the Capture icon \).

        The second screenshot is captured.

        Repeat the step to capture more screenshots, if required.

        **Note:**

        -   You can capture a total of 10 screenshots with the combined size of all captured screenshots not exceeding 10 MB.
        -   To enable the desktop app to send large screenshot data to the server, confirm that the following system properties are set exactly as shown below:

            |Property name|Type|Recommended value|
            |-------------|----|-----------------|
            |glide.rest.max\_content\_length|Integer|15|
            |glide.rest.scripted.max\_inbound\_content\_length\_mb|Integer|15|

            For more information, see [Configure system property](https://www.servicenow.com/docs/access?context=r_ControllingMaxRequestSize&version=australia&pubname=australia-api-reference&ft:locale=en-US)

            **Note:** You must have the admin role to set the system properties.

    5.  To complete the capture, select the Done icon \(\).

    6.  Select **Analyze**.

        The data is extracted from the screenshots and the form that you can update and submit is shown.

12. Depending on the type of Lens action selected, perform the following steps.

<table id="choicetable_vdv_pdx_mgc"><thead><tr><th align="left" id="d110200e600">

Task

</th><th align="left" id="d110200e603">

Steps

</th></tr></thead><tbody><tr><td id="d110200e609">

**Filling form**

</td><td>

1.  \(Optional\) In case of editable preview, if necessary, edit the auto-filled field values before saving.
2.  On the form header in the Preview window, select **Submit** to save the filled form on the instance.


</td></tr><tr><td id="d110200e630">

**Previewing extracted data**

</td><td>

1.  \(Optional\) In case of editable preview, if necessary, edit the auto-filled field values before saving or copying the values.
2.  \(Optional\) Copy the previewed data by selecting the Copy icon ![](../../../administer/document-intelligence/image/icon-docintel-na-copy.png).


</td></tr></tbody>
</table>13. End the current session by selecting **Start new session**.


