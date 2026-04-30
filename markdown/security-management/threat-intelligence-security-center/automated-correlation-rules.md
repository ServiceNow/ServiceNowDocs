---
title: Automated Correlation
description: Automated correlation helps you identify the relationships between observables, indicators, and objects.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-03-26"
reading_time_minutes: 5
breadcrumb: [Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Automated Correlation

Automated correlation helps you identify the relationships between observables, indicators, and objects.

With the correlation process, the application automatically establishes the correlation between threat intelligence records based on the predefined rules. Based on the type of the rule that is applied, the relationship can be a confirmed relationship or a potential relationship. If the relationships between the objects are confirmed, those objects are automatically displayed on the details view of that object under the **Related Records** section.

The following describes the relationships and potential relationships:

-   **Relationships**: Use the relationships objects to link together two observables or an observable and SDO to explain how they relate to each other.
-   **Potential Relationships**: Use the potential relationships to establish potentially possible relationships between two SDOs, two Observables or an observable and SDO by using the automated correlation.

    Correlation rules for potential relationships identify potential relationships between threat intelligence entities, indicators, and observables.

    **Note:** These rules are deactivated by default to prevent performance issues from excessive relationship creation. Enabling these rules can result in the creation of many potential relationships, depending on the volume of ingested data and shared observables.


The following are the predefined correlation rules provisioned within the base system:

<table id="table_dqb_dq2_nzb"><thead><tr><th>

Name

</th><th>

Description

</th><th>

Definition

</th><th>

Action

</th><th>

Status

</th></tr></thead><tbody><tr><td>

Observables with same file hash

</td><td>

The rule compares the observables' hash values of the same type and identifies if they share the same hash.

</td><td>

The rule compares the hash values of the same type of the indicators and identifies if they share the same hash.

</td><td>

Creates a Relationship

</td><td>

Enabled

</td></tr><tr><td>

URL Observables with same domain

</td><td>

The rule examines the commonalities in the structure of URLs to identify if they share the same base domain.

</td><td>

The rule examines the commonalities in the structure of URLs. Identifies if they share the same base domain and have a similar subdirectory structure.

</td><td>

Creates a Potential Relationship

</td><td>

Disabled

</td></tr><tr><td>

Observable found as sources in network object

</td><td>

The rule matches the Network source attribute value with IPV4, IPV6, or domain-name observables in the system and links as the Source of traffic.

</td><td>

The rule matches the Source attribute value with IPV4, IPV6 or domain-name observables in the system and links as Source of traffic.

</td><td>

Creates a Relationship

</td><td>

Enabled

</td></tr><tr><td>

Observable found as destination in network object

</td><td>

The rule matches the Network destination attribute value with IPV4, IPV6, or domain-name observables in the system and links as the destination of the traffic.

</td><td>

The rule matches the destination attribute value with IPV4, IPV6 or domain-name observables in the system and links as destination of traffic.

</td><td>

Creates a Relationship

</td><td>

Enabled

</td></tr><tr><td>

Relate observables based on communication

</td><td>

Based on network objects, the rule identifies all the observables \(IPV4, IPV6, and domain name\) that have communicated with the same destination \(IPV4, IPV6, or domain name\) and establishes a relationship between these observables. Also, related observables \(IPV4, IPV6, and domain name\) if they are related to the same network object as the source communicating with the destination.

</td><td>

Based on network objects, the rule identifies all the indicators that have communicated with the same destination \(IPV4, IPV6, mac-addr or domain-name\) and establishes a relationship between these indicators as connected to the same C2 infrastructure.

</td><td>

Creates a Relationship

</td><td>

Enabled

</td></tr><tr><td>

Related Root domain observables to sub domains

</td><td>

The rule ties together a root domain with sub-domains and vice versa for domain type of observables.

</td><td>

The rule ties together a root domain with sub-domains.

</td><td>

Creates a Relationship

</td><td>

Enabled

</td></tr><tr><td>

Related domains to IPs based on DNS resolutions

</td><td>

Using domain-ipv4 or domain-ipv6 attributes of domain observables, the rule establishes relationships between the domains and IPs.

</td><td>

Using the attributes domain-ipv4 or domain-ipv6, the rule identifies all the domains or sub-domains that resolve to the same IP address and establishes relationships between the indicators, indicating their connection to the same C2 infrastructure.

</td><td>

Creates a Relationship

</td><td>

Enabled

</td></tr><tr><td>

Matching domains with SSL Certificates

</td><td>

The rule analyzes the SSL certificate information associated with the domain observables and establishes a relation between them.

</td><td>

The rule analyzes the SSL certificate information associated with the indicators and identifies that both certificates are issued by the same certificate authority and share the same expiration date and establishes relationships between the indicators, indicating their connection to the same C2 infrastructure or threat campaign.

</td><td>

Creates a Relationship

</td><td>

Enabled

</td></tr><tr><td>

Relate entities based on common observables

</td><td>

The rule compares if the same observable is related to two different entities and relates them to each other.

</td><td>

The rule compares if the same observable is related to two different entities and identifies them as related to each other.

</td><td>

Creates a Potential Relationship

</td><td>

Disabled

</td></tr><tr><td>

Relate indicators based on common observables

</td><td>

The rule compares if the same observable is related to two different indicators and relates them to each other.

</td><td>

The rule compares if the same observable is related to two different indicators and identifies them as related to each other.

</td><td>

Creates a Potential Relationship

</td><td>

Disabled

</td></tr><tr><td>

Relate indicators with objects based on common observables

</td><td>

The rule compares if the same observable is related to indicators, and objects and relates them to each other.

</td><td>

The rule compares if the same observable is related to indicators and objects and identifies them as related to each other.

</td><td>

Creates a Potential Relationship

</td><td>

Disabled

</td></tr></tbody>
</table>**Parent Topic:**[Threat Intelligence Security Center Library](threat-intelligence-security-center-library.md)

**Related topics**  


[Understanding the Data Model](../reference/understanding-the-data-model.md)

[TISC Library Objects form view](tisc-library-home-page-view.md)

[TISC Library Repository](tisc-ioc.md)

[Access Vulnerability Downstream actions](downstream-actions-from-the-vulnerability-form-view.md)

[Deleting threat intelligence library records](../task/tisc-delete-lib-records.md)

[Export intelligence data](../task/tisc-export-observables.md)

[Confirm Potential Relationships from Related Records](../task/confirm-potential-relationships.md)

