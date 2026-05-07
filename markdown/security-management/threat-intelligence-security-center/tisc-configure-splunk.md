---
title: Configure TISC add-on in Splunk
description: Configure the TISC add-on in Splunk to connect your account, define data inputs, and pull observable records into the KV store for search and analysis.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [configure, tisc add-on, splunk]
breadcrumb: [TISC add-on for Splunk overview, Configure Sighting Search, TISC Enrichment integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Configure TISC add-on in Splunk

Configure the TISC add-on in Splunk to connect your account, define data inputs, and pull observable records into the KV store for search and analysis.

## Before you begin

Role required: Splunk admin

## About this task

The TISC add-on connects your ServiceNow account to Splunk and pulls observable records into the KV store.

## Procedure

1.  Search for **Threat Intelligence Security Center for Splunk** app from the left navigation.

2.  Select **Set up** under the **Actions** column.

    The **Configuration** page is displayed, and you can set up your ServiceNow TISC account.

3.  Select **Add**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Add Accounts**|
    |Name|A unique name for the account.|
    |User Name|The ServiceNow account user name. You can use the same user name created during role creation \[`sn_sec_tisc.api_obs_read_access`\] in the preceding step.|
    |Password|The ServiceNow account password.|
    |Instance URL|The ServiceNow instance URL.|

5.  Select **Add**.

    The ServiceNow instance account is added to the Splunk.

6.  Navigate to the **Inputs** page to manage your data inputs for your ServiceNow account.

7.  Select **Create Input**.

    The **Add Input** dialogue box is displayed for you to add the inputs to your ServiceNow account. After the input set is defined, the application sends the information to the TISC instance to retrieve a specific number of observables that meet the criteria.

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

The ServiceNow account user name. You can use the same user name created with the role `sn_sec_tisc.api_obs_read_access` in the preceding step.

</td></tr><tr><td>

Interval

</td><td>

Set time interval in seconds to retrieve the data from TISC.

</td></tr><tr><td>

Expiry Period\(in days\)

</td><td>

Option to set the expiry period in days.**Note:** The sample expiration is set to 30 days. For example, when data is pulled on a specific date, a set of 10,000 records may be retrieved. These records are stored in the KV \(Key-Value\) store within Splunk. Starting from the ingested date, the records are retained for 30 days. On the 31st day, they are automatically deleted from the KV store.

</td></tr><tr><td>

Never Expire

</td><td>

Choose this option if you don't want to expire the records ingested.

</td></tr><tr><td>

Additional Attributes

</td><td>

Additional attributes from the list of recommended options to include in the KV store. Attributes must be separated by commas.A list of allowed attributes is provided in the table following the mandatory attributes table.

</td></tr><tr><td>

Filters

</td><td>

Conditions that determine which data is imported and filtered. To set the filter conditions, you can define the criteria based on the fields such as threat score, confidence level, and type.

For simple conditions, use this filtering option. For complex conditions, add JSON filters.

-   The allowed integer operators are:

"=", "!=", "&gt;", "&lt;", "&gt;=", "&lt;="

-   The allowed string operators are:

"=", "!=", "IN"

Example of a simple filter:

```
{Sample filter format: Allowed Tokens: "threat_score", "confidence", "reputation", "type", "value". Allowed Integer Operators: "=", "!=", ">", "<", ">=", "<=". Allowed String Operators: "=", "!=", "IN". Example: reputation IN ("clean","suspicious","malicious") AND threat_score > 90 AND confidence > 90 AND type = "ip_v4_address"}
```

</td></tr><tr><td>

JSON

</td><td>

JSON-based filters for defining more complex conditions.

</td></tr></tbody>
</table>    Sample advanced filter:

    ```
    {"boolean_operator":"AND","filters":[{"field_name":"reputation","operator":"IN","field_value":"clean,suspicious,malicious"},{"field_name":"threat_score","operator":">","field_value":"90"},{"field_name":"confidence","operator":">","field_value":"90"},{"field_name":"type","operator":"=","field_value":"ip_v4_address"}]}
    ```

    **Note:** Accounts are active by default, but inputs are inactive by default. Activate inputs to start importing data. For possible filters refer to Observable\_filters section in [Adds observable source records to the Threat Intelligence Security Center \(TISC\)](https://www.servicenow.com/docs/bundle/australia-api-reference/page/integrate/inbound-rest/concept/tisc-api.html#title_tisc-POST-observables) application.

9.  Select **Add** to save the inputs.

10. Select **Clone** to copy and create an account based on the existing account.

    Deactivate the input before copying to avoid creating duplicate entries when importing data using the same criteria.

11. Review the information retrieved and stored in the KV store within Splunk along with the records pulled from TISC.

    |Field|Description|
    |-----|-----------|
    |confidence|Indicates the confidence level associated with the accuracy of the threat score.|
    |\[kvlookup\_created\_time\]|Indicates the record creation time in the key value store.|
    |\[kvlookup\_days\_till\_expiry\]|Indicates the number of days before the record is deleted from the KV store.|
    |instance\_url|Indicates the ServiceNow instance URL.|
    |reputation|Indicates the reputation of the entity involved.|
    |source\_reported\_score|The reported source score from TISC.|
    |sys\_id|Sys ID of the record from TISC.|
    |threat\_level|Indicates the severity level of the threat.|
    |threat\_score|The score indicating the level of threat associated with a record.|
    |threat\_severity|Indicates the threat severity of the observable.|
    |type|Indicates the observables type.|
    |updated\_by|The user who last updated the record.|
    |kvlookup\_updated\_time|Indicates the timestamp when the record was last updated in the key value store.|
    |value|Value of the record. For example, IP address, hash, and similar values.|

    |Field|Description|
    |-----|-----------|
    |additional\_context|Any additional context for the observable.|
    |attack\_phases|Indicates attack phases in a kill chain such as LM, MITRE ATT&amp;CK.|
    |author|Name of the author.|
    |comments|Any additional comments for the observable.|
    |created|Indicates when the observable was created.|
    |description|Description of the observable.|
    |expiration\_time|Specifies the expiration time of the observable record.|
    |extensions|Indicates the extensions of an observable.|
    |first\_observed|The first time when the data was observed.|
    |first\_seen|The first time this record was seen performing malicious activities.|
    |historically\_significant|Indicates if the observable is considered historically significant. This TISC system flag is used to exclude the observable from archival.|
    |id|Unique identifier assigned to the observable by the TISC system.|
    |is\_defanged|Flag indicating whether the observable value has been defanged.|
    |is\_false\_positive|Boolean flag that indicates if an observable is identified as false positive.|
    |language|Indicates the language of the text content in this object.|
    |last\_observed|The last time when the data was observed.|
    |last\_seen|The time that this object was last seen performing malicious activities.|
    |notes|Any additional notes for the observable record.|
    |number|System-generated number assigned to the observable by TISC.|
    |security\_type|Specifies whether the observable belongs to the Allowlist or Denylist.|
    |no\_of\_sources|Represents the number of unique sources that have contributed to the observable.|
    |sources|Specifies the threat source from which this record is created.|
    |status|Status of the observable: active or inactive.|
    |tisc\_tags|The TISC tags associated with the observable.|
    |taxonomies|The taxonomy associated with the observable.|
    |tlp|Unique value that indicates the Data sensitivity setting per TLP.|
    |updated|Indicates when the observable record was last updated|
    |usage\_categories|Categories that the observable falls under, such as botnet or phishing.|
    |watch\_list|Flag specifying if the observable is included in the watch list.|

    These fields along with any others defined by your criteria will be available in Splunk and can be viewed, searched, and analyzed through the search tab.


**Parent Topic:**[TISC add-on for Splunk overview](../concept/tisc-addon-splunk.md)

