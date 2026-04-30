---
title: Managing the Threat Lookup Reputation Calculator
description: You can use the Threat Lookup Finding Calculator to calculate the observable findings based on the responses received from threat lookup vendor.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Administration, Threat Intelligence Security Center, Security Operations]
---

# Managing the Threat Lookup Reputation Calculator

You can use the Threat Lookup Finding Calculator to calculate the observable findings based on the responses received from threat lookup vendor.

You can create a Threat Lookup Finding Calculator for your integration and use a script to determine how you want to identify the various observable findings. The Threat Lookup Finding Calculator includes a sample script that comes with the base system, which you can use to identify the observable findings or you can modify this script according to your requirements.

For third-party integrations that provide the computed results, the Threat Lookup Finding Calculator maps the results to supported findings in the base system.

## Rollup Threat Lookup Results

When you have multiple threat lookup results for an observable from the various integration vendors, then the recent threat lookup results from all the vendors are considered, and the overall observable findings are marked as follows:

|Latest Observable Finding|Overall Observable Finding|
|-------------------------|--------------------------|
|Malicious|If one of the integration vendors reports the observable as Malicious, then the overall observable finding is marked as Malicious.|
|Suspicious|If none of the integration vendors report the observable as Malicious, one of them reports it as Suspicious, and then the overall observable finding is marked as Suspicious.|
|Clean|If all the integration vendors report the observable as Clean, then the overall observable finding is marked as Clean.|
|Unknown|If none of the integration vendors report the observable as Malicious or Suspicious and one of them report it as Unknown, then the overall observable finding is marked as Unknown.|

## View Threat Lookup Reputation Calculators

You can view the Threat Lookup Finding Calculator to determine how reputation of observable is calculated based on response from specific threat lookup vendor.

Role required: sn\_sec\_tisc.admin

To view the Threat Lookup Reputation Calculator, perform the following steps:

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Administration**.
2.  Select the **Threat Lookup Reputation Calculator** section.

    You can view the list of Threat Lookup Reputation Calculators.

3.  Click on the required Threat Lookup Reputation Calculator to view the details of the calculator.

    ![View Threat Lookup Reputation Calculators](../image/enrich-view-threat-calculator.png)


## Create Threat Lookup Reputation Calculator

Role required: sn\_sec\_tisc.admin

**Note:** Only one threat lookup calculator can be active at any point of time per Threat lookup vendor.

To create a Threat Lookup Reputation Calculator, perform the following steps:

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Administration**.
2.  Select the **Threat Lookup Reputation Calculator** section.

    You can view the list of Threat Lookup Reputation Calculators.

3.  To create a Threat Lookup Reputation Calculator, click **New**.

    ![Create aThreat Lookup Reputation Calculator](../image/enrich-create-threat-calculator.png)

4.  On the form, fill the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the Threat Lookup Reputation Calculator.|
    |Active|Threat Lookup calculation runs only if Active option is selected.|
    |Threat Lookup Vendor|Name of the Threat Lookup vendor. For example, `CrowdStrike Falcon Intelligence`.|
    |Reputation Script|Script editor to determine how you want to identify the various observable findings. Every threat lookup integration comes with a base script for calculating threat lookup reputation.|

5.  Click **Save**.

