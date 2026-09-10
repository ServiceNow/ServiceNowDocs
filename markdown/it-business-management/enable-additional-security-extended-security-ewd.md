---
title: Enable additional security for partitions
description: Enable additional ACL enforcement for partitioned tables to strengthen access control validation. Select the tables where you want to apply enhanced security.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/enable-additional-security-extended-security-ewd.html
release: zurich
topic_type: task
last_updated: "2026-09-01"
reading_time_minutes: 1
breadcrumb: [Configure, SPM Enterprise-Wide Deployment, Strategic Portfolio Management]
---

# Enable additional security for partitions

Enable additional ACL enforcement for partitioned tables to strengthen access control validation. Select the tables where you want to apply enhanced security.

## About this task

You can enable additional security for the four tables as needed.

-   Project \(pm\_project\)
-   Demand \(dmn\_demand\)
-   Program \(pm\_program\)
-   Portfolio \(pm\_portfolio\)

\[Omitted image "enabling-additional-security-with-extennded-ewd.gif"\] Alt text: Enable additional security for partitions with Extended Security for EWD.

## Before you begin

Role required: admin

## Procedure

1.  From the Admin Home page, select **Strategic Portfolio Management** to navigate to the Strategic Portfolio Management page.

2.  Select **Configure** next to "Configure your product".

    The Configure SPM console opens, showing configuration options for your SPM deployment..

3.  Under **Partitions**, select **Enable additional security**.

    The Enable additional security page opens, displaying a table with the four available tables and check boxes for each.

4.  Review the table descriptions and select the tables where you want to enforce partition-based ACL checks.

    **Important:** Enabling additional security may restrict access for existing users who previously had cross-partition visibility through role assignments. Review your user access model before enabling to ensure users retain necessary access to their assigned partitions.

5.  Select the check box next to each table where you want to enable additional security.

    A check mark indicates that additional ACL enforcement is enabled or disabled for that table. Leave unchecked any tables where you want to maintain cross-partition visibility.

6.  Select **Save** to apply the settings.

    The additional security settings take effect immediately. Any subsequent queries or record access will enforce the new partition-based ACL rules.


