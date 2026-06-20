---
title: MITRE ATT&amp;CK Technique Extraction Rules
description: Extract MITRE techniques automatically from observables or objects ingested from various data sources and from threat lookup results on observable records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/threat-intelligence-security-center/mitre-extraction-rules.html
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-05-19"
reading_time_minutes: 5
breadcrumb: [About Rules Engine in TISC, Administer, Threat Intelligence Security Center, Security Operations]
---

# MITRE ATT&amp;CK Technique Extraction Rules

Extract MITRE techniques automatically from observables or objects ingested from various data sources and from threat lookup results on observable records.

## Before you begin

Role required: sn\_sec\_tisc.admin

**Note:** Ensure that MITRE ATT&amp;CK repository data is available in the instance. If the data is not available, extraction does not occur.

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence Security Center** &gt; **Administration**.

2.  Go to **Rules Engine** &gt; **MITRE ATT&amp;CK Technique Extraction Rules**.

    The MITRE ATT&amp;CK Technique Extraction Rules page displays.

    **Important:** Before enabling MITRE ATT&amp;CK Technique Extraction rules, an alert message displays prompting you to ensure that the MITRE ATT&amp;CK data is available in your instance. If the required dataset is not present, then the rule execution may not produce the expected results.

3.  Select **New**.

4.  On the form, fill in the fields in the **Extraction Rule** and **Extraction Method** sections.

<table id="choicetable_vcd_cj4_zbc"><thead><tr><th align="left" id="d457043e113">

Field

</th><th align="left" id="d457043e116">

Description

</th></tr></thead><tbody><tr><td id="d457043e122">

**Name**

</td><td>

Name of the MITRE ATT&amp;CK Technique Extraction rule.

</td></tr><tr><td id="d457043e131">

**Description**

</td><td>

Description of the MITRE ATT&amp;CK Technique Extraction rule.

</td></tr><tr><td id="d457043e140">

**Integration Type**

</td><td>

MITRE ATT&amp;CK Technique Extraction rule scope, based on data sources or threat lookup results. Select the data sources from the lookup.Options for Data Sources:

-   **Data Sources - All**: The rule applies to all data source types, including Threat Intel Feeds, Import Intelligence records, API Sources \(for example, observables created from API\), Sent from SIR \(observables sent from SIR\), and entities manually created in the Threat Intelligence library.
-   **Data Sources - Threat Intel Feeds**: The rule applies only to threat intelligence feeds.
-   **Data Sources - API Sources**: The rule applies only to API sources.
-   **RSS Feeds Only**: The rule applies only to the RSS feeds.
-   **Threat Lookup integrations**: The rule applies to all threat lookup integrations, such as VirusTotal.

**Note:** When you select this option, enter the vendor name for the threat lookup. Vendor names are automatically populated only when the threat lookup integrations are installed from the ServiceNow store. For threat intelligence data sources, extraction rules are supported only for STIX, MISP, and Custom Feed types.

-   **Observable Enrichment integrations**: The rule applies to all observable enrichment integrations.


</td></tr><tr><td id="d457043e189">

**Threat Feed Type**

</td><td>

For **Data Sources - Threat Intel Feeds**, select one of the following options:-   **STIX\(TAXII/HTTPS\)**: Filters threat feeds of the STIX TAXII or HTTPS feed type. Select the associated feeds from the lookup.
-   **MISP**: Filters threat feeds of the MISP feed type. Search for associated feeds using the lookup icon.
-   **Custom feed**: Filters threat feeds of the custom feed type. Search for associated feeds using the lookup icon.


</td></tr><tr><td id="d457043e219">

**Feeds**

</td><td>

For **RSS Feeds Only**, select one or more threat feed integrations.**Note:** If this field is blank, all threat feed integrations for the selected feed type are used for extraction.

</td></tr><tr><td id="d457043e233">

**Method to extract MITRE ATT&amp;CK tactics and techniques**

</td><td>

