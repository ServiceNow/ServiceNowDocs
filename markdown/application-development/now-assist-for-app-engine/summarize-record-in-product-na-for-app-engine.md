---
title: Summarize a record in-product using Now Assist for App Engine
description: Quickly understand the contents of a record in a custom application within Core UI or a custom workspace.
locale: en-US
release: zurich
product: Now Assist for App Engine
classification: now-assist-for-app-engine
topic_type: task
last_updated: "2025-10-08"
reading_time_minutes: 2
keywords: [summarize a record in a custom table, summarize a table in a custom app, generate summary for table]
breadcrumb: [Use, Now Assist for App Engine, AI in custom applications, Developing your application, Building applications]
---

# Summarize a record in-product using Now Assist for App Engine

Quickly understand the contents of a record in a custom application within Core UI or a custom workspace.

## Before you begin

Role required: admin

Verify that the custom app record summarization skill is activated and configured. For more information, see [Activate the custom app record summarization skill](activate-custom-app-record-summarization-na-for-app-engine.md).

The following procedure describes how to summarize a record from a custom application in-product in both Core UI and in a custom workspace. To learn how to add a record summarization card to your custom workspace, see the following resources:

-   [Customize UI Builder pages using components](../../../administer/ui-builder/concept/work-components.md)
-   [Components documentation for the AI summary card](https://horizon.servicenow.com/workspace/components/now-ai-summary-card?release=zurich)
-   [UI Builder setup documentation for the AI summary card](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/now-ai-summary-card/uib-setup)

.

You can also summarize the contents of a record through chat in the Now Assist panel. For more information, see [Summarize a record through chat using Now Assist for App Engine](summarize-record-through-chat-na-for-app-engine.md).

## Procedure

1.  In Core UI or a custom workspace, open the record that you want to summarize.

2.  Select **Summarize**.

    **Note:** Generating and displaying the summary may take several seconds.

3.  When you're finished summarizing a record, you can copy the summary, expand or collapse the summary, or provide feedback about the summary.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d38064e158">

Option

</th><th align="left" id="d38064e161">

Procedure

</th></tr></thead><tbody><tr><td id="d38064e167">

**Expand or collapse the summary**

</td><td>

Select the expand card icon \(![expand card icon.](../../../product/now-assist-itsm/image/icon-expand.png)\) to view the complete summary or the collapse card icon \(![collapse card icon.](../../../product/now-assist-itsm/image/icon-collapse.png)\) to view a collapsed summary.

</td></tr><tr><td id="d38064e188">

**Provide feedback about the summary**

</td><td>

If you think that the summary was helpful, select the helpful icon \(![Helpful icon.](../../../product/now-assist-itsm/image/icon-helpful.png)\). If you think that the summary wasn’t helpful, select the not helpful icon \(![Not helpful icon.](../../../product/now-assist-itsm/image/icon-not-helpful.png)\).**Note:** This feedback improves the generative AI model and can help to improve future versions of this skill.

</td></tr><tr><td id="d38064e211">

**Copy the record summary**

</td><td>

If you want to reuse the summary, select the copy to clipboard icon \(![Copy to clipboard icon.](../../../product/now-assist-itsm/image/icon-copy.png)\).

</td></tr></tbody>
</table>
**Parent Topic:**[Using Now Assist for App Engine](../../app-engine-studio/concept/use-now-assist-for-app-engine-enterprise.md)

