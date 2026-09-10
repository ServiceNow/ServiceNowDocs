---
title: Prepare to run the SAP HANA collector
description: Set up authentication and configure the necessary privileges before you run the SAP HANA metadata collector.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/prepare-to-run-sap-hana-collector.html
release: australia
topic_type: task
last_updated: "2026-07-28"
reading_time_minutes: 1
keywords: [SAP HANA collector, metadata collector, authentication, database roles]
breadcrumb: [SAP HANA metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Prepare to run the SAP HANA collector

Set up authentication and configure the necessary privileges before you run the SAP HANA metadata collector.

## Before you begin

Role required: admin

## About this task

An account is required with a role that has SELECT privileges on the resources that you want the collector to harvest metadata from. See [SAP HANA Database Roles](https://help.sap.com/docs/SAP_HANA_PLATFORM/52715f71adba4aaeb480d946c742d1f6/e7f358b6e85b4610a2b62c5a25755fc0.html?version=2.0.03).

## Procedure

1.  Log in to the SAP HANA instance.

2.  Set up a role with either of the following privileges:

    1.  System privileges \(CATALOG READ\)

    2.  Object privileges \(SELECT METADATA\)


**Parent Topic:**[SAP HANA metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/sap-hana-metadata-collector.md)

