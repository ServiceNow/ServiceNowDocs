---
title: Amendment and renewal interaction messages
description: Reference of the messages shown when an amendment and a renewal interact on the same contract, by scenario, state, and placement.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/contract-management-pro/cncore-renewal-messages.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [Renewal messages, Interaction messages, Amendment and renewal]
breadcrumb: [Reference, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Amendment and renewal interaction messages

Reference of the messages shown when an amendment and a renewal interact on the same contract, by scenario, state, and placement.

The following messages appear as an amendment and a renewal interact on the same contract. Placeholders such as the request type and contract links are replaced with the relevant values at run time.

|Scenario|Trigger or state|Placement|Type|Message|
|--------|----------------|---------|----|-------|
|Amendment then renewal|A request is in progress on the contract.|Contract record|Info|&lt;request type&gt; request &lt;contract\_type\_link&gt; is in progress for this contract.|
|Amendment then renewal|A request is cancelled.|Contract record|Info|&lt;request type&gt; request &lt;contract\_type\_link&gt; was cancelled. No changes were applied to this contract.|
|Amendment then renewal|The amendment is signed or closed complete.|Contract record|Info|&lt;request type&gt; request &lt;contract\_type\_link&gt; is applied to this contract. View the Amendment field changes tab for details.|
|Amendment then renewal|The renewal is executed.|Contract record|Success|This contract has been renewed as \{CNTR\_number\_with\_link\}.|
|Renewal then amendment|An amendment is submitted while a renewed contract exists.|Submission dialog and amendment request|Warning|Renewed contract \{cntr002\} already exists \(effective \{startDate\}\). Review dates and terms for overlaps and update manually as required.|
|Renewal then amendment|An amendment is in progress after the renewal is complete.|Both contract records|Warning|&lt;request\_type&gt; request \{AMR\_req\_with\_link\} for the contract is in progress. Review dates and terms with the renewed contract and update manually as required.|
|Parallel|One request is submitted while the other is in progress.|Submission dialog|Warning|\{requestType\} request \{req\_with\_link\} is already in progress. Review dates and terms for overlaps and update manually as required.|
|Parallel|Both requests are in progress and the renewed contract is not yet created.|Amendment request, renewal request, and contract record|Warning|Amendment \{AMR\_req\_with\_link\} and renewal \{RNWL\_req\_with\_link\} are both in progress for \{cntr001\}. Check dates for overlaps between the amended and renewed contracts, and correct manually as required.|

**Note:** When one request completes while the other is still in progress, the parallel messages stop and the sequential messages for the completed scenario apply.

**Parent Topic:**[Contract Management Pro reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cncore-ref.md)

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

[Contract analysis playbook tool messages]()

[Contract request ticket page actions]()

[Default availability of out-of-the-box record producers]()

[Contract Management Pro glossary]()

[Contract Management solutions]()

