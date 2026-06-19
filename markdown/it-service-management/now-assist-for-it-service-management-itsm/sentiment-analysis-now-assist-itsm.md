---
title: Analyze sentiments in Now Assist for IT Service Management \(ITSM\)
description: Make informed decisions on incidents based on requester's sentiment and the reasoning behind it in the Now Assist for IT Service Management \(ITSM\) application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/now-assist-for-it-service-management-itsm/sentiment-analysis-now-assist-itsm.html
release: zurich
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [Use generative AI skills, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Analyze sentiments in Now Assist for IT Service Management \(ITSM\)

Make informed decisions on incidents based on requester's sentiment and the reasoning behind it in the Now Assist for IT Service Management \(ITSM\) application.

## Before you begin

Role required: itil

## Procedure

1.  Navigate to the incident list or incident form in the Core UI or in Service Operations Workspace for ITSM.

<table id="choicetable_svt_mlg_w2c"><thead><tr><th align="left" id="d361563e88">

To

</th><th align="left" id="d361563e91">

Do this

</th></tr></thead><tbody><tr><td id="d361563e97">

**Navigate in Core UI**

</td><td>

1.  Go to **All** &gt; **Incident** &gt; **All**.

The incident list view appears.\[Omitted image "now-assist-itsm-sentiment-trend-coreui-list.png"\] Alt text: Sentiment analysis Core UI list view

You can analyze the Sentiment and Sentiment trend for the incident list.

2.  Select an incident.

The incident form view appears.

3.  In the **Sentiment** field, select the information icon \(\[Omitted image "icon-information.png"\] Alt text: Information icon\) to see the reasons for the sentiment.

\[Omitted image "now-assist-itsm-sentiment-trend-coreui-form.png"\] Alt text: Sentiment analysis Core UI form view that displays the reasons for the sentiment

**Note:** If the **Sentiment** field does not appear, you must configure the form layout. For more information, see  and add the **Sentiment** field.

</td></tr><tr><td id="d361563e169">

**Navigate in Service Operations Workspace for ITSM**

</td><td>

1.  Go to **Workspaces** &gt; **Service Operations Workspace**.
2.  Select the list icon \(\[Omitted image "icon-list.png"\] Alt text: List icon\).
3.  Go to **Incidents** &gt; **Open**.

The Service Operations Workspace for ITSM list view appears.\[Omitted image "now-assist-itsm-sentiment-trend-sow-list.png"\] Alt text: Sentiment analysis incident list view

4.  Select an incident.

The Service Operations Workspace for ITSM form view appears.

5.  Select the information icon \(\[Omitted image "icon-information.png"\] Alt text: Information icon\) to see the reasons for the sentiment.

\[Omitted image "now-assist-itsm-sentiment-trend-sow-form.png"\] Alt text: Sentiment analysis incident form view that displays the reasons for the sentiment

**Note:** If the **Sentiment** field does not appear, you must configure the form layout. For more information, see  and add the **Sentiment** field.

</td></tr></tbody>
</table>2.  In the Core UI or in Service Operations Workspace for ITSM list view, you can sort the incidents based on the sentiment and the sentiment trend.

3.  Manually refresh a sentiment.

    1.  In the Core UI or in Service Operations Workspace for ITSM, enter a comment in the Additional Comments field.
    2.  In the Service Operations Workspace for ITSM interface, a red dot appears on the information icon \(\[Omitted image "icon-information.png"\] Alt text: Information icon\) next to the sentiment.
    3.  Select the information icon \(\[Omitted image "icon-information.png"\] Alt text: Information icon\) and then select the refresh icon \(\[Omitted image "icon-refresh.png"\] Alt text: Refresh icon\) to see the updated sentiment and sentiment trend.

