---
title: Manage opportunity records
description: Retrieve, update, create, and delete opportunity records and related CRM data from an MCP client using plain language.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/manage-opportunity-records.html
release: australia
topic_type: task
last_updated: "2026-07-07"
reading_time_minutes: 5
breadcrumb: [Use generative AI, Now Assist for SFA, Sales Customer Relationship Management]
---

# Manage opportunity records

Retrieve, update, create, and delete opportunity records and related CRM data from an MCP client using plain language.

## Before you begin

Role required: admin

## About this task

All changes go through the same server-side business rules, validation scripts, and access controls that apply on the standard form. Every create, update, or delete action requires explicit confirmation before the agent commits.

## Procedure

1.  Connect through your MCP client.

    For information on how to connect to an MCP server from an MCP client, refer [Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/connect-mcp-server-client.md)

2.  Type a natural language prompt for the operation you want to perform.

<table id="table_wl4_fq2_kjc"><thead><tr><th>

Operation

</th><th>

What to type

</th></tr></thead><tbody><tr><td>

Retrieve

</td><td>

Examples by data type:

 -   **Pipeline**

"Show me all my open opportunities" or "What's my pipeline split by stage?"

-   **Product catalog**

"Search the product catalog for enterprise storage solutions" or "What products are available in the networking category?"

-   **Opportunity detail**

"I'm getting on a call with &lt;company name&gt; — fetch the open opportunity details."

-   **Opportunity lines**

"Show me all line items on the &lt;company name&gt; opportunity" or "Fetch the products being sold in OPTY100001."

-   **Tasks — today**

"What tasks do I have today including overdue?"

-   **Tasks — overdue**

"Show me all my overdue tasks."

-   **Tasks — by opportunity**

"Show me all open tasks for the &lt;company name&gt; opportunity."

-   **Touchpoints**

"Show me all touchpoints logged against &lt;company name&gt; in the last month."

-   **Touchpoint — notes**

"Fetch my last touchpoint for the &lt;company name&gt; opportunity" or "Show me the description of the discovery call touchpoint on OPTY100001."

-   **Contacts**

"Fetch all the stakeholders for this opportunity" or "Who are my contacts at &lt;company name&gt;?"

-   **Competitors**

"Fetch all competitors for the &lt;company name&gt; opportunity" or "Who are the competitors on OPTY100001?"

-   **Accounts**

"Show me all accounts I own."

</td></tr><tr><td>

Update

</td><td>

Examples by field or entity:

 -   **Opportunity lines**

"Update the quantity of the Pro License on the &lt;company name&gt; deal to five."

-   **Stage**

"Move the &lt;company name&gt; Q3 deal to Proposal/Price Quote" or "Move OPTY100001 to the next stage."

-   **Forecast category**

"Change the forecast category on the &lt;company name&gt; deal to Commit."

-   **Close date**

"Push the close date for &lt;company name&gt; to end of next month." Relative expressions such as "Q3 end" or "next Friday" are supported. Close dates can't be set in the past.

-   **Deal size**

"Set OPTY100001 amount to 350K." Formatted inputs such as $350,000 and 0.35M are supported.

-   **Work notes**

"Add a note to &lt;company name&gt;: 'Budget confirmed, decision in 30 days.'" Notes are appended and never overwritten.

-   **Custom or default fields**

"Set next steps on &lt;company name&gt;: 'Send revised proposal by Friday'" or "Update loss reasons on OPTY100001."

-   **Multi-field \(up to five fields\)**

"Update &lt;company name&gt;: stage to Negotiation, close date to June 30, forecast to Commit."

-   **Owner**

"Reassign the &lt;company name&gt; deal to Alex Johnson."

-   **Contact role**

"Change Alex Smith's role on &lt;company name&gt; from Influencer to Decision Maker."

-   **Competitor details**

"Mark Salesforce as the incumbent on the &lt;company name&gt; opportunity" or "Set Oracle's incumbent status to false on OPTY100001."

"Update the product family for Salesforce on the &lt;company name&gt; deal to Sales Cloud."

"Set the product offering for Oracle on OPTY100001 to Fusion CRM."

-   **Task — close**

"Mark my &lt;company name&gt; follow-up task as complete."

-   **Task — notes**

"Add a note to my &lt;company name&gt; call task: 'Left voicemail, retry Thursday.'"

-   **Task — reassign**

"Reassign my &lt;company name&gt; follow-up task to Alex Johnson."

-   **Touchpoint — complete**

"Mark my &lt;company name&gt; touchpoint from yesterday as completed."

-   **Touchpoint — outcome**

"Set the outcome of my last &lt;company name&gt; call to Positive."

-   **Touchpoint — notes**

"Update the notes on the last &lt;company name&gt; call: 'Champion requested a revised proposal.'"

-   **Contact fields**

"Update Alex Smith's mobile to +1-555-0199" or "Change Alex Smith's title to Chief Procurement Officer."

</td></tr><tr><td>

Create

</td><td>

Examples by record type:

 -   **Opportunity**

"Create a new opportunity for &lt;company name&gt;, $200K, closing in June." The account must already exist; if it's not found, the agent asks you to clarify.

-   **Opportunity lines**

"Add the Enterprise Storage 10TB product to the &lt;company name&gt; opportunity" or "Add two units of the Pro License to OPTY100001."

-   **Opportunity competitor**

"Add Salesforce as a competitor on the &lt;company name&gt; deal" or "Add Oracle to the competitor list for OPTY100001 with product family CRM."

**Note:** The agent prevents duplicate competitor entries on the same opportunity.

-   **Opportunity contact with role**

"Add Jane Smith as the economic buyer on &lt;company name&gt;." If the contact doesn't exist, the agent asks whether to create one.

-   **Opportunity task**

"Create a follow-up task on &lt;company name&gt; for next Monday." Relative due dates such as "next Thursday" are supported. The task is assigned to you by default.

-   **Touchpoint — call or meeting**

"Log a 30-minute discovery call with Jane Smith at &lt;company name&gt; today."

-   **Touchpoint — notes**

"Add a note to my &lt;company name&gt; touchpoint from yesterday: 'Budget confirmed, decision expected in 30 days."

-   **Contact**

"Create a contact: John Doe, VP Sales at &lt;company name&gt;, john@abcd.com."

</td></tr><tr><td>

Delete

</td><td>

Supported operations:

 -   **Opportunity lines**

"Remove the Basic Support package from the &lt;company name&gt; opportunity."

-   **Opportunity competitor**

"Remove Salesforce from the &lt;company name&gt; competitor list" or "Delete Oracle as a competitor on OPTY100001."

-   **Opportunity associated contact**

"Deactivate Jane Smith from the &lt;company name&gt; opportunity" or "Disassociate John Doe from OPTY100001."

</td></tr></tbody>
</table>3.  Provide any additional information the agent asks for.

    **Note:**

    -   For create operations, the agent asks for missing mandatory fields one at a time.
    -   For update operations, it resolves ambiguous record references by asking you to select from a list.
    -   Field-type validations run before any change is committed; if a value is invalid, the agent returns an error and suggests a correction.
4.  For create, update, and delete operations: review the confirmation card and confirm to commit.

    **Note:** The confirmation card shows what will change before anything is saved or deleted. For update operations, it shows the old and new value for each field. Retrieve operations return results directly without a confirmation step.

    The agent performs the operation and returns the result. For create operations, it returns the record name and a link. For delete operations, it confirms the record was removed. If you don't have the required access, the agent returns a permission denied message.


