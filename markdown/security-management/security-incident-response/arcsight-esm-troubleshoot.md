---
title: Troubleshooting ArcSight ESM event ingestion integration
description: This section provides information on how to troubleshoot any errors that may occur during event ingestion.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ArcSight ESM Event Ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Troubleshooting ArcSight ESM event ingestion integration

This section provides information on how to troubleshoot any errors that may occur during event ingestion.

## Integration runs

Navigate to **Event Ingestion Common** &gt; **Integration Runs**. An integration run takes place every minute and captures details regarding the events ingested during the scheduled job.

![ArcSight ESM: Integration run list](../image/sir-arcsight-integ-run-a.png)

You can see the list of integration runs and status of each run \(Success, Timed-out, Waiting\) and the number of security incidents that were created. Click on the Number link to drill down to the detailed Integration Run page.

![ArcSight ESM: Integration Run](../image/sir-arcsight-integ-run.png)

You can view details like the number of events that were ingested, the status, which event that was transformed into a security incident, and the different tasks there were performed during the ingestion. Additionally, you can click the link to view the flow execution details.

## Flow execution details

Click the execution details link to see the flow associated with the event ingestion.

![ArcSight ESM: Flow Execution](../image/sir-arcsight-flow-exec.png)

You can view a step by step execution of the flow detailing the various actions and subflows that were executed as part of the flow.

