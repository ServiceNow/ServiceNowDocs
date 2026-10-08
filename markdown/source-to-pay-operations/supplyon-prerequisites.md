---
title: SupplyOn integration prerequisites
description: Before configuring the SupplyOn integration, review the application dependencies, data requirements, and configuration sequence.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/source-to-pay-operations/supplyon-prerequisites.html
release: australia
topic_type: concept
last_updated: "2026-10-08"
reading_time_minutes: 2
breadcrumb: [Purchase Order Management integration with SupplyOn, Integrate with Purchase Order Management, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# SupplyOn integration prerequisites

Before configuring the SupplyOn integration, review the application dependencies, data requirements, and configuration sequence.

## Application and framework dependencies

-   Application: Activate the Purchase Order Integration with SupplyOn application \(scope `sn_supplyon_po`\).
-   S2P integration framework: The S2P integration framework \(tables prefixed `sn_spend_intg_`\) must be present. It provides the outbound staging tables, the integration-status life cycle, and the integration error tasks.
-   ERP integration framework: The ERP integration framework \(tables prefixed `sn_fin_` and `sn_fcms_intg_`\) must be present. It provides source configuration and subflow scheduling.

## Main data and configuration sequence

Before any purchase order can complete a round trip, the following configuration and primary data must exist on the ServiceNow instance and in SupplyOn. Complete these items in order.

1.  Connection and credential aliases for the target environment \(QAS or PRD\), with valid SupplyOn API Management \(APIM\) subscription keys. For more information, see [Configure the connection and credential aliases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/supplyon-configure-connection-aliases.md).
2.  ERP source and integration source routing records: An active `sn_fin_erp_source` paired with an `sn_fcms_intg_source` whose connection points at the SupplyOn Orders alias. See [Configure the SupplyOn source system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/supplyon-configure-source-system.md).
3.  Supplier primary records \(`sn_fin_supplier`\) that carry the ServiceNow supplier number \(the SUP... value\) in the number field. This value is the routing-triple supplier number.
4.  Legal entity to ERP source routing \(`sn_fin_legal_entity.erp_source`\) so that the Purchase Order Management flow stamps the SupplyOn ERP source onto each order outbound staging row.
5.  Routing-triple constants: The organization code and plant code, set as system properties. See [Configure the routing triple and payload properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/supplyon-configure-routing-triple.md).
6.  Supplier registration in SupplyOn for the buyer routing triple. The supplier self-registers when it receives its first order. In the SupplyOn base system, the registration invitation is valid for six days. If the supplier doesn't register within that time, SupplyOn returns an error.
7.  Async receiver endpoint registered in SupplyOn, plus the inbound service-account credential that SupplyOn uses to authenticate. For more information, see [Register the async receiver endpoint in SupplyOn](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/supplyon-register-receiver-endpoint.md).

**Note:** The ERP source record name does not affect routing. Outbound eligibility is determined by the connection-alias scope prefix \(`sn_supplyon_po`\), not by the record name, so you can name the ERP source to suit your landscape as long as it is wired to the SupplyOn Orders alias and the legal entity routes to it.

