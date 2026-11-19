---
title: MITRE ATLAS framework
description: The MITRE ATLAS framework documents adversarial tactics and techniques targeting AI \(artificial intelligence\) and ML \(machine learning\) systems, complementing traditional IT security frameworks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/security-management/about-mitre-atlas.html
release: yokohama
topic_type: concept
last_updated: "2026-08-05"
reading_time_minutes: 1
keywords: [MITRE ATLAS, AI security, machine learning threats]
breadcrumb: [Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# MITRE ATLAS framework

The MITRE ATLAS framework documents adversarial tactics and techniques targeting AI \(artificial intelligence\) and ML \(machine learning\) systems, complementing traditional IT security frameworks.

## Framework overview

The MITRE ATLAS \(Adversarial Threat Landscape for Artificial-Intelligence Systems\) framework provides a structured knowledge base for understanding and defending against attacks on AI and ML systems.

It complements the MITRE-ATT&amp;CK framework, which documents threats to traditional IT infrastructure.

**Note:** AI systems may produce inaccurate results. Implement human review processes when working with AI-generated data.

## Integration with Security Operations

MITRE ATLAS techniques and tactics are ingested, viewed, and associated with security incidents using the same MITRE-ATT&amp;CK Repository, MITRE-ATT&amp;CK Card, and association workflow as MITRE-ATT&amp;CK.

MITRE ATLAS is distinguished from MITRE-ATT&amp;CK by an AML-prefixed technique or tactic ID.

For example, a technique ID might be `AML.T0000`, and a tactic ID might be `AML.TA0002`.

Technique names can collide between the two frameworks, so the ID is the reliable indicator. There is no separate object type for MITRE ATLAS.

For setup steps, see [Activate the MITRE ATLAS framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/setup-mitre-atlas-profile.md).

## TAXII collection

Unlike MITRE-ATT&amp;CK, which exposes three TAXII collections \(Enterprise, Mobile, and ICS\), MITRE ATLAS exposes only one TAXII collection \("ATLAS"\).

## STIX object mapping

MITRE ATLAS techniques and tactics are ingested using the same STIX object types as MITRE-ATT&amp;CK \(for example, Attack Pattern for techniques and Course of Action for mitigations\).

The Data Source and Detection fields available for MITRE-ATT&amp;CK techniques are not populated for MITRE ATLAS techniques.

