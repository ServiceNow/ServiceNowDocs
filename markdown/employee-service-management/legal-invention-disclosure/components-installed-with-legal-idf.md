---
title: Components installed with Legal Invention Disclosure
description: Several types of components are installed with activation of the Legal Invention Disclosure plugin, including tables and user role.
locale: en-US
release: zurich
product: Legal Invention Disclosure
classification: legal-invention-disclosure
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Legal Invention Disclosure, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Components installed with Legal Invention Disclosure

Several types of components are installed with activation of the Legal Invention Disclosure plugin, including tables and user role.

## Roles

<table id="table_sr3_55b_syb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Patent Config \[sn\_lg\_ip.patent\_config\]

</td><td>

Configuration access for working on requests and matters.

</td><td>

sn\_lg\_ops.legal\_user

</td></tr><tr><td>

Legal Fulfiller \[sn\_lg\_ip.patent\_fulfiller\]

</td><td>

Fulfiller access for working on assigned requests and matters.

</td><td>

-   sn\_lg\_ops.legal\_fulfiller
-   sn\_doc.reader

</td></tr></tbody>
</table>## Tables

|Table|Description|
|-----|-----------|
|Patent Repository \[sn\_lg\_ip\_patent\_repository\]|Contains the details of all patents filed for a legal matter.|
|Patent Rewards Per Country \[sn\_lg\_ip\_patent\_rewards\]|Contains the details of the rewards for different stages of patent filing based on the country of the inventor.|
|Patent Reward Caps \[sn\_lg\_ip\_patent\_reward\_caps\]|Contains the details of the maximum amount to be rewarded to inventora for individual stages of the application process.|
|Stage Rewards \[sn\_lg\_ip\_stage\_rewards\]|Contains the details of the amounts of rewards for individual stages of the application process for each country.|

**Parent Topic:**[Legal Invention Disclosure reference](../concept/legal-invention-disclosure-reference.md)

