---
title: Classify ServiceNow assets
description: Run the Classify assets with ServiceNow Vault agent to get a recommended data class for each ServiceNow column in the Data Catalog, review the recommendations, and apply them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/classify-servicenow-assets-now-assist-vault.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [classify assets, data classification, Data Catalog, agentic AI]
breadcrumb: [Classifying ServiceNow assets with Vault agents agentic workflow, Use agentic AI, ServiceNow Vault]
---

# Classify ServiceNow assets

Run the Classify assets with ServiceNow Vault agent to get a recommended data class for each ServiceNow column in the Data Catalog, review the recommendations, and apply them.

## Before you begin

The following applications must be installed:

-   ServiceNow Data Catalog Governance \(sn\_dcg\_app\)
-   ServiceNow Otto for Vault version 3.1 or later

Role required: dcg\_data\_privacy\_admin

## About this task

The agent provides AI recommendations for the user to review before applying them. Recommendations are saved only after the user confirms.

## Procedure

1.  Open the ServiceNow Otto panel.

    You can start the agent from the platform ServiceNow Otto panel or from the Workflow Data Fabric panel. The agent is offered as a selectable option in the Workflow Data Fabric panel only.

2.  Select **Classify assets with ServiceNow Vault**.

    In the platform ServiceNow Otto panel, the agent isn't offered as an option. Enter a prompt such as `Classify my ServiceNow assets` or `Recommend data classes for columns in the Data Catalog`. Both methods start the same agent.

3.  Select the category of assets to classify:

    -   **Unclassified assets** — classify only the assets that have no data class.
    -   **Classified assets** — generate new recommendations for the assets that already have a data class. Existing classifications aren't replaced.
    -   **All assets** — classify every asset available to you.
    The agent starts generating recommendations in the background.

    If the agent reports that no assets were found, verify that the metadata collector has run for the ServiceNow source. Verify that assets exist in the category you selected.

4.  In the conversation, select the **Data sensitivity classification** link.

    The results open in a panel beside the conversation.

5.  Select **Refresh** to update the progress tracker and the results.

    Results appear as recommendation pages are generated. The progress tracker reports one of the states in the following table.

    |State|Description|
    |-----|-----------|
    |In progress|Some pages are still being generated. Refresh to check for more results.|
    |Complete|All pages are generated. The recommendations are ready to review.|
    |Complete with some columns skipped|Recommendations couldn't be generated for some assets because of large language model processing errors. Review the available results and confirm to apply them. Only the generated recommendations are saved.|

6.  Review the recommendations.

    Each row shows the table, the column, the recommended data class, and the reason for the recommendation. Scroll the results horizontally to see all columns.

    To narrow the results, filter by data class, sort by a column, or search by table or column name.

7.  When the agent asks whether to apply the recommended classifications, confirm or decline.

    |Option|Description|
    |------|-----------|
    |**Confirm**|The agent saves the recommended classifications in the background. Confirm only after all recommendations are generated. If recommendations are still being generated, the agent asks you to wait and then asks again.|
    |**Decline**|The agent asks you to confirm the cancellation. Select **Yes, cancel** to cancel the run, or **No, go back** to return to the apply question.|

    **Warning:**

    If no recommendations could be generated, the agent tells you that there's nothing to save and ends the run when you confirm. When you decline, processing doesn't stop immediately because the agent first finishes the work already in progress. This might take a minute or two. None of the recommendations from this run are applied.


## Result

The agent saves the recommended classifications to the ServiceNow classification tables in the background. The classifications appear on the corresponding data assets in the Data Catalog after the next ServiceNow metadata collector run.

**Note:**

If a recommended data class is already recorded against a column, no duplicate entry is created. If the recommended data class differs from an existing one, the recommended class is added and the existing class is retained.

To check the applied classifications after the collector runs, see [View data asset details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/view-data-asset-details.md).

If the run completes with some columns skipped, check the system logs for the cause of the processing errors. Run the agent again for the skipped assets.

**Parent Topic:**[Classifying ServiceNow assets with Vault agents agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/now-assist-vault-classify-servicenow-assets.md)

**Related topics**  


[Explore data assets in Data catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/explore-data-assets-in-data-catalog.md)

[Run metadata collectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/run-metadata-collectors-dc.md)

[Assign roles to Data catalog users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/assign-roles-to-data-catalog-users.md)

