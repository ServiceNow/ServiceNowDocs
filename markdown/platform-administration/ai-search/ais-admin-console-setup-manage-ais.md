---
title: Configure and manage AI Search in search applications
description: Configure and manage the AI Search settings for search applications that support the AI Search engine.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 10
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Using AI Search Admin console, AI Search Admin console, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure and manage AI Search in search applications

Configure and manage the AI Search settings for search applications that support the AI Search engine.

## Before you begin

Role required: ais\_admin

## About this task

You can modify existing search application configurations, or create and configure your own search application configurations with AI Search when you specify it as the search engine. By configuring the AI Search settings for a search application, you can customize the search experience for your specific needs. To set up the AI Search configuration, you do the following tasks from the search application configuration landing page:

1.  Assign a search profile.

    -   Create a search profile.
    -   Set the search sources as a priority to define the behavior of your search application.
    For more information, see [Search profiles in AI Search](../concept/defining-search-profiles-ais.md).

2.  Define the search app configuration.

    -   Configure the search profile to customize the user interface of your search application.
    For more information, see [Search application configurations](../concept/defining-search-app-cfgs-ais.md).

3.  Test and turn on AI Search.

    -   Display the options to test and verify AI Search in your search profile.
    -   Activate or deactivate AI Search based on its configuration status.
    For more information, see [AI Search Admin console Applications page](../reference/ais-admin-console-applications.md).


![Search application configuration landing page where you can configure the AI Search settings in the search application.](../image/ais-app-config1.png "Search application configuration landing page")

## Procedure

1.  Navigate to **All** &gt; **AI Search Admin** &gt; **AI Search Admin Home**.

2.  In Set up and Manage AI Search in your applications section, select a supported search application that you want to configure the AI Search settings for.

3.  In the application configuration landing page, assign a search profile.

<table id="choicetable_s2z_q1p_f2c"><thead><tr><th align="left" id="d362805e298">

Option

</th><th align="left" id="d362805e301">

Procedure

</th></tr></thead><tbody><tr><td id="d362805e307">

**Create a new search profile**

</td><td>

Select **Create new**.A new search profile is created automatically. You can rename it or use a different search profile. For more information about the search profile controls, see [AI Search Admin console Applications page](../reference/ais-admin-console-applications.md). For a description of the search profile field values, see [Search Profile form](../reference/search-profile-form-ais.md).

</td></tr><tr><td id="d362805e347">

**Link an existing search profile**

</td><td>

1.  Select **Select existing**.
2.  Select a profile from the list of existing search profiles.
3.  Select **Link to application name**.


</td></tr></tbody>
</table>    Each search profile contains the settings that determine how AI Search generates the search results for a search. The search profile settings include Search sources, Dictionaries, Result improvement rules, Genius results, and Review &amp; publish.

    ![AI Search Admin console search profile view.](../image/ai-search-profile.png)

    1.  Add Search sources to a search profile to make your searchable content available for your users.

        -   Create a search source:
            1.  On the **Search sources** tab, select **New**.
            2.  On the form, fill in the fields.

                For a description of the field values, see [Search Source form](../reference/search-source-form-ais.md).

            3.  Select **Submit**.
        -   Link an existing AI Search search source:
            1.  On the **Search sources** tab, select **Link**.
            2.  From the list of existing AI Search search sources, select one or more search sources.
            3.  Select **Link**.
        For more information, see [Search sources in AI Search](../concept/search-sources-ais.md).

    2.  Define the language-specific dictionaries of terms, such as equivalent terms \(synonyms\), common terms, and spell check.

        -   Create a AI Search term:
            1.  On the **Dictionaries** tab, select **New**.
            2.  On the form, fill in the fields.

                For a description of the field values, see [Dictionary and AI Search Dictionary forms](../reference/dictionary-form-ais.md).

            3.  Select **Submit**.
        -   Link an existing AI Search term:

            1.  On the **Dictionaries** tab, select **Link**.
            2.  From the list of existing AI Search dictionaries, select one or more dictionaries.
            3.  Select **Link**.
            For more information, see [Search profiles in AI Search](../concept/defining-search-profiles-ais.md).

    3.  Define the Result improvement rules to boost, block, or promote the search results for specific search queries.

        1.  On the **Result improvement rules** tab, select **New**.
        2.  On the form, fill in the fields.

            For a description of the field values, see [AI Search Results Improvement Rule form](../reference/result-improvement-rule-form-ais.md).

        3.  Select **Submit**.
        4.  From the Actions related list, create boost action, block, or promote documents to appear as search results.
        5.  Select **Update**.
        For more information, see [Result improvement rules](../concept/result-improvement-rules-ais.md).

    4.  Populate one or more Genius Result cards with concise, actionable answers that are derived from the relevant search results by linking AI Search Genius results configurations to your search profile.

        A search profile can include multiple Genius Result configuration links.

        1.  On the **Genius Results Configuration** tab, activate base system genius results for your search profile from the list of genius result configuration options.
        2.  Select **Save**.
        For more information, see [Genius Result configurations in the base system](../concept/default-genius-result-configs-ais.md).

    5.  Review and publish the search profile to make the profile's settings active in the linked search applications.

        1.  On the **Review &amp; publish** tab, review the summary of your search profile.
        2.  If all configurations look correct, select **Publish Profile**.
        3.  Select **Finish**.
    The search profile is published and assigned to the search application.

