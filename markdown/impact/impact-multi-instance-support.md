---
title: Impact multi-instance-support
description: Impact multi-instance support allows the Impact Delivery Instance to sync data with multiple production instances where the Impact Store Application is installed.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-04-22"
reading_time_minutes: 1
breadcrumb: [Exploring Impact Store Application, Impact Store Application, Impact]
---

# Impact multi-instance-support

Impact multi-instance support allows the Impact Delivery Instance to sync data with multiple production instances where the Impact Store Application is installed.

There is no need to offboard initial connections to set up additional instance connections; however, configuration and connection steps must be performed for each production instance that connects to the Impact Delivery Instance.

Account level data syncs from IDI to the Impact Store App and instance level data is synced at the instance level. For example, Recommendations contain account level information and syncs for availability to all production instances. Capabilities maps contain instance level data and syncs to each individual instance. See the diagram for an example of multi-instance configuration with Impact.

![Impact multi-instance configuration showing instance level data and account level data syncing with IDI.](../image/multi-instance.png)

For additional information about multi-instance support, see [Cross-instance application trust configuration](https://www.servicenow.com/docs/access?context=grant-access-v2&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

