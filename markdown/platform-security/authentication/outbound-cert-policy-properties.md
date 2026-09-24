---
title: Outbound certificate policies system properties
description: System properties that control outbound certificate policy enforcement, and the global certificate validation properties that apply to domains without a policy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/outbound-cert-policy-properties.html
release: brazil
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 1
keywords: [outbound certificate policy, system properties, certificate validation, glide properties, reference]
breadcrumb: [Outbound certificate policies, Authentication, Access Management]
---

# Outbound certificate policies system properties

System properties that control outbound certificate policy enforcement, and the global certificate validation properties that apply to domains without a policy.

## Feature system properties

The following system properties control outbound certificate policy enforcement.

|Property|Default|Description|
|--------|-------|-----------|
|`com.glide.communications.httpclient.outbound_cert_policy.enabled`|false|Enables outbound certificate policy enforcement. When false, policy records have no effect and all domains use the global certificate validation properties.|
|`com.glide.communications.httpclient.outbound_cert_policy.debug`|false|Enables debug logging for outbound certificate policy processing.|
|`com.glide.communications.httpclient.outbound_cert_policy.max_entries`|100|The maximum number of resolved policies the instance retains for reuse across outbound connections.|

## Global certificate validation properties

The following global properties define the default certificate validation behavior. They apply to any domain that does not have an outbound certificate policy.

|Property|Default|Description|
|--------|-------|-----------|
|`com.glide.communications.httpclient.verify_hostname`|true|When true, validates that a certificate matches the target hostname for outbound connections.|
|`com.glide.communications.httpclient.verify_revoked_certificate`|true|When true, verifies that a certificate has not been revoked for outbound connections.|
|`com.glide.communications.trustmanager_trust_all`|false|When true, the instance trusts all certificates for outbound connections. Leave this property false in production.|

