---
title: Contract analysis playbook tool messages
description: Messages that the playbook tool returns to an external AI tool when it cannot resolve or return a playbook for a contract. Each message tells the fulfiller how to correct the request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cmpro-negotiation-tool-messages.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: reference
last_updated: "2026-08-18"
reading_time_minutes: 3
keywords: [Contract negotiation, Playbook tool messages, Error messages, reference]
breadcrumb: [Reference, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Contract analysis playbook tool messages

Messages that the playbook tool returns to an external AI tool when it cannot resolve or return a playbook for a contract. Each message tells the fulfiller how to correct the request.

## Playbook tool messages

The messages that the playbook tool can return, and the condition that triggers each message, are described in the following table.

|Condition|Message|
|---------|-------|
|The contract request number is not valid.|This contract request number is invalid. Check the number and try again.|
|You do not have access to the contract.|You do not have access to view this contract. Contact your administrator for access.|
|No contract request number is provided.|Enter a contract request number to proceed.|
|The contract request number or document revision is not found.|The contract request number or document revision was not found. Verify both and try again.|
|The document revision cannot be found.|The contract document revision could not be found. Verify you are working with the correct version.|
|The selected document revision is not the latest.|This document revision is outdated. Open the latest version to continue.|
|The contract request is in a state that does not allow contract analysis.|This action isn't available because the contract request is in an not in Work in Progress state.|
|The specified playbook name is not found.|The Contract Negotiation playbook was not found. Verify the playbook name and try again.|
|The contract type is not valid.|The contract type is invalid. Check the contract type and try again.|
|The contract request has more than one contract type.|Multiple contract types are associated with this contract request. Select one to continue.|
|Active playbooks exist for the contract type, but none match the contract request conditions.|No playbook matched this contract request's conditions. Select one of the available playbooks for this contract type to proceed.|

**Parent Topic:**[Contract Management Pro reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-ref.md)

**Related topics**  


[Components installed with Contract Management Pro]()

[Components installed with Contract Workspace]()

[Components installed with Analytics Pack for Contract Management Pro]()

[Contract request State and Contract document status in Contract Management Pro]()

[Signatory roles]()

[Clause Variation form]()

[Contract Configuration form]()

[Properties installed to configure expiry notifications]()

[Properties installed to configure contracts integrations]()

[Expiring Contracts Condition form fields]()

[Action assignment form]()

[UFX Add on Event mapping form]()

[Obligation form]()

[Obligation Management notifications]()

[Contract Analysis Playbook form]()

[Contract Management Pro glossary]()

[Contract Management solutions]()

