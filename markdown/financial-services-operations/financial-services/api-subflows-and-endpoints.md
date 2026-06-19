---
title: API Subflows and Endpoints
description: The application is built on four sequentially orchestrated subflows. Each maps to a specific Verifi REST endpoint and triggers at a defined point in the dispute workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/financial-services/api-subflows-and-endpoints.html
release: australia
product: Financial Services
classification: financial-services
topic_type: reference
last_updated: "2026-04-06"
reading_time_minutes: 1
breadcrumb: [Reference, Verifi, Integrate, Financial Services Operations \(FSO\)]
---

# API Subflows and Endpoints

The application is built on four sequentially orchestrated subflows. Each maps to a specific Verifi REST endpoint and triggers at a defined point in the dispute workflow.

<table id="table_vtx_fmw_v3c"><thead><tr><th>

Subflows

</th><th>

API Endpoint

</th><th>

Method

</th><th>

Outcome

</th></tr></thead><tbody><tr><td>

1. Merchant Eligibility Inquiry

</td><td>

POST /issuers/cases

 \{inquiryOnly: 1\}

</td><td>

POST

</td><td>

Runs automatically in the background when the issuer agent opens the "Review Participating Merchant Alerts" task. No UI action required.

</td></tr><tr><td>

2. Create Case

</td><td>

POST /issuers/cases

 \{inquiryOnly: 0\}

</td><td>

POST

</td><td>

Runs immediately after a successful eligibility response \(HTTP 200\), sequentially in the same background flow. Manual fallback UI action available if the backend API call fails.

</td></tr><tr><td>

3. Get Cases \(Poll\)

</td><td>

GET /issuers/cases?caseId=$\{case\_ids\}

</td><td>

GET

</td><td>

Polls on a configurable interval while the task is in "Awaiting External Info." Terminates when case status = EXPORTING or when the 72-hour SLA window lapses \(statusCode 910\).

</td></tr><tr><td>

4. Get Single Case

</td><td>

GET /issuers/cases/$\{case\_id\}

</td><td>

GET

</td><td>

Poll for status on a single case.

</td></tr><tr><td>

5. Update Case

</td><td>

PATCH /issuers/cases/\{caseId\}

</td><td>

PATCH

</td><td>

Runs once when EXPORTING status is received and the merchant response is stored. Sends \{"status": "CLOSED"\} as the mandatory issuer acknowledgment handshake. Case is excluded from further polling.

</td></tr></tbody>
</table>**Parent Topic:**[Financial Services Operations Integration with Verifi reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/financial-services/referring-financial-services-operations-integration-with-verifi-cdrn.md)

