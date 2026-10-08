---
title: Bulk edit risk modification restrictions
description: Risk modification in the Bulk Edit dialog is restricted in specific scenarios based on the vulnerabilities mapped to the selected items and the vulnerability configuration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/bulk-edit-risk-restrictions.html
release: brazil
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 1
keywords: [bulk edit, risk reduction, restrictions, Security Exposure Management]
breadcrumb: [Using bulk edit in the Security Exposure Management Workspace, Bulk edit in the Security Exposure Management Workspace, Use, Unified Security Exposure Management, Security Operations]
---

# Bulk edit risk modification restrictions

Risk modification in the Bulk Edit dialog is restricted in specific scenarios based on the vulnerabilities mapped to the selected items and the vulnerability configuration.

## Selection and configuration restrictions

|Restriction|Behavior|Resolution|
|-----------|--------|----------|
|Items from multiple vulnerabilities selected|Risk modification is not available. The dialog displays the message: `This modification is restricted to involvement of multiple vulnerabilities`.|Select only items that map to the same vulnerability before opening Bulk Edit.|
|Risk modification inactive on the vulnerability|The **Risk rating** field does not appear in the Bulk Edit dialog.|**Enable risk change** on the vulnerability record before requesting a risk change for its associated items.|

## Application support

Bulk edit risk modification is supported in the host vulnerability and CVE-based vulnerable items applications. It is not supported in the Configuration Compliance application.

