---
title: MID Server profile configuration data
description: Use these tables to locate and manage MID Server profile records, configuration parameters, properties, and assignments stored in the instance database.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/mid-server/mid-server-profile-configuration-data.html
release: australia
product: MID Server
classification: mid-server
topic_type: reference
last_updated: "2026-07-27"
reading_time_minutes: 1
keywords: [MID Server profile tables, MID Server profile configuration data, wrapper configuration parameters]
breadcrumb: [MID Server profiles, Configuring MID Servers, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server profile configuration data

Use these tables to locate and manage MID Server profile records, configuration parameters, properties, and assignments stored in the instance database.

## MID Server profile tables

MID Server profile data is stored in the following tables.

|Table|Description|
|-----|-----------|
|`mid_server_profile`|Stores the profile record.|
|`mid_profile_config`|Stores instance configuration parameters that populate `config.xml` on the MID Server.|
|`mid_profile_wrapper_config`|Stores wrapper configuration parameters that populate `wrapper-profile-sync.conf` on the MID Server.|
|`mid_profile_property`|Stores MID Server properties associated with the profile.|
|`mid_profile_application_m2m`|Stores application assignments.|
|`mid_profile_capability_m2m`|Stores capability assignments.|
|`mid_profile_ip_range_m2m`|Stores IP range assignments.|
|`mid_profile_cluster_m2m`|Stores cluster assignments.|

