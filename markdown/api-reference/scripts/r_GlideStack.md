---
title: Glide stack
description: Glide is an extensible Web 2.0 development platform written in Java that facilitates rapid development of forms-based workflow applications \(work orders, trouble ticketing, and project management, for example\).
locale: en-US
release: australia
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Glide class overview, Scripting, API implementation, API implementation and reference]
---

# Glide stack

Glide is an extensible Web 2.0 development platform written in Java that facilitates rapid development of forms-based workflow applications \(work orders, trouble ticketing, and project management, for example\).

<table id="table_e5t_msn_vq"><thead><tr><th>

User interface and Java packages

</th><th>

Technologies used

</th></tr></thead><tbody><tr><td>

User Interface \(browser\)

</td><td>

-   AngularJS
-   HTML
-   CSS
-   JavaScript

</td></tr><tr><td>

GlideServlet com.glide.ui

com.glide.jelly

</td><td>

Apache Jelly

</td></tr><tr><td>

Business Rulescom.glide.script

</td><td>

Mozilla Rhino

</td></tr><tr><td>

Persistencecom.glide.db

</td><td>

JDBC

</td></tr></tbody>
</table><table id="table_jpl_1tn_vq"><thead><tr><th>

Name

</th><th>

Attributes

</th></tr></thead><tbody><tr><td>

GlideServlet

</td><td>

The primary driver of Glide, and the only servlet in the system, is found in GlideServlet.java.

-   Handles inbound action requests
-   Renders pages
-   Merges data with forms
-   Presents to user
-   Interfaces with script layer

</td></tr><tr><td>

Business Rules

</td><td>

-   ECMAScript implementation based on [Mozilla Rhino](http://www.mozilla.org/rhino/)
-   Interfaces with persistence layer using JDBC recordset interface
-   Merges persistence layer meta-data with data for easy correlation

</td></tr><tr><td>

Persistence

</td><td>

-   Persistence means any store
    -   RDBMS
    -   LDAP
    -   File system
-   Uniform access regardless of store type
-   Provides QUID and meta-data capabilities
-   Interfaces presented to callers
    -   RecordSet
    -   TableDescriptor
    -   ElementDescriptor

</td></tr></tbody>
</table>![Diagram of the Glide stack](../image/GlideServlet.svg "Glide stack")

**Parent Topic:**[Glide class overview](r_GlideClassOverview.md)

