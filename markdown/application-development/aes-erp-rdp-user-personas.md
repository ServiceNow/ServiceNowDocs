---
title: App Engine for ERP rapid deployment packs user personas
description: App Engine for ERP rapid deployment packs define four core personas, each with distinct permissions, workflows, and responsibilities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/aes-erp-rdp-user-personas.html
release: australia
topic_type: reference
last_updated: "2026-06-26"
reading_time_minutes: 1
keywords: [app, engine, erp, sap, rapid, deployment, pack, user, persona, type]
breadcrumb: [Reference, App Engine for ERP rapid deployment packs, Building low-code applications, Developing your application, Building applications]
---

# App Engine for ERP rapid deployment packs user personas

App Engine for ERP rapid deployment packs define four core personas, each with distinct permissions, workflows, and responsibilities.

<table id="table_hpz_zv3_sjc"><thead><tr><th>

Persona

</th><th>

Primary responsibility

</th><th>

Typical users

</th></tr></thead><tbody><tr><td>

Requestor

</td><td>

Create, update, deactivate, or bulk upload master data requests for assigned domains.

</td><td>

-   Salesperson requesting a customer record
-   Finance team member requesting a cost center
-   Materials planner requesting a material

</td></tr><tr><td>

Enricher

</td><td>

Add supplementary data before governance review.

</td><td>

-   Market intelligence analyst adding credit scores
-   Database administrator matching internal IDs

</td></tr><tr><td>

Governance user

</td><td>

Perform compliance and governance checks before approval.

</td><td>

-   Compliance officer
-   Internal auditor
-   Regulatory affairs manager

</td></tr><tr><td>

Approver

</td><td>

Review fully prepared requests across all packs and make the final business decision.

</td><td>

-   VP of Sales
-   CFO
-   VP of Finance
-   Manager authorized to sign off on new customers, materials, or financial transactions

</td></tr></tbody>
</table>## Persona assignment and permissions

Administrators assign personas based on role and domain responsibilities. Domain access is independent. You might be a requestor for the Customer domain but an enricher for the Cost Center domain. The enricher, governance, and approver personas typically don't have access to the Create New Request portal. They access only the requests that reach their workflow stage.

**Parent Topic:**[App Engine for ERP rapid deployment packs reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-reference.md)

