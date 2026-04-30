---
title: Create a record in an instance by using ServiceNow AI Lens
description: Create a record in the ServiceNow instance and auto-fill the data that is extracted from a screen by using the ServiceNow AI Lens application.
locale: en-US
release: yokohama
product: ServiceNow Lens
classification: servicenow-lens
topic_type: task
last_updated: "2025-03-17"
reading_time_minutes: 5
keywords: [Create record using ServiceNow lens, Scan document using ServiceNow lens, Scan image using ServiceNow lens, Scan scanned document using ServiceNow lens, Scan email using ServiceNow lens]
breadcrumb: [Use, ServiceNow AI Lens, Enable AI experiences]
---

# Create a record in an instance by using ServiceNow AI Lens

Create a record in the ServiceNow instance and auto-fill the data that is extracted from a screen by using the ServiceNow AI Lens application.

## Before you begin

You must perform this task in Core UI.

To access the ServiceNow AI Lens functionality, perform the following steps:

-   Install ServiceNow AI Lens on your ServiceNow instance. For more information, see [Install the ServiceNow Lens in the ServiceNow instance](install-sn-lens.md).
-   Turn on the ServiceNow AI Lens skill to add the generative AI capability. For more information, see [Activate the ServiceNow AI Lens skill](activate-lens-skill.md).
-   Download the ServiceNow AI Lens installer to scan your desktop screen. For more information, see [Download the ServiceNow AI Lens installer](download-sn-lens-msi.md).

Verify that ServiceNow AI Lens has access to record the screen on your system. For more information, see [Providing permission to ServiceNow AI Lens](download-sn-lens-msi.md#lens-permission).

You must have create and update access privileges to see the **Create with Lens** button in the list view of any table.

Don't scan any personally identifiable information, such as medical reports, financial reports, or other sensitive data, when using ServiceNow AI Lens as you don't want to expose the large language model \(LLM\) to any sensitive information.

Role required: lens\_user

## Procedure

1.  In your ServiceNow instance, navigate to the list view of any table.

2.  Create a record with the help of ServiceNow AI Lens by selecting **Create with Lens**.

    ![Create with Lens button on the ServiceNow instance.](../image/luanch-from-sn-instance.png)

    You must have create and update access privileges to see the **Create with Lens** button in the list view of any table.

3.  In the ServiceNow AI Lens.app dialog box, select Open ServiceNow AI Lens.app.

    **Tip:** This confirmation dialog appears when you select **Create with Lens** for the first time. You can make this a one-time step by selecting **Always allow &lt;instance-name.service-now.com&gt; to open links of this type in the associated app** before selecting Open ServiceNow AI Lens.app.

4.  On the onboarding journey widget, complete the onboarding and select **Got it**.

    ![Onboarding journey widget with three pages to show you the highlights of the application.](../image/onboarding-widget-lens.png)

    If you launch the ServiceNow AI Lens for the first time, the onboarding journey widget appears. You can select **Don't show me again** to hide the widget the next time you launch ServiceNow AI Lens.

5.  On your system, open an artifact that you want to scan.

    An artifact can be an image, scanned or handwritten note, website, or application.

6.  Place the ServiceNow AI Lensscannerwindow on the top of the artifact.

    You can resize the ServiceNow AI Lens scanner window by dragging its borders.

7.  Extract data from a single screen.

    1.  Enter additional instructions to extract, analyze, and organize data by selecting the Instructions icon \(![Instructions icon.](../image/lens-instructions-icon.png)\) and then enter the instructions.

        The default character limit is 500. Users with the admin role can increase this limit to up to 5000 characters by navigating to the `sn_lens_user_prompt_max_length` system property.

        **Note:** This is an optional step.

        ![Incident email captured by Lens.](../image/lens-incident-email.png)

    2.  Select **Analyze**.

        The form is filled with the extracted data.

        ![Notification that form is filled with extracted data.](../image/lens-form-filled-instance.png)

    3.  Confirm that the form fields are correctly updated.

8.  Extract the data from multiple screenshots.

    1.  Select the **Multi-capture** button ![](../image/multi-capture-icon.png).

    2.  Continue to take the required screenshots by selecting the **Capture** button ![](../image/capture-icon.png).

        You can capture up to 10 images to ServiceNow AI Lens.

        You can take multiple screenshots of the same artifact or different artifacts.

    3.  When you're finished taking screenshots, select **Done** ![](../image/done-icon.png).

        ![Done button after capturing multiple screenshots.](../image/lens-capture-complete.png)

        The window shows the thumbnails of the images that ServiceNow AI Lens captured.

        ![Multiple screens captured.](../image/lens-scanner-analyze-multiple-scrns.png)

9.  In the **Include additional directions** field, provide further instructions for analyzing and comprehending data.

    The default character limit is 500. Users with the admin role can increase this limit to up to 5000 characters by navigating to the `sn_lens_user_prompt_max_length` system property.

    The instruction text is used by the ServiceNow AI Lens skill to extract data according to your requirements and fill in the form. Use short, direct, and clear sentences to describe the expected outcome. Be specific, provide detailed descriptions, and avoid jargon and abbreviations.

    Example: If you must submit an invoice request using multiple bills, you can use ServiceNow AI Lens to extract bill information for a certain date to fill the Invoice form.

    `Extract only the bills with dates that match March 15, 2025. Ignore other dates and unrelated information. If multiple bills have the same date, use them all.`

    ![Additional instructions.](../image/lens-additional-instructions.png)

10. In the ServiceNow instance, review the text that is auto-filled by Now Assist into your record.

    The fields that are auto-filled by Now Assist are highlighted with the Sparkle icon ![](../../../common/image/icon-ai-sparkle.png).

    Only the field types that are supported by ServiceNow AI Lens get auto-populated with the extracted data. If the form doesn't have field types that are supported, then ServiceNow AI Lens won’t update the record. For more information about the supported fields, see [Field types supported](../reference/field-types-supported.md).

<table id="choicetable_jjf_zx2_s2c"><thead><tr><th align="left" id="d49483e520">

Option

</th><th align="left" id="d49483e523">

Action

</th></tr></thead><tbody><tr><td id="d49483e529">

**If the auto-filled text looks good**

</td><td>

Save the record by right-clicking on the form header and then selecting **Save**.

</td></tr><tr><td id="d49483e541">

**If the auto-filled text requires changes**

</td><td>

Do one of the following actions:-   Manually adjust the information in the fields and save the record.
-   In the ServiceNow AI Lens window, provide different instructions or take more screenshots and select **Analyze** so that ServiceNow AI Lens can extract, comprehend the data again, and auto-fill the data into the record. Save the record by selecting **Save**.

You can analyze the artifacts as many times as needed without reloading the form.

</td></tr></tbody>
</table>
**Related topics**  


[Supporting information for ServiceNow AI Lens](../concept/sn-lens-supporting-info.md)

[ServiceNow AI Lens limitations](../reference/sn-lens-limitations.md)

[Update a record in an instance by using ServiceNow AI Lens](update-record-sn-lens.md)

[Extract and analyze your data by using ServiceNow AI Lens in the standalone mode](sn-lens-standalone-app.md)

