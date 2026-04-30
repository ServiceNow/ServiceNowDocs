---
title: Deployment analyzer rules
description: The deployment analyzer contains five rules that are included by default with ReleaseOps.
locale: en-US
release: zurich
product: ReleaseOps
classification: releaseops
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, ReleaseOps, Deploying applications, Building applications]
---

# Deployment analyzer rules

The deployment analyzer contains five rules that are included by default with ReleaseOps.

|Rule name|Rule set|Match Type|Description|
|---------|--------|----------|-----------|
|Has Code Change|Default|Any|Detects any script change in the update sets.|
|Has Security ACL Roles|Security|Any|Detects any changes to roles or new roles in the update sets.|
|Has Security ACLs|Security|Any|Detects any changes to ACLs or new ACLs in the update sets.|
|Only Catalog Item Changes|Default|All|Verifies that the update sets contain only data from specific catalog tables.|
|Schema Change|Default|Any|Detects if new schema columns are added. Configured to only trigger if the table has more than 10,000 rows.|

**Note:** Any means that the rule will act as an or search with other rules. All means that the rule will match only if no other rules match.

**Parent Topic:**[ReleaseOps reference](releaseops-reference.md)

