---
title: Catalog Item Standards scope and examples
description: This reference describes the in-scope best practices that can be used for catalog item generation. It provides examples of in-scope and out-of-scope best practices and documents the rules for how best practices are applied.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-catalog/catalog-item-standards-scope-and-examples.html
release: australia
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2026-07-07"
reading_time_minutes: 2
breadcrumb: [Catalog item standards for catalog item generation, AI Authoring for Catalog Builder reference, AI Authoring for Catalog Builder, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Catalog Item Standards scope and examples

This reference describes the in-scope best practices that can be used for catalog item generation. It provides examples of in-scope and out-of-scope best practices and documents the rules for how best practices are applied.

## Scope of best practices

Best practices are honored only when they are within the scope of catalog generation capabilities. This means best practices apply only to what a user can create using the ServiceNow Otto conversational catalog item builder.

The following are examples of best practices that are within the scope of catalog generation and are honored by ServiceNow Otto.

<table id="table_vsp_wqd_vjc"><thead><tr><th>

Intent

</th><th>

Best practices

</th></tr></thead><tbody><tr><td>

Include help text for all mandatory fields

</td><td>

If a mandatory question does not have help text, highlight this as help text guides requesters on what is expected, reducing confusion and errors.

</td></tr><tr><td>

Avoid radio button questions with more than 20 choices

</td><td>

If a radio button \(single choice\) question has more than 10 to 15 choices, highlight this as a drop-down is cleaner for larger option sets and takes up less screen space.

</td></tr><tr><td>

Use clear question labels and avoid technical jargon

</td><td>

If a question label uses technical jargon, abbreviations, or acronyms that a typical requester may not understand, highlight this as plain-language labels are easier for everyone.

</td></tr></tbody>
</table>## Out-of-scope best practices examples

Best practices that require information not directly available to the LLM, or that depend on behavior beyond what's directly defined on the catalog item, aren't applied. This includes:

-   Role-based or permission-based restrictions on catalog authors
-   Runtime behavior or system configuration not defined on the catalog item itself

The following are examples of best practices that are outside the scope of catalog generation and aren't honored by ServiceNow Otto.

<table id="table_owq_3rd_vjc"><thead><tr><th>

Intent

</th><th>

Best practices

</th></tr></thead><tbody><tr><td>

Restrict lookup multiple-choice questions based on Catalog Builder Editor role

</td><td>

If the creator's role is Catalog Builder Editor, they must not be able to create a lookup multiple-choice question type. This restriction depends on role-based security rules not directly available to the LLM.

</td></tr><tr><td>

Add reference qualifiers for lookup questions with more than 1,000 choices

</td><td>

If a lookup question has more than 1,000 choices, add a reference qualifier to filter the options. This may require system configuration knowledge beyond catalog item properties.

</td></tr></tbody>
</table>## Rules for best practice application

The following rules define how ServiceNow Otto applies best practices:

-   Plain text requirement: ServiceNow Otto honors only best practices written in plain text in the article. Formatted text, images, and special markup are ignored.
-   Deviation: If there is a deviation, a catalog item is created, and then the user is prompted about the deviation.
-   Published version only: The LLM uses only the latest published version of the Catalog Best Practices article. Draft isn’t considered.

**Parent Topic:**[Catalog item standards for catalog item generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/guidance-for-catalog-item-creation.md)

**Related topics**  


[Catalog item standards for catalog item generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/guidance-for-catalog-item-creation.md)

