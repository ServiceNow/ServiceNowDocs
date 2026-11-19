---
title: Verify inbound mTLS support activation for your instance
description: Check whether inbound mTLS support is activated for your ServiceNow AI Platform instance. You need this feature activated to run crawls for external content connectors.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/verify-adcv2-inbound-mtls-enabled.html
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-11-16"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Install, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Verify inbound mTLS support activation for your instance

Check whether inbound mTLS support is activated for your ServiceNow AI Platform® instance. You need this feature activated to run crawls for external content connectors.

## Before you begin

Role required: none

## About this task

To run crawls for external content connectors, your ServiceNow AI Platform instance must have inbound mTLS support activated. You can check the activation status for this feature on your instance from a web browser or the curl command-line tool.

If inbound mTLS support isn't activated on your instance, you can create a Customer Service and Support case to request its activation.

## Procedure

1.  In a web browser, navigate to the `https://<instance-name>.service-now.com/adcv2/supports_tls` status page, where `<instance-name>` is the name of your ServiceNow AI Platform instance.

    You can also access this status page using the curl command-line tool, replacing `<instance-name>` with the name of your ServiceNow AI Platform instance:

    ```
    curl -k "https://<instance-name>.service-now.com/adcv2/supports_tls"
    ```

2.  Check the response from the `adcv2/supports_tls` request.


## What to do next

If the response from the `adcv2/supports_tls` request is `true`, inbound mTLS support is activated on your instance. You don't need to do anything else.

If the response from the `adcv2/supports_tls` request is anything other than `true`, inbound mTLS support isn't activated on your instance. Create a Customer Service and Support case at [https://support.servicenow.com/now?draw=case](https://support.servicenow.com/now?draw=case) to request activation of inbound mTLS support on your instance.

**Parent Topic:**[Install External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/install-ext-cont-connectors.md)

