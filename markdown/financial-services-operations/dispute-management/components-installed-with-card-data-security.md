---
title: Components installed with Card Data Security
description: Several types of components are installed with the activation of Card Data Security.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/components-installed-with-card-data-security.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [components installed with card data security, card data security roles, sn\_data\_sec admin role, sn\_data\_sec flow executor role, sn\_data\_sec\_resource\_config, tokenizer resource configuration table, installed roles, installed tables, card data security activation, sn\_data\_sec]
breadcrumb: [Reference, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Components installed with Card Data Security

Several types of components are installed with the activation of Card Data Security.

## Roles installed

<table id="table_wkr_xgm_rfc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Admin \[sn\_data\_sec.admin\]

</td><td>

This role gives access to the Tokenizer Resource Configuration table and admin privileges.

</td><td>

\(none\)

</td></tr><tr><td>

Flow executor \[sn\_data\_sec.flow\_executor\]

</td><td>

This role allows the execution of all subflows associated with the Card Data Security application.

</td><td>

-   script\_include\_admin
-   web\_service\_admin
-   sn\_data\_sec.admin
-   connection\_admin

</td></tr></tbody>
</table>## Tables installed

|Table|Description|
|-----|-----------|
|Tokenizer Resource Configuration \[sn\_data\_sec\_resource\_config\]|Stores information for each endpoint that sends and receives tokenized data.|

**Parent Topic:**[Card Data Security Reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/card-data-security-reference.md)

