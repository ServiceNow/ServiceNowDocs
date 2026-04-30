---
title: Configuring dispute decision tables
description: Decision tables in Dispute Management provide decision logic for card dispute processing.
locale: en-US
release: yokohama
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Understanding Dispute Management, Dispute Management, Using banking applications, Financial Services Operations \(FSO\)]
---

# Configuring dispute decision tables

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

**Note:** Users can extend the out-of-the-box rules based on their own policies.

</td></tr><tr><td>

Determine chargeback dispute reason code 

</td><td>

Determines the chargeback reason code for Visa disputes based on the case categorization and the responses to the following questions:-   What is incorrect about this transaction? 
-   This dispute is due to?

</td></tr><tr><td>

Determine Mastercard chargeback dispute reason code message

</td><td>

Determines the chargeback reason code.

</td></tr><tr><td>

Determine chargeback subflow by card network

</td><td>

Determines whether to update the chargeback dispute reason code.

</td></tr><tr><td>

Determine dispute category 

</td><td>

Determines the Dispute Case category based on the responses to the following questions: -   Do you recognize the merchant and the purchase? 
-   Did you provide authorization for the transaction? 
-   What is the issue that you are experiencing? 

</td></tr><tr><td>

Determine questionnaire table and view 

</td><td>

Used to determine the Dispute Case questionnaire based on Persona, Card network and Category .

</td></tr><tr><td>

Reg E resolution days 

</td><td>

Determines the Reg E resolution days for a case. The default duration is set to 45 days.

</td></tr></tbody>
</table>**Parent Topic:**[Understanding Dispute Management](../../fso-deposit-operations/concept/disputes-overview.md)

**Related topics**  


[Decision Tables](https://www.servicenow.com/docs/access?context=decision-table&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)

