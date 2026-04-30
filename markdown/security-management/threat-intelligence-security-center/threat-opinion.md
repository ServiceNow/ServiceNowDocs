---
title: Threat Opinion
description: An Opinion is an assessment of the accuracy of the information in a STIX Object produced by a different entity. Threat opinions apply for STIX 2.x.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Threat Entities, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Threat Opinion

An Opinion is an assessment of the accuracy of the information in a STIX Object produced by a different entity. Threat opinions apply for STIX 2.x.

The opinion property captures the level of agreement or disagreement using a fixed scale. The fixed scale also supports a numeric mapping to enable consistent statistical operations across opinions.

For example, an analyst from a consuming organization might say that they "strongly disagree" with a Campaign object and provide an explanation about why.

Opinions are subjective, and the specification does not address how best to interpret them.

Human analysts create Opinions and are composed of human-oriented text, they contain an extra property to capture the author that created the Opinion.

-   **[Define Threat Opinion](../task/define-threat-opinion.md)**  
Define threat opinions as an assessment of the accuracy of the information in a STIX object.

**Parent Topic:**[Threat Entities](tisc-threat-entities.md)

