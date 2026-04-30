---
title: TISC Data Archival
description: The Threat Intelligence Security Center is provisioned with archival rules in the base system for the TISC table. The related records are also added in the base system to the TISC archive rule.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [TISC Data Archival, Use, Threat Intelligence Security Center, Security Operations]
---

# TISC Data Archival

The Threat Intelligence Security Center is provisioned with archival rules in the base system for the TISC table. The related records are also added in the base system to the TISC archive rule.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Archiving** &gt; **Archival Rules**.

    The list of archival rules that are applicable for TISC are displayed. These archival rules are different for every object type and are applicable independently.

2.  Filter the tables names starts with sn\_sec\_tisc.

3.  View the TISC related records.

    |Threat Intelligence Record|Reference Table|
    |--------------------------|---------------|
    |Archive Attack Pattern|sn\_sec\_tisc\_attack\_pattern|
    |Archive Campaign|sn\_sec\_tisc\_campaign|
    |Archive Course of Action|sn\_sec\_tisc\_course\_of\_action|
    |Archive Data Component|sn\_sec\_tisc\_aggregated\_data\_component|
    |Archive Data Source|sn\_sec\_tisc\_aggregated\_data\_source|
    |Archive Identity|sn\_sec\_tisc\_identity|
    |Archive Infrastructure|sn\_sec\_tisc\_infrastructure|
    |Archive Intrusion Set|sn\_sec\_tisc\_intrusion\_set|
    |Archive Malware|sn\_sec\_tisc\_malware|
    |Archive Malware Analysis|sn\_sec\_tisc\_malware\_analysis|
    |Archive Marking Definition|sn\_sec\_tisc\_marking\_definition|
    |Archive Object Sighting|sn\_sec\_tisc\_object\_sighting|
    |Archive Observed Data|sn\_sec\_tisc\_observed\_data|
    |Archive Threat Actor|sn\_sec\_tisc\_threat\_actor|
    |Archive Threat Event|sn\_sec\_tisc\_threat\_event|
    |Archive Threat Grouping|sn\_sec\_tisc\_threat\_grouping|
    |Archive Threat Note|sn\_sec\_tisc\_threat\_note|
    |Archive Threat Opinion|sn\_sec\_tisc\_threat\_opinion|
    |Archive Threat Report|sn\_sec\_tisc\_threat\_report|
    |Archive Tool|sn\_sec\_tisc\_tool|
    |Archive Vulnerability|sn\_sec\_tisc\_vulnerability|
    |Artifact|sn\_sec\_tisc\_artifact|
    |AS Number|sn\_sec\_tisc\_as\_number|
    |Directory|sn\_sec\_tisc\_directory|
    |Email Address|sn\_sec\_tisc\_email\_address|
    |Email Message|sn\_sec\_tisc\_email\_message|
    |Email Subject|sn\_sec\_tisc\_email\_subject|
    |File|sn\_sec\_tisc\_file|
    |Indicator Archive Rule|sn\_sec\_tisc\_indicator|
    |IPv4 Address|sn\_sec\_tisc\_ipv4\_address|
    |IPv4 CIDR|sn\_sec\_tisc\_ipv4\_cidr|
    |IPv6 Address|sn\_sec\_tisc\_ipv6\_address|
    |Location|sn\_sec\_tisc\_location|
    |MAC Address|sn\_sec\_tisc\_mac\_address|
    |MD5 Hash|sn\_sec\_tisc\_md5\_hash|
    |Mutex Name|sn\_sec\_tisc\_mutex\_name|
    |Other Observable|sn\_sec\_tisc\_other\_observable|
    |Process|sn\_sec\_tisc\_process|
    |SHA1 Hash|sn\_sec\_tisc\_sha1\_hash|
    |SHA256 Hash|sn\_sec\_tisc\_sha256\_hash|
    |SHA512 Hash|sn\_sec\_tisc\_sha512\_hash|
    |URL|sn\_sec\_tisc\_url|
    |User Account|sn\_sec\_tisc\_user\_account|
    |Windows Registry Key|sn\_sec\_tisc\_windows\_registry\_key|
    |X.509 Certificate|sn\_sec\_tisc\_x\_509\_certificate|
    |Object-Object Relationship Archive Rule|sn\_sec\_tisc\_m2m\_object|
    |Object-Observable Relationship Archive Rule|sn\_sec\_tisc\_m2m\_object\_observable|
    |Related Indicator Archive Rule|sn\_sec\_tisc\_m2m\_indicator|
    |RSS Feed Archive Rule|sn\_sec\_tisc\_m2m\_object\_indicator|
    |Imports Archive Rules|sn\_sec\_tisc\_m2m\_indicator\_observable|

    **Note:**

    For information on how the archival rules are created, see [Create an archive rule](https://www.servicenow.com/docs/access?context=t_CreateAnArchiveRule&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

4.  Select an archival rule.

    For example, select Directory observable record to see the base system archival rule.

5.  Update the rule if required.


