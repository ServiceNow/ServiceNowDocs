---
title: Observable extraction from indicator patterns
description: Threat Intelligence Security Center extracts observables from indicators that use the STIX pattern type and links the extracted observables back to the source indicator.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-extract-observables-from-indicators.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-08-24"
reading_time_minutes: 2
keywords: [observable extraction, indicator pattern, STIX pattern]
breadcrumb: [Indicators, TISC Library Repository, Threat Intel Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Observable extraction from indicator patterns

Threat Intelligence Security Center extracts observables from indicators that use the STIX pattern type and links the extracted observables back to the source indicator.

## Key benefits

Observable extraction from indicator patterns provides the following benefits:

-   The system automatically creates individual observable records from pattern of Indicators of the STIX pattern type.
-   Extracted observables inherit the confidence, threat level, and severity values from the source indicator.
-   Each extracted observable maintains a link to its source indicator, preserving traceability to the original pattern.

## Extracted values

Extraction covers every observable type described in [Observables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/observables.md) except Email Message and Network. The system stores unrecognized STIX object types, such as vendor extensions, as Other Observables.

Within a pattern, only comparisons that resolve to a single literal value produce an observable. The system extracts comparisons that use the equals, IN, and ISSUBSET operators. The system skips comparisons that use inequality, greater-than, less-than, LIKE, MATCHES, ISSUPERSET, or EXISTS operators, and any comparison preceded by NOT.

Each extracted observable inherits the **Confidence**, **Expiration Time**, **TLP**, **Threat Level**, and **Threat Severity** values of the indicator source record, along with its source and source execution run values. The **Additional Context** field records the ID of the indicator the observable was extracted from.

## Considerations

Consider the following when working with extracted observables:

-   Extraction runs only when an indicator record is created. Editing the **Pattern** field on an existing aggregated indicator record doesn't extract observables from the revised pattern.
-   The system creates relationships between the indicator and each extracted observable only. The system does not create relationships between the extracted observables themselves.
-   If an observable with the same value, type, and source already exists, that record is linked.
-   An extracted value longer than 256 characters is truncated to 256 characters.
-   Extraction is enabled by default. To turn it off, set the **sn\_sec\_tisc.extract\_observables\_from\_indicator** property to false.

**Parent Topic:**[Indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/indicator.md)

**Related topics**  


[Observables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/observables.md)

