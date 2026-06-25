---
title: Manage tools
description: Manage the tools information that you imported from the MITRE TAXII collections. Tools are legitimate software that are used by threat actors to perform attacks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/manage-tools.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [MITRE-ATT&amp;CK administration, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Manage tools

Manage the tools information that you imported from the MITRE TAXII collections. Tools are legitimate software that are used by threat actors to perform attacks.

## Before you begin

Role required:

-   sn\_ti.admin: delete access
-   sn\_ti.read: read access
-   sn\_ti.write: create, write access

## About this task

Tools enable you to know how and when threat actors use them for executing campaigns. Unlike malware, these tools or software packages are often found on a system and have legitimate purposes for power users, administrators, network administrators, or even normal users.

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **MITRE ATT&amp;CK Repository** &gt; **Tools**.

    You can view the listed tools.

2.  Click a tool to view all the associated information.

    In the following illustration, you can view the details for the CARROTBALL tool, its ID, source, and other related information.\[Omitted image "mitre-tools-overview.gif"\] Alt text: View the details for the tools and their related information.

3.  To view how these objects are related, click **Show Relationships**.


## What to do next

Use the [techniques module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/view-techniques.md) to add or modify the tools data.

**Parent Topic:**[MITRE-ATT&amp;CK administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/mitre-att-ck-administration.md)

**Related topics**  


[Get started with MITRE-ATT&amp;CK framework]()

[Understand the MITRE to STIX data model]()

[Domain separation and MITRE-ATT&amp;CK]()

[Set up the MITRE-ATT&amp;CK framework]()

[Manage matrices]()

[Manage techniques]()

[Manage mitigations]()

[Manage groups]()

[Manage malware]()

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

