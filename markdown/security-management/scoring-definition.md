---
title: MITRE-ATT&amp;CK Scoring definition
description: Define your organization's MITRE-ATT&amp;CK scoring system so that you can measure how effectively your organization can detect specific adversary techniques.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Define the technique detection coverage, MITRE-ATT&amp;CK administration, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# MITRE-ATT&amp;CK Scoring definition

Define your organization's MITRE-ATT&amp;CK scoring system so that you can measure how effectively your organization can detect specific adversary techniques.

|Score|Score mapping|Description|
|-----|-------------|-----------|
|None|0|Insufficient data to detect a specific adversary technique.|
|Poor|1|Basic signatures and correlation rules are in place to detect specific adversary techniques. Threat detection is not in real time and covers only a minimal number of aspects of a technique. For example, hunting occurs only on one endpoint at a time. Your organization might still have thousands or hundreds of events that hunters must review and correlate with other events to find outliers. The number of false positives is high.|
|Fair|2|Collecting the right data to a great extent and the data quality is fair. For example, your organization might be starting to add Sysmon Logs, ETW, PowerShell logs, and the like. However, the threat detection is still not in real time. Your organization may not have all the right tools to effectively aggregate and analyze the data. Hunters must manually run queries and correlate to accurately analyze the data. The number of false positives is high.|
|Good|3|Real-time detection that correlates and integrates multiple data across your endpoints. Threat detection covers many aspects of a technique's procedures. Your adversaries could possibly bypass detection with evasion and obfuscation. Your organization can easily identify false positives and filter them out. Your organization uses basic data science techniques to analyze the data in the central repository.|
|Very Good|4|Effectively detect malicious techniques in real time and cover most aspects of a technique's procedures. The possibility of your adversaries bypassing detection with evasion and obfuscation methods is harder than at the Good level. Your organization can easily identify false positives and filter them out. Your organization uses advanced data science techniques to detect the adversary techniques.|
|Excellent|5|Effectively detect malicious techniques in real time and cover all aspects of a technique's procedures. Your organization has a good understanding of your environment with the right automation and quality of data. The possibility of your adversaries bypassing detection with evasion and obfuscation methods is not possible at this level. The number of false negatives is low.|

**Parent Topic:**[Define the technique detection coverage](../task/define-technique-coverage.md)

