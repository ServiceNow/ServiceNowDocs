---
title: Active MID Server post-cloning credential issues
description: The system provides automatic processes to detect and notify you of possible MID Server credential issues after instance cloning.
locale: en-US
release: zurich
product: MID Server
classification: mid-server
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Resolving MID Server issues, MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Active MID Server post-cloning credential issues

The system provides automatic processes to detect and notify you of possible MID Server credential issues after instance cloning.

During an instance clone, the MID Server \[ecc\_agent\] table is not copied from the source instance, but the User \[sys\_user\] table is copied. As a result, the source MID Server user credentials copied into the target instance might not match those used by the existing set of MID Servers used by the target. Bad credentials can cause those MID Servers to be down for the target instance. Processes on the instance notify you if a MID Server is down from suspected bad credentials following an instance clone.

## Table for post-cloning credential issues

The MID Server Issue \[ecc\_agent\_issue\] table stores active MID Server issues after an instance clone. Records in this table show a MID Server's current state, evaluation times, and the **Issue source**. For cases in which a MID Server for a cloned instance is down because of possible bad credentials, the **Issue source** is **InstanceClone**. Data from the MID Server Issue \[ecc\_agent\_issue\] table are displayed in a related list on a MID Server record. Records in this table are removed if they have not been detected for 30 days. Ongoing issues reappear as they occur.

## Post-cloning cleanup script and scheduled jobs

A cleanup script called Bad MID Server credentials after clone runs on the target instance after cloning and calls a script include called BadMIDCredentialAfterClone. This script include schedules the execution of the following jobs on the Schedule Item \[sys\_trigger\] table:

-   BadMIDCredentialAfterClone-1: Runs 15 minutes after clone execution.
-   BadMIDCredentialAfterClone-2: Runs 75 minutes after clone execution.

These jobs log to the MID Server Issue \[ecc\_agent\_issue\] table any MID Servers that existed on the target instance prior to the clone that are in the **Down** state. These MID Servers are not ready for normal processing and might be down due to invalid credentials resulting from the cloning process. The state of MID Servers added to the target instance after the clone is not evaluated.

**Note:** The [MID Server log](../concept/ecc-queue-mid-server.md#) shows that the MID Server user associated with the target instance could not be authenticated or was missing the proper role.

## Business rule that checks for bad credentials

The **Check for bad MID credential after clone** business rule monitors the MID Server \[ecc\_agent\] table for MID Servers that are transitioning from **Down** to **Up**. If the business rule finds a MID Server making that transition, the rule attempts to find a matching MID Server in the MID Server Issue \[ecc\_agent\_issue\] table that has an issue source of **InstanceClone** and a state other than **Resolved**. If a match is found, the business rule updates the state of the MID Server in the \[ecc\_agent\_issue\] table to **Resolved**.

## Resolving MID Server issues

The error message in the MID Server Issue \[ecc\_agent\_issue\] table names the affected MID Server user. This message appears each time the business rule runs and finds a MID Server that is down from suspected bad credentials:`MID Server not operational (status: Down), possibly due to recent clone. Verify credentials for logged in User 'local-midserver'.`

Attempt to resolve the issue first by comparing the user's credentials with the credentials that the affected MID Server is expecting. If the credentials are incorrect, fix the problem and check the MID Server status again. If the credentials are correct, but the MID Server remains down, check the [Knowledge Base](https://support.servicenow.com/nav_to.do?uri=%2Fkb_view.do%3Fsysparm_article%3DKB0597571) for other possible causes.

**Parent Topic:**[Resolving MID Server issues](r_MIDServerTroubleshooting.md)

