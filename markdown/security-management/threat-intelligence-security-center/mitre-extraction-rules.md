---
title: MITRE ATT&amp;CK Technique Extraction Rules
description: The system automatically extracts MITRE techniques from observables, objects, and RSS feeds ingested across various data sources. In addition, as part of the enrichment process, MITRE techniques are also extracted from threat lookup results, observable enrichment results associated with observables.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-02"
reading_time_minutes: 6
breadcrumb: [About Rules Engine in TISC, Administer, Threat Intelligence Security Center, Security Operations]
---

# MITRE ATT&amp;CK Technique Extraction Rules

The system automatically extracts MITRE techniques from observables, objects, and RSS feeds ingested across various data sources. In addition, as part of the enrichment process, MITRE techniques are also extracted from threat lookup results, observable enrichment results associated with observables.

## Before you begin

Role required: sn\_sec\_tisc.admin

**Note:** Ensure that the MITRE ATT&amp;CK repository data available in the instance you are using. If the repository data is unavailable then the application cannot perform the extraction.

MITRE ATT&amp;CK repository data can be fetched by running the relevant MITRE collections.

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence Security Center** &gt; **Administration**.

2.  Go to **Rules Engine** &gt; **MITRE ATT&amp;CK Technique Extraction Rules**.

    The MITRE ATT&amp;CK Technique Extraction Rules page displays.

    **Important:** Before enabling MITRE ATT&amp;CK Technique Extraction rules, an alert message displays prompting you to ensure that the MITRE ATT&amp;CK data is available in your instance. If the required dataset is not present, then the rule execution may not produce the expected results.

3.  Select **New**.

<table id="choicetable_vcd_cj4_zbc"><thead><tr><th align="left" id="d474074e164">

Field

</th><th align="left" id="d474074e167">

Description

</th></tr></thead><tbody><tr><td id="d474074e173">

**Name**

</td><td>

Enter a name for the MITRE ATT&amp;CK Technique Extraction rule.

</td></tr><tr><td id="d474074e182">

**Description**

</td><td>

Enter a description for the MITRE ATT&amp;CK Technique Extraction rule.

</td></tr><tr><td id="d474074e191">

**Integration Type**

</td><td>

Indicates the MITRE ATT&amp;CK Technique Extraction rule for Data Sources or Threat Lookup Results or Observable enrichment results.

 The following options are available under Data Sources:

 -   **Data Sources - All**: This means that the rule is applicable for all the type of data sources such as Threat Intel Feeds, Import Intelligence records, API Sources \(for example, observables created from API\), Sent from SIR \(observables that are sent from SIR\) and various entities that are manually created by the users in the Threat Intelligence library.
-   **Data Sources- Threat Intel Feeds**: This corresponds to the extraction rules that are only applicable for threat intelligence feeds.

**Note:** For the threat intelligence data sources, the extraction rules are only supported for STIX, MISP, and Custom Feed types.

-   **Data Sources- API Sources**: This corresponds to the extraction rules that are only applicable for observables created from API sources.
-   **RSS Feeds Only**: This corresponds to extract MITRE Techniques from any RSS feed data source.
-   **Threat Lookup integrations**: This corresponds to the extraction rule is applicable to all threat lookup integrations such as Virustotal.

**Note:** Optionally, you can provide specific vendor which indicates the extraction rule will only be applied for threat lookup results which corresponds to that specific vendor.

-   **Observable Enrichment integrations**: When you select this option, the extraction rule is applied across available observable enrichment integrations.

**Note:** Optionally, you can provide specific vendor which indicates the extraction rule will only be applied for observable enrichment integrations which corresponds to that specific vendor.

-   

</td></tr><tr><td id="d474074e329">

**Threat Feed Type**

</td><td>

Following are the available options for Threat Feed Type:-   **STIX\(TAXII/HTTPS\)**: Filters threat feeds of the STIX TAXII or HTTPS type.
-   **MISP**: Filters threat feeds of the MISP type.
-   **Custom feed**: Filters threat feeds configured as Custom feeds.
**Note:** This field appears when you select the **Integration Type**: **Data Sources- Threat Intel Feeds**.

</td></tr><tr><td id="d474074e384">

**Feeds**

</td><td>

Select one or more enabled data sources for the selected feed type.

**Note:** This field appears when you select the **Integration Type**: **Data Sources- Threat Intel Feeds/RSS Feeds**.

</td></tr><tr><td id="d474074e410">

**Method to extract MITRE ATT&amp;CK tactics and techniques**

</td><td>

Select the method used to extract MITRE ATT&amp;CK tactics and techniques.The following methods are available:

-   Use Regex \(default\)
-   Use Script
MITRE ATT&amp;CK tactic and technique extraction is supported for the following entities:

-   Observable source
-   Object source
-   Indicator source
-   Threat lookup results
-   RSS feeds
-   Observable enrichment results


</td></tr><tr><td id="d474074e476">

