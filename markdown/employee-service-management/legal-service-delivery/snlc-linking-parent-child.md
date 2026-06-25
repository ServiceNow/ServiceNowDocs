---
title: Linking parent-child contracts
description: Link a parent contract to a child contract to establish hierarchical relationships between contract requests and inherit fields from the parent contract request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/legal-service-delivery/snlc-linking-parent-child.html
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Linking parent-child contracts

Link a parent contract to a child contract to establish hierarchical relationships between contract requests and inherit fields from the parent contract request.

You can associate a contract request with a parent contract from the Related Contract Request tab. When linked, the **Parent contract** field in the contract request Details tab is automatically populated with the parent contract request number. Depending on configuration, child contracts can inherit fields from the parent contract. Additionally, the associated contract repository records for the parent and child contract requests are automatically linked.

To link a contract as a parent, the following conditions must be met:

-   The user must be assigned to the contract request, be a group manager, or a collaborator.
-   The contract request must be in one of the following states: Draft, Work in progress, Awaiting review, or Contract signed.

    **Note:** If the contract request is in Contract signed state, the parent contract request must be in Contract signed or Closed complete state.

-   The parent contract must not be in a Canceled state.
-   Only one parent contract can be selected while linking.
-   The parent contract must be a single contract type using own paper or third-party paper.

**Parent Topic:**[Use Contract Management Pro for Legal Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-service-delivery/snlc-use-sn-legal-cont-landing.md)

**Related topics**  


[Non-disclosure agreement requests]()

[Third-party contract review requests]()

[Contract amendments]()

[Internal review overview]()

[Signature workflow for a request]()

[Cancel a legal request]()

[View and download a signed contract document]()

[View contract requests]()

[Manage Contract Management Pro for Legal Service Delivery]()

[Link parent contract requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-link-parent-cmr.md)

[Link and inherit parent contract fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-link-inhrt-prnt-flds.md)

[Remove a linked contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-remove-linked-cntr.md)

[Configure field mapping for parent-child contract linking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncor-conf-parent-child.md)

