---
title: Organization tax details inbound staging table
description: The Organization tax details inbound \[sn\_fcms\_intg\_org\_tax\_detail\_inbound\] staging table temporarily stores important data about an organization's tax information before this data is sent to the Organization Tax Details \[sn\_fin\_org\_tax\_detail\] primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/slo-org-tax-details-inbound-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Inbound staging tables for Accounts Payable Operations, Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Organization tax details inbound staging table

The Organization tax details inbound \[sn\_fcms\_intg\_org\_tax\_detail\_inbound\] staging table temporarily stores important data about an organization's tax information before this data is sent to the Organization Tax Details \[sn\_fin\_org\_tax\_detail\] primary table.

## Organization tax details inbound staging table

The following table lists the mandatory fields for the Organization tax details inbound \[sn\_fcms\_intg\_org\_tax\_detail\_inbound\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|Organization|String|Name of the organization.|
|Tax ID|String|Tax ID of the organization.|

**Parent Topic:**[Inbound staging tables for Accounts Payable Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/inbound-staging-tables-for-apo.md)

**Related topics**  


[Invoice import inbound staging table]()

[Import error staging table]()

[Invoice line import inbound staging table]()

[Invoice payment detail import inbound table]()

[Invoice tax line staging table]()

[Invoice staging table]()

[Invoice line stage table]()

