---
title: Integration accounts with Web Service Access set to false
description: Display the findings about the accounts that are authentication ServiceNow with the Web Service Access set to false under the Security findings in the Machine Identity Console.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/identity/integration-accounts-wsa-false.html
release: australia
product: Identity
classification: identity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security findings, Exploring Machine Identity Console, Machine Identity Console, Identity]
---

# Integration accounts with Web Service Access set to false

Display the findings about the accounts that are authentication ServiceNow with the Web Service Access set to false under the Security findings in the Machine Identity Console.

Integration accounts with Web Service Access set to false displays the accounts that are using API without the Web Service Access set to false.

**Note:**

-   Any changes made to the record displayed on this page are immediately updated in the list, risk score resulting from those changes will be reflected the following day.
-   Accounts that have the **Internal Integration User** field set to `true` in their `sys_user` record will not populate data in the Machine Identity Console.

\[Omitted image "mic-wsa-false-overview.png"\] Alt text: Accounts with WSA set to false

You can select the machine identity name to know more about the account and the recommendation to maintain a good security posture for the account.

\[Omitted image "mic-recommendation-was-false.png"\] Alt text: Recommendation for the accounts with WSA set to false

