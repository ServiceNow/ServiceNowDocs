---
title: Manage groups
description: Manage the groups that have been imported from the MITRE TAXII collections. Groups are sets of related intrusion activity that are tracked by a common name in the security community. Analysts track clusters of activities using various terms such as threat groups, activity groups, threat actors, intrusion sets, and campaigns. In STIX, groups are known as intrusion sets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/manage-groups-threat-intel.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [MITRE-ATT&amp;CK administration, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Manage groups

Manage the groups that have been imported from the MITRE TAXII collections. Groups are sets of related intrusion activity that are tracked by a common name in the security community. Analysts track clusters of activities using various terms such as threat groups, activity groups, threat actors, intrusion sets, and campaigns. In STIX, groups are known as intrusion sets.

## Before you begin

Role required:

-   sn\_ti.admin: delete access
-   sn\_ti.read: read access
-   sn\_ti.write: create, write access

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **MITRE ATT&amp;CK Repository** &gt; **Groups**.

    You can view the listed groups.

2.  Click a group to view all the associated information.

    In the following illustration, you can view the details for the Ajax Security Team group, its ID, source, and other related information.\[Omitted image "mitre-groups-overview.gif"\] Alt text: View details for the group and other related information.

3.  To view how these objects are related, click **Show Relationships**.

    **Note:** To associate the threat groups to a security case for deeper investigation, click **Add to Security Case**.


## What to do next

Use the [techniques module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/view-techniques.md) to add or modify the groups data.

**Parent Topic:**[MITRE-ATT&amp;CK administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/mitre-att-ck-administration.md)

**Related topics**  


[Get started with MITRE-ATT&amp;CK framework]()

[Understand the MITRE to STIX data model]()

[Domain separation and MITRE-ATT&amp;CK]()

[Set up the MITRE-ATT&amp;CK framework]()

[Manage matrices]()

[Manage techniques]()

[Manage mitigations]()

[Manage malware]()

[Manage tools]()

[Manage MITRE relationships]()

[Manage CVE and technique mapping]()

[Extend the MITRE-ATT&amp;CK data]()

[Define the data source and detection tool mapping]()

[Define the data source and data component mapping]()

[Define the technique detection coverage]()

[Map your technique detection coverage to a technique]()

[Define the mitigation coverage]()

[Map your mitigation coverage to a technique]()

[Create and map detection rules]()

[Auto-extract technique rules for importing MITRE-ATT&amp;CK information]()

[Review threat group and MITRE-ATT&amp;CK techniques mapping]()

[Threat group to technique heatmap definition]()

[Review the MITRE-ATT&amp;CK system properties]()

