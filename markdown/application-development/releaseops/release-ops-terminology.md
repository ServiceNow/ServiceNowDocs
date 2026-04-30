---
title: ReleaseOps terminology
description: Before getting started with ReleaseOps, it's important to understand some key concepts used in the application.
locale: en-US
release: zurich
product: ReleaseOps
classification: releaseops
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, ReleaseOps, Deploying applications, Building applications]
---

# ReleaseOps terminology

Before getting started with ReleaseOps, it's important to understand some key concepts used in the application.

**Parent Topic:**[ReleaseOps reference](../reference/releaseops-reference.md)

## deployment analyzer

A service within ReleaseOps that compares changes represented in an update set with the target environment. The deployment analyzer then produces results based on defined rules, such as "contains metadata of type X" or "contains script changes". These results can then be consumed to decide different actions in the deployment process.

## deployment request

A record type that represents a portion of a deployment, typically containing a unit of work that was developed and can be deployed independently from other deployment requests. That unit of work is encapsulated in one or more update sets.

## deployment request update set

A mapping of an update set to a given deployment request, with some additional data. Although it’s visible to the user for verification purposes, there should be no need to edit these records.

## deployment task

As events \(such as Automatic Test Framework results or Instance Scan findings\) occur, the system can generate deployment tasks. These deployment tasks are assigned to an applicable person \(the Developer, Release Admin, and so on\) and must be resolved for the deployment or release to continue. Each task presents available resolution options.

## pipeline

The flow of a deployment within ReleaseOps, from a developer’s keyboard to the target instance. Pipelines are built on top of playbooks and represent the activities and flows for an application or update to get installed on that target instance. These activities and flows include required scans and tests and potentially other ServiceNow and third-party processes.

## release

The release record type and object that represents a full set of changes is destined to be deployed to production or another target environment. The set of changes includes information dictating the schedule of when a deployment should occur. It can contain one or more changes from one or more developers for one or more applications that might be related to each other. A release can be integrated with Change Management.

## update set

A low-level foundational concept that captures and groups configuration changes made in a development instance \(such as form customizations, workflows, scripts, or UI elements\). Update sets enable these changes to be tracked, bundled, and migrated to new instances. Update sets can contain the instruction for an application install.

