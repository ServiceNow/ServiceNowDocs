---
title: Clone terminology
description: A reference topic that contains various terms and definitions for cloning.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Clone terminology

A reference topic that contains various terms and definitions for cloning.

<table id="table_gkn_h2c_zfc"><thead><tr><th>

Term

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source Instance

</td><td>

The original database where data is copied from.

</td></tr><tr><td>

Target Instance

</td><td>

The new location where the data is copied to.

</td></tr><tr><td>

Data Preservers

</td><td>

Specified data from the target instance that is retained on the target instance during the clone. Preservers are defined on the source instance.

</td></tr><tr><td>

Table Exclusions

</td><td>

Data that is not cloned to your target instance.

</td></tr><tr><td>

Cleanup Scripts

</td><td>

Automated steps that run after cloning, such as changing data or settings.

</td></tr><tr><td>

Clone Profiles

</td><td>

Reusable template for clone settings, exclusions, preservers, and scripts.

</td></tr><tr><td>

Clone Admin Console

</td><td>

The Clone Admin Console is the default user interface that enables you to manage and track the cloning process.

</td></tr><tr><td>

On-Demand Backup

</td><td>

With on-demand backup enabled, clone takes a fresh on-demand differential backup at the specified clone start time. Clone uses this backup during the restore phase of the clone.

</td></tr><tr><td>

Clone Chaining

</td><td>

You can divide your clone operation into 2 steps. 1.  Cloning from production to your test \(non-production\) environment.
2.  Cloning from test to all your other environments.

You can save time if you're dealing with multiple instances and experience long clone durations. Using this strategy, you perform lengthy operations such as post-clone cleanup scripts or excluding Task data older than 90 days only once. The clones in step 2 have a lighter footprint and complete faster.

</td></tr></tbody>
</table>**Parent Topic:**[Instance Clone reference](instance-clone-reference.md)

