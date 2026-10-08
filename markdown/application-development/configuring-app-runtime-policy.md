---
title: Configuring Application Runtime Policy
description: Configure Application Runtime Policy to automatically approve generated policies, or to require review and manual approval.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/configuring-app-runtime-policy.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [configure]
breadcrumb: [Application Runtime Policy \(ARP\), Developing your application, Building applications]
---

# Configuring Application Runtime Policy

Configure Application Runtime Policy to automatically approve generated policies, or to require review and manual approval.

## Configuration overview

Application Runtime Policy \(ARP\) is free and available by default on all production and non-production instances. You don't have to activate a plugin.

When you begin developing an application, ARP is inactive by default. To enable automatic policy generation, you must set ARP to either tracking or enforcing mode from the custom application form.

-   **[Opt in to Application Runtime Policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/arp-opt-in.md)**  
Enable Application Runtime Policy for an application that's in development by setting the policy mode on the custom application form.
-   **[Application Runtime Policy modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/arp-modes.md)**  
When enabled, Application Runtime Policy operates in two possible modes: Tracking and Enforcing. Tracking mode automatically allows out-of-scope access attempts, while Enforcing mode automatically blocks out-of-scope access attempts until you review them.

**Parent Topic:**[Application Runtime Policy \(ARP\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/application-runtime-policy.md)

