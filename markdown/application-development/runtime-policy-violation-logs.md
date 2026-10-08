---
title: Violation Logs
description: The Runtime Policy Violation Log records network, record, and scripting violations encountered while exercising application functions, giving you a consolidated view of cross-origin or out-of-scope access attempts. The ARL Violation Log records violations of event handlers, scheduled jobs, and API and UI transactions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/runtime-policy-violation-logs.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Explore, Application Runtime Policy \(ARP\), Developing your application, Building applications]
---

# Violation Logs

The Runtime Policy Violation Log records network, record, and scripting violations encountered while exercising application functions, giving you a consolidated view of cross-origin or out-of-scope access attempts. The ARL Violation Log records violations of event handlers, scheduled jobs, and API and UI transactions.

## Runtime Policy Violation Log

When Application Runtime Policy \(ARP\) is enabled in Tracking or Enforcing mode, the first instance of every network, record, and scripting policy violation is recorded in the Runtime Policy Violation Log. You can review the log by navigating to **All** &gt; **System Policy** &gt; **Application Runtime Policy** &gt; **Runtime Policy Violation Log**. If access attempts that you want to allow are blocked while developing an application, you can use the log to find the policy record that needs to be reviewed and approved.

## ARL Violation Log

After the application is installed, platform resource usage violations are recorded at runtime. The ARL Violation Log includes violation records related to API and UI transactions, event handlers, and scheduled jobs. Administrators can review the log by navigating to **All** &gt; **System Policy** &gt; **Application Runtime Policy** &gt; **ARL Violation Log** to determine whether to manually create policies on their instance for any violations.

