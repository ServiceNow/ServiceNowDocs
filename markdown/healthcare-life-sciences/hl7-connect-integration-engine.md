---
title: Connect your integration engine to ServiceNow
description: Configure your integration engine to POST HL7 v2.x messages to the ServiceNow HL7 endpoint so that messages are received, logged, and acknowledged automatically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hl7-connect-integration-engine.html
release: australia
topic_type: task
last_updated: "2026-05-11"
reading_time_minutes: 1
keywords: [integration engine, HL7 endpoint, connect]
breadcrumb: [HL7 v2.x Integration, Healthcare Integrations, Healthcare and Life Sciences]
---

# Connect your integration engine to ServiceNow

Configure your integration engine to POST HL7 v2.x messages to the ServiceNow HL7 endpoint so that messages are received, logged, and acknowledged automatically.

## Before you begin

Role required: `sn_hl7_v2.admin`

You need the ServiceNow HL7 endpoint URL and credentials from your ServiceNow administrator. For endpoint URL, supported authentication methods, and request and response schema details, see the [HL7 Inbound API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/hl7-inbound-api.md) reference.

## About this task

The ServiceNow HL7 endpoint accepts HTTP POST requests containing raw HL7 v2.x messages in ER7 format. The endpoint returns a standard HL7 ACK response in the HTTP 200 response body for every message — your integration engine receives the ACK exactly as it would from any HL7-capable system. No custom configuration is required on the integration engine beyond the endpoint URL and credentials.

**For a detailed example of request and response, see the [HL7 Inbound API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/hl7-inbound-api.md) reference.**

## Procedure

1.  In your integration engine, create a new outbound HTTPS destination pointing to the ServiceNow HL7 endpoint URL.

    For the endpoint URL, see the [HL7 Inbound API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/hl7-inbound-api.md) reference.

2.  Set the HTTP method to **POST**.

3.  Set the `Content-Type` header to `x-application/hl7-v2+er7`.

    The endpoint accepts only pipe-delimited ER7 format. Any other `Content-Type` value is rejected.

    **Important:** ServiceNow enforces UTF-8 encoding. If your integration engine sets an encoding in the `Content-Type` header \(for example, `charset=ISO-8859-1`\), that value takes precedence over any encoding declared in MSH-18. Ensure your integration engine sends UTF-8 encoded messages.

4.  Configure authentication using one of the supported methods: Basic Auth, OAuth, or API key.

    For authentication configuration details, see the [HL7 Inbound API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/hl7-inbound-api.md) reference.

5.  Configure your integration engine to accept an HTTP 200 response with an HL7 ACK body as a successful acknowledgment.

    ServiceNow returns HTTP 200 for all application-level responses, including AE \(Application Error\) and AR \(Application Rejection\). Your integration engine must read the ACK code in the MSA segment of the response body to determine whether the message was accepted. Non-2xx status codes indicate transport failures \(authentication failure, server error\) only — these responses do not contain an HL7 ACK body.

6.  Send a test message from your integration engine and verify that an ACK\(AA\) response is returned and a new record appears in the ServiceNow HL7 message log.


