---
title: Customize scripted extension points
description: Customize specific parts of the Fortinet connector's behavior by implementing scripted extension points.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/configure-extension-points.html
release: brazil
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [extension points scripted fortinet license]
breadcrumb: [Configure Fortinet SGC, Configure Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Customize scripted extension points

Customize specific parts of the Fortinet connector's behavior by implementing scripted extension points.

## Before you begin

Service Graph Connector for Fortinet must be installed. For instructions, see [Configure a Fortinet SD-WAN Service Graph Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-fortinet-service-graph-connector.md).

Role required: tsom\_visibility\_admin

## About this task

The Service Graph Connector for Fortinet exposes nine scripted extension points. Each extension point controls a specific part of the connector's behavior, such as request payloads, ADOM filtering, or how a CIs Life Cycle Stage Status is set. Every extension point follows the same pattern: an extension point record defines the contract \(the functions your implementation must provide\), and an extension instance record wires your implementation to that extension point. See [Fortinet extension points reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/fortinet-extension-points-reference.md) to find the extension point that controls the behavior you want to change.

The following steps apply to any of the nine extension points. This example customizes `FortinetCustomizedContractParsing` to change how license expiration dates are stored on CIs.

## Procedure

1.  Navigate to **All** &gt; **System Scripted Extension Points** &gt; **Scripted Extension Points**.

2.  Search for Fortinet in the **Extension Points** search field.

3.  From the **API Name** search results list, select the extension point you want to customize, for example **sn\_sgc\_fortinet.FortinetCustomizedContractParsing**.

4.  Select the **Create implementation** related link.

5.  In the **Script** field, implement the function stubs for the extension point's contract.

    The docstring on each stub describes what your function must return.

6.  Run your implementation before the default by setting the **Order** field to a value less than `100`.

    The default implementation has an order of 100; implementations with a lower order number execute first and take precedence.

7.  Select **Update**.


## Result

Your custom implementation is saved and active. The connector picks it up automatically on its next scheduled run — no restart or cache clear needed.

## Example: Customize license expiration date storage

By default, Fortinet SGC stores license expiration dates as separate CI key-value pairs for each device, using the naming convention `license_expiration_date_*SERVICE\_CODE*`. This example customizes `FortinetCustomizedContractParsing` to store only the earliest expiration date across all devices instead.

In the **Script** field, modify the `buildLicenseAttributes` function to return an array of `{key, value}` objects containing the CI key-value pairs you need to store. Loop through `contractItems` to find the minimum date value, then return it as a single object: `{ key: "license_expiration_date", value: "<earliest_date>" }`.\[Omitted image "contract-items-parsing.png"\] Alt text: Contract items parsing implementation interface

The next time Fortinet SGC discovers devices, your script runs first. It stores the license key-value pairs you defined on the relevant CIs, overriding the default per-device key-value pairs behavior.

**Related topics**  


[Fortinet extension points reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/fortinet-extension-points-reference.md)

[Extension points](https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/extension-points.html)

[Create a scripted extension point](https://www.servicenow.com/docs/r/api-reference/web-services/create-scripted-ext-pt.html)

