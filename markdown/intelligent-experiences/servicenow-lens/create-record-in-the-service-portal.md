---
title: Auto-fill catalog item form in the Service Portal
description: Use ServiceNow AI Lens to extract data from documents and auto-fill catalog item forms in Service Portal. For example, auto-fill a new vendor onboarding form by extracting key details such as vendor name, address, contact email, and banking information from multiple documents, that includes Excel files, emails, images, and PDF documents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/servicenow-lens/create-record-in-the-service-portal.html
release: australia
product: ServiceNow Lens
classification: servicenow-lens
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Use, ServiceNow AI Lens, Enable AI experiences]
---

# Auto-fill catalog item form in the Service Portal

Use ServiceNow AI Lens to extract data from documents and auto-fill catalog item forms in Service Portal. For example, auto-fill a new vendor onboarding form by extracting key details such as vendor name, address, contact email, and banking information from multiple documents, that includes Excel files, emails, images, and PDF documents.

## Before you begin

Role required: lens\_user

## About this task

You can auto-fill catalog item forms in the Service Portal in two ways:

-   **From your browser**: Use ServiceNow AI Lens to capture a screen from the browser, analyze the contents of the captured screen and auto-fill the form fields in the Service Portal — no download or installation of the desktop app required. For more information, see [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/create-record-in-the-service-portal.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/create-record-in-the-service-portal.md).

    **Note:**

    -   The screen capture experience may vary depending on your browser.

        **Tip:** For the best experience, use ServiceNow AI Lens on any Chromium-based browser.

    -   The browser-based experience supports single-screen capture. To capture multiple screens or upload files, see [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/create-record-in-the-service-portal.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/create-record-in-the-service-portal.md).
-   **From the desktop app**: Use the ServiceNow AI Lens desktop app for the full range of capture and analysis capabilities, such as multi-image capture and file uploads. For more information, see [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/create-record-in-the-service-portal.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/create-record-in-the-service-portal.md).

## Procedure

1.  Auto-fill catalog item forms in Service Portal by performing any of the following methods.

<table id="choicetable_zd4_nxq_pjc"><thead><tr><th align="left" id="d59669e122">

Method

</th><th align="left" id="d59669e125">

Steps

</th></tr></thead><tbody><tr><td id="auto-fill-catalog-from-browser">

**From your browser**

</td><td>

1.  Navigate to the Service Portal and log in.

The URL is

    ```
https://<instance-name>.service-now.com/sp
    ```

This procedure demonstrates how to request an iPhone from the Service Portal by capturing the browser screen and auto-filling the form.

2.  Navigate to the item that you want to request and select it.
3.  Select **Fill with Lens**.

\[Omitted image "lens-select-fill-with-lens.png"\] Alt text: Fill with Lens button.

4.  Select **Capture screen**.

\[Omitted image "lens-sel-capture-screen.png"\] Alt text: Capture screen button.

5.  Select the screen that you want to capture, and then select **Share**.

**Note:**

    -   The screen capture options depend on your browser.
    -   For illustration purpose, the following steps show the capturing of an Outlook email screen from Chrome tab and the auto-filling of a catalog item form fields for an iPhone.
\[Omitted image "lens-select-capture-element.png"\] Alt text: Browser dialog to select a screen to capture.

ServiceNow AI Lens shows the captured Outlook email screen that it will analyze.

\[Omitted image "lens-email-screen-shared.png"\] Alt text: Screen shared.

6.  \(Optional step\). To specify the area of the captured screen that you want ServiceNow AI Lens to analyze, select **Crop**, and then use the crop handles.
7.  Select **Confirm**.
8.  \(Optional steps\). Perform the following steps:
    -   In the Additional instructions field, enter specific instructions to guide ServiceNow AI Lens in extracting the information you need from the captured screen.
    -   Select **Re-capture** to discard the current capture and capture a new screen.
    -   Select **Revert to original** to undo the crop and restore the full captured image.
    -   Select **Crop** to further refine your selection by cropping the already cropped screen.
9.  To let ServiceNow AI Lens analyze the captured screen, select **Analyze**.

ServiceNow AI Lens notifies that it has auto-filled the catalog item form fields.

\[Omitted image "lens-catalog-form-auto-filled.png"\] Alt text: Catalog form fields auto-fill notification.

10. Navigate to the catalog item form that you wanted to auto-fill and verify that the fields are correctly filled.

\[Omitted image "lens-catalog-form-autofilled.png"\] Alt text: Catalog form fields auto-filled.

**Note:**

The AI sparkle icon \(\[Omitted image "lens-sp-sparkle-icon.png"\] Alt text: AI sparkle icon.\) next to a field indicates that the field is auto-filled by ServiceNow AI Lens.

</td></tr><tr><td id="use-desktop-app">

**From the desktop app**

</td><td>

1.  Navigate to the Service Portal.

The URL is:

    ```
https://<instance-name>.service-now.com
    ```

This procedure demonstrates how to auto-fill a vendor onboarding form in the Service Portal.

2.  Navigate to the item that you want to request and select it.

For example, you could select New Vendor Registration.

3.  Select **Fill with Lens**.

\[Omitted image "lens-select-fill-with-lens.png"\] Alt text: Fill with Lens button.

4.  Select **Open AI Lens desktop**.

