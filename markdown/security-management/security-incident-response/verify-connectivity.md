---
title: Verify connectivity for LogRhythm
description: Verify your connection to the LogRhythm Client Console by sending curl requests to test the LogRhythm REST API. The verification process is optional.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Troubleshooting the LogRhythm integration, LogRhythm Overview, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Verify connectivity for LogRhythm

Verify your connection to the LogRhythm Client Console by sending curl requests to test the LogRhythm REST API. The verification process is optional.

## Before you begin

Role required: sn\_si.admin

## About this task

To verify the connection to the LogRhythm Client Console is working properly after you set up the LogRhythm REST APIs, send two curl requests from the computer hosting the MID Server you configured in [Install the plugin and configure LogRhythm](install-and-config-logrhythm.md).

The LogRhythm REST API uses WSSE for authentication, which requires some outside scripting to work with Curl and Postman.

The LogRhythm REST API uses a token for authentication, so you can make the actual validation call that the integration uses. The “0” at the end of the URL is a LogRhythm Alarm ID. The LogRhythm REST API with a default configuration requires port 8501. This port number should be included in the URL that you plan to use for the test.

## Procedure

1.  Update the URL **&lt;LogRhythm REST url&gt;** and token **&lt;api token&gt;** in the following curl request and send it to validate the LogRhythm REST API: `curl -k -i -v --trace-time -o /dev/null -H "Content-Type: text/json" -H "Authorization: Bearer <api token>" "https://<cache drilldown url>/lr-drilldown-cache-api/drilldown/0"`

    For a successful connection to the LogRhythm REST API, you should receive an HTTP 404, but the response body contains `Alarm ID: 0 not found`.


**Parent Topic:**[Troubleshooting the LogRhythm integration](../concept/troubleshooting-logrhythm-integration.md)

