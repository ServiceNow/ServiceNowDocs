---
title: MITRE ATT&amp;CK Technique Extraction Rules
description: Extract MITRE techniques automatically from observables or objects ingested from various data sources and also extract MITRE techniques from threat lookup results on observable record.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-04-06"
reading_time_minutes: 5
breadcrumb: [About Rules Engine in TISC, Administer Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# MITRE ATT&amp;CK Technique Extraction Rules

Extract MITRE techniques automatically from observables or objects ingested from various data sources and also extract MITRE techniques from threat lookup results on observable record.

## Before you begin

Role required: sn\_sec\_tisc.admin

**Note:** Make sure to verify that the MITRE ATT&amp;CK repository data available in the instance that you are using. If the data is not available then the application will not perform the extraction.

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence Security Center** &gt; **Administration**.

2.  Go to **Rules Engine** &gt; **MITRE ATT&amp;CK Technique Extraction Rules**.

    The MITRE ATT&amp;CK Technique Extraction Rules page displays.

3.  Click **New**.

<table id="choicetable_vcd_cj4_zbc"><thead><tr><th align="left" id="d470613e100">

Field

</th><th align="left" id="d470613e103">

Description

</th></tr></thead><tbody><tr><td id="d470613e109">

**Name**

</td><td>

Enter a name for the MITRE ATT&amp;CK Technique Extraction rule.

</td></tr><tr><td id="d470613e118">

**Description**

</td><td>

Enter a description for the MITRE ATT&amp;CK Technique Extraction rule.

</td></tr><tr><td id="d470613e127">

**Integration Type**

</td><td>

Indicates the MITRE ATT&amp;CK Technique Extraction rule for the Data Sources or Threat Lookup Results. Select the list of data sources from the lookup.Following are the options available for Data Sources:

-   **Data Sources - All**: which means that the rule is applicable for all the type of data sources such as Threat Intel Feeds, Import Intelligence records, API Sources \(for example, observables created from API\), Sent from SIR \(observables that are sent from SIR\) and various entities that are manually created by the users in the Threat Intelligence library.
-   **Data Sources - Threat Intel Feeds**: This corresponds to the extraction rules that are only applicable for threat intelligence feeds.
-   **Data Sources - API Sources**: This corresponds to the extraction rules that are only applicable for API Sources.
-   **Threat Lookup integrations**: for this type of option, the extraction rule is applicable to all threat lookup integrations such as Virustotal.

**Note:**

    -   When you select this option, you must enter the vendor name for the threat lookup. The vendor names are automatically populated only when the threat lookup integrations are installed from ServiceNow store.
    -   For the threat intelligence data sources, the extraction rules are only supported for STIX, MISP, and Custom Feed types.


</td></tr><tr><td id="d470613e174">

**Threat Feed Type**

</td><td>

Following are the options available for Threat Feed Type:-   **STIX\(TAXII/HTTPS\)**: Option to filter the threat feeds of the STIX TAXII or HTTPS feed type and select the associated feeds from the lookup.
-   **MISP**: Option to filter the threat feeds of the MISP feed type and select the associated feeds by searching using the lookup icon.
-   **Custom feed**: Option to filter the threat feeds of the custom feed type and select the associated feeds by searching using the lookup icon.


</td></tr><tr><td id="d470613e201">

**Feeds**

</td><td>

Select one or more threat feed integrations for the selected feed type.**Note:** If this field is left blank then all the threat feed integrations for the selected feed type will be automatically considered for the extraction.

</td></tr><tr><td id="d470613e212">

**Method to extract MITRE ATT&amp;CK tactics and techniques**

</td><td>

Option to select the extract MITRE ATT&amp;CK tactics and techniques method. The two available methods are:1.  Use Regex
2.  Use Script


</td></tr><tr><td id="d470613e229">

**Extraction Method - Use Regex**

</td><td>

This method uses a regular expression that allows the threat analysts to define a pattern with a sequence of characters to perform extraction method.

</td></tr><tr><td id="d470613e238">

**Tactic Regex**

</td><td>

Option to provide regular expression for the extraction of MITRE ATT&amp;CK tactic ID\(s\).

</td></tr><tr><td id="d470613e247">

**Technique Regex**

</td><td>

Option to provide regular expression for the extraction of MITRE ATT&amp;CK technique ID\(s\).

</td></tr><tr><td id="d470613e256">

**Extraction Method - Use script**

</td><td>

This method uses a script format to perform the extraction on the observable source or object source or indicator source or threat lookup results.**Note:**

-   This script method can be used to extract MITRE tactics and techniques from entity source record and link the tactics and techniques to the entity source record itself.
-   This script method can be used to extract MITRE tactics and techniques from threat lookup results and link the tactics and techniques to the entity record.
The sample script is shown below for your reference:

```
(function process(lookupResultRawData, recordGr, ruleGr, lookupResultGr) {
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
</table>4.  Click **Enable** to enable the MITRE ATT&amp;CK Technique Extraction rule after you create a new rule.

    If you don't enable the MITRE ATT&amp;CK Technique Extraction rule then the rule will not be applied to the record.

    **Note:**

    1.  Data sources: Whenever you enable the extraction rule, the combination of data sources and integration type should not be matching any of the existing enabled extraction rules, and if so then the application will display an error message for you to modify the existing combinations and re enable the rule.
    2.  Threat Lookup: Whenever you enable the extraction rule, the vendor name should not be matching any of the existing enabled extraction rules, and if so then the application will display an error message for you to modify the vendor name and re enable the rule.
    3.  A sample MITRE ATT&amp;CK Technique Extraction rules are provisioned for the users in the base system and these rules will be in disabled state by default and you must enable and activate the rule.

        |Field|Description|
        |-----|-----------|
        |Generic Rule for data sources ingestion|This is a generic rule for ingestion from all types of data sources including Import Intelligence and manual creation.|
        |Generic Rule for Threat Lookup|This is a generic rule for any threat lookup integrations.|

5.  Select **Duplicate** to create a copy of the extraction rule.

6.  Select **Disable** to disable the extraction rule.

    **Note:** After you disable the rule, it is no longer considered for the extraction of MITRE data.

7.  Select **Save** to apply the changes.

8.  Select **Delete** if you wish to delete any MITRE ATT&amp;CK Technique Extraction rule.