**Extraction Method - Use Regex**

</td><td>

This method uses a regular expression that allows the threat analysts to define a pattern with a sequence of characters to perform extraction method.

</td></tr><tr><td id="d474074e485">

**Tactic Regex**

</td><td>

Option to provide regular expression for the extraction of MITRE ATT&amp;CK tactic ID\(s\).

</td></tr><tr><td id="d474074e494">

**Technique Regex**

</td><td>

Option to provide regular expression for the extraction of MITRE ATT&amp;CK technique ID\(s\).

</td></tr><tr><td id="d474074e503">

**Extraction Method - Use script**

</td><td>

This method uses a script format to perform the extraction. The following are the supported entities:

-   Observable source
-   Object source
-   Indicator source
-   Threat lookup results
-   RSS feeds
-   Observable enrichment results
**Note:**

-   This script method can be used to extract MITRE tactics and techniques from entity source record and link the tactics and techniques to the entity source record itself.
-   This script method can be used to extract MITRE tactics and techniques from threat lookup results and observable enrichment results, and link the tactics and techniques to the entity record.
-   This method can also be used to extract MITRE tactics and techniques from RSS feed records, and link the tactics and techniques to the entity record.
The sample script is shown below for your reference:

```
(function process(lookupResultRawData, RssFeed Data,recordGr, ruleGr, lookupResultGr) {
/*********************************
 
* - threatLookupResult: The raw data of the threat lookup result  in stringified JSON format.
* - recordGr: The GlideRecord of the observable record.
* - ruleGr: GlideRecord of matched MITRE extraction rule
*
* Once you extracted MITRE tactic IDs and technique IDs,
* then you can use this method to link the tactics and techniques to the observable record.
  **********************************/  
var utils = new MITREExtractionUtils();
var parsedRawData =JSON.parse(lookupResultRawData);
var mitreDataField = parsedRawData.mitre_data; 
var response = utils.extractMITREDataUsingRegex(mitreDataField,'TA[0-9][0-9][0-9][0-9]','T[0-9][0-9][0-9][0-9].[0-9][0-9][0-9]|T[0-9][0-9][0-9][0-9]');
utils.addTacticTechniquesForLookup(response.tacticIds, response.techniqueIds, recordGr, ruleGr.getUniqueValue(), lookupResultGr);
 
})(lookupResultRawData, recordGr, ruleGr, lookupResultGr);
 
Here is a sample script example for the extraction rule for threat lookup integrations where the script logic is parsing the threat lookup raw payload and performing the extraction only on a specific field inside the raw payload and associates the extracted tactics/techniques to the observable record.
```

</td></tr></tbody>
</table>4.  Select **Enable** to enable the MITRE ATT&amp;CK Technique Extraction rule after you create a new rule.

    **Note:** If you don't enable the MITRE ATT&amp;CK Technique Extraction rule then the rule will not be applied to the record.

    -   Data sources: Whenever you enable the extraction rule, the combination of data sources and integration type should not be matching any of the existing enabled extraction rules, and if so then the application will display an error message for you to modify the existing combinations and re enable the rule.
    -   Threat Lookup/Observable enrichment results: Whenever you enable the extraction rule, the vendor name should not be matching any of the existing enabled extraction rules, and if so then the application will display an error message for you to modify the vendor name and re enable the rule.
    -   A sample MITRE ATT&amp;CK Technique Extraction rules are provisioned for the users in the base system and these rules will be in disabled state by default and you must enable and activate the rule.
    -   MITRE ATT&amp;CK Technique Extraction rules are executed automatically when an RSS feed record is inserted or updated. The rule is evaluated for every insert or update operation on the RSS feed records. The extraction rule is executed only during the insertion of observable/object source.
    |Name|Description|Status|Integration Type|Method to extract MITRE ATT&amp;CK tactics and techniques|
    |----|-----------|------|----------------|---------------------------------------------------------|
    |Generic Rule for data sources ingestion|This is a generic rule for ingestion from all types of data sources including Import Intelligence and manual creation.|Disabled|Data Sources - All|Use regex|
    |Generic Rule for Observable Enrichment Integrations|This is a generic rule for any Observable enrichment integrations.|Disabled|Observable Enrichment Integrations|Use regex|
    |Generic Rule for RSS Feeds|This is a generic rule for extracting MITRE Techniques from any RSS feed data source.|Disabled|RSS Feeds Only|Use regex|
    |Generic Rule for Threat Lookup|This is a generic rule for any threat lookup integrations.|Disabled|Threat Lookup Integrations|Use regex|

5.  Select **Duplicate** to create a copy of the extraction rule.

6.  Select **Disable** to disable the extraction rule.

    **Important:** Once it is disabled the rule will no longer be considered for the extraction of MITRE ATT&amp;CK data.

7.  Select **Save**.

8.  Select **Delete** if you wish to delete any MITRE ATT&amp;CK Technique Extraction rule.


