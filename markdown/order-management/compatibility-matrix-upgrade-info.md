---
title: Compatibility information for Customer Engagement Sequences
description: The features that are supported in Customer Engagement Sequences are determined by combinations of ServiceNow AI Platform, Playbooks in Workflow Studio, and the Customer Engagement Sequences app version.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customer Engagement Sequences, Lead and opportunity management apps, Configure, Sales Customer Relationship Management]
---

# Compatibility information for Customer Engagement Sequences

The features that are supported in Customer Engagement Sequences are determined by combinations of ServiceNow AI Platform, Playbooks in Workflow Studio, and the Customer Engagement Sequences app version.

The following versions of the Customer Engagement Sequences application are compatible with the ServiceNow® Xanadu, Yokohama, Zurich, and Australia releases:

-   Customer Engagement Sequences 1.0.0
-   Customer Engagement Sequences 2.0.1
-   Customer Engagement Sequences 2.1.0

The following table provides a comparison of features available with two Customer Engagement Sequences version 1.0.0 and 2.0.1.

<table id="table_xmx_jzr_ghc"><thead><tr><th>

Feature

</th><th>

Customer Engagement Sequences 1.0.0

</th><th>

Customer Engagement Sequences starting with version 2.0.1

</th></tr></thead><tbody><tr><td>

Roles

 For more information, see [Components installed with Customer Engagement Sequences](components-installed-customer-engagement-sequences.md).

</td><td>

-   Sequence viewer
-   Sequence task read granular

</td><td>

-   Sequence admin \(granular admin role\)
-   Sequence executor \(renamed from Sequence viewer\)
-   Sequence writer
-   Sequence reader

Provides the ability to view the sequences in Playbooks starting with the Zurich release.

-   Sequence task read granular

</td></tr><tr><td>

Schedule call activity

</td><td>

Unavailable

</td><td>

Available starting with the Xanadu release.

</td></tr><tr><td>

Multi-trigger capability

</td><td>

Available starting with the Zurich release and Playbooks version 28.1.

</td><td>

Available starting with the Zurich release and Playbooks version 28.1.

</td></tr><tr><td>

Decision branches for stages

 Demo data

</td><td>

Available starting with the Zurich release and Playbooks versions 28.3.

</td><td>

Available starting with the Zurich release and Playbooks version 28.3.

</td></tr><tr><td>

Runtime permissions

</td><td>

Available starting with the Zurich release and Playbooks version 28.1.

</td><td>

Available starting with the Zurich release and Playbooks version 28.1.

</td></tr></tbody>
</table>**Note:** The click-to-call capability and activity picker options for the Schedule call activity in Workflow Studio vary by release.

-   In Xanadu and Yokohama, only the **Schedule call** activity is available in the activity picker and does not include the click-to-call capability.
-   Starting with Zurich and Customer Engagement Sequences 2.1.0, both **Schedule call** and **Schedule call - Deprecated** appear in the activity picker. Use the **Schedule call** activity to enable the click-to-call capability.

