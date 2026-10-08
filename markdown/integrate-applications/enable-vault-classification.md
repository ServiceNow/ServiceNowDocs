---
title: Enable Vault classification for a metadata collector
description: Enable a metadata collector to classify harvested columns using ServiceNow Vault.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/enable-vault-classification.html
release: brazil
topic_type: task
last_updated: "2026-09-28"
reading_time_minutes: 1
keywords: [Vault classification, sensitive data classification, metadata collector, Connect Hub, Workflow Data Fabric]
breadcrumb: [Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Enable Vault classification for a metadata collector

Enable a metadata collector to classify harvested columns using ServiceNow Vault.

## Before you begin

-   The metadata collector is created and saved. This option is available only from the connection details of a saved collector.
-   An active entitlement to ServiceNow Vault is required. If the entitlement isn't present, the **Enable vault classification** toggle is disabled.

Role required: connection-admin

## About this task

The following metadata collector types support Vault classification: Snowflake, Amazon Redshift, Databricks, Oracle, PostgreSQL, Teradata, MySQL, Microsoft SQL Server, and SAP HANA.

ServiceNow Vault uses Data Classification to organize data into data classes, such as Personally Identifiable Information \(PII\), so it can be governed at the class level. Enabling this option extends Data Classification to the columns that a collector harvests from an external database. For more information, see [Data Classification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/data-classification.md).

To identify the type of data in a column, the metadata collector reads a small sample of values from each harvested column in the source database. The collector sends the sample over an encrypted \(HTTPS\) connection to the Vault Discovery service on your ServiceNow instance. Vault scans the sample for sensitive data patterns, such as email addresses or Social Security numbers, and returns the classification result. Sample values aren't stored. Neither the Data Catalog nor Vault persists them. Only the resulting classification labels are saved and displayed in the Data Catalog.

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **** &gt; **Workflow Data Fabric Home**.

2.  Select the Connect Hub icon in the left sidebar.

3.  Select **Connectors**.

4.  Select **Metadata collector**.

5.  Select a saved collector to open its connection details.

6.  Select the **Classification** tab.

7.  Enable the **Enable vault classification** toggle and complete the form.

    **Note:** An active entitlement to ServiceNow Vault is required. If the entitlement isn't present, the Enable vault classification toggle is disabled.

    |Field|Description|
    |-----|-----------|
    |Username|Username for the ServiceNow instance.|
    |Password|Password for the user.|

8.  Select **Save**.


## Result

Vault classification is applied to columns the collector harvests. When the **Enable vault classification** toggle is cleared, columns aren't classified.

**Parent Topic:**[Configuring metadata collectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/configure-metadata-collectors-dc.md)

