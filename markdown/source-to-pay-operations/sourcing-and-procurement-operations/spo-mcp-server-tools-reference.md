---
title: SPO MCP Server tools
description: Tools available in the SPO MCP Server, their internal names, and what each tools does.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/spo-mcp-server-tools-reference.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-08-25"
reading_time_minutes: 1
keywords: [SPO MCP Server, MCP tools, procurement tools]
breadcrumb: [Activate SPO MCP Server, Use SPO MCP Server, ServiceNow Otto for SPO, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# SPO MCP Server tools

Tools available in the SPO MCP Server, their internal names, and what each tools does.

<table id="table_hyj_kzb_jkc"><thead><tr><th>

Tool label

</th><th>

Tool name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Describe Intake Requirements

</td><td>

sn\_spend\_gen\_ai.spo\_describe\_intake\_requirements

</td><td>

Returns the required intake fields and submission instructions for a selected product or catalog item.

 This tool applies after the user selects an item from `spo_search_catalog_offerings`. It collects the required information, then presents a prefilled submission link for the user to review and submit.

</td></tr><tr><td>

Initialize Procurement Session

</td><td>

sn\_spend\_gen\_ai.spo\_initialize\_procurement\_session

</td><td>

Returns the user's profile, relevant knowledge base articles, suppliers, and approval requirements at the start of a procurement conversation.

 When the user's opening question is provided, the tool returns relevant suggestions. Without it, the tool returns profile data only. `spo_search_catalog_offerings` is the next tool to use after the user's purchase intent is clear.

</td></tr><tr><td>

Query Procurement Records

</td><td>

sn\_spend\_gen\_ai.spo\_query\_procurement\_detail

</td><td>

Finds and returns details on purchase requisitions, purchase orders, sourcing requests, and related tasks. Supports search by description or look up by record number.

</td></tr><tr><td>

Search Catalog Offerings

</td><td>

sn\_spend\_gen\_ai.search\_catalog\_offerings

</td><td>

Finds supplier products and catalog intake forms matching the user's purchase intent. After the user selects an item, `spo_describe_intake_requirements` applies to that selection.

</td></tr><tr><td>

SPO Execute Procurement Task Action

</td><td>

sn\_spend\_gen\_ai.spo\_execute\_procurement\_task\_action

</td><td>

Acts on procurement tasks such as approving, rejecting, or confirming receipt. Explicit user confirmation is required before the action proceeds.

</td></tr></tbody>
</table>