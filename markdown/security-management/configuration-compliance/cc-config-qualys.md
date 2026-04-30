---
title: Configure the PCRS parameters
description: Starting with v12.6.3 of Qualys Integration for Security Operations, you can use the Qualys PCRS Policy Host Integration and Qualys PCRS Test Results Integration for importing test results with new sets of Qualys APIs. These integrations need a gateway URL to fetch information from Qualys.
locale: en-US
release: zurich
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Qualys, Integrate, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Configure the PCRS parameters

Starting with v12.6.3 of Qualys Integration for Security Operations, you can use the Qualys PCRS Policy Host Integration and Qualys PCRS Test Results Integration for importing test results with new sets of Qualys APIs. These integrations need a gateway URL to fetch information from Qualys.

## Before you begin

Role required: admin

## About this task

When you install the Qualys Integration for Security Operations for Vulnerability Response, you can configure the **gateway\_url** and **posture\_api\_version parameters**for the new PCRS integrations in Configuration Compliance. For more information on how to find the gateway URL for your API URL, see [Identify your Qualys platform](https://www.qualys.com/platform-identification/).

The gateway URL must be added in your ServiceNow instance.

**Note:** Starting with v12.21.0 Qualys Integration for Security Operations and v30.3.0 of Unified Security Exposure Management, you can configure the `posture_api_version` integration instance parameter to select the API version for PCRS integrations.

## Procedure

1.  Navigate to **All** &gt; **Qualys Vulnerability Integration** &gt; **Administration** &gt; **Integration Instances**.

    **Note:** Ensure that the scope you are in is Qualys for Security Operations.

2.  Open the instance that is used by the PCRS integrations.

3.  On the Integration Instance Parameters tab, add the gateway url for **gateway\_url** configuration.

    **Note:** The Qualys PCRS Test Results Integration is dependent on the Qualys PCRS Policy Host Integration. So, if you backdate the integration Qualys PCRS Test Results, you might have to run them in the same order again.

4.  On the Integration Instance Parameters tab, locate the **posture\_api\_version** parameter and set the value to 2.0 or 5.0 as required.


