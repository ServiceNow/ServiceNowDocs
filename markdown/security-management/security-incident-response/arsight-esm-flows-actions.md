---
title: Flow Designer usage with ArcSight ESM event ingestion integration
description: Using the Integration Hub and Flow Designer, several flows, subflows, and actions are available with the ArcSight ESM integration.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ArcSight ESM Event Ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Flow Designer usage with ArcSight ESM event ingestion integration

Using the Integration Hub and Flow Designer, several flows, subflows, and actions are available with the ArcSight ESM integration.

To view these subflows, navigate to **Flow Designer** &gt; **Designer** and click on the **SubFlows** tab. The figure below shows the important subflows used during profile creation and the scheduled ingestion job.

![ArcSight ESM: Flows](../image/sir-arcsight-esm-flows.png)

These subflows are listed in the sequence in which they are executed below:

-   **Connection and credential validation**: This subflow validates ServiceNow connectivity with the ArcSight ESM server and the specified credentials. This subflow is used when you click the **Configure** button in the **ArcSight ESM - Event Ingestion**tile in the **Security Operations** &gt; **Integrations** &gt; **Integrations Configuration** page.
-   **ArcSight Get Auth Token**: This subflow generates the ArcSight ESM Authentication token from the Username and Password using the ArcSight ESM Login Service. The Login Service provides the authentication token that can be used to call any other ArcSight ESM endpoint. This subflow is used in all other subflows.
-   **Query Viewer ID Validation**: This subflow verifies if the Query Viewer ID specified during profile creation is present in the ArcSight ESM server.
-   **Correlation Rule Retrieval**: This subflow retrieves the correlation rules based on the Query Viewer ID.
-   **Get Sample Event**: This subflow fetches the sample correlation events from the ArcSight ESM server. These sample events are then mapped to the security incident fields in the Mapping section of the profile.
-   **Stage Resource ID Validation**: This subflow validates the specified Stage Resource ID in the ArcSight ESM console and fetches the Resource Name.
-   **Update Correlated Event Comments**: This subflow updates the Correlated Event comments in the Initial and Closure of Incident sections in the Additional Options page of the profile.
-   **Retrieve Correlated Events Based on Polling Schedule**: This subflow runs the scheduled job that fetches the correlated events based on the polling interval.

During execution, the above subflows also trigger several other subflows and actions either directly or indirectly as shown below.

![ArcSight ESM: Additional subflows](../image/sir-arcsight-esm-flows-subflows.png)

