---
title: Types of configuration data supported by DevOps Config
description: DevOps Config stores configuration data of every layer of the IT stack in a centralized location.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/devops-family/config-data-devops-config.html
release: zurich
product: DevOps \(Family\)
classification: devops-family
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [DevOps Config reference, DevOps Config, IT Service Management]
---

# Types of configuration data supported by DevOps Config

DevOps Config stores configuration data of every layer of the IT stack in a centralized location.

**Important:** Starting with the Washington D.C. release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

Configuration data includes:

-   App and service configuration
-   Middleware configuration \(databases, message queues, load balancers, for example\)
-   Kubernetes and Service Mesh configuration
-   Cloud resources configuration \(AWS, GGP, Azure DevOps, for example\)
-   Traditional infra configuration \(servers, VMs, network, for example\)

<table id="table_dsh_shd_3pb"><tbody><tr><td>

API keys

</td><td>

passwords

</td><td>

usernames

</td><td>

feature toggles

</td></tr><tr><td>

install paths

</td><td>

load balancing methods

</td><td>

database connections

</td><td>

heap sizes

</td></tr><tr><td>

scaling rules

</td><td>

geo regions

</td><td>

host names

</td><td>

IPs

</td></tr><tr><td>

cluster settings

</td><td>

sizing

</td><td>

sudo user lists

</td><td>

ssh

</td></tr><tr><td>

patching levels

</td><td>

firewalls

</td><td>

URLs

</td><td>

certificates

</td></tr><tr><td>

versions

</td><td>

build numbers

</td><td>

hot fixes

</td><td>

--

</td></tr></tbody>
</table>Typically configuration data is stored in files \(.json, .yaml, .properties, .ini, .xml, .csv\) and is located in a variety of places, including GIT repos, network folders, third-party tools \(JFrog artifactory, Sonatype Nexus\) other databases.

DevOps Config manages and validates your configuration data in a centralized location as the single source of truth.

**Parent Topic:**[DevOps Config reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-family/devops-config-reference.md)

