---
title: Clone terminology
description: Key terms and definitions used in instance clone documentation and the Clone Admin Console.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/clone-terminology.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Reference, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Clone terminology

Key terms and definitions used in instance clone documentation and the Clone Admin Console.

<table id="table_gkn_h2c_zfc"><thead><tr><th>

Term

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Preflight Check

</td><td>

A stage in the clone process that verifies the source and target instances are in a healthy state before the clone proceeds.

</td></tr><tr><td>

Provision DBI

</td><td>

A stage in the clone process where a new target database instance \(DBI\) is set up to receive the restored data.

</td></tr><tr><td>

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

Client ID / OAuth

</td><td>

An authentication method used to preserve OAuth credentials on the target instance during a clone. The identity type for OAuth is human. The **oauth\_admin** role is required to manage OAuth credentials preserved during a clone.

</td></tr><tr><td>

Cleanup Scripts

</td><td>

Automated steps that run after cloning, such as changing data or settings.

</td></tr><tr><td>

Clone Profiles

</td><td>

Reusable template for clone settings, exclusions, preservers, and scripts.

</td></tr><tr><td>

Multi-Instance View

</td><td>

A feature in the Clone Admin Console that enables administrators to monitor and manage clone operations across multiple linked instances from a single primary instance, without logging in to each instance separately.

</td></tr><tr><td>

Node Repoint

</td><td>

A stage in the clone process where the system switches traffic from the old target instance to the newly cloned instance. Node Repoint is a clone stage, not a clone state.

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
</table>**Parent Topic:**[Instance Clone reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/instance-clone-reference.md)

