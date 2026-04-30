---
title: Configure Telecom Discrepancy Identification and Reconciliation
description: This guide outlines the steps to configure Telecom Discrepancy Identification &amp; Reconciliation \(part of TSOM Visibility\) to confirm accurate discovery and resolution of discrepancies in telecom network resources within your ServiceNow CMDB/TNI instance.Audit Results are created for each audit executed on records that matched the selection \(see matching conditions in Initial Certification Audit Run\).
locale: en-US
release: yokohama
product: Telecom Visibility
classification: telecom-visibility
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Telecom Discrepancy Identification and Reconciliation, TSOM Visibility, Telecommunications Service Operations Management]
---

# Configure Telecom Discrepancy Identification and Reconciliation

This guide outlines the steps to configure Telecom Discrepancy Identification &amp; Reconciliation \(part of TSOM Visibility\) to confirm accurate discovery and resolution of discrepancies in telecom network resources within your ServiceNow CMDB/TNI instance.

## Before you begin

To use Telecom Discrepancy Identification &amp; Reconciliation, you need a subscription to TSOM.

Role required: admin

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Dependencies and Requirements

TSOM Visibility plugin dependencies:

-   Telecom Service Operation Core \(sn\_tsom\_core\) CMDB CI Class Models\(App ID: sn\_cmdb\_ci\_class, Type: Store\)
-   Expanded Model and Asset Classes Application \(App ID: sn\_ent, Type: Store\)
-   Visibility Content \(App ID: sn\_pattern\_design, Type: Store\)
-   Integration Commons for CMDB \(App ID: sn\_cmdb\_int\_util, Type: Store\)
-   ServiceNow IntegrationHub Starter Pack Installer \(Plugin ID: com.glide.hub.integration, Type: Family\)

Discovery Core plugin \(com.snc.discovery.core\), which is automatically installed by Discovery.

ITOM Discovery License plugin \(**com.snc.itom.discovery.license**\). You must activate this plugin.

ITOM Licensing plugin \(**com.snc.itom.license**\).

For more information, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

## Installation

The TSOM Visibility plugin \(sn\_tsom\_core\) is automatically installed with Telecommunications Discovery Patterns \(sn\_tsom\_patterns\) or with the Nokia Altiplano Service Graph Connector \(sn\_sgc\_altiplano\_connector\). All logic and system properties are installed on your ServiceNow instance.

To install TSOM Visibility plugin, see [Configure Telecommunications Discovery \(TSOM\) Patterns](../concept/configuring-telecommunications-discovery-patterns.md#) or [Configure Service Graph Connector for Nokia Altiplano](../concept/configuring-service-graph-connector-nokia-altiplano.md#).

## TSOM Visibility Installation Disclaimer

See [TSOM Visibility Installation Disclaimer](../concept/tsom-visibility.md#section_wn4_2fk_b2c) for important information and requirements related to the installation process.

## Execution

The Telecom Discrepancy Identification &amp; Reconciliation solution relies on CMDB Health/Compliance, which runs Certification Audits on selected tables and records in the CMDB. It operates independently of Discovery and can be run on-demand or scheduled.

For more information about CMDB Compliance, see [CMDB Compliance](https://www.servicenow.com/docs/access?context=c_Compliance&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) and [Certification audits](https://www.servicenow.com/docs/access?context=c_CertificationAudits&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Compliance** &gt; **Audits** &gt; **Service Operation CMDB Compliance Audit \(“cert\_audit” table\)**.

2.  Select **Run Audit**.

    ![run audit.](../images/telecom-run-audit.png)

    It executes various scripts and operations.


**Parent Topic:**[Telecom Discrepancy Identification and Reconciliation](../concept/telecom-reconciliation.md)

## Certification Audit Logics

Audit Results are created for each audit executed on records that matched the selection \(see matching conditions in Initial Certification Audit Run\).

The result's state can be certified or failed. A Follow-On Task is created for each ‘failed’ Audit Result record.

### Initial Certification Audit Run

Validating specific CMDB tables for anomalies.

The Service Operation CMDB Compliance Audit starts to run on the CI Relationship table \(cmdb\_rel\_ci\), but only on specific records with matching conditions as follows:

-   Parent AND child CI classes are supported classes, including extended tables as follows:

    slot \(cmdb\_ci\_container\_slot\), subslot \(cmdb\_ci\_container\_subslot\), card \(cmdb\_ci\_interface\_card\), interface \(cmdb\_ci\_ni\_interface\), telco equipment \(cmdb\_ci\_ni\_telco\_equipment\), IP switch \(cmdb\_ci\_ip\_switch\), and IP router \(cmdb\_ci\_ip\_router\).

    **Note:** These properties can be configured via sn\_tsom\_core.audit.\* system properties.

-   Parent OR child is created or updated by Discovery \(discovery\_source = SG-Altiplano, ServiceNow\).

    **Note:** This property can be configured in the sn\_tsom\_core.audit.discovery\_sources system property.

-   Parent AND child life-cycle Stage is Operational.
-   The CI Relationship Type is Contains::Contained By.

    **Note:** This property can be configured in the sn\_tsom\_core.audit.relationship\_types system property.


### Subsequent Certification Audit Runs

Follows the same logic as the Initial Certification Audit Run, but with the following additional matching selection criteria:

The timestamp in the Updated field in the CI Relationship table, or the timestamp in the Updated field of a Parent CI, or the timestamp in the Updated field of child CIs is later than the timestamp in the ‘Last run date’ field in the Service Operation CMDB Compliance Audit \(this means that there was a change since the last audit\).

