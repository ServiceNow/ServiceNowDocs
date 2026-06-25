---
title: Analyze sentiments in Now Assist for Customer Service Management \(CSM\)
description: Make informed decisions on cases and email interactions based on requester's sentiment and the reasoning behind it in the Now Assist for Customer Service Management \(CSM\) application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/now-assist-for-csm/analyze-sentiments-in-now-assist-for-csm.html
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Use generative AI, Now Assist for CSM, Customer Service Management]
---

# Analyze sentiments in Now Assist for Customer Service Management \(CSM\)

Make informed decisions on cases and email interactions based on requester's sentiment and the reasoning behind it in the Now Assist for Customer Service Management \(CSM\) application.

## Before you begin

Role required: sn\_customerservice\_agent and sn\_customerservice.consumer\_agent role

## Procedure

1.  Navigate to the case or case form in the Core UI or in CSM Configurable Workspace.

2.  <table id="table_emg_jm5_w2c"><thead><tr><th>

To

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

Navigate in Core UI

</td><td>

1.  Go to **All** &gt; **Cases**

The case list view appears.

\[Omitted image "sentiment-analysis-coreui-case-list-view.png"\] Alt text: Sentiment analysis Core UI list view

You can analyze the Sentiment and Sentiment trend for the case list.

2.  Select a case.

The case form view appears.

\[Omitted image "sentiment-analysis-coreui-form-view.png"\] Alt text: Sentiment analysis Core UI form view that displays the reasons for the sentiment

3.  In the Sentiment field, select the information icon \[Omitted image "circle-info-outline-24.svg"\] Alt text: icon for seeing information about sentiment when you select to see the reasons for the sentiment.


</td></tr><tr><td>

Navigate in CSM Configurable Workspace

</td><td>

1.  Go to **Workspaces** &gt; **CSM Configurable Workspace**
2.  Select the List icon \[Omitted image "List\_MenuIcon.png"\] Alt text: icon for seeing the list of cases.
3.  Go to **Cases** &gt; **Open**

The CSM Configurable Workspace list view appears.

\[Omitted image "sentiment-analysis-case-list-view-configurable-workspace.png"\] Alt text: Sentiment analysis case list view

4.  Select a case.

The CSM Configurable Workspace form view appears.

\[Omitted image "sentiment-analysis-form-view-configurable-workspace.png"\] Alt text: Sentiment analysis case form view that displays the reasons for the sentiment

5.  Select the information icon \[Omitted image "circle-info-outline-24.svg"\] Alt text: The information icon provides an explanation for why a particular sentiment has been assigned to see the reasons for the sentiment.


</td></tr></tbody>
</table>3.  Navigate to the interaction or interaction form in Core UI or in CSM Configurable Workspace.

4.  <table id="table_vrd_hh1_s3c"><thead><tr><th>

To

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

Navigate in Core UI

</td><td>

1.  Go to **All** &gt; **Interaction**

The interactions list view appears.

    -   Remove the default **My Interactions** filter to see all interactions
    -   Apply filter for **Email** interaction type to view interactions with sentiment analysis
\[Omitted image "core-ui-list-view-interaction.png"\] Alt text: Interactions list view filtered to Email type, displaying sentiment analysis columns including Sentiment and Sentiment Trend.

You can analyze the Sentiment and Sentiment trend for the interaction list.

**Important:** By default, sentiment and sentiment trend values aren't displayed in the list view, even when the skill is enabled. You must manually personalize the list view to add these columns. To add sentiment columns do the following:

    1.  Navigate to the desired list page, for example, case list.
    2.  Right-click the column header and select **List Layout**.
    3.  Search for Sentiment\[+\], expand it, and move Sentiment and Sentiment Trend to the Selected list.
    4.  Select **Save**.The sentiment columns now appear in the list view.
2.  Select an interaction.

The interaction form view appears.

\[Omitted image "core-ui-form-view-interaction.png"\] Alt text: Interaction form for an email record in New state, showing a Positive sentiment and Improving sentiment trend.

