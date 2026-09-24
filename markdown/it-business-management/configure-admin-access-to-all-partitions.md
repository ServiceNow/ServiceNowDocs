---
title: Configure administrator access to all partitions
description: Enable or disable the system property to control whether system administrators can access all partitioned data across your enterprise deployment, or only their assigned partitions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/configure-admin-access-to-all-partitions.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [system property, partition access, administrator, Enterprise Wide Deployment, EWD, Portfolio Management]
breadcrumb: [Configure, SPM Enterprise-Wide Deployment, Strategic Portfolio Management]
---

# Configure administrator access to all partitions

Enable or disable the system property to control whether system administrators can access all partitioned data across your enterprise deployment, or only their assigned partitions.

## Before you begin

Role required: admin or sn\_spm\_ewd.ewd\_admin

## About this task

The **sn\_spm\_ewd.allow\_admin\_access\_to\_all\_partitions** system property controls whether administrators with the appropriate role can access all partitions across the deployment, or only the partitions they are explicitly assigned to.

-   **Default behavior \(false\):** Administrators can only access partitions they are assigned to. This provides data isolation and governance.
-   **Enterprise access \(true\):** Administrators can view and manage all partitions across the entire deployment. This is useful for enterprise-wide system administration tasks.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Search and open the **sn\_spm\_ewd.allow\_admin\_access\_to\_all\_partitions** system property.

3.  In the **Value** field, provide the input as `true` or `false`.

    The default value is **false**.

4.  Select **Update** to save the changes.

    The new setting takes effect immediately for new administrator sessions.


## Result

