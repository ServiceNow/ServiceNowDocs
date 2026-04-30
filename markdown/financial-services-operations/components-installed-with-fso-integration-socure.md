---
title: Components installed with the Financial Services Operations Integration with Socure
description: Several types of components are installed with activation of the Financial Services Operations Integration with Socure \(com.sn\_fso\_intg\_socure\) plugin, including tables.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integrating with Socure, Integrating with third-party applications, Integrating applications, Financial Services Operations \(FSO\)]
---

# Components installed with the Financial Services Operations Integration with Socure

Several types of components are installed with activation of the Financial Services Operations Integration with Socure \(com.sn\_fso\_intg\_socure\) plugin, including tables.

## Plugins installed

These plugins are installed with the Financial Services Operations Integration with Socure application \(com.sn\_fso\_intg\_socure\) plugin:

|Plugin|Description|
|------|-----------|
|Financial Services Know Your Customer \(com.sn\_bom\_kyc\)|This application is automatically installed when you install any of the following Financial Services Know Your Customer \(KYC\) applications. Financial Services Know Your Customer manages the KYC tasks that are used in workflows across Financial Services Operations applications.|
|Socure Spoke \(com.sn\_socure\_spoke\)|This application provides a list of actions to help companies perform required due diligent activities for onboarding new customers.|

## Roles

There are multiple roles installed for the KYC process to complete. The roles installed with Financial Services Business Lifecycle, Financial Services Client Lifecycle, and Financial Services Know Your Customer applications work asynchronously to complete all KYC tasks.

-   For a business client: sn\_bom\_clo\_b2b.admin, sn\_bom\_clo\_b2b.agent\_connector, sn\_bom\_clo\_b2b.contact\_lifecycle\_agent, sn\_bom\_clo\_b2b.manager, sn\_bom\_kyc.b2b\_account\_agent, sn\_bom\_kyc.b2b\_contact\_agent.
-   For a personal client: sn\_bom\_clo\_b2c.admin, sn\_bom\_clo\_b2c.manager or sn\_bom\_clo\_b2c.agent, sn\_bom\_kyc.admin, sn\_bom\_kyc.b2c\_account\_agent, or sn\_bom\_kyc.b2c\_contact\_agent

## Tables installed

<table><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Socure Score\[sn\_bom\_kyc\_socure\]

</td><td>

Stores Financial Services Know Your Customer Socure scores.

</td></tr><tr><td>

Address Risk\[sn\_bom\_kyc\_socure\_address\_risk\]

</td><td>

Stores Financial Services Know Your Customer address risk scores. This table extends the \[Socure Score\] table.

</td></tr><tr><td>

Email Risk\[sn\_bom\_kyc\_socure\_email\_risk\]

</td><td>

Stores Financial Services Know Your Customer email risk scores. This table extends the \[Socure Score\] table.

</td></tr><tr><td>

Customer Score\[sn\_bom\_kyc\_socure\_kyc\]

</td><td>

Stores Financial Services Know Your Customer customer scores. This table extends the \[Socure Score\] table.

</td></tr><tr><td>

Phone Risk\[sn\_bom\_kyc\_socure\_phone\_risk\]

</td><td>

Stores Financial Services Know Your Customer phone risk scores. This table extends the \[Socure Score\] table.

</td></tr><tr><td>

Reason Code\[sn\_bom\_kyc\_socure\_reason\_code\]

</td><td>

Stores Financial Services Know Your Customer reason codes.

</td></tr><tr><td>

Sanction\[sn\_bom\_kyc\_socure\_sanction\]

</td><td>

Stores Financial Services Know Your Customer sanctions list.

</td></tr><tr><td>

Watchlist\[sn\_bom\_kyc\_socure\_watch\_list\]

</td><td>

Stores Financial Services Know Your Customer watch list.

</td></tr><tr><td>

Fraud Scores\(sn\_bom\_kyc\_socure\_fraud\_response\)

</td><td>

Stores Financial Services Know Your Customer fraud scores.

</td></tr></tbody>
</table>