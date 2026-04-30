---
title: Configure TISC add-on in Splunk
description: Follow this below procedure to configure the application.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 6
keywords: [configure, tisc add-on, splunk]
breadcrumb: [TISC add-on for Splunk overview, Configure Sighting Search, Sighting Search, TISC Enrichment integrations, TISC Integrations, Integrate Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# Configure TISC add-on in Splunk

Follow this below procedure to configure the application.

## Before you begin

Role required: Splunk admin

## About this task

The below procedure describes the configuration of TISC add-on in Splunk.

## Procedure

1.  Search for **Threat Intelligence Security Center for Splunk** app from the left navigation.

2.  Click on **Set up** under the **Actions** column.

    The **Configuration** page is displayed, and you can set up your ServiceNow TISC account.

3.  Select **Add**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Add Accounts**|
    |Name|A unique name for the account.|
    |User Name|Provide your ServiceNow account user name. You can use the same user name that is used for the users which is created during the role creation `sn_sec_tisc.api_obs_read_access` in the above step.|
    |Password|Provide ServiceNow account password.|
    |Instance URL|Provide the ServiceNow instance URL address.|

5.  Click **Add**.

    The ServiceNow instance account is added to the Splunk.

6.  Navigate to the **Inputs** page to create collections manage your data inputs for your ServiceNow account.

7.  Click **Create New Input**.

    The **Add Input** dialogue box is displayed for you to add the inputs to your ServiceNow account.

    Once the input set is defined, the application sends the information to the TISC instance to retrieve a specific number of observables that meet the criteria.

8.  Fill in the input details, as appropriate.

<table id="table_mhq_hcg_12c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique name for your input. For example, malicious IP list.

</td></tr><tr><td>

Account

</td><td>

Provide your ServiceNow account user name. You can use the same user name that is used for the users that is created with the role `sn_sec_tisc.api_obs_read_access` in the above step.

</td></tr><tr><td>

Interval

</td><td>

Set time interval in seconds to retrieve the data from TISC.

</td></tr><tr><td>

Expiry Period\(in days\)

</td><td>

Option to set the expiry period in days.**Note:** The sample expiration is set to 30 days. For example, when data is pulled on a specific date, a set of 10,000 records may be retrieved. These records will be stored in the KV \(Key-Value\) store within Splunk. Starting from the ingested date, the records will be retained for 30 days. On the 31st day, they will be automatically deleted from the KV store.

</td></tr><tr><td>

Never Expire

</td><td>

Choose this option if you don’t wish to expire the records ingested.

</td></tr><tr><td>

Additional Attributes

</td><td>

Allows you to add additional attributes from the list of recommended options to include in the KV store. Attributes must be separated by commas.A list of allowed attributes is provided in the table following the mandatory attributes table.

</td></tr><tr><td>

Filters

</td><td>

Define the conditions based on which data should be imported will be filtered.To set the filter conditions, you can define the criteria based on the fields such as threat score, confidence level, and type.

For simple filter conditions, you can use this filtering option. However, if the filter conditions are more complex and for any advanced filtering then you can choose to add JSON filters.

-   The allowed integer operators are:

"=", "!=", "&gt;", "&lt;", "&gt;=", "&lt;="

-   The allowed string operators are:

"=", "!=", "IN"

**Below is an example of a simple filter**:

```
{Sample filter format: Allowed Tokens: "threat_score", "confidence", "reputation", "type", "value". Allowed Integer Operators: "=", "!=", ">", "<", ">=", "<=". Allowed String Operators: "=", "!=", "IN". Example: reputation IN ("clean","suspicious","malicious") AND threat_score > 90 AND confidence > 90 AND type = "ip_v4_address"}
```

</td></tr><tr><td>

JSON

</td><td>

JSON based filters allows you to define more intricate conditions.

</td></tr></tbody>
</table>    **Sample advanced filter**:

    ```
    {"boolean_operator":"AND","filters":[{"field_name":"reputation","operator":"IN","field_value":"clean,suspicious,malicious"},{"field_name":"threat_score","operator":">","field_value":"90"},{"field_name":"confidence","operator":">","field_value":"90"},{"field_name":"type","operator":"=","field_value":"ip_v4_address"}]}
    ```

    **Note:** Accounts are active by default, but inputs are inactive by default, you must activate them to start importing the data. For possible filters refer to Observable\_filters section in [Adds observable source records to the Threat Intelligence Security Center \(TISC\)](https://www.servicenow.com/docs/bundle/yokohama-api-reference/page/integrate/inbound-rest/concept/tisc-api.html#title_tisc-POST-observables) application.

9.  Click **Add** to add the inputs.

10. Click **Clone** or copy to copy and create a new account based on the existing account.

    Make sure that the input is deactivated before cloning to avoid creating duplicate entries when importing data using the same criteria.

11. Once the data is pulled in, the following information will be retrieved and stored in the KV store within Splunk along with the records pulled from TISC:

    |Field|Description|
    |-----|-----------|
    |confidence|Indicates the confidence level associated with the accuracy of the threat score.|
    |kvlookup\_created\_time|Indicates the record creation time in the key value store.|
    |kvlookup\_days\_till\_expiry|Indicates the number of days after which the record will be deleted from the KV store.|
    |instance\_url|Indicates the ServiceNow instance URL address.|
    |reputation|Indicates the reputation of the entity involved.|
    |source\_reported\_score|The reported source score from TISC.|
    |sys\_id|Sys ID of the record which is coming through TISC.|
    |threat\_level|Indicates the severity level of the threat.|
    |threat\_score|The score indicating the level of threat associated with a record.|
    |threat\_severity|Indicates the threat severity of the observable.|
    |type|Indicates the observables type.|
    |updated\_by|Provides the information on who has last updated the record.|
    |kvlookup\_updated\_time|Indicates the time stamp when the record was last updated in the key value store.|
    |value|Value of the record. For example, IP, hash and so on.|

    |Field|Description|
    |-----|-----------|
    |additional\_context|Provide any additional context, as needed.|
    |attack\_phases|Indicates attack phases in a kill chain such as LM, MITRE ATT&amp;CK.|
    |author|Provide the author name.|
    |comments|Add any additional comments as needed.|
    |created|Indicates when the observable was created.|
    |description|Provide the description.|
    |expiration\_time|Specifies the expiration time of the observable record.|
    |extensions|Indicates the extensions of an observable.|
    |first\_observed|The first time when the data was observed.|
    |first\_seen|The first time that this record was first seen performing malicious activities.|
    |historically\_significant|Indicates if the observable is considered historically significant. This TISC system flag is used to exclude the observable from archival.|
    |id|Unique identifier assigned to the observable by the TISC system.|
    |is\_defanged|Flag indicating whether the observable value has been defanged.|
    |is\_false\_positive|A boolean flag that indicates if observable is identified as false positive.|
    |language|Indicates the language of the text content in this object.|
    |last\_observed|The last time when the data was observed.|
    |last\_seen|The time that this object was last seen performing malicious activities.|
    |notes|Add any additional notes for an observable record.|
    |number|System-generated number assigned to the observable by TISC.|
    |security\_type|Specifies whether the observable belongs to the Allowlist or Denylist.|
    |no\_of\_sources|Represents the number of unique sources that have contributed to the observable.|
    |sources|Specifies the threat source from which this record is created.|
    |status|Enter the status of the observable if active or inactive.|
    |tisc\_tags|Select the TISC tags that are associated with an observable.|
    |taxonomies|Select the Taxonomy that is associated with an observable.|
    |tlp|Unique value that indicates the Data sensitivity setting per TLP.|
    |updated|Indicates when the observable record was last updated|
    |usage\_categories|Categories that the observable falls under, such as botnet or phishing.|
    |watch\_list|Flag specifying if the observable is included in the watch list.|

    These fields along with any others defined by your criteria will be available in Splunk and can be viewed, searched, and analyzed through the search tab.


-   **[Data storage in Splunk](../concept/tisc-storage-splunk.md)**  
This section outlines how TISC utilizes lookups during the integration within Splunk's Key-Value store for data storage. It details how these lookups are configured and retrieved within Splunk.

**Parent Topic:**[TISC add-on for Splunk overview](../concept/tisc-addon-splunk.md)