4.  Define the search application configuration.

<table id="choicetable_c42_rxp_f2c"><thead><tr><th align="left" id="d362805e758">

Option

</th><th align="left" id="d362805e761">

Procedure

</th></tr></thead><tbody><tr><td id="d362805e767">

**Create a new search application configuration**

</td><td>

Select **Create new**.A new search application configuration is created automatically. You can rename it or use a different configuration. For more information about the search application configuration controls, see [AI Search Admin console Applications page](../reference/ais-admin-console-applications.md). For a description of the search application configuration field values, see [Search Application Configuration form](../reference/search-app-config-form-ais.md).

</td></tr><tr><td id="d362805e807">

**Link an existing search application configuration**

</td><td>

1.  Select **Select existing**.
2.  Select an application from the list of existing search application configurations.
3.  Select **Link to application name**.


</td></tr></tbody>
</table>    Each search application configuration contains the settings that determine how search results are displayed to users of the application. The search application configuration settings include Auto-complete, Navigation tabs, Sort options, Facet filters, Result-card interface, and Review &amp; finish.

    ![AI Search Adminconsole search application configuration view.](../image/aisearch-app-config.png)

    1.  Display the intelligent suggestions in your search application's input field by adding auto-complete suggestions to the search application configuration.

        -   Create a suggestion:
            1.  On the **Auto-complete suggestions** tab, select **New**.
            2.  On the form, fill in the fields.

                For a description of the field values, see [Suggestion Reader Group form](../reference/sugg-reader-group-form-ais.md).

            3.  Select **Submit**.
        -   Link an existing suggestion to the search application:
            1.  On the **Auto-complete suggestions** tab, select **Link**.
            2.  From the list of existing suggestions, select one or more search application.
            3.  Select **Link**.
        For more information, see [Auto-complete suggestions in AI Search applications](../concept/auto-complete-ais.md#).

    2.  Edit the display settings for navigation tabs to help users navigate within the search application to access and manage information.

        1.  On the **Navigation tabs** tab, select the **Navigation tabs List Actions icon \(![](../image/list-actions-icon.png)\)** &gt; **Edit columns**.
        2.  On the form, fill in the fields.

            For a description of the field values, see [Source Facet Bucket form](../reference/navigation-tab-form-ais.md).

        **Note:** AI Search automatically defines the navigation tabs for search application configurations. You can't create or delete these navigation tabs.

    3.  Display the search results in a specific order by defining the Sort options for your AI Search application \(such as sorting the search results based on the date\).

        1.  On the **Sort Options** tab, select **New**.
        2.  On the form, fill in the fields.

            For a description of the field values, see [Sort Option form](../reference/sort-option-form-ais.md).

        3.  Select **Submit**.
    4.  Define the facets to filter your searches by using categories that are dynamically generated from the current search results \(such as filtering the search results based on the dates or keywords\).

        1.  On the Facet filters page, select **New**.
        2.  On the form, fill in the fields.

            For a description of the field values, see [Facet form](../reference/facet-form-ais.md).

        3.  Select **Submit**.
    5.  Select the result-card interface of your AI Search application to customize the appearance and layout of search results in AI Search applications.

        1.  On the Result-card interface page, select **Choose**.
        2.  Create or update the result-card interface for the AI Search application.

<table id="table_fhr_311_h2c"><thead><tr><th>

Option

</th><th>

Procedure

</th></tr></thead><tbody><tr><td>

Select from the existing result-card interfaces for your search application.

</td><td>

1.  Select **Use an existing result-card interface**.
2.  From the Result card interface list, select an option.


</td></tr><tr><td>

Add a new result-card interface for your search application

</td><td>

1.  Select **Create new interface**.
2.  In the **Configuration name** field, enter the name.


</td></tr></tbody>
</table>        3.  Select **Save**.

            For more information, see [Create or edit an EVAM view definition](ais-admin-console-evam-configurations.md).

    6.  Review the search application configurations of your AI Search application.

5.  Go back to the application configuration landing page and select **Test search profile** to verify that the search application works as intended.

6.  Activate AI Search in the search application by selecting **Go to turn on**.


## Result

The AI Search engine is ready to use AI Search in the search application.

**Parent Topic:**[Using AI Search Admin console](../concept/using-ais-admin-console.md)

**Related topics**  


[AI Search Admin console Applications page](../reference/ais-admin-console-applications.md)

