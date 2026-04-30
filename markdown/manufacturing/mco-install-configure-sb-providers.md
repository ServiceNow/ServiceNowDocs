---
title: Installing and configuring Service Exchange for Providers
description: To set up and configure the Service Exchange for Providers application for Manufacturing Commercial Operations, follow these steps.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-12-02"
reading_time_minutes: 1
breadcrumb: [Configuring Manufacturing Commercial Operations, Manufacturing]
---

# Installing and configuring Service Exchange for Providers

To set up and configure the Service Exchange for Providers application for Manufacturing Commercial Operations, follow these steps.

**Note:** Service Exchange 2.x.x that is being released with the Xanadu release does not support migration of the Service Exchange \(Legacy\) versions. If you are using a Service Bridge \(Legacy\) version, before you upgrade to the Xanadu release, you must follow instructions in the [Service Bridge for Providers \(Legacy\) - Migration Utility \(KB1499823\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1499823) to migrate your configuration data.

## Pre-installation checks

**Check the glide.servlet.uri property**: Ensure that the `glide.servlet.uri` property in the Glide instance is set to the correct instance URL. An issue can occur when an instance is cloned from production, but still refers to the production URL for the `glide.servlet.uri` property.

<table id="table_xkj_nxd_yxb"><thead><tr><th>

Task

</th><th>

Link

</th></tr></thead><tbody><tr><td>

Install the Service Exchange for Providers application.

</td><td>

See [Install Service Exchange for Providers](https://www.servicenow.com/docs/access?context=install-service-bridge-v2-provider&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US).

</td></tr><tr><td>

Upgrade from version 1.x.x of Service Exchange for Providers if required.

</td><td>

See [Upgrade Guide - Service Bridge for Providers and Consumers application \(v2.x.x release - KB1700387\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1700387).

</td></tr><tr><td>

Migrate from Service Exchange legacy version if required.

</td><td>

See [Migrate from Service Exchange \(legacy\)](https://www.servicenow.com/docs/access?context=service-bridge-v2-migrate&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US).**Note:** This feature is supported only for Service Exchange 1.x.x versions.

</td></tr><tr><td>

Set up a new provider record.

</td><td>

See [Set up a Service Exchange provider record](https://www.servicenow.com/docs/access?context=service-bridge-v2-new-provider&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US).

</td></tr><tr><td>

Assign Service Exchange roles for providers.

</td><td>

See [User roles for providers](https://www.servicenow.com/docs/access?context=service-bridge-v2-personas&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US).

</td></tr><tr><td>

Create catalog personas.

</td><td>

See [Create catalog personas](https://www.servicenow.com/docs/access?context=service-bridge-v2-create-catalog-persona&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US).

</td></tr><tr><td>

Create remote choice definitions.

</td><td>

See [Create remote choice definitions in Service Exchange for Providers](https://www.servicenow.com/docs/access?context=service-bridge-v2-create-remote-choice-fld-defs&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US)

</td></tr><tr><td>

Create remote catalog items.

</td><td>

See [Create remote catalogs in Service Exchange for providers](https://www.servicenow.com/docs/access?context=service-bridge-v2-remote-catalog&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US).

</td></tr><tr><td>

Create remote task definitions.

</td><td>

See [Create remote task definitions in Service Exchange for Providers](https://www.servicenow.com/docs/access?context=service-bridge-v2-create-remote-tasks-defs&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US).

</td></tr><tr><td>

Create transforms.

</td><td>

See [Create a transform in Service Exchange](https://www.servicenow.com/docs/access?context=service-bridge-v2-create-transform&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US).

</td></tr><tr><td>

Update Authorized Users settings.

</td><td>

See [Update settings for Authorized Users](https://www.servicenow.com/docs/access?context=service-bridge-v2-configure-settings&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US).

</td></tr></tbody>
</table>