---
title: Enabling Now Assist Q&amp;A Genius Results
description: As a search administrator, you can use the Now Assist Q&amp;A Genius Results skill in AI Search portals and mobile applications by enabling Now Assist Q&amp;A Genius Results in search profiles. You can also use the skill in global search by enabling Now Assist Q&amp;A Genius Results in the AI Search for Next Experience application.Enable Now Assist Q&amp;A Genius Results in global search using the AI Search for Next Experience application.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI, Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Now Assist Q&amp;A Genius Results, Configuring Now Assist in AI Search, Now Assist in AI Search, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Enabling Now Assist Q&amp;A Genius Results

As a search administrator, you can use the Now Assist Q&amp;A Genius Results skill in AI Search portals and mobile applications by enabling Now Assist Q&amp;A Genius Results in search profiles. You can also use the skill in global search by enabling Now Assist Q&amp;A Genius Results in the AI Search for Next Experience application.

## Enable Now Assist Q&amp;A Genius Results in AI Search portals and mobile applications

For details on how to enable Now Assist Q&amp;A Genius Results and other Now Assist Genius Results in your AI Search portals and mobile applications, see [Enable Now Assist Genius Results in AI Search portals and mobile applications](../task/enable-now-assist-gr-ais-apps.md).

**Parent Topic:**[Now Assist Q&amp;A Genius Results](now-assist-qna-genius-results.md)

## Enable Now Assist Q&amp;A Genius Results in global search

Enable Now Assist Q&amp;A Genius Results in global search using the AI Search for Next Experience application.

### Before you begin

The [Next Experience UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-landing-page.md) must be activated on your instance. To learn about activating Next Experience UI, see [Considerations for activating Next Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-adoption-paths.md).

The AI Search for Next Experience application must be installed and enabled on your instance. For more information about the application, see [AI Search for Next Experience](ais-next-experience-app.md).

The Now Assist for Search application must be installed on your instance. For details on installing this application from the Now Assist Admin console, see [Install Now Assist in AI Search](../task/install-now-assist-ais.md).

Role required: ais\_admin

### About this task

As a search administrator, you can enable agentic AI model answer generation for Knowledge article results in global searches by adding the Now Assist Q&amp;A Genius Result configuration to the Next Experience Search Configuration search profile used by [AI Search for Next Experience](ais-next-experience-app.md).

**Note:** Linking the Now Assist Q&amp;A Genius Result configuration to the Next Experience Search Configuration search profile changes the status of the Now Assist Q&amp;A Genius Results skill to **Active** in the Now Assist Admin console. The skill remains active as long as any search profile includes a link to the Now Assist Q&amp;A Genius Result configuration.

When you enable Now Assist Q&amp;A Genius Results in global search, they're enabled for all users.

### Procedure

1.  In the Unified Navigation, select the application scope and update set icon ![](../image/unified-nav-scope-icon.png), and then set the application scope to **AI Search for Next Experience**.

2.  If you have version 1.x or 2.x of the AI Search for Next Experience application installed on a Tokyo or Utah instance, add the Genius Result data source to the AI Search For Next Search EVAM definition.

    If you have version 3.x or a later version of the AI Search for Next Experience installed, or are on Vancouver or a later release, go to the next step.

    1.  Navigate to **All** &gt; **Entity View Action Mapper \(EVAM\)** &gt; **EVAM Definitions**.

    2.  Open the AI Search For Next Search definition record by selecting it from the list.

    3.  In the EVAM Datasource M2Ms related list, select **Link Existing**.

    4.  On the EVAM Datasource M2M form, populate the **Datasource** field with a reference to the Genius Result Data Source record from the EVAM Datasources table by using the Lookup using list icon ![](../image/icon-lookup-using-list.png).

    5.  Select **Submit**.

        The Genius Result Data Source reference appears in the EVAM Datasource M2Ms related list.

3.  Add the Now Assist Q&amp;A Genius Result configuration to the search profile used by AI Search for Next Experience.

    1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles**.

    2.  Open the Next Experience Search Configuration search profile record by selecting it from the list.

    3.  In the Genius Results related list, select **Link Existing**.

    4.  On the Search Profile - Genius Result Mapping form, fill in the following field values.

<table id="table_hjh_qzj_k1c"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Genius Result Configuration

</td><td>

Enter or select **Now Assist Q&amp;A**.

</td></tr><tr><td>

Order

</td><td>

Specify the evaluation order for the Now Assist Q&amp;A Genius Result configuration in the search profile. AI Search evaluates active Genius Result configurations for a search profile in order, from lowest **Order** field value to highest. For more details on the evaluation order for Genius Results, see [Set the evaluation order for Genius Result configurations in a search profile](../task/set-gr-eval-order-srch-profile-ais.md).

</td></tr></tbody>
</table>    5.  Select **Submit**.

4.  Select the existing related list row for the Q&amp;A Genius Result configuration, and then select **Unlink Selected**.

    The Now Assist Q&amp;A Genius Result configuration supersedes the original Q&amp;A Genius Result configuration. You don't need both configurations in the same search profile.


### Result

The Now Assist Q&amp;A Genius Result configuration is enabled for global searches.

In the Now Assist Admin console, the status for the Now Assist Q&amp;A Genius Results skill is **Active**.

