---
title: Delete by domain
description: Clean up inactive leaf level domains in the domain hierarchy with a controlled and automated tool.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setup and administration, Domain separation for service providers, Access Management]
---

# Delete by domain

Clean up inactive leaf level domains in the domain hierarchy with a controlled and automated tool.

## Before you begin

Role required: domain separation admin

## Procedure

1.  **All** &gt; **Domain Admin** &gt; **Cleanup Queue**

2.  Select the **Prepare For Cleanup** button.

3.  Select the domains to queue for deletion.

    The list shows all the available inactive leaf level domains that can be selected for deletion.

4.  Select **Save**.

    Selected domains will now reflect a **Ready for Staging** state in the table. Domains must be staged before they are queued for deletion.

5.  Select the **Move to Staging** button.

6.  Enter the number of days to retain the staged domain before deletion.

    **Note:** Once the domain moves to the **Staged and Deletion Planned** state, it cannot be removed from the clean up queue.

7.  Before a domain is deleted, domain administrators can access the data footprint of the domain.
8.  Select the **Preview Domain Data** button.

    A job will be queued to scan the inactive domains for metadata.

9.  After the job has executed, select a domain record to view its metadata.


