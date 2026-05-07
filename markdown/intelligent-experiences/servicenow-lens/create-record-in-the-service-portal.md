---
title: Autofill catalog item form in the Service Portal
description: Use ServiceNow AI Lens to extract data from artifacts and autofill catalog item forms in Service Portal. For example, autofill a new vendor onboarding form by extracting key details such as vendor name, address, contact email, and banking information from multiple artifacts, including Excel files, emails, images, and PDF documents.
locale: en-US
release: australia
product: ServiceNow Lens
classification: servicenow-lens
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
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

8.  Place the ServiceNow AI Lensscannerwindow on the top of the document.

    You can resize the ServiceNow AI Lens scanner window by dragging the scanner window borders.

9.  Perform any one of the set of steps given below.

<table id="choicetable_eml_wsz_33c"><thead><tr><th align="left" id="d55873e181">

Method

</th><th align="left" id="d55873e184">

Steps

</th></tr></thead><tbody><tr><td id="d55873e190">

**Extract data from a single screenshot and auto-fill the form**

</td><td>

1.  \(Optional step\). To provide instructions to extract the data from the document in a specific way, select the Edit icon \(![Capture instructions icon.](../image/lens-instructions-icon.png)\) and enter instructions to analyze.

The default character limit is 500. Users with the admin role can increase this limit to up to 5000 characters by navigating to the `sn_lens_user_prompt_max_length` system property.

![Enter specific instructions.](../image/lens-vendor-form-capture.png "Enter specific instructions")

2.  Select **Analyze**.

ServiceNow AI Lens confirms that the catalog item form is filled.

![New vendor registration form filled.](../image/lens-new-vendor-reg-form-filled.png "New Vendor Registration form fields auto-filled")

</td></tr><tr><td id="d55873e254">

**Extract data from multiple screenshots and auto-fill the form**

</td><td>

1.  Select the Multi-capture icon \(![Multi-capture icon.](../image/lens-multi-capture-icon.png)\), and then place the scanner window over the document that you want to scan.

You can resize the scanner window by dragging its borders.

2.  \(Optional step\). To provide instructions to extract the data from the document in a specific way, select the Edit icon \(![Instructions icon.](../image/lens-instructions-icon.png)\), and enter the instructions.

![Enter specific instructions.](../image/lens-vendor-form-capture.png "Enter specific instructions")

The default character limit is 500. Users with the admin role can increase this limit to up to 5000 characters by navigating to the `sn_lens_user_prompt_max_length` system property.

3.  Select the Capture icon \(![Capture icon.](../image/capture-icon.png)\).

The first screenshot is captured.

4.  Place the ServiceNow AI Lensscannerwindow over the page of another or the same document and then select the Capture icon \(![Capture icon.](../image/capture-icon.png)\).

The second screenshot is captured.

Repeat the step to capture more screenshots, if required.

![View the number of screenshots you've captured](../image/lens-venform-multi-capture.png "View the number of screenshots you've captured")

5.  \(Optional step\) To remove a screenshot that you had captured, select the Delete icon.

![Remove captured screenshot](../image/lens-vendor-form-remove-scrnsht.png "Remove captured screenshot")

6.  To complete the capture, select the Done icon \(![Capture complete icon.](../image/lens-capture-done-icon.png)\).

The ServiceNow AI Lens preview window displays the screenshots that you've captured.

![Preview of multiple captured screenshots](../image/lens-vendor-form-multi-scrnshts-captured.png "Preview of multiple captured screenshots")

7.  Select **Analyze**.

The catalog item form is auto-filled.

![New vendor registration form filled.](../image/lens-new-vendor-reg-form-filled.png "New Vendor Registration form fields auto-filled") ![Fields of New Vendor Registration field auto-filled with data from the artifact.]( "New Vendor Registration form fields auto-filled")

</td></tr></tbody>
</table>10. In the catalog item request form, confirm that the catalog item form fields are correctly filled.

    The fields that are auto-filled by Now Assist are highlighted with the Sparkle icon ![Service Portal AI Sparkle icon.](../image/lens-sp-sparkle-icon.png).

    Only the field types that are supported by ServiceNow AI Lens get auto-populated with the extracted data. If the form doesn't have field types that are supported, then ServiceNow AI Lens won’t update the record. For more information about the supported fields, see [Field types supported](../reference/field-types-supported.md).

<table id="choicetable_g1q_l32_2hc"><thead><tr><th align="left" id="d55873e461">

Option

</th><th align="left" id="d55873e464">

Action

</th></tr></thead><tbody><tr><td id="d55873e470">

**If the auto-filled text looks good**

</td><td>

Save the record by selecting **Submit**.

</td></tr><tr><td id="d55873e482">

**If the auto-filled text requires changes**

</td><td>

Do one of the following actions:-   Manually adjust the information in the fields and save the record.
-   In the ServiceNow AI Lens window, provide different instructions or take more screenshots and select **Analyze** so that ServiceNow AI Lens can extract, comprehend the data again, and auto-fill the data into the record. Save the record by selecting **Submit**.

You can analyze the artifacts as many times as needed without reloading the form.

</td></tr></tbody>
</table>
