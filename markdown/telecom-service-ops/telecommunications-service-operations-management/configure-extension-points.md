---
title: Customize scripted extension points
description: Customize how license expiration dates for Fortinet devices are stored on CIs by implementing scripted extension points.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/configure-extension-points.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2024-12-19"
reading_time_minutes: 1
keywords: [extension points scripted fortinet license]
breadcrumb: [Configure Fortinet SGC, Configure Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Customize scripted extension points

Customize how license expiration dates for Fortinet devices are stored on CIs by implementing scripted extension points.

## Before you begin

Service Graph Connector for Fortinet must be installed. For instructions, see [Configure a Fortinet SD-WAN Service Graph Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-fortinet-service-graph-connector.md).

Role required: tsom\_visibility\_admin

## About this task

By default, Fortinet SGC stores license expiration dates as separate CI key-value pairs for each device, using the naming convention `license_expiration_date_*SERVICE\_CODE*`. You can customize this behavior using scripted extension points to implement alternative storage logic, such as storing only the earliest expiration date across all devices.

## Procedure

1.  Navigate to **All** &gt; **System Scripted Extension Points** &gt; **Scripted Extension Points**.

2.  Search for Fortinet in the **Extension Points** search field.

3.  From the **API Name** search results list, select **sn\_gnc\_fortinet.FortinetCustomizedContractParsing**.

4.  Select the **Create implementation** related link.

5.  In the **Script** field, modify the `buildLicenseAttributes` function to return an array of `{key, value}` objects containing the CI key-value pairs you want to store.

    For example, to store only the earliest expiration date across all devices instead of one key-value pair per device, the script would need to loop through `contractItems`, find the minimum date value, and return it as a single object: `{ key: "license_expiration_date", value: "<earliest_date>" }`.\[Omitted image "contract-items-parsing.png"\] Alt text: Contract items parsing implementation interface

6.  Run your implementation before the default by setting the **Order** field to a value less than `100`.

    The default implementation has an order of 100; implementations with a lower order number execute first and take precedence.

7.  Select **Update**.


## Result

Your custom implementation is saved and active. The next time Fortinet SGCSGC discovers devices, your script runs first and stores the license key-value pairs you defined on the relevant CIs, overriding the default per-device key-value pairs behavior.

**Related topics**  


[Extension points](https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/extension-points.html)

[Create a scripted extension point](https://www.servicenow.com/docs/r/api-reference/web-services/create-scripted-ext-pt.html)

