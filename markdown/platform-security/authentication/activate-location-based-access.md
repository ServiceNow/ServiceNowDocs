---
title: Activate Location Based Access
description: Activate the Zero Trust - Location Based Access \(com.snc.zero\_trust\_location\_access\) to allow admins to configure adaptive authentication policies based on the location of the user.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Location Filter, Filter criteria, Adaptive authentication, Authentication, Access Management]
---

# Activate Location Based Access

Activate the **Zero Trust - Location Based Access** \(`com.snc.zero_trust_location_access`\) to allow admins to configure adaptive authentication policies based on the location of the user.

## Before you begin

Role required: admin

-   Dependant plugin: Adaptive authentication
-   Plugin type: Paid and requires license.
-   The instance should be on ADCv2. If the instance is not on ADCv2, then user location information will not be available.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the **Zero Trust - Location Based Access** \(`com.snc.zero_trust_location_access`\) plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


