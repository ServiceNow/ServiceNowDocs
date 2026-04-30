---
title: Oracle Multitenant option use cases
description: You can view the following use cases to better understand licensing requirements for the Oracle Multitenant option.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Oracle licensing in multitenant architectures, Software Asset Management publisher pack for Oracle, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Oracle Multitenant option use cases

You can view the following use cases to better understand licensing requirements for the Oracle Multitenant option.

## The Oracle Multitenant option is not in use

![Oracle Multitenant option not in use.](../image/mmasset0021823-multitenant-not-in-use.svg "Oracle Multitenant option not in use example")

In this scenario, Database Instance 1 and Database Instance 2 are running Oracle Database 12.1 Enterprise Edition and contain one user-created PDB each. Database Instance 3 is running Oracle Database 18c Enterprise Edition and also contains one user-created PDB. Since none of the database instances meet or exceed the minimum number of user-created PDBs for which the Oracle Multitenant option is required, the option is not in use on any of the database instances. Additional licensing for the Oracle Multitenant option is not required on any hosts within the cluster.

## The Oracle Multitenant option is in use

![Oracle Multitenant option in use.](../image/mmasset0021822-multitenant-in-use.svg "Oracle Multitenant option in use example")

In this scenario, Database Instance 1 and Database Instance 2 are running Oracle Database 12.1 Enterprise Edition. Database Instance 1 contains three user-created PDBs, while Database Instance 2 contains one user-created PDB. Database Instance 3 is running Oracle Database 18c Enterprise Edition and contains five user-created PDBs. Since both Database Instance 1 and Database Instance 3 exceed the minimum number of user-created PDBs for which the Oracle Multitenant option is required, the option is in use on both database instances. Additional licensing for the Oracle Multitenant option is required on all hosts within the cluster.

## The Oracle Multitenant option is in use but exceeds the maximum PDB amount

![Oracle Multitenant option in use but exceeds maximum PDB amount.](../image/mmasset0021821-multitenant-in-use-exceeds-max-allowed.svg "Oracle Multitenant option in use but exceedx maximum PDB amount example")

In this scenario, Database Instance 1 and Database Instance 2 are running Oracle Database 12.1 Enterprise Edition. Database Instance 1 contains three user-created PDBs, while Database Instance 2 contains one user-created PDB. Database Instance 3 is running Oracle Database 18c Enterprise Edition and contains 255 user-created PDBs. Since both Database Instance 1 and Database Instance 3 exceed the minimum number of user-created PDBs for which the Oracle Multitenant option is required, the option is in use on both database instances. Additional licensing for the Oracle Multitenant option is required on all hosts within the cluster.

However, Database Instance 3 is considered to be out of compliance. Based on licensing rules for the Oracle Multitenant option, the maximum number of user-created PDBs that are supported on database instances running Oracle Database 18c Enterprise Edition is 252. Since Database Instance 3 contains 255 user-created PDBs, Software Asset Management creates removal candidates for the three additional user-created PDBs. These additional PDBs must be removed to maintain compliance.

**Parent Topic:**[Oracle Database licensing in multitenant architectures](oracle-licensing-multitenant-architectures.md)

