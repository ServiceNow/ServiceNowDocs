---
title: Activate REST API Auth Scope
description: You can activate the REST API Auth Scope plugin \(com.glide.rest.auth.scope\) to link the OAuth entity with authentication scopes.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [REST API Auth Scope, REST API access policies, API access policy, Authentication, Access Management]
---

# Activate REST API Auth Scope

You can activate the REST API Auth Scope plugin \(com.glide.rest.auth.scope\) to link the OAuth entity with authentication scopes.

## Before you begin

Install the following plugins:

-   OAuth 2.0
-   REST API Provider
-   Authentication scope
-   REST API Scope

**Note:** The **REST API Scope** plugin is added as part of the Tokyo release.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the REST API auth Scope \(com.glide.rest.auth.scope\) plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


