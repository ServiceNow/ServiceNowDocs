---
title: Working with ServiceNow Arc agent records
description: Track every installation of ServiceNow Arc across your organization and stop it from running on specific devices, all from one record in the AI Control Tower inventory.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/disc-working-with-arc-agent-records.html
release: australia
topic_type: concept
last_updated: "2026-10-28"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, use, Arc, fleet]
breadcrumb: [Discover and manage AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Working with ServiceNow Arc agent records

Track every installation of ServiceNow Arc across your organization and stop it from running on specific devices, all from one record in the AI Control Tower inventory.

ServiceNow Arc is an autonomous AI agent that runs commands, reads and writes files, and reaches external systems on behalf of users. It connects to your enterprise applications and carries out multi-step tasks within the security, access, and governance policies that you define. For an overview of the product, see .

## How Arc appears in the inventory

AI Control Tower represents Arc as a single AI system asset in the inventory, the ServiceNow Arc agent record. The record belongs to the Agentic client model category. Governance, value, and trace data for Arc roll up to this one asset rather than to individual installations.

Each installation of Arc on a user's machine is tracked as an instance of that asset. An installation reports to AI Control Tower when Arc is first discovered on a device, and periodically after that. A person who uses Arc on more than one machine has one instance for each.

## What the Fleet tab shows

The Fleet tab appears on asset records in the Agentic client model category, including the ServiceNow Arc agent record. It lists every instance of the asset, with one row per installation.

|Column|Description|
|------|-----------|
|Assigned to|The person whose machine has an ServiceNow Arc installation. Select the name to view the user record.|
|Most recent discovery|The date that the installation last reported to AI Control Tower.|
|First discovered|The date that the installation was first registered.|
|Install Status|Whether Arc can run on the device. Installed means users can launch Arc. In Maintenance means the instance is blocked.|
|Session status|Whether Arc is currently running on the device. The value is Active or Inactive.|
|Location|The city and state recorded for the installation, when available.|

## Blocking and unblocking instances

Blocking lets you stop Arc on specific machines from the Fleet tab. A blocked instance can't start, so the user on that device can't launch Arc until you unblock it. Blocking affects only the instances that you select. Other installations and the asset record itself are unchanged.

Only AI stewards can block and unblock instances.

