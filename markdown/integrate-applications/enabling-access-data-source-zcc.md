---
title: Enabling access to a data source
description: Work with your data source administrator to enable access to your external data source.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/enabling-access-data-source-zcc.html
release: brazil
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Zero Copy Connectors, Workflow Data Fabric]
---

# Enabling access to a data source

Work with your data source administrator to enable access to your external data source.

To connect to a data source behind a private network using a zero copy connection, there are three general approaches:

|Approach|Description|
|--------|-----------|
|IP allowlist|Your data source admin must allow access to a source IP range based on where the zero copy queries are coming from. For help with identifying the correct IP range, contact your account manager or Customer Service and Support and reference the [Source IP Addresses for Snowsk8s \(kubernetes\) Workloads \[KB1706533\]](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB1706533) article in the Now Support Knowledge Base. If you're unable to access the KB article and need immediate assistance, use one of the contact numbers from [support contact page](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1000420).|
|Private connectivity|For data sources hosted behind private Virtual Private Clouds \(VPCs\) or Virtual Networks \(VNets\) in the public cloud, connectivity options are available. These options enable query traffic to transit over private IP address space, end to end. This private connectivity is enabled by technologies such as [Private Link](https://learn.microsoft.com/en-us/azure/private-link/private-link-overview). Each cloud provider implements this technology differently. To explore private connectivity options for your specific topology, contact your account manager or Customer Service and Support.|
|Reverse Tunnel|For data sources in a private network that can't be reached by IP allowlist or private cloud connectivity, a private relay running on a host in your network establishes an outbound encrypted connection to the Reverse Tunnel gateway. Query traffic then flows through the relay without requiring inbound firewall rules on your network.|

## Configuring a reverse tunnel

A private relay is a lightweight process that runs on a host machine in your network and connects outbound to the Reverse Tunnel gateway. After the relay registers, zero copy queries route through the tunnel without requiring inbound firewall rules.

Before you begin, verify the following requirements:

-   The host machine must be running Linux x86-64 or Windows x86-64.
-   The host machine must have outbound network access to your ServiceNow instance on port 443.
-   After the relay registers, the host machine must also have outbound access to each gateway host on its data port \(8090\) and admin port \(8081\).
-   Role required: sn\_zc\_tunnel.relay\_manager

To set up the relay and connect it to a zero copy connection, see [Connect a private relay to the Reverse Tunnel gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/connect-customer-relay.md). While setting up the zero copy connection, the connection URL hostname must exactly match the fully qualified domain name \(FQDN\) registered as a service endpoint on the relay.

**Parent Topic:**[Configuring Zero Copy Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/configuring-zcc.md)

