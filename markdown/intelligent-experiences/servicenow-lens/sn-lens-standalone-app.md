---
title: Extract and analyze data with ServiceNow AI Lens desktop app
description: Extract and analyze data from one or more screenshots that you capture , and then preview the data analysis.
locale: en-US
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

Extract and analyze data from one or more screenshots that you capture , and then preview the data analysis.

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

<table id="choicetable_xtj_f4t_g3c"><thead><tr><th align="left" id="d157425e246">

Method

</th><th align="left" id="d157425e249">

Steps

</th></tr></thead><tbody><tr><td id="d157425e255">

**Capture a single screenshot of a document and analyze the data.**

</td><td>

1.  Select **Capture**.

The ServiceNow AI Lens scanner window is launched.

**Note:** Use the scanner window to scan the data of the screenshot so you can submit it for analysis.

2.  Open a document that you want to scan.

Example of a document: image, scanned handwritten note, Excel sheet, web page, or any document that gives visual data.

3.  Place the ServiceNow AI Lensscannerwindow over the document.
4.  \(Optional step\). To provide instructions to analyze the data in the screenshot in a specific way, select the Edit icon \(![Edit icon.](../image/lens-instructions-icon.png)\), and enter the instructions.

The default character limit is 500. Users with the admin role can increase this limit to up to 5000 characters by navigating to the `sn_lens_user_prompt_max_length` system property.

5.  To analyze the data in the screenshot that you captured, select **Analyze**.
6.  The preview of the analysis is displayed on the ServiceNow AI Lens preview window.


</td></tr><tr><td id="d157425e322">

**Capture multiple screenshots from one or more documents.**

</td><td>

1.  Select **Capture**.
2.  Open one or more documents from which you want to capture the screenshots.

Example of a document: image, scanned handwritten note, Excel sheet, web page, or any document that gives visual data.

3.  Select the Multi-capture icon \(![Multi-capture icon.](../image/lens-multi-capture-icon.png)\), and then place the scanner window over the document that you want to scan.

You can resize the scanner window by dragging its borders.

4.  \(Optional step\). To provide instructions to analyze the data in the screenshots in a specific way, select the Instructions icon \(![Instructions icon.](../image/lens-instructions-icon.png)\), and enter the instructions.

The default character limit is 500. Users with the admin role can increase this limit to up to 5000 characters by navigating to the `sn_lens_user_prompt_max_length` system property.

5.  Select the Capture icon \(\)

The first screenshot is captured.

6.  Place the ServiceNow AI Lensscannerwindow over the page of another or the same document and then select the Capture icon \(\).

The second screenshot is captured.

Repeat the step to capture more screenshots, if required.

7.  \(Optional step\) To remove a screenshot that you had captured, select the Delete icon.

**Tip:**

    -   Repeat the step as many times to remove as many screenshots.
    -   The last screenshot that you had captured is removed at the first click.
    -   You can capture one or more new screenshots after removing the screenshots.
8.  To complete the capture, select the Done icon \(\).
 The ServiceNow AI Lens preview window displays the screenshots that you've captured.

</td></tr></tbody>
</table>7.  Select **Analyze**.

    ServiceNow AI Lens displays the preview of the response

8.  Select **Submit** to trigger post processing.

    The **Submit** button appears on the Preview window if the post-processing is enabled in the related ServiceNow AI Lens action.

9.  Copy the previewed data by selecting the Copy icon ![Copy icon.](../../../administer/document-intelligence/image/icon-docintel-na-copy.png).

10. End the current session by selecting **Start new session**.


**Related topics**  


[Supporting information for ServiceNow AI Lens](../concept/sn-lens-supporting-info.md)

[ServiceNow AI Lens limitations](../reference/sn-lens-limitations.md)

[Create a record in an instance by using ServiceNow AI Lens](create-record-sn-lens.md)

[Update a record in an instance by using ServiceNow AI Lens](update-record-sn-lens.md)

