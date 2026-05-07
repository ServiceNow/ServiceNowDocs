---
title: IPAM integration
description: Use an IP address management \(IPAM\) tool like Infoblox to manage cloud IP addresses, networks, and subnets within your cloud catalog offerings. However, it's important to note that this functionality is not supported with our template-based cloud catalogs.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# IPAM integration

Use an IP address management \(IPAM\) tool like Infoblox to manage cloud IP addresses, networks, and subnets within your cloud catalog offerings. However, it's important to note that this functionality is not supported with our template-based cloud catalogs.

## Infoblox integration

By default, Cloud Provisioning and Governance supports Infoblox integration. You can create Infoblox credentials and then set up an Infoblox instance record. See [Register an Infoblox server](../task/create-infoblox.md) for instructions.

**Note:** IPAM integration is not supported with template based cloud catalog items.

**Note:** This integration is supported with legacy blueprints only. Refer to this [Knowledge Base](https://community.servicenow.com/community?id=community_article&sys_id=291c39dbdb17d4547d3e02d5ca96193e) article to learn more.

## Subnets

If you have subnets in your AWS and Azure clouds, Cloud Provisioning and Governance finds them when Discovery runs on a service or cloud account.

**Note:** If you have networks and subnets in a VMware vSphere platform, Discovery does not create subnet records in the CMDB and cannot map the subnet to the appropriate network. You must create the records manually.

