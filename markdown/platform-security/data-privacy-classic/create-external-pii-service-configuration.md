---
title: Create an external PII detection service configuration
description: create external PII detection service configuration to connect your custom detection service to ServiceNow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/data-privacy-classic/create-external-pii-service-configuration.html
release: brazil
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 1
breadcrumb: [Bring Your Own PII Detection Service, Data anonymization, Data privacy, Data Privacy, Platform Privacy]
---

# Create an external PII detection service configuration

create external PII detection service configuration to connect your custom detection service to ServiceNow.

## Before you begin

Before you begin, verify you have:

-   Access to the Data Privacy module
-   The endpoint URL for your external PII detection service
-   Authentication credentials \(API key, username/password, or OAuth tokens\) for your external service
-   Documentation of your external service's API contract \(request and response formats\)

Role required: data\_privacy\_processor and admin

## Procedure

1.  Navigate to **System Security** &gt; **Data Privacy** &gt; **Anonymization**.

2.  Select **External Anonymization Services**.

3.  Select **Create new service** to create an external service configuration.

    The creation form opens in a modal or page, depending on your deployment.

4.  Enter a descriptive **Service label** for your external service configuration.

    This will also be the **Service name**.

5.  Write a script to shape the request sent to your service, and map its response back into ServiceNow's format.

    The interface contains additional guidelines to follow.

6.  Configure the authentication details for the external service.

    Different external services require different authentication approaches. Consult your external service's documentation for the correct authentication details.

7.  Select **Active** if you want to enable the external service policy.

8.  Select Default to make the policy the automatic destination for all matching channel calls.

    **Note:** Only one external service policy can be set as default.

9.  Select **Test Connection** to initiate a test of the external service.

    Enter sample text for the test, then select **Run test**. The system sends a test request to the external service endpoint to verify connectivity and basic functionality.

10. Wait for the test to complete and review the test results.

    -   If the test is successful, you should see a confirmation message indicating the external service is accessible and responding correctly. Select **OK** to return to the configuration screen.
    -   If the test fails, review the error message to diagnose the issue \(connection timeout, authentication failure, invalid endpoint, and so on\). Select **Edit connection**
11. Once you have successfully tested the connection, select **Publish** to create the external service configuration.

    The new configuration is now available in the **External anonymization services** home page.


