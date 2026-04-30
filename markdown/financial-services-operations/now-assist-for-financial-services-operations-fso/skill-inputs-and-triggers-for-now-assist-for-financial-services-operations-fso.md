---
title: Skill inputs for Now Assist for Financial Services Operations \(FSO\)
description: Review the inputs for each skill to see how a skill is used.
locale: en-US
release: xanadu
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
keywords: [generative AI for financial services operations skill inputs, generative AI for FSO skill inputs]
breadcrumb: [Configuring Now Assist for Financial Services Operations \(FSO\), Now Assist for Financial Services Operations \(FSO\), Financial Services Operations \(FSO\)]
---

# Skill inputs for Now Assist for Financial Services Operations \(FSO\)

Review the inputs for each skill to see how a skill is used.

## Overview

You can review the inputs for the available skills in Now Assist for FSO. These settings describe how a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate a case summary.

## Insurance claim summarization skill

The insurance claim summarization skill includes the inputs that identify the table and fields that are used to generate a case summary.

The data source contains the tables and fields that the skill relies on.

The following table lists the inputs for the insurance claim summarization skill.

<table id="table_h1h_hgq_mbc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

-   Claim Base \[sn\_bom\_claim\_base\]
-   Claim Participant-&gt;Case
-   Claim Incident-&gt;Case
-   Participant Role-&gt;Case

</td></tr><tr><td>

Input fields

</td><td>

Claim Base

 -   Incident description
-   Incident location
-   Incident date
-   Nature of loss
-   Stage
-   Assigned to
-   Insurance policy
-   Total claim amount

 Claim Participant-&gt;Case

 -   Name
-   Type

 Claim Incident-&gt;Case

 -   Involved entity
-   Description

 Participant Role-&gt;Case

 -   Role
-   Claim participant
-   Claim incident

</td></tr></tbody>
</table>## Banking dispute summarization skill

The banking dispute summarization skill includes the inputs that identify the table and fields that are used to generate a case summary.

The data source contains the tables and fields that the skill relies on.

The following table lists the inputs for the banking dispute summarization skill.

<table id="table_cdj_mkq_mbc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

-   Card Disputes Service Case \[sn\_bom\_credit\_card\_disputes\_service\]
-   Card Disputes Transaction-&gt;Parent
-   Card Disputes Task-&gt;Parent

</td></tr><tr><td>

Input fields

</td><td>

Card Disputes Service Case

 -   Short description
-   Created
-   Assigned to
-   Stage
-   Dispute amount
-   Card network
-   Category
-   Reason code
-   Consumer
-   Account
-   Service
-   Product

 Card Disputes Transaction-&gt;Parent

 -   Outcome
-   Financial transaction
-   Merchant name
-   Chargeback eligibility
-   Activity status
-   Payment status

 Card Disputes Task-&gt;Parent

 -   Pursue chargeback
-   Dispute service
-   State
-   Created
-   Merchant response

</td></tr></tbody>
</table>