\[Omitted image "lens-open-desktop-app.png"\] Alt text: Open AI lens desktop button.

5.  In the ServiceNow AI Lens.app dialog box, select Open ServiceNow AI Lens.app.

**Note:** This confirmation dialog appears when you select **Fill with Lens** for the first time. You can make this a one-time step by selecting **Always allow &lt;instance-name.service-now.com&gt; to open links of this type in the associated app** before selecting Open ServiceNow AI Lens.app.

6.  \(Optional step\). On the onboarding journey widget, complete the onboarding and select **Got it**.

\[Omitted image "onboarding-widget-lens.png"\] Alt text: Onboarding journey widget with three pages to show you the highlights of the application.

If you launch the ServiceNow AI Lens for the first time, the onboarding journey widget appears. You can select **Don't show me again** to hide the widget the next time you launch ServiceNow AI Lens.

7.  Place the ServiceNow AI Lensscannerwindow on the top of the document.

You can resize the ServiceNow AI Lens scanner window by dragging the scanner window borders.

8.  Perform any one of the following steps.

**Extract data from a single screenshot and auto-fill the form**

    1.  \(Optional step\). To provide instructions to extract the data from the document in a specific way, select the Edit icon \(\[Omitted image "lens-instructions-icon.png"\] Alt text: Capture instructions icon.\) and enter instructions to analyze.

The default character limit is 500. Users with the admin role can increase this limit to up to 5000 characters by navigating to the `sn_lens_user_prompt_max_length` system property.

\[Omitted image "lens-vendor-form-capture.png"\] Alt text: Enter specific instructions.

    2.  Select **Analyze**.

ServiceNow AI Lens confirms that the catalog item form is filled.

\[Omitted image "lens-new-vendor-reg-form-filled.png"\] Alt text: New vendor registration form filled.

**Extract data from multiple screenshots and auto-fill the form**

        1.  Select the Multi-capture icon \(\[Omitted image "lens-multi-capture-icon.png"\] Alt text: Multi-capture icon.\), and then place the scanner window over the document that you want to scan.

You can resize the scanner window by dragging its borders.

        2.  \(Optional step\). To provide instructions to extract the data from the document in a specific way, select the Edit icon \(\[Omitted image "lens-instructions-icon.png"\] Alt text: Instructions icon.\), and enter the instructions.

\[Omitted image "lens-vendor-form-capture.png"\] Alt text: Enter specific instructions.

The default character limit is 500. Users with the admin role can increase this limit to up to 5000 characters by navigating to the `sn_lens_user_prompt_max_length` system property.

        3.  Select the Capture icon \(\[Omitted image "capture-icon.png"\] Alt text: Capture icon.\).

The first screenshot is captured.

        4.  Place the ServiceNow AI Lensscannerwindow over the page of another or the same document and then select the Capture icon \(\[Omitted image "capture-icon.png"\] Alt text: Capture icon.\).

The second screenshot is captured.

Repeat the step to capture more screenshots, if required.

\[Omitted image "lens-venform-multi-capture.png"\] Alt text: View the number of screenshots you've captured

        5.  \(Optional step\) To remove a screenshot that you had captured, select the Delete icon.

\[Omitted image "lens-vendor-form-remove-scrnsht.png"\] Alt text: Remove captured screenshot

        6.  To complete the capture, select the Done icon \(\[Omitted image "lens-capture-done-icon.png"\] Alt text: Capture complete icon.\).

The ServiceNow AI Lens preview window displays the screenshots that you've captured.

\[Omitted image "lens-vendor-form-multi-scrnshts-captured.png"\] Alt text: Preview of multiple captured screenshots

        7.  Select **Analyze**.

The catalog item form is auto-filled.

\[Omitted image "lens-new-vendor-reg-form-filled.png"\] Alt text: New vendor registration form filled. \[Omitted image ""\] Alt text: Fields of New Vendor Registration field auto-filled with data from the artifact.

</td></tr></tbody>
</table>2.  In the catalog item request form, confirm that the catalog item form fields are correctly filled.

    The fields that are auto-filled by Now Assist are highlighted with the Sparkle icon \[Omitted image "lens-sp-sparkle-icon.png"\] Alt text: Service Portal AI Sparkle icon..

    Only the field types that are supported by ServiceNow AI Lens get auto-populated with the extracted data. If the form doesn't have field types that are supported, then ServiceNow AI Lens won’t update the record. For more information about the supported fields, see [Field types supported](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/field-types-supported.md).

<table id="choicetable_g1q_l32_2hc"><thead><tr><th align="left" id="d59669e676">

Option

</th><th align="left" id="d59669e679">

Action

</th></tr></thead><tbody><tr><td id="d59669e685">

**If the auto-filled text looks good**

</td><td>

Save the record by selecting **Submit**.

</td></tr><tr><td id="d59669e697">

**If the auto-filled text requires changes**

</td><td>

Do one of the following actions:-   Manually adjust the information in the fields and save the record.
-   In the ServiceNow AI Lens window, provide different instructions or take more screenshots and select **Analyze** so that ServiceNow AI Lens can extract, comprehend the data again, and auto-fill the data into the record. Save the record by selecting **Submit**.

You can analyze the artifacts as many times as needed without reloading the form.

</td></tr></tbody>
</table>
