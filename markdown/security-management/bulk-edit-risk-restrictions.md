---
title: Bulk edit risk reduction restrictions
description: Risk reduction in the Bulk Edit dialog is restricted in specific scenarios based on the vulnerabilities mapped to the selected items and the vulnerability configuration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/bulk-edit-risk-restrictions.html
release: zurich
topic_type: reference
last_updated: "2026-06-04"
reading_time_minutes: 1
keywords: [bulk edit, risk reduction, restrictions, Security Exposure Management]
breadcrumb: [Using bulk edit in the Security Exposure Management Workspace, Bulk edit in the Security Exposure Management Workspace, Use, Unified Security Exposure Management, Security Operations]
---

# Bulk edit risk reduction restrictions

Risk reduction in the Bulk Edit dialog is restricted in specific scenarios based on the vulnerabilities mapped to the selected items and the vulnerability configuration.

## Selection and configuration restrictions

|Restriction|Behavior|Resolution|
|-----------|--------|----------|
|Items from multiple vulnerabilities selected|Risk reduction is not available. The dialog displays the message: `This reduction is restricted to involvement of multiple vulnerabilities`. Deferral requests can still be submitted.|Select only items that map to the same vulnerability before opening Bulk Edit.|
|Risk reduction inactive on the vulnerability|The **Request for Risk Reduction** option does not appear in the Bulk Edit dialog.|Enable risk reduction on the vulnerability record before requesting a risk reduction for its associated items.|

## Application support

Bulk edit risk reduction is supported in the host vulnerability and CVE-based vulnerable items applications. It is not supported in the Configuration Compliance application.

**Parent Topic:**[Using bulk edit in the Security Exposure Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-using-bulk-edit.md)

