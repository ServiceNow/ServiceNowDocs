---
title: Generate recommended actions in UI16 for a security incident with Now Assist for Security Incident Response
description: Automatically generate the next steps your analysts can take to help them close a security incident in the UI16 \(legacy\) view. The recommended steps are based on existing security incidents and knowledge articles.
locale: en-US
release: xanadu
product: Now Assist for Security Incident Response \(SIR\)
classification: now-assist-for-security-incident-response-sir
topic_type: task
last_updated: "2025-02-10"
reading_time_minutes: 1
breadcrumb: [Generate recommended actions for a security incident with Now Assist for Security Incident Response, Using Now Assist for Security Incident Response to close security incidents, Now Assist for Security Incident Response, Security Operations]
---

# Generate recommended actions in UI16 for a security incident with Now Assist for Security Incident Response

Automatically generate the next steps your analysts can take to help them close a security incident in the UI16 \(legacy\) view. The recommended steps are based on existing security incidents and knowledge articles.

## Before you begin

Generating recommended actions works for active security incidents in any states other than **Closed** or **Cancelled**.

The AI Search application must be enabled so that the Recommended Actions skill works for security incidents. To verify AI Search is enabled on your instance, navigate to **All** &gt; **AI Search** &gt; **AI Search Status**. Contact support if the page indicates AI Search is not enabled.

The recommended actions skill must be activated before you can see the **Recommended actions** button on a security incident.

Roles required: sn\_si.analyst, sn\_si.manager or sn\_si.basic

## Procedure

1.  In the legacy Core UI, navigate to **All** &gt; **Security Incident** &gt; **Incidents** and open a security incident that is assigned to you.

2.  Locate and select **Recommended actions** under the Short description field.

    The recommended actions are listed along with the reference links.

    The recommended actions remain cached for one hour. You can refresh them if you leave the page, log out, log back in, and return within one hour to the security incident.


