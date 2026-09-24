---
title: Employee consent for device remedial actions
description: The L1 IT Service Desk AI Specialist prompts employees to approve or decline device remedial actions in real time through incident activity stream.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/collect-emp-consent.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Use, L1 IT Service Desk AI Specialist, IT Service Management]
---

# Employee consent for device remedial actions

The L1 IT Service Desk AI Specialist prompts employees to approve or decline device remedial actions in real time through incident activity stream.

Some remedial actions require employee approval before the AI specialist can proceed. To decide what actions need consent, `sn_itsm_aia.consent_bypass_actions` sys property needs to be set. All the sys\_ids for the remedial actions that don't need a consent, are added in this sys property.

Once the sys property is set, the ZTSD is triggered and the DEX Remediation trigger AI agent checks the sys property to determine if consent is required. If the consent is required, the system triggers the employee engagement through the activity stream. The incident state changes to On hold-Awaiting caller until the employee responds or the timeout period expires. You can configure the time in sn\_itsm\_aia.engagement\_timeout\_minutes and if the user does not respond within the set time, the request is timed out. The default time is one day \(1440 minutes\) after which the request is timed out. Each consent exchange creates an engagement record. The event is logged to incident work notes. The employee can respond through the incident activity stream.

