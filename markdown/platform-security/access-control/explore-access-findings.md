---
title: Explore Access findings
description: Access findings feature displays the potential vulnerabilities that are discovered the last time access checks were ran on your ServiceNow AI Platform.
locale: en-US
release: australia
product: Access Control
classification: access-control
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Access findings, Access Management]
---

# Explore Access findings

Access findings feature displays the potential vulnerabilities that are discovered the last time access checks were ran on your ServiceNow AI Platform.

To include a robust security scanning capability designed to automatically detect and report potential vulnerabilities in your instance there are two core components working in tandem: **Access checks** and **Access findings**.

Together, these features provide a continuous, automated audit of your instance's security posture, helping you identify risks in real-time rather than waiting for manual reviews. To effectively manage your instance security, it is helpful to understand the distinct roles of checks and findings.

## Access checks \(Rules\)

Access checks are the security definitions and logic that run in the background. They serve as the blueprints for a secure instance. Each check represents a specific security rule or best practice, for example:

-   `Do all client-callable Script Includes have appropriate Access Controls?`
-   `Are there any public pages that should be restricted?`

Think of Access checks as the questions the system asks about your configuration. They define what to look for.

## Access findings \(Results\)

Access findings are the actionable records generated when an Access check detects a violation. If a specific configuration in your instance fails a check, the system creates a finding.

Think of Access findings as the answers or results. They represent specific instances of a vulnerability that need your attention \(for example, `"Script Include 'UpdateAllKnowledge' is missing an ACL"`\).

## How They Work Together

The relationship between checks and findings is linear and automated:

1.  Definition: An Access check is defined with specific criteria for what constitutes a security risk.
2.  Scan: The system runs these checks against your entire instance configuration.
3.  Generation: If a configuration matches the risk criteria of a check, the system generates an Access finding.

    **Note:** A single Access check can generate multiple Access findings if the same vulnerability exists in multiple records.

4.  Remediation: You resolve the finding by fixing the configuration. Once fixed, the finding is marked as `Resolved`.

## How This Helps You

This combined capability transforms security from a manual, reactive task into an automated, proactive workflow.

-   Automated Detection: Instead of manually auditing thousands of scripts and ACLs, the system automatically flags issues for you.
-   Prioritized Remediation: findings are categorized by priority \(for example, High, Medium\), allowing you to focus your limited time on the most critical vulnerabilities first.
-   Clear Context: Every finding links back to the specific check that triggered it and the Source record involved. This tells you exactly why it was flagged and where to fix it, eliminating the guesswork in security patching.

By using the Access findings dashboard to monitor these results, you ensure that your instance remains compliant with security best practices and that potential entry points—like client-callable scripts—are properly secured.

