---
title: Analyze sentiments in Now Assist for IT Service Management \(ITSM\)
description: Make informed decisions on incidents based on requester's sentiment and the reasoning behind it in the Now Assist for IT Service Management \(ITSM\) application.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2026-03-12"
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

<table id="choicetable_svt_mlg_w2c"><thead><tr><th align="left" id="d374656e88">

To

</th><th align="left" id="d374656e91">

Do this

</th></tr></thead><tbody><tr><td id="d374656e97">

**Navigate in Core UI**

</td><td>

1.  Go to **All** &gt; **Incident** &gt; **All**.

The incident list view appears.![Sentiment analysis Core UI list view](../image/now-assist-itsm-sentiment-trend-coreui-list.png)

You can analyze the Sentiment and Sentiment trend for the incident list.

2.  Select an incident.

The incident form view appears.

3.  In the **Sentiment** field, select the information icon \(![Information icon](../../../administer/on-call-scheduling/image/icon-information.png)\) to see the reasons for the sentiment.

![Sentiment analysis Core UI form view that displays the reasons for the sentiment](../image/now-assist-itsm-sentiment-trend-coreui-form.png)

**Note:** If the **Sentiment** field does not appear, you must configure the form layout. For more information, see Configuring the form layout and add the **Sentiment** field.

</td></tr><tr><td id="d374656e170">

**Navigate in Service Operations Workspace for ITSM**

</td><td>

1.  Go to **Workspaces** &gt; **Service Operations Workspace**.
2.  Select the list icon \(![List icon](../../../common/image/icon-list.png)\).
3.  Go to **Incidents** &gt; **Open**.

The Service Operations Workspace for ITSM list view appears.![Sentiment analysis incident list view](../image/now-assist-itsm-sentiment-trend-sow-list.png)

4.  Select an incident.

The Service Operations Workspace for ITSM form view appears.

5.  Select the information icon \(![Information icon](../../../administer/on-call-scheduling/image/icon-information.png)\) to see the reasons for the sentiment.

![Sentiment analysis incident form view that displays the reasons for the sentiment](../image/now-assist-itsm-sentiment-trend-sow-form.png)

**Note:** If the **Sentiment** field does not appear, you must configure the form layout. For more information, see Configuring the form layout and add the **Sentiment** field.

</td></tr></tbody>
</table>2.  In the Core UI or in Service Operations Workspace for ITSM list view, you can sort the incidents based on the sentiment and the sentiment trend.

3.  Manually refresh a sentiment.

    1.  In the Core UI or in Service Operations Workspace for ITSM, enter a comment in the Additional Comments field.
    2.  In the Service Operations Workspace for ITSM interface, a red dot appears on the information icon \(![Information icon](../../../administer/on-call-scheduling/image/icon-information.png)\) next to the sentiment.
    3.  Select the information icon \(![Information icon](../../../administer/on-call-scheduling/image/icon-information.png)\) and then select the refresh icon \(![Refresh icon](../../site-reliability-ops/image/icon-refresh.png)\) to see the updated sentiment and sentiment trend.