3.  In the Sentiment field, select the information icon \[Omitted image "circle-info-outline-24.svg"\] Alt text: icon for seeing more details about sentiment. to see the reasons for the sentiment.

**Important:** By default, sentiment and sentiment trend values aren't displayed in the form view, even when the skill is enabled. You must manually personalize the form view to add these columns. To add sentiment columns do the following:

    1.  Open an interaction record.
    2.  Select and hold the form header and select **Configure** &gt; **Form Layout**.

**Tip:** You must select and hold the list header and select **Configure** &gt; **Form Layout** &gt; **.**.

    3.  In the form layout editor, locate the Sentiment section.
    4.  Expand Sentiment\(sn\_ai\_sentiment\)+.
    5.  Select and drag the fields you want to display on the form:
        -   Sentiment \(current sentiment state\)
        -   Sentiment Score
        -   Sentiment Trend \(declining, improving, stable\)
        -   Sentiment Reasoning
    6.  Position the fields in your desired location on the form.
    7.  Save the form layout.


</td></tr><tr><td>

Navigate in CSM Configurable Workspace

</td><td>

1.  Go to **Workspaces** &gt; **CSM Configurable Workspace**
2.  Select the List icon \[Omitted image "List\_MenuIcon.png"\] Alt text: icon for seeing the list of interactions.
3.  Go to **Interactions** &gt; **My interactions**

The CSM Configurable Workspace list view for interactions appears.

\[Omitted image "csm-configurable-workspace-list-view-interaction.png"\] Alt text: CSM Configurable Workspace showing the interactions- My Interactions list view with a positive sentiment and improving sentiment trend,

4.  Select an interaction.

The CSM Configurable Workspace form view appears.

\[Omitted image "csm-configurable-workspace-form-view-interaction.png"\] Alt text: CSM Configurable Workspace form view for an interaction,showing a Closed Complete chat with a negative sentiment badge

5.  Select the information icon \[Omitted image "circle-info-outline-24.svg"\] Alt text: The information icon provides an explanation for why a particular sentiment has been assigned to see the reasons for the sentiment.

**Important:** By default, sentiment and sentiment trend values aren't displayed in the list view, even when the skill is enabled. You must manually personalize the list view to add these columns. To add sentiment columns do the following:

    1.  Select the list personalization icon.
    2.  Navigate to Sentiment.
    3.  Expand Sentiment\(sn\_ai\_sentiment\)+.
    4.  Select the fields to display:
        -   Sentiment \(current sentiment state\)
        -   Sentiment Score
        -   Sentiment Trend \(declining, improving, stable\)
        -   Sentiment Reasoning
    5.  Save the personalized view.


</td></tr></tbody>
</table>5.  In Core UI or CSM Configurable Workspace list view, you can sort the cases and interactions based on the sentiment scale \(Very Positive, Positive, Neutral, Negative, or Very Negative\) and the sentiment trend.

6.  Manually refresh a sentiment.

    1.  In the Core UI or in CSM Configurable Workspace, enter a comment in the Additional Comments field.

    2.  In the CSM Configurable Workspace interface, a red dot appears on the information icon\[Omitted image "circle-info-outline-24.svg"\] Alt text: The information icon provides an explanation for why a particular sentiment has been assigned next to the sentiment.

    3.  Select the information icon \[Omitted image "circle-info-outline-24.svg"\] Alt text: The information icon provides an explanation for why a particular sentiment has been assigned and then select the refresh icon \[Omitted image "refresh-sync-new.png"\] Alt text: Refreshes content to see the updated sentiment scale \(Very Positive, Positive, Neutral, Negative, or Very Negative\)and sentiment trend.


**Parent Topic:**[Using Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/now-assist-csm-using.md)

**Related topics**  


[Enable and configure the Sentiment Analysis](https://support.servicenow.com/kb?sys_kb_id=ec531aab47a48794b6d8aa25126d4322&id=kb_article_view)

[Sentiment analysis for email interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/sentiment-analysis-interaction.md)

