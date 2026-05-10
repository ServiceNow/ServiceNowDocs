---
title: Perform the Article Quality Index review
description: Perform the Article Quality Index \(AQI\) review to evaluate the quality of the article.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use Article Quality Index, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Perform the Article Quality Index review

Perform the Article Quality Index \(AQI\) review to evaluate the quality of the article.

## Before you begin

The knowledge base must have an assigned AQI checklist.

Role required: knowledge\_domain\_expert, knowledge\_coach, knowledge\_admin, or admin

## About this task

Configure the **glide.knowman.aqi.article\_workflow\_states** property to set the article workflow states where you could perform AQI reviews. You can perform several AQI reviews for an article. If you perform several AQI reviews for the same version of the article, the latest AQI score appears in the **Latest AQI** field in the article.

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Articles** and click **Published**.

2.  Click an article link.

    **Note:** To read the article and perform the AQI review simultaneously, open the article in two separate tabs or window in your browser. You can then read the article from one tab or window and perform the AQI from another tab or window.

3.  Perform the AQI review.

    |Option|Instructions|
    |------|------------|
    |**The AQI review is not yet started.**|Click **Perform AQI** in the form header.|
    |**The AQI review was started and is pending.**|Click **Continue AQI** in the form header.|

4.  In the **Article Checklist Answers** related list, read the questions and evaluate which ones are true.

    Double-click the **Answer** cell for each question that is true, select **true**, and select the green check mark.

    **Note:** The associated **Weighted Score** is applied to the AQI score when the answer is set to **true.**

    ![AQI Checklist Summary..](../image/KnowledgeTrueFalse.png)

    **Note:**

    -   If you perform several AQI reviews for the same version, the latest AQI score appears in the **Latest AQI** field in the article.
    -   If you’re using Knowledge Management within the Customer Service Management application, you can automatically make knowledge public by running the Make KM Service Portal Pages Public fix script after you install the Customer Service Management plugin \(com.sn\_customerservice\).
    Standard Pagination - Displays the search results in multiple pages.

    Infinite Scroll - Displays the search results while scrolling.

5.  Perform one of the following actions.

<table id="choicetable_vhz_t4m_nbb"><thead><tr><th align="left" id="d361639e216">

To

</th><th align="left" id="d361639e219">

Do This

</th></tr></thead><tbody><tr><td id="d361639e225">

**Submit the completed AQI review.**

</td><td>

Click **Submit**. The form refreshes and the total score of the AQI review is displayed in the **AQI score** field.

 The system sends an email notification as follows:

-   If the AQI review was performed on the first version of the article, the system sends an email notification to the author of the article.
-   If the AQI review was performed on subsequent versions of the article, the system sends an email notification to the author and creator of the article versions.

**Note:** The notification includes the AQI review score and AQI review result. You can customize the content and design of the notification emails. In cases where the Ownership Group is enabled, the email notifications are sent to the Ownership Group as well.

</td></tr><tr><td id="d361639e259">

**Save the pending review to complete later.**

</td><td>

Click **Update** and return to the **Article Checklist Summaries** list. The checklist with pending reviews is added to the **My Pending AQI Checklists** queue. When you want to complete the AQI reviews, navigate to **Knowledge** &gt; **My Pending AQI Checklists** and complete the reviews.

</td></tr></tbody>
</table>
## What to do next

To view all the AQI reviews you completed, navigate to **Knowledge** &gt; **My Completed AQI Checklists**.

**Parent Topic:**[Use Article Quality Index](../concept/use-article-quality-index.md)

