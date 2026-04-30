---
title: Autofill catalog item form in the Service Portal
description: Use ServiceNow AI Lens to extract data from artifacts and autofill catalog item forms in Service Portal. For example, autofill a new vendor onboarding form by extracting key details such as vendor name, address, contact email, and banking information from multiple artifacts, including Excel files, emails, images, and PDF documents.
locale: en-US
release: yokohama
product: ServiceNow Lens
classification: servicenow-lens
topic_type: task
last_updated: "2025-10-29"
reading_time_minutes: 3
breadcrumb: [Use, ServiceNow AI Lens, Enable AI experiences]
---

# Autofill catalog item form in the Service Portal

Use ServiceNow AI Lens to extract data from artifacts and autofill catalog item forms in Service Portal. For example, autofill a new vendor onboarding form by extracting key details such as vendor name, address, contact email, and banking information from multiple artifacts, including Excel files, emails, images, and PDF documents.

## Before you begin

Role required: lens\_user

## Procedure

1.  Navigate to the Service Portal.

    The URL is:

    ```
    https://<instance-name>.service-now.com/sp
    ```

2.  Navigate to the page that lists the catalog item that you need.

3.  Select the item category and the item from the catalog.

    For example, you could select New Vendor Registration.

4.  Select **Fill with Lens**.

5.  In the ServiceNow AI Lens.app dialog box, select Open ServiceNow AI Lens.app.

    **Tip:** This confirmation dialog appears when you select **Fill with Lens** for the first time. You can make this a one-time step by selecting **Always allow &lt;instance-name.service-now.com&gt; to open links of this type in the associated app** before selecting Open ServiceNow AI Lens.app.

6.  On the onboarding journey widget, complete the onboarding and select **Got it**.

    ![Onboarding journey widget with three pages to show you the highlights of the application.](../image/onboarding-widget-lens.png)

    If you launch the ServiceNow AI Lens for the first time, the onboarding journey widget appears. You can select **Don't show me again** to hide the widget the next time you launch ServiceNow AI Lens.

7.  On your system, open an artifact that you want to scan.

    An artifact can be an image, scanned or handwritten note, website, or application.

8.  Place the ServiceNow AI Lensscannerwindow on the top of the artifact.

    You can resize the ServiceNow AI Lens scanner window by dragging the scanner window borders.

9.  To extract data from a single screenshot of the artifact, do the steps.

    1.  Select the capture instructions icon \(![Capture instructions icon.](../image/lens-instructions-icon.png)\) and enter instructions to analyze.

        The default character limit is 500. Users with the admin role can increase this limit to up to 5000 characters by navigating to the `sn_lens_user_prompt_max_length` system property.

        **Note:** This is an optional step.

        ![Capture instructions field.](../image/lens-vendor-form-capture.png)

    2.  Select **Analyze**.

    ServiceNow AI Lens confirms that the catalog item form is filled.

    ![Single screen of artifact captured.](../image/lens-sp-single-scrn.png)

    ![New vendor registration form filled.](../image/lens-new-vendor-reg-form-filled.png "New Vendor Registration form fields auto-filled") ![Fields of New Vendor Registration field auto-filled with data from the artifact.]( "New Vendor Registration form fields auto-filled")

10. Extract the data from multiple screenshots.

    1.  Select the **Multi-capture** button ![](../image/multi-capture-icon.png).

    2.  Continue to take the required screenshots by selecting the **Capture** button ![](../image/capture-icon.png).

        You can capture up to 10 images to ServiceNow AI Lens.

        You can take multiple screenshots of the same artifact or different artifacts.

    3.  When you're finished taking screenshots, select **Done** ![](../image/done-icon.png).

        The window shows the thumbnails of the images that ServiceNow Lens captured.

        ![Multiple images captured.](../image/lens-catalog-multi-capture.png)

11. To provide additional instructions to Now Assist to extract the data from the screenshots, enter the instructions in the **Include additional directions** field.

    The default character limit is 500. Users with the admin role can increase this limit to up to 5000 characters by navigating to the `sn_lens_user_prompt_max_length` system property.

12. Select **Analyze**.

    The catalog item request form is filled with the extracted data.

13. In the catalog item request form, confirm that the catalog item form fields are correctly filled.

    The fields that are auto-filled by Now Assist are highlighted with the Sparkle icon ![Service Portal AI Sparkle icon.](../image/lens-sp-sparkle-icon.png).

    Only the field types that are supported by ServiceNow AI Lens get auto-populated with the extracted data. If the form doesn't have field types that are supported, then ServiceNow AI Lens won’t update the record. For more information about the supported fields, see [Field types supported](../reference/field-types-supported.md).

<table id="choicetable_g1q_l32_2hc"><thead><tr><th align="left" id="d72655e380">

Option

</th><th align="left" id="d72655e383">

Action

</th></tr></thead><tbody><tr><td id="d72655e389">

**If the auto-filled text looks good**

</td><td>

Save the record by selecting **Submit**.

</td></tr><tr><td id="d72655e401">

**If the auto-filled text requires changes**

</td><td>

Do one of the following actions:-   Manually adjust the information in the fields and save the record.
-   In the ServiceNow AI Lens window, provide different instructions or take more screenshots and select **Analyze** so that ServiceNow AI Lens can extract, comprehend the data again, and auto-fill the data into the record. Save the record by selecting **Submit**.

You can analyze the artifacts as many times as needed without reloading the form.

</td></tr></tbody>
</table>
