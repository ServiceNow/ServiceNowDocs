---
title: Mitigation controls to vulnerable item mapping
description: Mitigation controls data is mapped to vulnerable items. You can view a list of mitigation controls that are used to mitigate the vulnerabilities and underlying Common Vulnerabilities and Exposures \(CVEs\) associated with the vulnerable items.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use mitigation controls, Security Posture Control, Security Operations]
---

# Mitigation controls to vulnerable item mapping

Mitigation controls data is mapped to vulnerable items. You can view a list of mitigation controls that are used to mitigate the vulnerabilities and underlying Common Vulnerabilities and Exposures \(CVEs\) associated with the vulnerable items.

After identifying a specific mitigation control on an asset, Security Posture Control automatically identifies any vulnerable items that are mitigated by that control. For example, any vulnerable items with CVEs that are part of signatures in Web Application Firewall \(WAF\) policies are marked as mitigated vulnerable items. This identification might be useful for vulnerability management teams to help them automatically reduce risk scores for vulnerable items that are mitigated.

## Vulnerable item mitigation controls table

The Vulnerable item mitigation controls \[sn\_vul\_vulnerable\_item\_mitigation\_control\] table has been created to map mitigation control data to mitigated vulnerable items \(VITs\). This table lists mitigated VITs and the detected mitigation controls that were used to mitigate the vulnerabilities and their underlying CVEs associated with the vulnerable items. The mitigated CVE records contain references to the mitigation control used for the assets, for example, Exploit Protection \(EDR\).

Example data is shown in the following table.

|Mitigation control exists|Mitigation control effectiveness|Detected mitigation control type|CVEs mitigated|Vulnerable item|
|-------------------------|--------------------------------|--------------------------------|--------------|---------------|
|Yes/No|Moderate|Exploit Protection \(EDR\)|CVE-2009-3373|VIT0018323|

Open a mitigation control record \(Detected mitigation control type\) on the table to review details about how a CVE and its related Common Weakness Enumeration \(CWE\) vulnerability is mitigated by the mitigation control associated with an asset. The mitigation control record contains details about the CWEs that have been mitigated, for example, how a mitigation setting satisfies vulnerabilities specified in a CWE.

## Risk calculator and risk calculator rules

Mitigation information might be used to help you set up customized risk calculator rules to help you recalculate the risk scores on VITs that have specific types of vulnerabilities and mitigation controls associated with them. For this example rule, which is based on the preceding table, the default risk calculator calculates a risk score of 60 for VITs that have the mitigation control type, Exploit Protection \(EDR\) on detected assets. This calculation score is due to the moderate risk that is associated with the vulnerability with this mitigation in place.

Example risk calculator rule with the following conditions:

**\[Mitigation control details\] \[is not\] \[empty\]** **AND** **\[Mitigation control details, Detected mitigation control type\] \[is\] \[Exploit Protection \(EDR\)\]**.

Values:

**\[Risk score\]****\[is\]****\[60\]**

See [Define fields and weights for the risk rule for Vulnerability Response Risk Calculators](../../vulnerability-response/task/vuln-calc-define-risk-rule-fields.md) for more information.

