---
title: Catalog request states
description: States and resolution codes for incidents and catalog requests that the L1 IT Service Desk AI Specialist drafts or submits.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/catalog-request-states-l1-sd-ai-spec.html
release: brazil
topic_type: reference
last_updated: "2026-09-25"
reading_time_minutes: 1
keywords: [state, resolution code, catalog request, incident]
breadcrumb: [Reference, L1 IT Service Desk AI Specialist, IT Service Management]
---

# Catalog request states

States and resolution codes for incidents and catalog requests that the L1 IT Service Desk AI Specialist drafts or submits.

|Scenario|Incident state|Request state|Resolution code|
|--------|--------------|-------------|---------------|
|Auto-submit disabled; request drafted and awaiting review.|On Hold \(Awaiting Caller\)|Open \(draft\)|Not yet set.|
|Requester completes and submits the drafted request.|Resolved|Submitted|Resolved by catalog request.|
|Auto-submit enabled; all mandatory variables filled.|On Hold \(Awaiting Caller\)|Open \(submitted automatically\)|Not yet set.|
|Auto-submit enabled, but a mandatory variable could not be filled.|On Hold \(Awaiting Caller\)|Open \(draft\)|Not yet set.|
|Requester adds a negative comment to the incident.|In Progress|Closed Incomplete|Not yet set.|

