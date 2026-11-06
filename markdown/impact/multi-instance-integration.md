---
title: Integrations across multiple instances
description: A stack with more than two instances needs an OAuth provider registry and an OAuth client registry for every instance in the stack.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/impact/multi-instance-integration.html
release: australia
topic_type: concept
last_updated: "2026-10-28"
reading_time_minutes: 2
breadcrumb: [Scan Engine integrations, Activate Scan Engine and review settings, Configuring Impact, Impact]
---

# Integrations across multiple instances

A stack with more than two instances needs an OAuth provider registry and an OAuth client registry for every instance in the stack.

A development and production pair is the simplest integration stack. Most organizations run more non-production instances, such as development, QA, and test. In that case, every instance in the stack needs an OAuth provider registry and an OAuth client registry for each instance, and you export those records to every instance.

## Stack model

|Instance role|Records required|
|-------------|----------------|
|Production|A My SN Instances record for itself, marked Production, and one for each non-production instance it communicates with.|
|Each non-production instance|A My SN Instances record for itself, marked Development or Test, and one for production.|
|Every instance in the stack|An integration user, and an OAuth provider registry and an OAuth client registry for each instance in the stack. Export both records to every instance. In a stack of development, test, and production, each instance has six OAuth registry records, one provider and one client for each instance.|

**Important:** Only one instance in the stack can be designated Production.

## Setup order

Complete the setup for the first development and production pair before you add more instances. Then repeat the non-production steps for each additional instance.

1.  Create the integration user on each instance, using [Create an integration user account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/task-create-integration-user.md).
2.  Register every instance in the stack, using [Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/register-your-instance.md).
3.  Set up OAuth for the first development and production pair, using [Configure the OAuth authentication method development instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-oauth-auth-method.md) and [Configure the OAuth authentication method production instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-oauth-auth-method-prod.md).
4.  For each additional non-production instance, create an OAuth provider registry and an OAuth client registry on that instance. Export both records, and import them into every other instance in the stack. Then create the My SN Instances record for that instance on production.
5.  Grant KMF access on each instance that receives imported records, using [Grant Key Management Framework access on an instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/complete-kmf-access.md).
6.  Validate every My SN Instances record on every instance, using [Validate your instance connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/validate-instance-connection.md).

**Parent Topic:**[Scan Engine integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/instance-integration-scan-engine.md)

