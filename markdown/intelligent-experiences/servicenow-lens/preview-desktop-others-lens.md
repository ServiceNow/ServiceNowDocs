---
title: Trigger ServiceNow AI Lens from the desktop app
description: Trigger ServiceNow AI Lens from a desktop by using a Lens action to preview the extracted data and initiate post processing or auto-fill a form.
locale: en-US
release: yokohama
product: ServiceNow Lens
classification: servicenow-lens
topic_type: task
last_updated: "2025-07-17"
reading_time_minutes: 5
breadcrumb: [Use, ServiceNow AI Lens, Enable AI experiences]
---

# Trigger ServiceNow AI Lens from the desktop app

Trigger ServiceNow AI Lens from a desktop by using a Lens action to preview the extracted data and initiate post processing or auto-fill a form.

## Before you begin

To access the ServiceNow AI Lens functionality, perform the following steps:

-   Install ServiceNow AI Lens on your ServiceNow instance. For more information, see [Install the ServiceNow Lens in the ServiceNow instance](install-sn-lens.md).
-   Turn on the ServiceNow AI Lens skill to add the generative AI capability. For more information, see [Activate the ServiceNow AI Lens skill](activate-lens-skill.md).
-   Download the ServiceNow AI Lens installer to scan your desktop screen. For more information, see [Download the ServiceNow AI Lens installer](download-sn-lens-msi.md).

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

    When ServiceNow AI Lens is triggered from the desktop app, it does one of the following things:

    -   Shows preview of the extracted data.
    -   Creates a record on the ServiceNow instance.
7.  Select **Proceed with Lens**.

    ![Proceed with Lens button.](../image/lens-actions-home-screen.png)

    Lens scanner opens in a separate window.

8.  On your system, open an artifact that you want to scan.

    An artifact can be an image, scanned or handwritten note, website, or application.

9.  Place the ServiceNow AI Lensscannerwindow on the top of the artifact.

    You can resize the ServiceNow AI Lens scanner window by dragging its borders.

10. Extract data from a single screen.

    1.  Enter additional instructions to extract, analyze, and organize data by selecting the Instructions icon \(![Instructions icon.](../image/lens-instructions-icon.png)\) and then enter the instructions.

        The default character limit is 500. Users with the admin role can increase this limit to up to 5000 characters by navigating to the `sn_lens_user_prompt_max_length` system property.

        ![Lens incident email.](../image/lens-incident-email.png)

    2.  Select **Analyze**.

        The ServiceNow AI Lens preview window displays the extracted output.

        ![Preview window showing output.](../image/lens-action-preview.png)

11. Extract the data from multiple screenshots.

    1.  Select the **Multi-capture** button ![](../image/multi-capture-icon.png).

    2.  Continue to take the required screenshots by selecting the **Capture** button ![](../image/capture-icon.png).

        You can capture up to 10 images to ServiceNow AI Lens.

        You can take multiple screenshots of the same artifact or different artifacts.

    3.  When you're finished taking screenshots, select **Done** ![](../image/done-icon.png).

        ![Done button after capturing multiple screenshots.](../image/lens-capture-complete.png)

        The window shows the thumbnails of the images that ServiceNow AI Lens captured.

        ![Multiple screens captured.](../image/lens-scanner-analyze-multiple-scrns.png)

12. In the **Additional directions for Now Assist** field, provide further instructions for analyzing and comprehending data.

    The default character limit is 500. Users with the admin role can increase this limit to up to 5000 characters by navigating to the `sn_lens_user_prompt_max_length` system property.

    The instruction text is used by the ServiceNow AI Lens skill to extract data or generate output according to your requirements. Use short, direct, and clear sentences to describe the expected outcome. Be specific, provide detailed descriptions, and avoid jargon and abbreviations.

    Example: You can use ServiceNow AI Lens to extract data from multiple screenshots and provide you with an output in the JSON format. You can see this output in the Preview window.

    `Extract name, user email ID, and designation from the resumes and present data in a JSON format.`

    ![Field for inserting Now Assist instructions to extract data in a specific way.](../image/now-assist-instructions-lens-1.png)

13. Analyze and comprehend the data by selecting **Analyze**.

    ![Analyze button on the scanner window for the single capture.](../image/single-analyze-lens.png "Analyzing the single image")

    ![Analyze button on the Home page window for the multi-capture.](../image/multi-analyze-lens.png "Analyzing the multiple images")

    The extracted data is shown in the Preview window. ServiceNow AI Lens uses Now Assist to extract, comprehend, and show a preview of the data.

    ![Editable Form preview.](../image/lens-form-preview.png "Editable preview of the form")

    ![Editable preview of the extracted data.](../image/sn-lens-home-page-preview.png "Editable preview of the extracted data")

14. Depending on the type of Lens action selected, perform the following steps.

<table id="choicetable_vdv_pdx_mgc"><thead><tr><th align="left" id="d51837e601">

Task

</th><th align="left" id="d51837e604">

Steps

</th></tr></thead><tbody><tr><td id="d51837e610">

**Filling form**

</td><td>

1.  \(Optional\) In case of editable preview, if necessary, edit the auto-filled field values before saving.
2.  On the form header in the Preview window, select **Submit** to save the filled form on the instance.


</td></tr><tr><td id="d51837e631">

**Previewing extracted data**

</td><td>

1.  \(Optional\) In case of editable preview, if necessary, edit the auto-filled field values before saving or copying the values.
2.  \(Optional\) Copy the previewed data by selecting the Copy icon ![](../../../administer/document-intelligence/image/icon-docintel-na-copy.png).
3.  Select **Submit**.


</td></tr></tbody>
</table>15. End the current session by selecting **Start new session**.


