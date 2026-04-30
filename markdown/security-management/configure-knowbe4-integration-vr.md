---
title: Configure Knowbe4 integration
description: Gain immediate insights into your staff's vulnerability to phishing attacks by integrating with KnowBe4, a leading cybersecurity awareness training platform. Through KnowBe4 integration, identify trends and areas of improvement in your cybersecurity training programs, monitor overall phishing resilience and proactively strengthen your organization's security measures.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [ServiceNow, Knowbe4 integration, phishing integrations, how to configure Knowbe4 inetgration, cybersecurity awareness training]
breadcrumb: [Security Simulation and Training Integration for Security Operations, Cybersecurity Executive Dashboard, Security Operations]
---

# Configure Knowbe4 integration

Gain immediate insights into your staff's vulnerability to phishing attacks by integrating with KnowBe4, a leading cybersecurity awareness training platform. Through KnowBe4 integration, identify trends and areas of improvement in your cybersecurity training programs, monitor overall phishing resilience and proactively strengthen your organization's security measures.

## Before you begin

Role required: sn\_sec\_phish.admin and sn\_sec\_phish\_kb4.kb4\_admin

## Procedure

1.  Navigate to **All** &gt; **KnowBe4 Integration** &gt; **KnowBe4 Configurations**.

2.  Select **New**.

3.  On the form, fill in the details:

    |Field|Description|
    |-----|-----------|
    |Integration Instance|Name of the integration instance. Select the integration instance using the Lookup icon.|
    |Base URL|URL to integrate with KnowBe4.|
    |API Key|API key acquired from KnowBe4 account.|
    |Page|Page number from where simulations should be fetched.|
    |Page Size|Number of simulations that should be included.|

    1.  Select **New** if no integration instance is available.

    2.  On the form, fill in the details:

        |Field|Description|
        |-----|-----------|
        |Name|Name for the integration instance.|
        |Application|Name of the application \(KnowBe4 Integration for SecOps\).|
        |Integration|KnowBe4 is the default.|
        |Active|Default is activated \(selected\). If cleared, the instance isn’t active.|
        |Description|Short description of the integration instance.|

4.  Select **Submit**.

5.  Navigate to **All** &gt; **Security Simulation and Training** &gt; **Integrations**.

6.  Select Knowbe4 integration.

7.  Select **Execute Now** to execute and collect data from KnowBe4.


