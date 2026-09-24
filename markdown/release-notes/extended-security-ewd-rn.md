---
title: Extended Security for Enterprise-Wide Deployment release notes
description: The ServiceNow Extended Security for Enterprise-Wide Deployment application provides additional security for Enterprise-Wide Deployment that extends partition access controls across APIs, agentic workflows, indirect references, and unpartitioned parent tables. See the following sections for release notes by version.Version 1.0.0 enables organizations configure additional security for Project, Demand, Portfolio, and Program records, with transparent access restriction messaging for improved governance visibility.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/extended-security-ewd-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Strategic Portfolio Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Extended Security for Enterprise-Wide Deployment release notes

The ServiceNow® Extended Security for Enterprise-Wide Deployment application provides additional security for Enterprise-Wide Deployment that extends partition access controls across APIs, agentic workflows, indirect references, and unpartitioned parent tables. See the following sections for release notes by version.

## About Extended Security for Enterprise-Wide Deployment

Enable additional ACL enforcement on partitioned tables \(Project, Demand, Portfolio, Program\) through the SPM Configuration console with table-specific configuration options for flexible, granular security deployment.

See [SPM Enterprise-Wide Deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/ewd-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Extended Security for Enterprise-Wide Deployment by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store.


**Parent Topic:**[Strategic Portfolio Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/it-business-management-rn-landing.md)

## Version 1.0.0

Version 1.0.0 enables organizations configure additional security for Project, Demand, Portfolio, and Program records, with transparent access restriction messaging for improved governance visibility.

### What's new

-   **[Additional security on partitioned tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/enable-additional-security-extended-security-ewd.md)**

    Enable additional security \(ACL enforcement\) for partitioned tables to strengthen access control validation. Administrators can configure enhanced security on individual partitioned tables \(Project, Demand, Portfolio, Program\) through the **Configure SPM** console under **Partitions** &gt; **Enable additional security**. When enabled, users without partition role access see transparent access-restricted messages and security constraint indicators, including row counts of records hidden due to partition access restrictions. This provides clear governance visibility without exposing sensitive data.

-   **[Supported tables for additional security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/enable-additional-security-extended-security-ewd.md)**

    When enabled additional security on a table, partition role validation becomes mandatory for all users accessing records in that table. Additional security is supported for the following tables.

    -   Project \(pm\_project\) — Enforce partition access on project records and its related records data.
    -   Demand \(dmn\_demand\) — Enforce partition access on demand records and its related records data.
    -   Program \(pm\_program\) — Enforce partition access on program records and its related records data.
    -   Portfolio \(pm\_portfolio\) — Enforce partition access on portfolio records and its related records data.

