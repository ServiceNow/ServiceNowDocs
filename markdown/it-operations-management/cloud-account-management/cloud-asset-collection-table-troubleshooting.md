---
title: Assets are missing from Cloud Asset Explorer
description: Resolve missing or outdated assets in Cloud asset explorer by checking the Cloud Asset Collection Configs table, the CI relationships, and the asset refresh.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/cloud-account-management/cloud-asset-collection-table-troubleshooting.html
release: brazil
product: Cloud Account Management
classification: cloud-account-management
topic_type: topic
last_updated: "2026-11-17"
reading_time_minutes: 2
keywords: [missing assets, cloud asset explorer]
breadcrumb: [Reference, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Assets are missing from Cloud Asset Explorer

Resolve missing or outdated assets in Cloud asset explorer by checking the Cloud Asset Collection Configs table, the CI relationships, and the asset refresh.

## Symptom

An asset that you expect to see is missing from Cloud asset explorer, or the list shows outdated information.

## Cause

The CI class isn't marked active in the Cloud Asset Collection Configs table.

## Resolution

## Procedure

1.  Mark the CI class record as active.

    For the steps, see [Configure the Cloud Asset Collection Configs table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/configure-cloud-asset-collection-table.md). The next run picks up the CI class.


## Cause

The CI doesn't have a relationship to a logical data center or a cloud service account in the CMDB.

## Resolution

## Procedure

1.  Verify that the CI has a relationship to a logical data center and a cloud service account in the `cmdb_rel_ci` table.

    An asset appears in the list only after both relationships exist and the next run finishes.


## Cause

The first run isn't finished, or the batch size is too large for the available nodes.

## Resolution

## Procedure

1.  Wait for the first run to finish.

2.  If records are still missing, reduce the value of the **sn\_itom\_cam.cmdb.query.batchsize** system property.


## Cause

A deleted CI or a new CI relationship is waiting for the next run.

## Resolution

## Procedure

1.  If a deleted CI still appears, verify in the CMDB table that the CI is deleted.

2.  Wait for the next run, and then check the list again.

    The list refreshes every 30 minutes.


## Cause

A CI is missing from the list even though its CI class is active and the CI has valid relationships.

## Resolution

## Procedure

1.  Clear the **Last Processed Time** field in the record for the CI class in the Cloud Asset Collection Configs table.

    During the next run, all CI records from that table are processed, and reconciliation corrects the missing data in the list. For a description of the field, see [Cloud Asset Collection Configs table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/cloud-asset-collection-table.md).


## Cause

The list shows incorrect CI relationships.

## Resolution

## Procedure

1.  Set the **sn\_itom\_cam.asset\_table\_force\_sync** system property to true.

    A full reconciliation runs and corrects the CI relationships in the list.


**Parent Topic:**[Cloud Account Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/cam-reference.md)

