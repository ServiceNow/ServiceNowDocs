---
title: MITRE D3FEND framework
description: MITRE D3FEND is a knowledge graph of cybersecurity countermeasure techniques that complements the MITRE-ATT&amp;CK framework by providing defensive techniques.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# MITRE D3FEND framework

MITRE D3FEND is a knowledge graph of cybersecurity countermeasure techniques that complements the MITRE-ATT&amp;CK framework by providing defensive techniques.

## MITRE D3FEND framework overview

MITRE D3FEND \(Detection, Denial, and Disruption Framework Empowering Network Defense\) is a knowledge graph developed by MITRE that catalogs defensive cybersecurity countermeasure techniques. It provides a standardized taxonomy of over 200 defensive techniques organized into seven tactical categories.

While MITRE ATT&amp;CK describes "how adversaries attack," D3FEND describes "how defenders respond." The two frameworks are complementary and bidirectionally mapped, enabling security teams to identify appropriate defensive countermeasures for specific attack techniques.

## Key concepts

**Defensive Techniques**

Over 200 standardized defensive techniques organized hierarchically with parent techniques and sub-techniques. Each technique includes a definition, digital artifacts it operates on, and mappings to ATT&amp;CK offensive techniques.

**D3FEND Tactics**

Seven high-level tactical categories organize defensive techniques:

-   Model: Understand the system and its behavior
-   Harden: Reduce attack surface and vulnerabilities
-   Detect: Identify malicious activity
-   Isolate: Contain threats and limit damage
-   Deceive: Entice, and allow potential attackers access to an observed/ controlled environment
-   Evict: Remove threats from the environment
-   Restore: Return the system to a better state

**Digital Artifacts**

Over 800 asset types that defensive techniques operate on or protect, including processes, files, network traffic, user accounts, system calls, and more.

**ATT&amp;CK Mappings**

Bidirectional mappings between D3FEND defensive techniques and ATT&amp;CK offensive techniques, showing which defensive techniques can counter specific attack methods.

## Integration with Threat Intelligence

The ServiceNow Threat Intelligence application integrates D3FEND to provide:

-   Automatic ingestion of D3FEND techniques, tactics, and artifacts via API
-   Bidirectional mapping between D3FEND defensive and ATT&amp;CK offensive techniques
-   Coverage analysis showing defensive posture against ATT&amp;CK techniques
-   Task tracking for implementing defensive countermeasures

