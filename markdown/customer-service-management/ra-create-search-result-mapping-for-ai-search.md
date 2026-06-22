---
title: Map AI search results with guidance inputs in Recommended Actions
description: Create mappings between AI search results and guidance inputs to recommend relevant actions to agents using AI search or enable agents to use AI search to search for the relevant resources.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/ra-create-search-result-mapping-for-ai-search.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring AI search, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Map AI search results with guidance inputs in Recommended Actions

Create mappings between AI search results and guidance inputs to recommend relevant actions to agents using AI search or enable agents to use AI search to search for the relevant resources.

## Before you begin

Role required: sn\_nb\_action.next\_best\_action\_author, admin

## Procedure

1.  Navigate to **All** &gt; **Recommended Actions** &gt; **Contexts**.

2.  Select a context for the AI search.

    If a message appears about the application scope, select **here** to be able to edit the record.

3.  In the **Search Application Configuration** field, select the Lookup using list icon \[Omitted image "lookup-list.jpg"\] Alt text: Lookup using list icon and select either the base system CSM Configurable Workspace Search Config or a custom configuration that specifies AI search as the search engine and contains your desired search settings.

    You can configure the search result display and refinement settings in the search application configuration. For more information, see [Search application configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/defining-search-app-cfgs-ais.md).

    The **\[CSM AIS\] Configurable Workspace Search Config** search application configuration is provided with the CSM Configurable Workspace store application. To access this configuration, navigate to **AI Search** &gt; **Search Experience** &gt; **Search Applications**.

4.  In the Search result mapping related list, select **New**.

5.  In the **Action type** field, select Guidance as an action type.

6.  In the **Action** field, select an action to associate with the guidance.

    The available actions are determined by the selection in the **Action type** field.

    1.  In the **Action** field, select the Lookup using list icon \(\[Omitted image "lookup-list.jpg"\] Alt text: Lookup using list icon\).

        In the resulting pop-up window, the **Table name** field is auto-populated with the table that stores the available actions for the selected action type.

    2.  In the **Document** field, select the Lookup documents using list icon \(\[Omitted image "lookup-list.jpg"\] Alt text: Lookup documents using list icon\) and then select the action.

    3.  Select **OK**.

    4.  Save the record.

        Saving the record displays the required action inputs.

7.  Configure the AI search result type.

<table id="choicetable_dwg_dbj_zyb"><thead><tr><th align="left" id="d40816e224">

Option

</th><th align="left" id="d40816e227">

Steps

</th></tr></thead><tbody><tr><td id="d40816e233">

**Map genius result: No**

</td><td>

1.  In the **Map genius result** field, select **No** to enable AI search result mapping to guidance inputs.
2.  In the **Search source table** field, select a source table to map the required fields to guidance inputs.

This field shows all the source tables mapped to the search profile of your search application configuration.

</td></tr><tr><td id="d40816e262">

**Map genius result: Yes**

</td><td>

1.  In the **Map genius result** field, select **Yes** to enable genius result mapping to guidance inputs.
2.  In the **Genius result configuration** field, select a genius result configuration to map the return fields to guidance inputs.

This field shows return fields of the genius result configuration that is linked to the search profile of your search application configuration. For more information, see [AI Search Genius Result Configuration form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/genius-result-cfg-form-ais.md).

</td></tr></tbody>
</table>8.  Save the record.

    The AI search parameters display in the pill picker.

9.  Map the action inputs.

    Action types and actions need inputs. These parameters enable agents to complete an action. You can choose static values for action inputs or you can use the pill picker to supply dynamic values.

<table id="choicetable_o2j_nbj_zyb"><thead><tr><th align="left" id="d40816e316">

Option

</th><th align="left" id="d40816e319">

Steps

</th></tr></thead><tbody><tr><td id="d40816e325">

**Use a static value**

</td><td>

Enter a value in the input field or use the lookup icon to select a value from the list.

</td></tr><tr><td id="d40816e334">

**Use a pill picker**

</td><td>

1.  Select the pill picker next to the field. The following are available in the pill picker:
    -   Context
    -   The outputs from the search source table or genius result configuration
    -   Search query term, search result preview, search result sysId, search result table, search result teaser, search result title, and search result url

Search query term: When an agent searches in the AI Search tab of the Recommended Actions side panel and selects a matching search result, the system automatically captures the search query term and passes it to the configured guidance as a dynamic input. This provides the ability for agents to include the search query term as a guidance input.

2.  Select the output from the pill picker.


</td></tr></tbody>
</table>10. Select **Update**.


