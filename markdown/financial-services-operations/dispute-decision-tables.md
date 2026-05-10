---
title: Dispute decision tables
description: Decision tables in Dispute Management provide decision logic for card dispute processing.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Card Disputes, Data Models, Explore, Financial Services Operations \(FSO\)]
---

# Dispute decision tables

Decision tables in Dispute Management provide decision logic for card dispute processing.

The following table lists the decision tables used in Dispute Management.

**Note:** The rules shown here are provided as example rules. Review and configure to reflect your own processing policy.

<table id="table_u14_5q2_5cc"><thead><tr><th>

Decision table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Card dispute rules for internal policy 

</td><td>

Determines the appropriate financial action based on the details of a dispute case. The results can be: -   Immediate provisional credit
-   Immediate final credit
-   Deny
-   No credit

**Note:** You can extend the predefined rules based on your own policies.

</td></tr><tr><td>

Derive Dispute Category without Content Pack

</td><td>

Determines the chargeback dispute category based on the dispute category and dispute reason whenever a dispute content pack isn’t installed.

</td></tr><tr><td>

Derive Disputes Case Priority

</td><td>

Triages a dispute case based on the dispute category, transaction category, and SEC code \(for ACH disputes\).

</td></tr><tr><td>

Derive Intake Answers from Chargeback Reason Code and Messages

</td><td>

Determines answers to the following questions, based on the reason code:

-   What is this dispute due to?
-   What is incorrect about this transaction?

 The answer determines which questionnaire to render in the playbook.

</td></tr><tr><td>

Determine chargeback dispute reason code 

</td><td>

Determines the chargeback reason code for Visa disputes based on the case categorization and the responses to the following questions:-   What is incorrect about this transaction? 
-   This dispute is due to?

</td></tr><tr><td>

Determine Chargeback Subflow by Network ID

</td><td>

Determines which chargeback eligibility subflows run based on the network ID of the disputed transaction.

</td></tr><tr><td>

Determine dispute category 

</td><td>

Determines the Dispute Case category based on the responses to the following questions: -   Do you recognize the merchant and the purchase? 
-   Did you provide authorization for the transaction? 
-   What is the issue that you’re experiencing? 

</td></tr><tr><td>

Determine Dispute Category Options

</td><td>

Determines the dispute category options that are displayed in the dispute questionnaire \(based on the Network ID\).

</td></tr><tr><td>

Determine Dispute Reason Options

</td><td>

Determines the dispute reason options that are displayed in the dispute questionnaire \(based on the selected dispute category\).

</td></tr><tr><td>

Determine Dispute Transaction Outcome

</td><td>

Determines the outcome status of the transaction based on the chargeback category, dispute service, and representment/response/appeal status.

</td></tr><tr><td>

Determine Next Activity Status

</td><td>

Determines the next activity in the card dispute workflow.

</td></tr><tr><td>

Determine questionnaire table and view 

</td><td>

Used to determine the Dispute Case questionnaire based on persona, card network, and category.

</td></tr><tr><td>

Determine Mastercard chargeback dispute reason code message

</td><td>

Determines the chargeback reason code.

</td></tr><tr><td>

Determine Reason Code and Category Subflow by Network ID

</td><td>

Determines the reason code and category subflow based on the network ID of the disputed transaction.

</td></tr><tr><td>

Dispute Document Rules

</td><td>

Determines whether an ACH dispute requires a Written Statement of Unauthorized Debit \(WSUD\).

</td></tr></tbody>
</table>**Parent Topic:**[Card Disputes data model](../reference/dispute-data-model.md)

**Related topics**  


[Decision Tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/decision-tables/decision-table.md)

