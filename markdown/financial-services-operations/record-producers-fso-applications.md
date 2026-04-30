---
title: Record producers for Financial Services Operations applications
description: A record producer enables your users to submit banking requests from the Banking Service catalog and Consumer Service portal and stores the requested information as a record in the associated table.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Record producers, Configure, Financial Services Operations \(FSO\)]
---

# Record producers for Financial Services Operations applications

A record producer enables your users to submit banking requests from the Banking Service catalog and Consumer Service portal and stores the requested information as a record in the associated table.

The following table lists the record producers that are available with Financial Services Operations applications. The record producers are available in the Record Producer \[sc\_cat\_item\_producer\] table.

<table id="table_nsl_nfd_jmb"><thead><tr><th>

Application

</th><th>

Record producer

</th><th>

Associated Table name

</th></tr></thead><tbody><tr><td rowspan="4">

Financial Services Payment Operations

</td><td>

Beneficiary Claim Non-Receipt​

</td><td>

Payment Inquiry Case \[sn\_bom\_payment\_inquiry\]

</td></tr><tr><td>

Payment made In Error

</td><td>

Payment Inquiry Case \[sn\_bom\_payment\_inquiry\]

</td></tr><tr><td>

Internal Claim

</td><td>

Claim \[sn\_bom\_payment\_claim\]

</td></tr><tr><td>

Create Claim Case

</td><td>

Claim \[sn\_bom\_payment\_claim\]

</td></tr><tr><td rowspan="7">

Financial Services Card Operations

</td><td>

Apply for a new credit card**Note:** This record producer is available with the demo data. However, as an admin, you can use it to create credit card record producers for each of your credit card product models.

</td><td>

Credit Card Service \[sn\_bom\_credit\_card\_service\]

</td></tr><tr><td>

Increase Credit Limit Request

</td><td>

Credit Card Service \[sn\_bom\_credit\_card\_service\]

</td></tr><tr><td>

Temporary Increase Credit Limit Request

</td><td>

Credit Card Service \[sn\_bom\_credit\_card\_service\]

</td></tr><tr><td>

Decrease Credit Limit Request

</td><td>

Credit Card Service \[sn\_bom\_credit\_card\_service\]

</td></tr><tr><td>

Block Credit Card Request

</td><td>

Credit Card Service \[sn\_bom\_credit\_card\_service\]

</td></tr><tr><td>

Unblock Credit Card Request

</td><td>

Credit Card Service \[sn\_bom\_credit\_card\_service\]

</td></tr><tr><td>

Close Credit Card Request

</td><td>

Credit Card Service \[sn\_bom\_credit\_card\_service\]

</td></tr></tbody>
</table>