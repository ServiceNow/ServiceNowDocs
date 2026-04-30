---
title: Enable versioning for a scripted REST API
description: Enable versioning for a scripted REST API to provide multiple versions of the API while maintaining compatibility with existing integrations.
locale: en-US
release: xanadu
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a scripted REST API, Scripted REST APIs, REST APIs, Web services, API implementation, API implementation and reference]
---

# Enable versioning for a scripted REST API

Enable versioning for a scripted REST API to provide multiple versions of the API while maintaining compatibility with existing integrations.

## Before you begin

There must be a scripted REST API defined before you can enable versioning.

Role required: web\_service\_admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted REST APIs**.

2.  Select a scripted REST API.

3.  Under **Related Links**, click **Enable versioning**.

    The **Enable versioning** pop up appears. The **Make version v1 default** check box is selected by default.

4.  Clear the **Make version v1 default** check box to enable versioning without a default version.

    Versioned APIs without a default version are accessible only by using the version-specific URI. Make version v1 default, or select a different version as default after you enable versioning.

5.  Click **OK**.

    The **Versioning** embedded list is added to the Scripted REST Service form. You can add new versions or control which version is default from this list.


-   **[Add a version to a scripted REST API](t_AddAVersion.md)**  
Add a new version to a versioned scripted REST API to define new API behavior without impacting older versions.

**Parent Topic:**[Create a scripted REST API](t_CreateAScriptedRESTService.md)