Method for extracting MITRE ATT&amp;CK tactics and techniques. Available methods are-   **Tactic and Technique Regex**: Extracts paired tactic and technique IDs from the data using regex patterns, preserving the explicit tactic-to-technique mapping.
-   **Technique Regex**: Extracts only technique IDs using regex; all possible tactic-technique pairs from MITRE ATT&amp;CK are mapped automatically, which may lead to multiple tactics per technique.
-   **Script**:Runs a custom script to handle extraction with full control over the logic.


</td></tr><tr><td id="d457043e259">

**Combined Tactic-Technique Regex**

</td><td>

Regex pattern that matches a MITRE ATT&amp;CK tactic ID and its associated technique or sub-technique ID, so that they are extracted as a linked pair. Applies when the extraction method is set to Tactic and Technique Regex.

</td></tr><tr><td id="d457043e268">

**Technique Regex**

</td><td>

Regex pattern that matches MITRE ATT&amp;CK technique or sub-technique IDs, extracting them independently without tactic association. Applies when the extraction method is set to Technique Regex.

</td></tr><tr><td id="d457043e277">

**Tactic Regex**

</td><td>

Regex pattern that matches MITRE ATT&amp;CK tactic IDs. Used alongside the combined tactic-technique regex to identify tactic IDs within the matched tactic-technique pairs.

</td></tr><tr><td id="d457043e286">

**Script**

</td><td>

Uses a script to perform extraction on the observable source, object source, indicator source, or threat lookup results. Use this method as an alternative to extract MITRE tactics and techniques from an entity source record and threat lookup results and link them to the entity source record. The following sample script extracts MITRE data from a threat lookup integration by parsing the raw payload and extracting from a specific field, then associates the extracted tactics and techniques to the observable record.

 ```
(function process(lookupResultRawData, recordGr, ruleGr, lookupResultGr) {
/*********************************
 
* - threatLookupResult: The raw data of the threat lookup result  in stringified JSON format.
* - recordGr: The GlideRecord of the observable record.
* - ruleGr: GlideRecord of matched MITRE extraction rule
*
* After extracting MITRE tactic IDs and technique IDs,
* use this method to link the tactics and techniques to the observable record.
  **********************************/  
var utils = new MITREExtractionUtils();
var parsedRawData =JSON.parse(lookupResultRawData);
var mitreDataField = parsedRawData.mitre_data; 
var response = utils.extractMITREDataUsingRegex(mitreDataField,'TA[0-9][0-9][0-9][0-9]','T[0-9][0-9][0-9][0-9].[0-9][0-9][0-9]|T[0-9][0-9][0-9][0-9]');
utils.addTacticTechniquesForLookup(response.tacticIds, response.techniqueIds, recordGr, ruleGr.getUniqueValue(), lookupResultGr);
 
})(lookupResultRawData, recordGr, ruleGr, lookupResultGr);
```

</td></tr></tbody>
</table>5.  Select **Enable** to enable the MITRE ATT&amp;CK Technique Extraction rule after creating a rule.

    If the rule is not enabled, it is not applied to records.

    **Note:** When enabling a rule for data sources, the combination of data sources and integration type must not match any existing enabled extraction rule. If a conflict exists, an error message appears — modify the existing combination and re-enable the rule. When enabling a rule for threat lookup, the vendor name must not match any existing enabled extraction rule. If a conflict exists, an error message appears — modify the vendor name and re-enable the rule.

    Sample MITRE ATT&amp;CK Technique Extraction rules are available in the base system in a disabled state by default. Enable and activate each rule before use.

    |Rule|Description|
    |----|-----------|
    |Generic Rule for data sources ingestion|Generic rule for ingestion from all data source types, including Import Intelligence and manual creation.|
    |Generic rule for CrowdStrike Feed|Generic rule for extracting MITRE Tactic &amp; Technique pairs from the data ingested by CrowdStrike Feed.|
    |Generic Rule for Threat Lookup|Generic rule for any threat lookup integrations.|
    |Generic Rule for Observable Enrichment Integrations|Generic rule for any observable enrichment integrations.|

6.  Select **Duplicate** to copy the extraction rule.

7.  Select **Disable** to disable the extraction rule.

    **Note:** After disabling the rule, it is no longer used for MITRE data extraction.

8.  Select **Save**.

9.  Select **Delete** to delete a MITRE ATT&amp;CK Technique Extraction rule.


