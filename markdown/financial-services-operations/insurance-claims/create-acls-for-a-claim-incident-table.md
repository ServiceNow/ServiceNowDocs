---
title: Create an access control list for a claim incident table
description: Create an access control list \(ACL\) for a claim incident table by using the Insurance claims application. By creating an ACL, you ensure that users with specific roles can interact with tables for particular claim incidents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/financial-services-operations/insurance-claims/create-acls-for-a-claim-incident-table.html
release: zurich
product: Insurance Claims
classification: insurance-claims
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Claim incidents, Configure, Insurance claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Create an access control list for a claim incident table

Create an access control list \(ACL\) for a claim incident table by using the Insurance claims application. By creating an ACL, you ensure that users with specific roles can interact with tables for particular claim incidents.

## Before you begin

Set the application scope of your instance to **Insurance Claims Core**.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Search for and open the claim incident table.

3.  Elevate your role to security\_admin.

4.  In the Access Controls related list, select **New**.

5.  Add the reader and writer roles to the Requires role list.

    Refer to the existing ACLs in the Trip Incident \[sn\_ins\_claim\_trip\] table as an example.


## What to do next

Grant Insurance claims roles access to the claim incident table so that they can read and write entries during the claim creation process. For more information, see [Grant Insurance claims roles access to a claim incident table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/insurance-claims/update-insurance-claim-roles-for-a-claim-incident-table.md).

