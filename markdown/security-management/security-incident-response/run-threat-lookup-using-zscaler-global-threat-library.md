---
title: Run a threat lookup by using the Zscaler global threat library
description: Run a threat lookup on an observable by using the Zscaler Internet Access product’s global threat library. Zscaler supports lookups against observables type IPs, URLs, and domains.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security Incident Response integration with Zscaler, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Run a threat lookup by using the Zscaler global threat library

Run a threat lookup on an observable by using the Zscaler Internet Access product’s global threat library. Zscaler supports lookups against observables type IPs, URLs, and domains.

## Before you begin

Role required: sn\_si.admin

## About this task

You can perform threat intelligence lookups on one or more observables to determine whether they are associated with known security threats. When an observable is associated with a security incident for the first time, all the active threat lookup implementations in the ServiceNow AI Platform perform an auto-threat lookup. You can view the results against the Threat Look Up Results related list.

By default, the configuration with the least order is picked to perform the threat lookup against Zscaler Internet Access product's global threat library. You can also perform the threat lookup manually.

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Incidents** &gt; **Show All Incidents**.

2.  Select the security incident that you want to run the threat lookup on.

3.  Click **Show All Related Lists** and the **Associated Observables** tab.

4.  Select the observable and then from the Actions menu, click **Run Threat Lookup**.

    In this example, you see how to select a security incident and an observable, how to run a threat lookup, and how to view the results in the Work notes.![Threat lookup that is triggered on an observable.](../image/zscaler-threat-lookup.gif)


## Result

After you initiate the threat lookup, you can view the Work notes to see the status of your submission.

