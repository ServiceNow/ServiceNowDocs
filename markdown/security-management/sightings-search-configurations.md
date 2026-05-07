---
title: Create sightings search configuration records
description: Create multiple sightings search configuration records and use them while querying multiple log stores or varying the search parameters.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Security Operations Integration- Sightings Search capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Create sightings search configuration records

Create multiple sightings search configuration records and use them while querying multiple log stores or varying the search parameters.

## Before you begin

Role required: sn\_si.admin

-   The CIM add-on must be installed on the Splunk instance.
-   Saved Searches and Inplace queries are supported for Splunk Integration only.

## About this task

You can also create sightings search configuration records to invoke [saved searches](https://docs.splunk.com/Splexicon:Savedsearch) on the Splunk enterprise log store.

**Note:** The search configuration queries rely on Splunk log data to be Splunk Common Information Model \(CIM\) compliant.

With saved search configurations, you can:

-   Create custom searches that combine multiple event records.
-   Design-efficient and effective searches.
-   Use parametrized inputs in the Splunk saved search.

The base system includes the sample configurations.

The saved search and Inplace configuration queries are example queries and can be substituted with appropriate parameters for your environment. Create additional saved search configurations as required. When you define a saved search configuration, the name and the parameters in the search query must match the saved configuration defined on your Splunk instance. If the name and parameters are not the same, you may not see accurate results when you perform a sightings search.

**Note:** On your Splunk instance, navigate to the Searches, Reports, and Alerts page and locate your saved search query. Select the **Permissions** link to navigate to the Permissions page. Select the **All Apps** radio button and enable the **Read Permission** option for **Everyone**. This will change the Sharing column value from Private to App for your saved search query. If this is not set, saved search query may not return any results.

To verify if the saved search configuration matches the configuration defined on your Splunk instance:

1.  Navigate to **Settings** &gt; **Searches, Reports, and Alerts**.
2.  Change **App Context** to **All**.

    A list of search reports is displayed.

3.  Confirm that the saved search query is present in the list.

For example, the Sightings Search Configuration form contains the email address and email sender as search parameters:

![Saved configuration](../image/cj-sir-si-saved-config.png "Sightings Search Configuration form")

In your Splunk instance, define the saved search with the same name, Default Saved Search - Emails, and the same search parameters for the email address and email subject. If the name and search parameters are not the same, sightings search does not generate accurate result.

## Procedure

1.  Navigate to **Security Operations** &gt; **Integrations** &gt; **Sightings Search Configuration** and create a new record \(see table for field descriptions\).

    |Field|Description|
    |-----|-----------|
    |Name|Name of the configuration.|
    |Is saved search|Saved search configuration is created if you select this option.|
    |Sightings search source|The source for the sightings search. Select the Splunk log store as the source.|
    |Active|Option for the saved search status. Only active search configurations can be used to perform a sightings search.|
    |Observable type|Observable type can be any observable type such as IP, hash value, URL, domain name, and so on.|
    |Maximum observables per search|Maximum number of observables to be returned from the search.|
    |Search|The default search string is`$(observable)`, but you can define your own search query by specifying parameters that are supported by the Splunk log store.|

2.  Select **Submit**.


## Result

You have created a sightings search configuration record.

## What to do next

After defining the search query, select **Generate Sightings Search Test Query**, and specify a list of observable values to generate a test query based on this saved search configuration.

-   **[Run a Sightings Search](../../security-operations-common/task/run-sightings-search.md)**  
Determine the prevalence of a threat over time or test remediation or eradication efforts. You can select individual or multiple observables and the date range for your search from a security incident. Results are included in the **Security Incident Observables** related list.
-   **[Security Operations Integration - Sightings Search Flow](../../security-operations-integrations/task/secops-integration-sightings-search-workflow.md)**  
**Security Operations Integration - Sightings Search** flow is a high-level flow independent of integrations. It uses the configured queries to search for a set of observables based on the configured integrations which support the capability. Use it to fulfill an integration such as Splunk or Elasticsearch.
-   **[View Sightings Search Results](../../security-operations-common/task/view-sightings-search-results.md)**  
You can review Sightings Search Results for internal and external malicious indicators.
-   **[View Sightings Search Details](../../security-operations-common/task/view-sightings-search-details.md)**  
Review the aggregate details of all sighting searches.
-   **[View Sightings Search Data](../../security-operations-common/task/view-sightings-search-data.md)**  
Review the aggregate data of all sighting searches.

**Parent Topic:**[Security Operations Integration- Sightings Search capability](../../security-operations-common/concept/sightings-search-capability.md)

