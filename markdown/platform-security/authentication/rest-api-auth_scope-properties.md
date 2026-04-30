---
title: REST API Auth Scope properties and tables
description: The REST API Auth Scope plugin \(com.glide.rest.auth.scope\) includes the following system properties, tables, and scripts.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [REST API Auth Scope, REST API access policies, API access policy, Authentication, Access Management]
---

# REST API Auth Scope properties and tables

The REST API Auth Scope plugin \(com.glide.rest.auth.scope\) includes the following system properties, tables, and scripts.

## REST API Auth Scope Properties

REST API Auth Scope adds the following system properties.

<table id="table_zyl_dyx_ctb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**com.glide.rest.api.auth.scope.check.enable**

</td><td>

This property is used to turn-off the platform level auth scope check. If set to false, during the runtime the auth scope check is skipped whether it is linked or not linked with the REST API.

 By default this property is set to true. This properties is used when you want to revert to previous release behavior.

</td></tr><tr><td>

**glide.oauth.token.scope.useraccount**

</td><td>

This property is only used when **useraccount** auth scope is deleted and is added back manually by end user.In this case, the sys ID for the **useraccount** is changed. It is required to update this property to the new sys\_id.

 During the runtime, auth scope sys ID is used instead of auth scope name.

</td></tr></tbody>
</table>## REST API Auth Scope Tables

REST API Auth Scope the following tables.

<table id="table_evn_5nf_htb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Authentication Scope \(sys\_auth\_scope\)

</td><td>

This table defines the auth scope that can be linked with the REST API and OAuth entity. The auth scope name must be unique and it is global.

</td></tr><tr><td>

REST API Auth Scope \(sys\_api\_access\_scope\)

</td><td>

This table links REST API with auth scope.

</td></tr></tbody>
</table>