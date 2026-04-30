---
title: MITRE ATT&amp;CK Technique Extraction method
description: MITRE ATT&amp;CK Technique Extraction method describes how the extraction methods are performed and associated techniques are verified.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2024-10-21"
reading_time_minutes: 2
breadcrumb: [MITRE ATT&amp;CK Technique Extraction Rules, About Rules Engine in TISC, Administration, Threat Intelligence Security Center, Security Operations]
---

# MITRE ATT&amp;CK Technique Extraction method

MITRE ATT&amp;CK Technique Extraction method describes how the extraction methods are performed and associated techniques are verified.

1.  The extraction rules for data sources \(threat lookups are not applicable\) are processed whenever an entity \(for example, observable source or object source\) source record gets created.
2.  The rules are applicable for any fields within the entity source record \(except date, number fields, and Usage category and Attack phases\).
3.  The extracted MITRE techniques are associated to the corresponding entity record and you view the records in the MITRE techniques related list in the **Related Records** tab.

    **Note:** The MITRE techniques are first extracted and associated to the entity source record then the techniques associations are de-duplicated and aggregated to the parent entity record.


## View MITRE techniques

1.  Navigate to **Threat Intel Library**any entity \(observable or object\) record using the .
2.  Click on the **Related Records** tab.
3.  Select **MITRE Techniques** and view the associated techniques which are extracted.
4.  Click on the MITRE technique ID to view and access the MITRE technique association record. The **Sources** column displays all the sources \(also separated by a comma if there are one or more sources\) which are associated to the entity source record on which the MITRE extraction is performed.

    **Note:** If the same tactic and technique IDs are extracted from multiple sources then only one tactic and technique association record is displayed and the **Sources** column displays all the extracted sources.

5.  For troubleshooting, you can view the MITRE Extraction rule which was responsible for extraction of the tactic and technique associations by navigating to the **Technique Source Relations**.

    **Note:** Make sure to add the **Extraction Rule** column using the **List Actions** icon in case if you don't see the Extraction Rule column.


The extraction rules for threat lookups are processed whenever the threat lookup result record is created for any observable for which **Run threat lookup** action is triggered and the extraction is performed only on the raw data \(raw\_data field\) payload which is available in the threat lookup result record.

**Note:**

-   If there is no tactic ID present in the extracted entity \(observable or object\) source or threat lookup result for any MITRE ATT&amp;CK technique, then the technique associations are created for all the tactics that are associated to the corresponding technique in the MITRE repository.
-   If there is any tactic ID present in the extracted entity \(observable or object\) source or threat lookup result for any MITRE ATT&amp;CK technique, then the technique associations is specifically created only for all that extracted tactic\(s\) that are associated to the corresponding technique in the MITRE repository.

