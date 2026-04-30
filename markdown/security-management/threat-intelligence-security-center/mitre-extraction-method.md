---
title: View extracted MITRE ATT&amp;CK Techniques
description: MITRE ATT&amp;CK Technique Extraction method describes how the extraction methods are performed and associated techniques are verified for observables, objects, and RSS feeds.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-03-05"
reading_time_minutes: 3
breadcrumb: [MITRE ATT&amp;CK Technique Extraction Rules, About Rules Engine in TISC, Administer, Threat Intelligence Security Center, Security Operations]
---

# View extracted MITRE ATT&amp;CK Techniques

MITRE ATT&amp;CK Technique Extraction method describes how the extraction methods are performed and associated techniques are verified for observables, objects, and RSS feeds.

You must have access to the Threat Intelligence Security Center workspace. Role required: none.

About MITRE ATT&amp;CK technique extraction:

-   The extraction rules for data sources \(threat lookups are not applicable\) are processed whenever an entity \(for example, observable source or object source\) source record gets created.
-   The rules are applicable for any fields within the entity source record \(except date, number fields, and Usage category and Attack phases\).
-   The extracted MITRE techniques are associated to the corresponding entity record and you view the records in the MITRE techniques related list in the **Related Records** tab.

    **Note:** The MITRE techniques are first extracted and associated to the entity source record then the techniques associations are de-duplicated and aggregated to the parent entity record.


The extraction rules for threat lookups or observable enrichment are processed whenever the threat lookup observable enrichment result or observable enrichment record is record is created for any observable for which **Run threat lookup** or **Run observable enrichment** action is triggered and the extraction is performed only on the raw data \(raw\_data field\) payload which is available in the threat lookup result or observable enrichment record.

## Viewing MITRE ATT&amp;CK techniques

1.  View MITRE ATT&amp;CK techniques for Observables/ Objects
2.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Threat Intel Library** &gt; **Observables**.
3.  Select any Observable record.
4.  Go to **Related Records** tab.
5.  Select **MITRE Techniques** section to view the extracted MITRE ATT&amp;CK techniques.
6.  Click on the MITRE technique ID to view the MITRE technique association record. The **Sources** column displays all the sources \(separated by a comma if there are one or more sources\) which are associated to the entity source record on which the MITRE extraction is performed.

    **Note:** If the same tactic and technique IDs are extracted from multiple sources then only one tactic and technique association record is displayed and the **Sources** column displays all the extracted sources.

7.  For troubleshooting, you can view the MITRE Extraction rule which was responsible for extraction of the tactic and technique associations by navigating to the **Technique Source Relations**.

    **Note:** Make sure to add the **Extraction Rule** column using the **List Actions** icon in case if you don't see the Extraction Rule column.

8.  View MITRE ATT&amp;CK techniques for RSS feeds
9.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Threat Intel Library** &gt; **RSS Feeds** &gt; **All RSS Feeds**
    -   Whenever an RSS feed record is created or updated, the MITRE ATT&amp;CK technique extraction rules are processed.
    -   The rules are applicable for any fields within the RSS feed record \(except date, number fields, and Attack phases\).
    -   The extracted MITRE techniques are associated to the corresponding RSS feed record and you can view these records in the **MITRE techniques** related records list in the **Related Records** section.
10. Select any RSS feed record.
11. Go to **Related Records** tab.
12. Select **MITRE Techniques** to view the extracted MITRE ATT&amp;CK techniques.
13. Click on the **MITRE technique ID** to view the MITRE technique association record.
14. For troubleshooting, you can view the MITRE Extraction rule which was responsible for extraction of the tactic and technique associations.

**Note:**

-   If there is no tactic ID present in the extracted entity \(observable or object\) source or threat lookup result for any MITRE ATT&amp;CK technique, then the technique associations are created for all the tactics that are associated to the corresponding technique in the MITRE repository.
-   If there is any tactic ID present in the extracted entity \(observable or object\) source or threat lookup result for any MITRE ATT&amp;CK technique, then the technique associations is specifically created only for all that extracted tactic\(s\) that are associated to the corresponding technique in the MITRE repository.

