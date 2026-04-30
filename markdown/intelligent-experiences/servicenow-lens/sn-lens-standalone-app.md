---
title: Extract and analyze your data by using ServiceNow AI Lens in the standalone mode
description: Extract and analyze your data by using the ServiceNow AI Lens as a standalone application. You can scan visual data, such as handwritten texts, images, applications, and websites and then preview the generated outcome according to the instructions that you provide.
locale: en-US
release: yokohama
product: ServiceNow Lens
classification: servicenow-lens
topic_type: task
last_updated: "2025-03-18"
reading_time_minutes: 5
keywords: [standalone app, ServiceNow lens as standalone app, Start ServiceNow lens from desktop, Start ServiceNow lens from Windows, Start ServiceNow lens from MacOS, Use ServiceNow lens from desktop, Use ServiceNow lens from Windows, Use ServiceNow lens from MacOS]
breadcrumb: [Use, ServiceNow AI Lens, Enable AI experiences]
---

# Extract and analyze your data by using ServiceNow AI Lens in the standalone mode

Extract and analyze your data by using the ServiceNow AI Lens as a standalone application. You can scan visual data, such as handwritten texts, images, applications, and websites and then preview the generated outcome according to the instructions that you provide.

## Before you begin

To access the ServiceNow AI Lens functionality, perform the following steps:

-   Install ServiceNow AI Lens on your ServiceNow instance. For more information, see [Install the ServiceNow Lens in the ServiceNow instance](install-sn-lens.md).
-   Turn on the ServiceNow AI Lens skill to add the generative AI capability. For more information, see [Activate the ServiceNow AI Lens skill](activate-lens-skill.md).
-   Download the ServiceNow AI Lens installer to scan your desktop screen. For more information, see [Download the ServiceNow AI Lens installer](download-sn-lens-msi.md).

Don't scan any personally identifiable information, such as medical reports, financial reports, or other sensitive data, when using ServiceNow AI Lens as you don't want to expose the large language model \(LLM\) to any sensitive information.

Verify that you have provided permission to ServiceNow AI Lens to record the screen on your system.

Role required: lens\_user

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

6.  Scan and extract the data from artifacts such as handwritten texts, images, documents, and websites by selecting **Capture with Lens**.

7.  On your system, open an artifact that you want to scan.

    An artifact can be an image, scanned or handwritten note, website, or application.

8.  Place the ServiceNow AI Lensscannerwindow on the top of the artifact.

    You can resize the ServiceNow AI Lens scanner window by dragging its borders.

9.  Extract data from a single screen.

    1.  Enter additional instructions to extract, analyze, and organize data by selecting the Instructions icon \(![Instructions icon.](../image/lens-instructions-icon.png)\) and then enter the instructions.

        The default character limit is 500. Users with the admin role can increase this limit to up to 5000 characters by navigating to the `sn_lens_user_prompt_max_length` system property.

        **Note:** This is an optional step.

        ![Field that accepts additional instructions.](../image/lens-scanner-additional-instructions.png)

10. Extract the data from multiple screenshots.

    1.  Select the **Multi-capture** button ![](../image/multi-capture-icon.png).

    2.  Continue to take the required screenshots by selecting the **Capture** button ![](../image/capture-icon.png).

        You can capture up to 10 images to ServiceNow AI Lens.

        You can take multiple screenshots of the same artifact or different artifacts.

    3.  When you're finished taking screenshots, select **Done** ![](../image/done-icon.png).

        ![Done button after capturing multiple screenshots.](../image/lens-capture-complete.png)

        The window shows the thumbnails of the images that ServiceNow AI Lens captured.

        ![Multiple screens captured.](../image/lens-scanner-analyze-multiple-scrns.png)

11. In the **Include additional directions** field, provide further instructions for analyzing and comprehending data.

    The default character limit is 500. Users with the admin role can increase this limit to up to 5000 characters by navigating to the `sn_lens_user_prompt_max_length` system property.

    The instruction text is used by the ServiceNow AI Lens skill to extract data or generate output according to your requirements. Use short, direct, and clear sentences to describe the expected outcome. Be specific, provide detailed descriptions, and avoid jargon and abbreviations.

    Example: You can use ServiceNow AI Lens to extract data from multiple screenshots and provide you with an output in the JSON format. You can see this output in the Preview window.

    `Extract name, user email ID, and designation from the resumes and present data in a JSON format.`![Additional instructions for processing.](../image/lens-addnl-instructions-post-capture.png)

12. Analyze and comprehend the data by selecting **Analyze**.

    ![Analyze button on the scanner window for the single capture.](../image/single-analyze-lens.png "Analyzing the single screenshot")

    ![Analyze button on the Home page window for the multi-capture.](../image/multi-analyze-lens.png "Analyzing the multiple screenshots")

    The extracted data is shown in the Preview window. ServiceNow AI Lens uses Now Assist to extract, comprehend, and show a preview of the data.

13. Select **Submit** to trigger post processing.

    The **Submit** button appears on the Preview window if the post-processing is enabled in the related ServiceNow AI Lens action.

14. Copy the previewed data by selecting the Copy icon ![Copy icon.](../../../administer/document-intelligence/image/icon-docintel-na-copy.png).

15. End the current session by selecting **Start new session**.


**Related topics**  


[Supporting information for ServiceNow AI Lens](../concept/sn-lens-supporting-info.md)

[ServiceNow AI Lens limitations](../reference/sn-lens-limitations.md)

[Create a record in an instance by using ServiceNow AI Lens](create-record-sn-lens.md)

[Update a record in an instance by using ServiceNow AI Lens](update-record-sn-lens.md)

