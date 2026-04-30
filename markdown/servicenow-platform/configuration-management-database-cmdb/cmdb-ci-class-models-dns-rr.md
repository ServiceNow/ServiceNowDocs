---
title: DNS resource record classes
description: A DNS record, also known as a DNS resource record \(RR\), is an entry in the domain name system \(DNS\) database that provides information about a specific aspect of a domain name.
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2024-10-29"
reading_time_minutes: 3
breadcrumb: [CMDB CI Class Models, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# DNS resource record classes

A DNS record, also known as a DNS resource record \(RR\), is an entry in the domain name system \(DNS\) database that provides information about a specific aspect of a domain name.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## DNS zone resource records

Each DNS record contains data associated with a domain name, such as IP addresses, mail server addresses, or other resources. Each type of record serves a specific purpose, such as mapping domain names to IP addresses \(A records\), identifying mail servers for a domain \(MX records\), and providing aliases for domain names \(CNAME records\), among others. DNS resource records are essential for the proper functioning of the DNS infrastructure on the internet.

**Note:** In CMDB CI Class Models release 1.57, existing classes in the CMDB schema that represent DNS resource records like A, AAAA, CName, and so on are deprecated. The following classes are defined with an ideal base, child class, and identification rule.

## Supported DNS resource record types

-   A Record: Holds the IP address of a domain.
-   AAAA Record: Contains the IPv6 address of a domain.
-   CNAME Record: Forwards one domain or subdomain to another domain. Does not provide an IP address.
-   MX Record: Directs mail to an email server.

The supported record types enable actions like the following:

-   Capture domain name registration in the CMDB and create workflow to request, approve, and track life cycle.
-   Auto-populate the data from integration to the registrar.
-   Connect the data to an IPAM record.
-   Connect the data to the certificate on the DNS.
-   Connect the data to the CDN provider.

![DNS resource record class model.](../image/cmdb-ci-class-models-dns.png "DNS resource record classes integrated with the CMDB class hierarchy")

## Table: cmdb\_ci\_dns\_resource\_record

DNS record detail from Domain Name Server \(DNS\) for a WWW domain.

<table id="table_j3w_nfm_bdc"><thead><tr><th>

Column

</th><th>

Description

</th><th>

Details

</th></tr></thead><tbody><tr><td>

DNS Service Provider \[service\_provider\]

 Replaces the deprecated column: DNS Service Provider \[name\]

</td><td>

Defines which DNS service provider supplied this value, examples like Cloudflare,Google DNS, OpenDNS, Local DNS,Private DNS,empty, and so on.

</td><td>

Identification Rule \(name+service\_provider\) allow null

 String \(255\)

</td></tr><tr><td>

Time to Live \[ttl\]

</td><td>

Time, in seconds, that a DNS record will be cached by an outside DNS server or resolver.

</td><td>

integer

</td></tr><tr><td>

Record Class \[record\_class\]

</td><td>

Class of DNS record.

</td><td>

-   IN \(Internet\) \(default\)
-   CH \(Chaosnet\)
-   HS \(Hesiod\)

</td></tr></tbody>
</table>## Table: cmdb\_ci\_dns\_zone\_a\_record

A records hold only IPv4 addresses.

<table id="table_umf_snm_bdc"><thead><tr><th>

Column

</th><th>

Description

</th><th>

Details

</th></tr></thead><tbody><tr><td>

A IP Address \[ip\_address\]

</td><td>

IPv4 address

</td><td>

ip\_addrIdentification Rule \(name+service\_provider+ip\_address\) allow null

</td></tr></tbody>
</table>## Table: cmdb\_ci\_dns\_zone\_aaaa\_record

AAAA records hold only IPv6 addresses.

<table id="table_hv2_g4m_bdc"><thead><tr><th>

Column

</th><th>

Description

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AAAA IP Address \[ip\_address\]

</td><td>

IPv6 address

</td><td>

ip\_addrIdentification Rule \(name+service\_provider+ip\_address\) allow null

</td></tr></tbody>
</table>## Table: cmdb\_ci\_dns\_zone\_cname\_record

A canonical name \(CNAME\) record points from an alias domain to a canonical domain.

<table id="table_qnx_l4m_bdc"><thead><tr><th>

Column

</th><th>

Description

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Canonical Name \[cname\]

</td><td>

Fully qualified domain name / Canonical Name.

</td><td>

String \(255\)Identification Rule \(name+service\_provider+cname\) allow null

</td></tr></tbody>
</table>## Table: cmdb\_ci\_dns\_zone\_alias\_record

An ALIAS record points domain name to a hostname instead of an IP address.

<table id="table_e1g_54m_bdc"><thead><tr><th>

Column

</th><th>

Description

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Alias Name \[alias\_name\]

</td><td>

Alias name of the DNS record.

</td><td>

String \(255\)Identification Rule \(name+service\_provider+alias\_name\) allow null

</td></tr></tbody>
</table>## Table: cmdb\_ci\_dns\_domain\_info

Domain Name enables you to trace ownership and tenure of domain name details using DNS lookup tools like whois.

<table id="table_azk_1pm_bdc"><thead><tr><th>

Column

</th><th>

Description

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Domain Name \[domain\_name\]

</td><td>

WWW Domain Name value from the DNS lookup tool.

</td><td>

String \(255\)Identification Rule \(Name\)

</td></tr><tr><td>

Registry Domain ID \[registry\_domain\_id\]

</td><td>

Registry Domain ID value from the DNS lookup tool.

</td><td>

String \(255\)

</td></tr><tr><td>

Registrar \[registrar\]

</td><td>

Registrar value from the DNS lookup tool.

</td><td>

String \(255\)

</td></tr><tr><td>

Domain Creation Date \[domain\_creation\_date\]

</td><td>

Creation Date of the domain from the DNS lookup tool.

</td><td>

glide\_date\_time

</td></tr><tr><td>

Domain Updated Date \[domain\_updated\_date\]

</td><td>

Updated Date of the domain from the DNS lookup tool.

</td><td>

glide\_date\_time

</td></tr><tr><td>

Registrar Registration Expiration Date \[registrar\_registration\_expiration\_date\]

</td><td>

Registrar Registration Expiration Date value from the DNS lookup tool.

</td><td>

glide\_date\_time

</td></tr></tbody>
</table>