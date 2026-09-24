---
title: Vulnerability Response release notes
description: The ServiceNow Vulnerability Response application brings security and IT together to enable you to remediate your most critical vulnerabilities more quickly and efficiently. See the following sections for release notes by release.This release automatically re-evaluates remediation tasks when a vulnerable item's preferred solution changes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/secops-vuln-resp-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Vulnerability Response, Patch Orchestration]
breadcrumb: [Security Operations release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Vulnerability Response release notes

The ServiceNow® Vulnerability Response application brings security and IT together to enable you to remediate your most critical vulnerabilities more quickly and efficiently. See the following sections for release notes by release.

## About Vulnerability Response

-   Remediate your most critical vulnerabilities quickly and efficiently by connecting security and IT teams.
-   Consolidate vulnerability data from multiple sources into a single authoritative record with the Central Vulnerability Database \(CVDB\).
-   Filter, group, and assign vulnerable items to remediation tasks based on configurable rules.
-   Configure background jobs and other administration settings directly from the Vulnerability Response Workspace.

See [Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/vuln-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Vulnerability Response and supported third-party integrations by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Additional requirements**

    The Security Support Common plugin is activated automatically when any of the plugins for the main Security Operations applications are activated. These applications include Vulnerability Response, Security Incident Response, Threat Intelligence, and Configuration Compliance.


**Parent Topic:**[Security Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/security-operations-rn-landing.md)

## Brazil Early Availability

This release automatically re-evaluates remediation tasks when a vulnerable item's preferred solution changes.

### What's new

-   **[Automatic re-evaluation of remediation tasks on preferred solution change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/vulnerability-groups.md)**

    Remediation tasks can now automatically re-evaluate vulnerable items when their Preferred solution changes, so items are regrouped into the appropriate remediation task without manual intervention. This helps keep remediation tasks accurate and reduces manual cleanup.


